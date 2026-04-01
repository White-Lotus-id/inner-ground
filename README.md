# Inner Ground

A personal growth companion for building self-awareness and emotional clarity. Runs as a Progressive Web App (PWA) — installable on Android via Chrome and fully functional offline.

---

## Features

- **Dump** — Log emotional moments with triggers, body sensations, and what you need
- **No** — Track every time you set a boundary, with weekly counts
- **People** — Audit relationships and track energy patterns over time
- **Reframe** — Catch negative thoughts and record more honest versions
- **Anchor** — Set one weekly goal with a 30-minute action and track your streak
- **Pattern** — Dashboard showing your activity over the last 30 days

All data is stored locally on your device using `localStorage`. Nothing is sent to a server.

---

## File Structure

```
inner-ground/
  index.html       Main app
  manifest.json    PWA manifest
  sw.js            Service worker for offline support
  icons/
    icon-192.png   Home screen icon (192x192)
    icon-512.png   Splash screen icon (512x512)
```

---

## Deploying to GitHub Pages

1. Create a new repository named `inner-ground` on GitHub
2. Push all files to the `main` branch keeping the structure above
3. Go to Settings > Pages > set source to `main` branch, root folder
4. Your app will be live at `https://<your-username>.github.io/inner-ground/`

If you use a different repo name, update `start_url` and `scope` in `manifest.json` to match.

---

## Installing on Android

1. Open Chrome on Android and visit the live GitHub Pages URL
2. Interact with the page for at least 30 seconds
3. Tap the three-dot menu and select "Add to Home Screen"
4. The app will appear on your home screen like a native app

The first visit requires an internet connection. After that, the app loads fully offline.

---

## Offline Support

The service worker (`sw.js`) caches all app files on first load. Subsequent visits load from cache with no network required. The cache is named `inner-ground-v1`. To force a cache refresh after updates, increment the version number in `sw.js`.

---

## Tech Stack

- Vanilla HTML, CSS, JavaScript
- No frameworks or dependencies
- PWA: Web App Manifest + Service Worker
- Storage: browser `localStorage`
