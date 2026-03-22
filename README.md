# Fuel Saver PWA

## Files
```
fuel-saver-pwa/
├── index.html        ← The app
├── manifest.json     ← PWA config
├── sw.js             ← Service worker (offline support)
└── icons/
    ├── apple-touch-icon.png   ← 180×180 (iPhone home screen)
    ├── icon-192.png           ← 192×192 (Android)
    └── icon-512.png           ← 512×512 (splash screen)
```

## Deploy options

### Option A — GitHub Pages (free, recommended)
1. Create a new repo on github.com (e.g. `fuel-saver`)
2. Upload all these files keeping the same folder structure
3. Go to Settings → Pages → Source: main branch / root
4. Your URL will be: `https://yourusername.github.io/fuel-saver/`

### Option B — Any web host
Upload all files to a folder on your existing hosting.
Must be served over **HTTPS** for the service worker to work.
(e.g. `https://yourdomain.com/fuel-saver/`)

## Add to iPhone home screen
1. Open the URL in **Safari** on iPhone (must be Safari, not Chrome)
2. Tap the **Share** button (box with arrow pointing up)
3. Scroll down and tap **"Add to Home Screen"**
4. Tap **Add** — done!

The app will launch fullscreen with no browser chrome, just like a native app.
It also works offline after the first load.

## Notes
- Service worker caches the app after first visit
- Works offline for all calculations (no internet needed)
- Safe-area insets handle iPhone notch / Dynamic Island automatically
- `inputmode="decimal"` gives numeric keyboard on iOS without the annoying +/- buttons
