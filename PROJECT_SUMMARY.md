# The Weight — Project Summary

A master overview for continuing the project — the orientation file to read first.
**Current state: the system is build-complete and ready to use. The next real step is
binding the keystone (M-001), not more building.**

---

## What it is

A personal promise-ledger across three integrated layers, plus an app:
- **Physical** — metal discs (stamped + hand-engraved coins) kept in jars and
  separate vessels.
- **Ritual** — ceremonies that bind, keep, and break promises (`RITUALS.md`).
- **Language** — a personal mythic "fate-language" of engraved marks
  (`FATE_LANGUAGE.md`).
- **App** — an installable PWA ledger that mirrors and assists all three
  (`index.html`).

The meaning of the whole system lives in `SYMBOLISM.md` (read that for the "why").

---

## The system in brief

- **Four jars** — Open · Standing · Kept · Dead — plus **two separate vessels**: the
  Dead jar (failed promises, one-way) and a distinct **Memorial** vessel, a lantern,
  for people who have died (kept apart — the dead are not failures).
- **Three metals = weight tiers:** aluminum (ordinary, left **bare to age**), brass
  (serious, **waxed**), copper (standing, **waxed**). Material is permanence.
- **Two disc faces:** front = label + hand-engraved keyword + fate-glyph; back = the
  **always-hand-engraved** maker's mark (whole, or **scored** if you failed it).
- **The keystone:** M-001 · CODE — *"I will do what I believe is right, and bear the
  cost of it."* Bound first and alone via *The Founding*; carries its own founding
  glyph; judges all other promises.
- **Favors:** bearer-token IOUs, protected by the hand-engraved mark + a verification
  number matching the ledger. They outlive the people given them (no death-fate).

---

## The app (built, deployed as a GitHub Pages PWA)

Single-file `index.html` (+ `sw.js`, `manifest.webmanifest`, icons at repo root).
Current features:
- Tabs: **The Jars · Favors · Memorial · Ledger.**
- Four themed jars with value-reflecting coins — each coin rendered in its tier metal
  (aluminum/brass/copper), sized by weight, **settling to the jar floor and stacking
  with gravity.**
- Custom vessels for **Favors** (offering dish) and **Memorial** (lantern).
- **Glyph-picker:** choose a promise's circumstance glyph (abandoned/taken/death for
  dead; sacrifice/easily/overdue/though-gone for kept).
- **Keystone:** M-001 distinguished (gold tag, sorts first), its glyph drawn on its
  disc, its vow surfaced as judgment when you break another promise.
- **Reckoning banner:** open promises untouched 90+ days.
- **Promotion re-forge flag** (non-copper disc promoted to standing).
- **Carried total** (open + standing grams, standing ×3).
- **Ledger tab:** cumulative chart of taken-on / kept / died over time, toggling
  weight ↔ count.
- **Memorial input via in-app sheet** (reliable in installed iOS PWAs).
- Disc-maker with metallic disc previews and per-disc engraving instructions.
- Local autosave + optional linked cloud-file sync + export/import + engraving CSV.

---

## The rituals (`RITUALS.md`) — all defined

- **The Founding** — the keystone alone, once ever.
- **The Binding** — every promise.
- **The Keeping** — a promise fulfilled.
- **The Breaking** — a promise let die (branches: chosen vs. taken).
- *To design later:* promoting, redeeming a favor, the death/memorial rite, periodic
  review.

---

## The fate-language (`FATE_LANGUAGE.md`) — glyphs drawn so far

Maker's mark ("The Eternal Path"), keystone (#0, "the plumb and the level"), death
(#1), abandoned (#2), taken (#3), eternity (#4). SVGs live in `glyphs/` (placeholders
for your eventual hand-drawn-then-engraved versions). Many circumstance glyphs remain
in the parking lot — **to be drawn as real promises call for them, not in advance.**

---

## Physical build (`PHYSICAL_BUILD.md`)

Now an inventory-driven doc. Owned: OWDEN punches, HimaPro block + 1 lb brass hammer,
diamond-tip engraver, enamel marker, MyIntent backup; aluminum/brass/copper blanks;
mason jars + UV-black Infinity Jar (Dead). Renaissance Wax (200 ml) for brass/copper.
Decisions: maker's mark always hand-engraved; aluminum left bare to age. Vessel
upgrades chosen (Open/Standing/Kept/Memorial) but not yet bought. Has an upgrade log.

---

## Open threads / next steps

1. **Use the system** — bind M-001 (The Founding), then live with it. This is the
   real next step; the build is done.
2. Draw new glyphs only as real promises require them.
3. Someday: a "book of the weight" export that renders the whole ledger as a readable
   life-record (the "read backward someday" idea) — not yet.
4. Still-to-design rituals (promote, redeem, death, review) — one at a time.

---

## Keeping the docs in sync (important)

These docs are the project's memory between sessions. They drift if updated files
aren't all uploaded to the repo. When a meaning-bearing decision is made, update every
affected file (`SYMBOLISM`, `FATE_LANGUAGE`, `RITUALS`, `PHYSICAL_BUILD`, `README`,
and the app) together and upload them all. Each has a change/upgrade log.

---

## Doc files in the project

- `SYMBOLISM.md` — the meaning of every element (start here)
- `README.md` — what goes live + system-in-brief + doc index
- `PROJECT_SUMMARY.md` — this file
- `RITUALS.md` — the four rites
- `FATE_LANGUAGE.md` — the lexicon (+ `glyphs/` — must travel together)
- `PHYSICAL_BUILD.md` — inventory, build, upgrades
- App: `index.html`, `sw.js`, `manifest.webmanifest`, icons (repo root)
