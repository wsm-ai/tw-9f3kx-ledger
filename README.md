# The Weight — Promise Ledger

A private, single-file app for recording every long-term promise you make — to
yourself and to others — and tracking what becomes of it. It mirrors the
physical four-jar / metal-disc system: each promise gets a numbered **disc**,
and lives in one of four **jars**.

---

## The four jars

| Jar | Meaning | Moves out? |
|-----|---------|------------|
| **Open** | A promise in progress. Will eventually be kept, broken, or promoted. | Yes |
| **Standing** | A persistent promise with no finish line (values, "always" commitments). | Only if broken. |
| **Kept** | Fulfilled. Your proof you follow through. | Can be reopened. |
| **Broken** | A promise you let go of. Honest, not punishing — stores an optional *reason* so you can learn the pattern. | Can be reopened. |

### How a promise moves
```
            ┌─────────────► KEPT
            │
  OPEN ─────┼─────────────► BROKEN ◄──────── STANDING
            │                                   ▲
            └────── promote ────────────────────┘
```
- **Open → Kept** — you honored it.
- **Open → Standing** — you realized it's actually a forever commitment (the promotion you asked for).
- **Open → Broken** — you didn't keep it (prompts for an optional reason).
- **Standing → Broken** — you let go of a forever commitment (the heaviest kind).
- **Kept / Broken → Reopen** — undo, back to Open.

---

## Colour coding (who the promise is to)

- **Green spine / tag** = a promise **to yourself**
- **Purple spine / tag** = a promise **to someone else**

