# Trimarchi Stencil – app per AIMO M08F

**File dell'app:** `trimarchi-stencil.html` (versione 2.1, 26 ottobre 2026)
**Link:** https://deskinkgestionale.github.io/stampante-m08f/ (su iPhone/iPad aprirlo in Bluefy)

## Come aprirla
- **Mac:** apri il file con Google Chrome (Safari non ha il Bluetooth per le pagine web).
- **iPhone / iPad:** serve l'app gratuita **Bluefy** e un indirizzo https → carica `trimarchi-stencil.html` nell'archivio GitHub `stampante-m08f` rinominandolo `index.html` e attiva GitHub Pages.
- Prima di collegarti chiudi l'app ePrinter, altrimenti la stampante resta occupata.

## Cosa fa (2.0)
- **Foglio sempre visibile** (A4, Lettera, Legal, A5, rotolo) con il disegno dentro in proporzione reale
- Sposta con un dito, ingrandisci e ruota con due dita; maniglie per eliminare, specchiare, duplicare, ruotare+ingrandire; linee guida al centro
- Fino a 9 elementi: immagini e scritte con font da tatuaggio
- **Fogli per zona del corpo** come ePrinter: 1×2 braccia, 2×1 petto, 2×2 schiena, 3×2 petto, 2×3 gambe, 3×3 petto e schiena, oppure griglia a scelta
- Anteprima di ogni foglio prima di stampare; i fogli vuoti vengono saltati
- **Scala 1:1**: il disegno a grandezza reale sullo schermo, con righelli in cm e i punti esatti della testina; misura stimata dal modello di iPhone/iPad, calibrabile con una carta di credito o un righello
- Archivio con tutto il progetto (fogli, elementi, carta, intensità)

## Funzioni della versione 1.1 (sempre presenti)
- Carica disegno da galleria, file, fotocamera (o incolla / trascina sul Mac)
- Misure in mm con proporzioni bloccate, rotazione, taglio, "togli bordi bianchi"
- Stile: Originale (foto senza effetti), Linee (stencil dai contorni), Nero pieno (soglia), Puntinato
- Formati: A4, Lettera, Legal, A5, rotolo a lunghezza libera
- Misure per zona del corpo (polso, avambraccio, manica, gamba, schiena…) con numero di fogli calcolato; zone modificabili e personalizzabili
- **Archivio clienti:** salva lo stencil con cliente, disegno, zona, misura e impostazioni; ricerca; riapri o ristampa identico; backup/ripristino
- Luminosità, contrasto, nitidezza, inverti
- Disegni più grandi del foglio divisi in più fogli, con sovrapposizione, crocette e numero del foglio; stampa foglio per foglio
- **Le mie carte:** ogni marca con la sua densità (1–15) e calore, sempre modificabili
- Prova intensità: scala 1→15 e scala calore, per trovare il valore giusto per ogni carta
- Specchiatura automatica per stencil, copie, cronologia delle ultime 8 stampe
- Esporta / importa le carte per passarle tra iPhone, iPad e Mac

## Da verificare alla prima prova
1. Collega e stampa la **scala 1→15** con la carta che ti dava problemi.
2. Se tutte le strisce escono uguali, in *Prova e avanzate → Comando densità* prova la variante "1B 4E 04" o "Entrambi" e ripeti.
3. Se la stampa si blocca o salta righe: abbassa "Pacchetto" (es. 100) o alza "Pausa" (es. 20 ms).
4. Copia il registro e incollalo in chat a Claude.

## Copyright
L'app è scritta da zero: codice, testi e grafica sono nuovi. Dall'analisi di ePrinter abbiamo usato solo i comandi con cui il telefono parla con la stampante (interoperabilità). Non usa i server, i cataloghi né i servizi a pagamento del produttore.

## Cronologia
- 25/10: analisi del protocollo, pagina di test
- 26/10: versione 1.0 completa dell'app
- 26/10: versione 1.1 – originale, formati A4/Lettera/Legal, zone del corpo, archivio clienti
- 26/10: studio della modalità tatuaggio di ePrinter (vedi FUNZIONI-EPRINTER-TATUAGGIO.md)
- 26/10: versione 2.0 – nuovo editor con foglio, gesti con le dita, griglie di fogli come ePrinter
- 26/10: versione 2.1 – anteprima a grandezza reale (scala 1:1) con calibrazione
