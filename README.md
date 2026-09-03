# Drawmaha — EDB

Five bomb-pot mixed games against bots, with an equity and exchange solver.
Single page, no server, no network — everything (fonts included) is inside `index.html`.

Games: **Drawmaha · Drawmabo · Samtiubo 三條 · Big Scoop · Fixed Scoop**

## Putting it online

1. Create a repository on GitHub — public is simplest. Anything private needs a paid plan for Pages.
2. Upload **every file in this folder** to the repository root. Not a subfolder: `index.html` has to sit at the top level.
3. Repository → **Settings** → **Pages** → Source: **Deploy from a branch**, branch `main`, folder `/ (root)` → Save.
4. Wait a minute, then open `https://<your-username>.github.io/<repo-name>/`.

## Putting it on the home screen

On the phone, open that URL **in Safari** (not from a bookmark — iOS only offers a custom
icon from Safari's share sheet), then **Share → Add to Home Screen**.

Check the icon in the preview *before* you tap Add. A grey letter tile there means a file
is missing from the repository root — every path in this folder is relative for exactly
that reason, since a project page lives at `/<repo-name>/` and a root-absolute path 404s.

Added this way it opens full-screen with no browser chrome, and the table is laid out
upright for a phone held in portrait.

## What is in this folder

| file | why it is here |
|---|---|
| `index.html` | the whole app |
| `manifest.webmanifest` | name, icons and standalone display for Android and Chrome |
| `apple-touch-icon.png` | the only icon iOS reads |
| `icon-192.png` · `icon-512.png` | Android and Chrome, via the manifest |
| `icon-maskable-512.png` | Android crops icons to the launcher's shape; this one is full-bleed |
| `favicon.svg` · `favicon-32.png` · `favicon.ico` | browser tabs |

All of them must be at the repository root. Nothing else is needed.

## Notes

- **Your session is stored on the device**, in that browser's local storage. Different
  phone, different browser, or a cleared cache means a fresh session.
- **It works offline once loaded** — there is nothing to fetch.
- Updating it is one commit: replace `index.html`. Hard-refresh on the phone to pick it up.

© Ernest Tung