When a promise is to someone else, you can also record **their name** (e.g. "to
Mom", "to Jordan"). The name shows on the entry's tag, and you can **search by
it** to pull up every promise made to a given person. Promises to yourself don't
use a name; if you mark a promise as "to someone else" but leave the name blank,
it just reads "to someone."

This is independent of the jar, so a glance at any jar shows the balance of who
you're showing up for.

---

## The weight

Each jar shows a **gram figure** under its count. It's symbolic, not a scale
reading: every disc counts as ~7g, and **standing promises are weighted ×3** —
so the forever-commitments jar grows heaviest fastest, by design. That's the
"weight I put on myself" made visible. (You can change the multipliers in
`index.html` → `WEIGHTS`.)

For real physical heft in the actual jars, use heavier blanks (steel washers) or
add weighted filler — metal discs alone are light.

---

## The discs

Every promise is assigned an auto-incrementing disc number the moment you make
it. The disc is labelled with **who it's to + the number**, so you stamp it
directly:

- **`M-047`** — a promise **to myself** (M = me), disc 47
- **`O-047`** — a promise **to someone else** (O = other), disc 47

So recipient is stamped right alongside the number — no separate marking needed.

### Metal = the weight of the promise
You also choose a **weight tier** when you make each promise, which tells you
**which metal to stamp it in**:

| Tier | Metal | Meaning |
|------|-------|---------|
| Ordinary | **Aluminum** (lightest) | everyday commitments |
| Serious | **Brass** | the ones that cost you something |
| Standing | **Copper** (heaviest) | forever promises |

Heavier promise → heavier metal → heavier jar. The Standing jar, full of copper,
becomes the literal heaviest in the set. The app records the tier, shows it on
each entry, and tells you the metal to grab when you create the promise.

> Note: if you **promote** an open promise to standing later, its disc was likely
> stamped in a lighter metal. Either re-stamp a copper disc and retire the old
> one, or keep the original as a record of where the promise began — your call.

### Marking discs as stamped
Each promise has a **stamped / to-stamp** state. When you've physically made the
disc, hit **Mark stamped** on that entry. Until then it counts as pending.

### The stamping worklist + reminder
- A banner at the top — **"N discs waiting to be stamped"** — appears whenever you
  have unstamped promises. Tap **Show** to see each pending disc with its exact
  label (e.g. `M-047`) and metal, so it doubles as your stamping job list.
- In the evening (after 8 PM local), if discs are still unstamped and the app is
  open, it shows a reminder. If you grant notification permission, it'll use a
  real notification; otherwise an in-app message.

> **Honest limit:** a guaranteed phone push at end of day — fired while the app is
> closed — isn't reliably possible for an installed web app, especially on iPhone.
> The banner (always visible when you open the app) is the dependable reminder. If
> you want a hard daily nudge, set a simple recurring phone alarm titled "stamp
> your promises" as a backstop.

**Export discs for engraving (.csv)** now includes the stamp label, the metal,
and whether each is already stamped — a complete batch-stamping worklist.

---

## Using it across your computer, Samsung tablet, and iPhone

This is a **PWA (installable web app)** in one HTML file. Same file, all three
devices.

### Install
- **Windows (Chrome/Edge):** open `index.html`, click the install icon in the
  address bar → *Install*.
- **Samsung tablet (Chrome/Samsung Internet):** open it, menu → *Add to Home
  screen* / *Install app*.
- **iPhone (Safari):** open it, Share → *Add to Home Screen*.

### One shared ledger (sync)

The app **autosaves on every change** — you never have to remember to save. How
that reaches your other devices depends on the device:

#### Computer & Samsung tablet — true auto-sync (no export step)
1. Click **Link ledger file (auto-sync)**.
2. Either pick an existing ledger `.json` in your cloud folder (Google Drive /
   iCloud Drive / Dropbox / OneDrive), or create a new one there.
3. From then on, **every change writes straight to that file automatically.** The
   cloud app syncs it to your other devices. No exporting, nothing to forget.

The status badge under the buttons tells you the state at a glance:
- **Saved on this device** (grey) — local only, not linked to a file yet.
- **Saving to cloud file…** (gold, pulsing) — a change is being written.
- **Auto-synced to cloud file** (green) — the linked file is up to date.

On a second linked device, **Link ledger file** → pick the *same* file once;
after that it stays in sync automatically.

#### iPhone — autosave on device + a safety net
iOS Safari doesn't allow apps to write files directly, so the iPhone can't
auto-write the cloud file. Instead:
- Changes still **autosave on the device** instantly (you can't lose work).
- If you try to leave the app with changes you haven't exported, the browser
  **warns you before you go**, so you can't silently drift out of sync.
- When you're done on the iPhone: **Export ledger** → save into your cloud folder
  (overwrite the file). On your computer/tablet the linked file picks it up.

> **Rule of thumb:** On computer/tablet, link the file once and forget about it.
> On iPhone, export to your cloud folder when you finish a session — and you'll
> be reminded if you forget. Don't edit two devices at the same time (last write
> wins).

#### Manual export/import (works everywhere, anytime)
- **Export ledger (.json)** — save a copy (also your backup).
- **Import ledger** — load a `.json` from another device.

### Sharing with someone (only if you choose to)
Send them the `index.html` file. They get their own empty ledger — your data is
never included unless you also send them your `.json`.

---

## Your data & privacy
- Everything is stored locally (browser `localStorage`, autosaved on every
  change) plus, if you link one, a `.json` file in your own cloud folder. Nothing
  is sent anywhere — there is no server and no account.
- Clearing the browser's site data **will** erase the local copy, so keeping a
  linked file (or a recent `.json` export) in your cloud folder is your real
  backup and source of truth.

---

## Technical notes (for you, the builder)

- **Stack:** one self-contained `index.html` — vanilla JS, inline CSS, inline web
  manifest, and a blob service worker for installability. No build step, no
  dependencies.
- **Data model** (per promise):
  ```
  id          uuid
  disc        integer (auto-increment, never reused)
  text        string
  who         "self" | "other"
  name        string                 (recipient's name; only for "other")
  tier        "ordinary"|"serious"|"standing"  (→ Aluminum/Brass/Copper)
  stamped     boolean                (physical disc made yet?)
  status      "open" | "standing" | "kept" | "broken"
  date_made   ISO timestamp
  date_closed ISO timestamp | null   (set on kept/broken)
  reason      string                 (mainly for broken)
  ```
  The disc is stamped as `M-###` (to self) or `O-###` (to other).
  Top level also holds `nextDisc`.
- **Where to extend:**
  - `WEIGHTS` / `DISC_GRAMS` — tune the symbolic weight model.
  - `exportEngraving()` — this is the hook for the machine. It currently writes a
    CSV. To drive a CNC/laser later, replace/extend it to emit G-code or call the
    engraver's API/SDK; the disc number + `stamp_text` are already prepared.
  - `jarSVG()` — the jar fill visualization.
- **Migrating to true sync later** (if you ever want it): swap `load()`/`save()`
  to read/write a small backend (or a cloud file API) instead of `localStorage`.
  The rest of the app doesn't care where the data comes from.

---

## Quick start
1. Open `index.html`.
2. Tap **＋ Make a promise**, write it, choose **to myself / someone else** and
   **has an end / standing**, then **Bind it**.
3. Use the action buttons on each entry to mark it **Kept**, **Make standing**,
   or **Broke it**.
4. Tap any **jar** to see what's inside; filter by recipient or search up top.
5. **Export ledger** to your cloud folder when you're done; **Import** it on the
   next device.
