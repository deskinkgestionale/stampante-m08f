# Come funziona la modalità tatuaggio di ePrinter (studio del 26/10/2026)

Fonte: lettura della struttura dell'app Android `com.quyin.eprinter` (schermate, testi, logica), solo per capire le funzioni. Nessun codice, testo o grafica è stato copiato nell'app Trimarchi Stencil.

## Editor ("Modifica tatuaggi")
- Foglio sempre visibile in proporzione; misure in mm o pollici
- Fino a 9 elementi sul foglio (immagini + scritte con font tatuaggio)
- Ogni elemento: sposta, ingrandisci e ruota con le dita; specchia, duplica, elimina
- Linee guida di allineamento mentre si sposta
- Se l'immagine supera il foglio: scelta tra "Taglia" (più fogli) e "Continua modifica" (adatta al foglio)
- Le zone vuote non vengono stampate

## Taglio su più fogli ("Taglio del tatuaggio")
Griglie = fogli in larghezza × fogli in altezza (il foglio di lavoro diventa grande quanto la griglia):
| Griglia | Zona suggerita |
|---|---|
| 1 × 2 | Braccia |
| 2 × 1 | Petto |
| 2 × 2 | Schiena |
| 3 × 2 | Petto |
| 2 × 3 | Gambe |
| 3 × 3 | Petto e schiena |
| personalizzata | — |
Carta a rotolo: 1, 2, 3 o 4 fogli in larghezza (braccia e gambe / petto, schiena e gambe / petto e schiena).
In stampa: linee guida per unire i fogli; stampa foglio per foglio.

## Impostazioni di stampa
Quantità, formato carta, marca della carta (lista dai loro server), densità (Più chiaro / Consigliato / Più intenso), anti-pieghe, modalità di stampa.

## Anti-pieghe (anti rughe)
- Opzioni: Spento / Leggero / Forte (predefinito in ePrinter: Forte)
- È un comando inviato alla stampante a inizio lavoro: `1F 11 88 nn` con nn = 01 leggero, 02 forte, 03 spento; la stampante aggiunge righe sottili ai lati del foglio
- Ordine dei comandi a inizio lavoro: reset, densità, tipo carta, compressione, anti-pieghe, poi l'immagine

## Archivio
Ogni lavoro salvato con nome, tipo e formato carta, griglia, misura.
