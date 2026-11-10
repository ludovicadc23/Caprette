# Around Caprette

PWA mobile-first in HTML/CSS/JavaScript vanilla.

## Avvio locale
1. Estrai lo ZIP.
2. Apri un terminale nella cartella `around-caprette`.
3. Avvia un server locale, ad esempio:
   - Python: `python -m http.server 8000`
   - Node: `npx serve .`
4. Apri `http://localhost:8000`.

Non aprire `index.html` con `file://`: Service Worker e installazione PWA richiedono HTTPS o localhost.

## Funzioni
- 6 categorie e 48 frasi incluse nel bundle JavaScript (più `database.json` leggibile).
- Ricerca offline IT/EN, preferiti in localStorage.
- Traduzione MyMemory online; non è garantita né disponibile offline.
- Text-to-Speech tramite SpeechSynthesis e dettatura tramite Web Speech API, se supportate dal browser.
- Service Worker cache-first per shell e dati locali.

## Note tecniche
- Per la prima installazione apri l'app online almeno una volta, così il Service Worker può precacheare i file.
- Tailwind CDN, Lucide CDN e Google Fonts migliorano la presentazione ma richiedono rete al primo caricamento; l'app resta usabile offline grazie agli stili locali e alle icone SVG/emoji già presenti nel markup, ma alcuni asset esterni possono non essere disponibili offline.
- MyMemory è un servizio pubblico di terze parti: applica limiti e condizioni propri. Evita di inserire dati personali o sanitari.
- La disponibilità di microfono e voci inglesi dipende da browser, sistema operativo, permessi e pacchetti vocali installati.
- Il 112 è il numero unico di emergenza nell'Unione Europea; fuori dall'UE usa il numero locale.
