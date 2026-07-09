# Equipment Tracker (PWA)

A simple installable web app for tracking rehab equipment status per patient.

## How to publish on GitHub Pages

1. Create a new GitHub repository (e.g. `equipment-tracker`).
2. Upload all files in this folder **keeping the folder structure**:
   - `index.html`
   - `manifest.json`
   - `sw.js`
   - `icons/icon-192.png`
   - `icons/icon-512.png`
3. Go to your repo's **Settings → Pages**.
4. Under "Build and deployment", set Source to **Deploy from a branch**, branch `main`, folder `/ (root)`. Save.
5. GitHub will give you a URL like `https://yourusername.github.io/equipment-tracker/`. Wait a minute or two after saving, then open it.
6. On your phone or computer, open that URL in the browser and look for an **"Install"** option (a banner will appear, or use the browser menu → "Add to Home Screen" / "Install App").

Once installed, the app works offline and behaves like a normal app icon on your device. Your patient data stays stored locally on each device you use it on — it does not sync between devices.

## Notes

- If you rename the repo, the folder-relative links (`manifest.json`, `sw.js`, `icons/...`) will still work fine, since everything is relative — no need to edit any file paths.
- If you update `index.html` later, bump the `CACHE_NAME` value inside `sw.js` (e.g. `equipment-tracker-v2`) so installed devices pick up the new version instead of showing a cached copy.
