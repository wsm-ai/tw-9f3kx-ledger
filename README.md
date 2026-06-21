# The Weight

A personal promise-ledger: a metal-disc system of jars and separate vessels, backed
by an installable web app, with a mythic fate-language for marking how each promise
ends and rituals for binding, keeping, and breaking them.

## What goes live (GitHub Pages)

These files at the repo **root** are the app. Pages serves them as the site:

- `index.html` — the app
- `sw.js` — service worker (installability + offline)
- `manifest.webmanifest` — PWA manifest
- `icon-192.png`, `icon-512.png` — app icons

Keep them at the root, together. After uploading, hard-refresh (Ctrl/Cmd+Shift+R) so
the new version loads.

## The system, in brief

- **Four jars** — Open · Standing · Kept · Dead — plus **two separate vessels**: the
  Dead jar holds failed promises (one-way), and a distinct **Memorial** vessel (a
  lantern) holds discs for people who have died, kept apart because the dead are not
  failures.
- **Three metals by weight tier** — aluminum (ordinary, left bare to age), brass
  (serious, waxed), copper (standing, waxed). Material is permanence: ordinary
  promises wear their age; serious and standing ones are preserved.
- **Two faces per disc** — front carries the label, keyword, and fate-glyph; back
  carries the always-hand-engraved maker's mark (whole, or scored if you failed it).
- **The keystone** — M-001, the founding promise that judges all others; bound first
  and alone, carrying its own founding glyph.
- **Favors** — bearer-token IOUs, protected by the hand-engraved mark and a
  verification number that must match the ledger.

## Documentation (`docs/` — not part of the live app)

- `docs/SYMBOLISM.md` — the canonical meaning of every element (start here)
- `docs/README.md` — how the app works (jars, discs, favors, sync, install), if kept
- `docs/PHYSICAL_BUILD.md` — inventory + build spec + upgrades
- `docs/RITUALS.md` — the Founding, the Binding, the Keeping, the Breaking
- `docs/FATE_LANGUAGE.md` — the fate-language lexicon (grows over time)
- `docs/glyphs/` — the glyph images the lexicon and the app reference. **Keep this
  folder next to `FATE_LANGUAGE.md`** or the images won't show.
- `docs/PROJECT_SUMMARY.md` — the master overview / pick-up point

> Physical gear is tracked as a live inventory in `PHYSICAL_BUILD.md` (with an upgrade
> log), which supersedes the old starter shopping list.

The `docs/` folder can live in the repo for safekeeping; it doesn't affect the live
site.

## Keeping the docs in sync

These docs are the project's memory — they travel with it. When a meaning-bearing
decision is made, update every affected file (`SYMBOLISM`, `FATE_LANGUAGE`,
`RITUALS`, `PHYSICAL_BUILD`, and the app) together, and add a dated line to the
relevant change/upgrade log, so nothing drifts.
