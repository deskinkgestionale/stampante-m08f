# Analisi dell'app ePrinter (Android 1.23.0) per la AIMO M08F

Fonte: decompilazione dell'app `com.quyin.eprinter` (Zhuhai Quin Technology), fatta solo per capire come parlare con la stampante. Il codice decompilato NON è in questo archivio.

## Modello
- M08F: testina 216 mm, 0,125 mm per punto (203 dpi), **1728 punti per riga** (216 byte).
- Foglio singolo A4: circa 2338 righe. In modalità tatuaggio l'app aggiunge margini fino a 2360 righe (A4).
- Per i tatuaggi l'app **specchia sempre l'immagine** in orizzontale prima di stamparla.

## Sequenza di stampa che usa ePrinter
1. `1B 40` – reset (ESC @)
2. Densità (se non arriva un comando dal server, vedi sotto):
   - `1F 11 02 nn` – livello di densità
   - `1F 11 37 hh` – calore/energia, `64` normale, `96` per il livello più forte
   - Livelli usati dall'app: 1 → `02 01`, 2 → `02 02`, 3 → `02 04`, 4 → `02 04` + `37 96`, 13 → `02 0D`
3. `1F 11 nn` – tipo di carta: `0B` foglio singolo/stencil, `26` tacca nera, `38` formato speciale
4. `1F 11 35 00` – dati immagine non compressi
5. Immagine raster, 1 = nero

## Perché nell'app non puoi scegliere la carta
Per la modalità tatuaggio l'app chiede ai server Quin, in base a modello e numero di serie della stampante, la lista delle **carte (consumable)** e delle **densità consentite** per ciascuna:
- `/neutral/api/v1/app/tattoo/concentration/config`
- `/neutral/api/v1/app/tattoo/concentration/full/config`
- `/neutral/api/v1/app/tattoo/concentration/intelligence/config`

Ogni voce contiene il nome della carta e un **comando esadecimale già pronto** che l'app invia così com'è alla stampante. Se il server non prevede la tua carta, l'app non ti lascia scegliere: per questo il controllo è bloccato.

## Cosa faremo nella nostra app
- Lista carte gestita da te (marca + densità + calore + tipo carta), salvata sul telefono
- Densità e calore sempre regolabili a mano
- Stampa oltre l'A4 divisa in più fogli
