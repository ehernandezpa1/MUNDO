# Mundo

A single-page app for daily routines, rewards and a World Bible. No build step, no dependencies, no server. All data stays on your device (localStorage and IndexedDB).

## Deploy on GitHub Pages

1. Create a new repository on GitHub and upload all files in this folder (keep the folder structure, including the hidden `.github` folder).
2. Go to **Settings → Pages**, and under **Build and deployment** set **Source** to **GitHub Actions**.
3. Push to `main`. The workflow in `.github/workflows/pages.yml` publishes the site. Your app will be at `https://<your-username>.github.io/<repo-name>/`.

Prefer no Actions? Set **Source** to **Deploy from a branch**, pick `main` and `/ (root)`, and delete the `.github` folder.

## Install as an app

Open the live URL on your phone or computer and use **Add to Home Screen** (iOS Safari) or **Install** (Chrome/Edge). It works offline after the first visit.

## Run locally

Open `index.html` directly, or serve the folder (needed for the service worker):

```
python3 -m http.server 8000
```

## Updating

Edit `index.html`, then bump `CACHE` in `sw.js` (for example `mundo-v2`) so installed copies pick up the change.

## Your data

Progress is saved per browser and per site address. Use the in-app **Backup** screen to export it before clearing browser data or switching devices.

## Files

| File | Purpose |
|---|---|
| `index.html` | The whole app |
| `manifest.webmanifest` | Install metadata |
| `sw.js` | Offline caching |
| `icons/` | App icons |
| `.github/workflows/pages.yml` | Auto-deploy to GitHub Pages |
