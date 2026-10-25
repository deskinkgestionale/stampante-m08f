# Progetto stampante AIMO M08F – appunti

Stampante: AIMO M08F (rebrand Phomemo M08F). App originale: ePrinter, Zhuhai Quin Technology (com.quyin.eprinter).

## Comandi da provare (protocollo Phomemo, decifrato da phomemo-tools su GitHub)
- Densità variante A: 1F 11 02 nn   (nn = 01…0F)
- Densità variante B: 1B 4E 04 nn   (nn = 01…0F)
- Tipo carta: 1F 11 0B continua · 1F 11 0A con spazi · 1F 11 26 tacca nera
- Dati non compressi: 1F 11 35 00
- Immagine: 1D 76 30 00 xL xH yL yH + bitmap (1 = nero)
- Avanza carta: 1B 64 02

## Test (domani)
1. Apri test-stampante-m08f.html in Bluefy sull'iPhone (serve un link https, vedi chat)
2. Collega, prova "Scala 1 → 15" con comando A, poi con B
3. Annota quale variante cambia davvero l'intensità e copia il registro in chat
