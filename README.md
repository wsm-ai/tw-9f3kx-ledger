# The Weight

A personal promise-ledger: a four-jar / metal-disc system backed by an installable
web app, with a mythic fate-language for marking how each promise ends.

## What goes live (GitHub Pages)

These five files at the repo **root** are the app. Pages serves them as the site:

- `index.html` — the app
- `sw.js` — service worker (installability + offline)
- `manifest.webmanifest` — PWA manifest
- `icon-192.png`, `icon-512.png` — app icons

Keep all five at the root, together. After uploading, hard-refresh (Ctrl/Cmd+Shift+R)
so the new version loads.

## Documentation (`docs/` — not part of the live app)

- `docs/README.md` — how the app works (jars, discs, favors, sync, install)
- `docs/PHYSICAL_BUILD.md` — full physical build spec
- `docs/STARTER_SHOPPING_LIST.md` — the ~$100–150 starter kit
- `docs/FATE_LANGUAGE.md` — the fate-language lexicon (grows over time)
- `docs/glyphs/` — the glyph images the lexicon embeds. **Keep this folder next to
  `FATE_LANGUAGE.md`** or the images won't show. View the lexicon on GitHub (or any
  markdown viewer that renders images) to see the glyphs.

The `docs/` folder can live in the repo for safekeeping; it doesn't affect the live
site.
