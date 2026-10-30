Sylvie AI web app files

Upload these files to the ROOT of your existing GitHub repository (same folder as index.html):
- index.html
- manifest.json
- sw.js
- icon-192.png
- icon-512.png

Keep your existing Cloudflare Worker URL in index.html. It is configured as:
https://sylvie-ai-backend.ronitklenka.workers.dev

Important:
- Chat history is stored locally in this browser/device using localStorage.
- The app sends up to 12 recent conversation messages to the Worker.
- Your Cloudflare Worker must accept body.history and map assistant messages to role "assistant".
- For language choice, the frontend adds a language instruction to the user's message.
- Installable PWA requires HTTPS (GitHub Pages provides HTTPS).
