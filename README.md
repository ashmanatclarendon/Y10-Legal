# Build a 90s Teenager – Year 10 Legal

A single-page quiz game that works as an installable app on phones (iPhone, iPad and Android) and offline once opened.

## Put it on GitHub Pages

1. Create a new **public** repository (e.g. `legal-90s-teen`).
2. Upload **everything in this folder** to the root of the repository (there are no subfolders: every file sits at the top level, including the icons).
3. Go to **Settings → Pages**, set *Source* to **Deploy from a branch**, choose **main** and **/ (root)**, then **Save**.
4. After a minute your app is live at `https://<your-username>.github.io/<repo-name>/`.

## Install on a phone

- **iPhone / iPad:** open the link in **Safari** → **Share** → **Add to Home Screen** → **Add**. The icon is a flat, square, non-transparent PNG at 180 × 180, so iOS applies its own rounded corners.
- **Android:** open in Chrome → **⋮ → Install app** (or *Add to Home screen*).

After the first load the game works with no signal.

## Updating the questions

Build a new `index.html` with the game creator and upload it over the old one. Then open `sw.js` and change `legal-90s-teen-v1` to `-v2` (and so on) so phones fetch the new version.

If you replace `index.html` with a file straight from the creator, it will not contain the app tags. Copy the lines between `<meta name="theme-color">` and `</head>` from this version, the safe-area CSS block, and the small script before `</body>`.

## Changing the icon

The artwork is in `icon-artwork.svg`. iOS caches home-screen icons, so if you change it, delete the app from the home screen and add it again.

## Files (all at the top level)

| File | Purpose |
|---|---|
| `index.html` | The game (60 Legal Studies questions built in) |
| `manifest.webmanifest` | App name, colours and icons |
| `sw.js` | Offline cache |
| `apple-touch-icon.png` | 180 x 180 iOS home-screen icon |
| `icon-192.png`, `icon-512.png` | Android / general icons |
| `icon-maskable-512.png` | Android adaptive icon, extra margin |
| `favicon-32.png`, `favicon.ico` | Browser tab icon |
| `icon-artwork.svg` | Editable source of the icon artwork |
| `.nojekyll` | Tells GitHub Pages to serve files as they are |
