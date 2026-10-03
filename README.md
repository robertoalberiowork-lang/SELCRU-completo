# Selcru: catalogo pubblico e area riservata

Sito statico di SELCRU SRL su GitHub Pages.

- `index.html`: catalogo dei vini, regioni, come funziona l'ordine, pagina Login. Vini e produttori sono in codice (W001…, P01…), i prezzi solo in fasce ex cellar.
- `area.html`: area riservata. I dati di admin, venditori e cantine sono cifrati (AES-GCM, chiave da password con PBKDF2-SHA256, 310.000 iterazioni). Senza password il file contiene solo testo illeggibile. Ogni password apre solo i dati della sua persona.
- Il sito non salva nulla: ordini, documenti e date di prontezza partono via email verso office@selcru.com.
- `area.html` si rigenera con `build.py`, che non sta in questo repository.

Controllo di riservatezza del 03/10/2026: nessun dato riservato in chiaro (restano solo falsi positivi come la proprietà CSS «margin»).
