# Wrestling Drill Caller

Solo wrestling drill partner. It calls out moves aloud at random intervals (circle left/right, level change, down block, single, double, high crotch, knee-down single, knee-down single to double, plus your own) and tallies every rep.

- Static site: no backend, no build step.
- Voice: the browser's built-in speech (Web Speech API). On iPhone/Mac, download an "Enhanced" voice in Settings → Accessibility → Spoken Content → Voices, then choose it in the app.
- Tallies and settings are saved in the browser on each device (localStorage).
- Installable and works offline: open it in Safari/Chrome and choose "Add to Home Screen".

## Run locally

```sh
python3 -m http.server 8000
# open http://localhost:8000
```

To use it from your phone on the same Wi-Fi, open `http://<your-computer-ip>:8000`. Offline mode and installing need HTTPS (GitHub Pages provides it).

## Deploy to GitHub Pages

Settings → Pages → Source: "Deploy from a branch" → `main` / `(root)` → Save.
The site will be at `https://<username>.github.io/<repo-name>/`.

## Updating

When you change any file, bump `VERSION` in `sw.js` so installed copies refresh.

## Later: pre-recorded clips

Planned: one audio clip per built-in move, with browser speech as the fallback for custom moves.
