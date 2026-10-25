# 02 · Intake

Project: ShopBase website redesign · type **C · Rebrand** · page **P01 Home** · files in English · Gate 0 = `APPROVED` (2026-10-24, `_progress.md`).

**Status: done (updated 2026-10-24).** W1 resolved: `01-strategy/brief.md` now exists and the user answered its questions; Step 03 may run. Font and icons are needed before Step 16 (W2, W3).

## Input checklist

| Input | Where | Required | Status | Detail |
|---|---|---|---|---|
| Strategy pack | `01-strategy/01-strategy-pack.md` | Yes, Gate 0 | ✅ found | Gate 0 APPROVED. AI USP is `UNPROVEN` (blocks Step 09, not Steps 02–08). |
| Brief (client brief or 5–10 lines) | `01-strategy/` | Yes, without it STOP | ✅ found (updated 2026-10-24) | `01-strategy/brief.md` now exists, confirmed by the user's answers. Text below is the original finding: No brief file exists. `01-strategy/` holds only `00-project-type.md`, `01-strategy-pack.md`, `personas-draft.md`, `source-persona-sheets.md`, `strategy-pack-template.md`, `README.md`. The strategy pack and the user's chat decisions (2026-10-24, logged in `_progress.md`) cover type, USP, audience and product structure, but they are not a brief. See W1. |
| Logo (SVG/PNG) | `02-assets/logo/` | C: yes | ✅ found (3 SVG files, see table below) | Real vector paths, no embedded raster. Licence: the user supplied it as their own brand logo (own brand, `ASSUMPTION` that the user owns the files; no licence text is in the folder). |
| Logo for dark surfaces | `02-assets/logo/` | Only if dark mode or dark headers are planned | ✅ file exists, ⚠ need unknown | `Logo (1).svg` has a white wordmark (see table). Whether dark headers or dark mode are planned is not stated (Q4). |
| Font, files or `font-name.txt` | `02-assets/fonts/` | Before Step 16 | ⚠ missing | Folder does not exist (no `fonts/` directory in `02-assets/`). See W2. |
| Icons, SVG or `icon-library.txt` | `02-assets/icons/` | Before Step 16 | ⚠ missing | Folder does not exist. See W3. |
| Moodboard, 2–4 images | `02-assets/moodboard/` | Recommended | ⚠ missing | Folder does not exist. Not blocking (Step 17 can start from references found in Step 08). |
| Existing page link + numbers + feedback | `01-strategy/` | B, C: yes | ⚠ partial | Link ✅ `https://www.shopbase.com/` (`01-strategy/00-project-type.md`). Numbers ⚠ not supplied. Feedback ⚠ not supplied. Must-keep list: not supplied. Default "none" applied at Step 00 (`00-project-type.md` answer 3, `ASSUMPTION`; not an explicit user answer). See W5. |

`02-assets/images/` (not needed until Step 21): updated 2026-10-24, now holds the user's hero screenshot `hero-2.0-reference.png` (reference only).

### The three logo files (measured, files untouched)

Measured by reading the SVG text (tag counts, `viewBox`, `fill` values) and by rendering each with macOS `qlmanage -t -s 512` (renders at `/private/tmp/claude-501/-Users-nguyentoan-Documents-SB-v2-LD/fb8c2ff0-4f7d-46ed-a2f8-aeb17aa0cde3/scratchpad/r/`, outside the project). Each file has only `<svg>` and `<path>` elements, 0 `data:image` / `<image>` matches: **all three are real vector, not a screenshot or embedded raster**.

| File | What it is | width × height / viewBox | Paths | Fill colours (count) |
|---|---|---|---|---|
| `Logo (1).svg` | Full logo (icon + "ShopBase" wordmark), **white wordmark**, for dark surfaces. Rendered on a white background the wordmark is invisible; only the blue icon shows. | 254 × 48, `0 0 254 48` (ratio 5.29:1) | 11 | `white` ×9 (8 wordmark glyph paths + the smile in the icon), `#497BDF` ×1, `#8BCDF6` ×1 |
| `Logo (3).svg` | **Icon only** (blue rounded bag with a white smile; no wordmark). | 48 × 48, `0 0 48 48` (1:1) | 3 | `#497BDF` ×1, `#8BCDF6` ×1, `white` ×1 |
| `Logo (6).svg` | Full logo (icon + wordmark), **dark wordmark**, for light surfaces. Rendered: clear on white. | 254 × 48, `0 0 254 48` (5.29:1) | 11 | `#373B43` ×8 (wordmark), `#497BDF` ×1, `#8BCDF6` ×1, `white` ×1 |

Notes: Logo (1) and Logo (6) are identical except the wordmark fill (white vs `#373B43`); their file sizes are 11,992 and 12,008 bytes. No background rectangle was found in any file (the paths are the icon and the glyphs), so Logo (1) is transparent and needs a dark background to be seen. Vector files have no pixel resolution limit; the nominal size is 254 × 48 units and scales without loss.

### Logo colours vs the colour scale

| Colour | Hex | RGB | Hue / saturation / value (computed) | Contrast vs white (computed) |
|---|---|---|---|---|
| Logo blue (icon top) | `#497BDF` | 73, 123, 223 | 220° / 67.3% / 87.5% | 4.05:1 |
| Logo light blue (icon base) | `#8BCDF6` | 139, 205, 246 | 203° / 43.5% / 96.5% | 1.73:1 |
| Logo dark wordmark | `#373B43` | 55, 59, 67 | 220° / 17.9% / 26.3% | 11.24:1 |
| "Blue (Primary) 500" from the user's colour-scale screenshot | `#0096ED` | 0, 150, 237 | 202° / 100% / 92.9% | 3.19:1 |

Computed with a Python script (WCAG relative luminance; Euclidean RGB distance). **The logo blue `#497BDF` and the scale's Primary 500 `#0096ED` are not the same colour:** RGB distance 79.1 (of a maximum 441.7), hue 220° vs 202° (18° apart), saturation (HSV) 67% vs 100%. The logo's `#8BCDF6` (hue 203°) is closer in hue to `#0096ED` but is much lighter. So "the logo colours stay" and "the colour scale's Primary is `#0096ed`" currently point to two different blues. The screenshot is not stored in the project, so `#0096ED` and the Neutral / Green / Red / Yellow / Indigo scales are taken from the user's chat only (not verifiable here). Which blue is the brand primary is a Step 16 decision and is asked as Q2.

## Warnings

| # | Where | Problem | Options |
|---|---|---|---|
| W1 ✅ resolved 2026-10-24 (brief written and answered) | `01-strategy/` (no brief file) | The prompt says no brief means STOP. The step file can be written, but the step cannot be called complete and Step 03 (Brief analysis & frame lock) must not start without a brief. Not invented here. | (a) The user writes 5–10 lines into `01-strategy/brief.md`: what the page must achieve, for whom, what changes in 2.0, what must stay, deadline or constraints. (b) The user states in words that `00-project-type.md` plus `01-strategy-pack.md` are to be treated as the brief; Claude then records that decision in `_progress.md` and continues. The choice is the user's. |
| W2 ⚠ | `02-assets/fonts/` (missing) | No font files and no `font-name.txt`. The typography screenshot (chat: h1 28px/36 … small 12px/16) shows sizes and line heights but no family name; the family is not guessed here. Licence risk: a font that is not open-source or not licensed for web use cannot be shipped. | (a) Add the licensed font files (woff2/ttf) the current ShopBase site uses, plus licence proof. (b) Add `font-name.txt` naming one open-source font (for example Inter). Needed before Step 16, not before. |
| W3 ⚠ | `02-assets/icons/` (missing) | No icons and no `icon-library.txt`. Licence risk: icons copied from another product or a paid pack cannot be redistributed. | (a) Add ShopBase's own SVG icon set. (b) Add `icon-library.txt` naming one open-source library (for example Lucide). One style only. Needed before Step 16, not before. |
| W4 ⚠ | `02-assets/moodboard/` (missing) | No moodboard images. Recommended, not required. | (a) Add 2–4 screenshots of UI styles you like. (b) Skip: Step 08 reference sites feed Step 17. |
| W5 ⚠ | `01-strategy/` (numbers, feedback) | No traffic, conversion, scroll-depth numbers or user feedback for P01. Step 05 (Measurement) and Step 04 (Audit) have no baseline. | (a) Add a few numbers and any feedback to `01-strategy/`. (b) Keep the Step 00 default (none, `ASSUMPTION`); Step 05 records "no baseline". |
| W6 ⚠ | `02-assets/logo/Logo (1).svg` | Only the white-wordmark version needs a dark background; if no dark surface is planned it is unused. Also the white version has no background of its own, so it looks empty on white (checked by render). | (a) Confirm dark headers or dark mode are planned (then keep). (b) If not planned, leave unused; nothing to change. |
| W7 ⚠ | Logo vs colour scale (`02-assets/logo/` and chat screenshot) | Logo blue `#497BDF` differs from Primary 500 `#0096ED` (measured above). White text on `#497BDF` is 4.05:1; on `#0096ED` it is 3.19:1 (fails the 4.5:1 normal-text level, computed). | (a) Keep the logo colours as the brand and derive the primary scale from `#497BDF`. (b) Keep `#0096ED` as the UI primary and use the logo colours only inside the logo. Decide at Step 16. |
| W8 ⚠ | `02-assets/logo/` (licence) | No licence or ownership note for the three SVGs. `ASSUMPTION`: the user owns them as the ShopBase brand logo. | The user confirms in one line that ShopBase owns the logo files. |
| W9 ⚠ | Chat only, not in the project | The colour-scale and typography screenshots are not stored in the project. Later steps cannot cite them as files. | (a) Add both screenshots, or a note with the values typed in (for example `design-scale-notes.md`), to `01-strategy/`. (b) Re-send them when Step 16 starts. |

## What I understood

- **Project:** ShopBase website redesign (https://www.shopbase.com/), type **C · Rebrand**, page P01 Home, files in English. ShopBase 2.0 is one independent product; PrintBase and PlusBase are no longer brands.
- **Product in one line:** an e-commerce platform for building a store ("Build a profitable E-commerce business in a few clicks with ShopBase" is today's headline), repositioned as "ShopBase for the AI era".
- **Brand colour from the logo:** blue `#497BDF` with light blue `#8BCDF6`, dark wordmark `#373B43` (measured). It does not equal the `#0096ED` in the colour-scale screenshot.
- **Primary persona:** experienced dropshipping and print-on-demand sellers based in Vietnam, selling to buyers in the US and EU (personas A and B equal; all persona content is unverified, `ASSUMPTION`).
- **USP (the user's words, `UNPROVEN`):** AI-first. AI ("CR Scan" and "AOV") helps raise the store's conversion rate and average order value, and the seller stays in control and makes the final decision. No proof supplied.

I understand this. (Updated 2026-10-24: W1 answered; Step 02 done.)

## Assumptions

1. The user owns the three logo SVGs; no licence note was supplied. `ASSUMPTION`
2. `Logo (1).svg` is the dark-surface version (white wordmark) and `Logo (6).svg` the light-surface version; this is read from the fills, the user did not label them. `ASSUMPTION` on intent, measured on content.
3. `#0096ED` is read from the user's chat screenshot, which is not stored in the project; the font family is not visible there and is not guessed. `ASSUMPTION` / unverifiable.
4. No numbers, no feedback and no must-keep list exist (Step 00 default, `ASSUMPTION`; the user has not confirmed it in words).
5. ~~No brief was supplied.~~ Updated 2026-10-24: `01-strategy/brief.md` exists and was confirmed by the user's answers.
6. Whether dark headers or dark mode are planned is unknown; default: not planned (`ASSUMPTION`).

## Questions

### 🔴 Must answer
1. ~~**[BLOCKER] Brief.**~~ Closed 2026-10-24: `01-strategy/brief.md` written and answered by the user.

### 🟡 Should answer
2. Which blue is the brand primary: logo `#497BDF` or the scale's `#0096ED`? *Default: logo `#497BDF` stays the brand colour (you said logo and colours stay); revisit at Step 16.*
3. What is the font family (name and licence), and which icon set (or `icon-library.txt`)? *Default: none chosen; nothing guessed; required before Step 16.*
4. Are dark headers or dark mode planned? *Default: no; `Logo (1).svg` stays unused.*

### ⚪ Nice to have
5. A moodboard (2–4 images). *Default: Step 08 references feed Step 17.*
6. Numbers and feedback for Home. *Default: none (Step 00 default, `ASSUMPTION`).*
7. Confirm ShopBase owns the logo files. *Default: yes (`ASSUMPTION`).*

## Step 02 check-list

- [x] Every row of the checklist has a status.
- [x] Every ⚠ has a location and at least one option.
- [x] Logo resolution and licence risks were checked, not assumed. Resolution: measured (vector, 254 × 48 and 48 × 48 units, no raster). Licence: no licence text in the folder; ownership is an `ASSUMPTION` (W8).
- [x] Brief present. Met on 2026-10-24 (`01-strategy/brief.md`; W1 resolved).
- [ ] Font and icons present. NOT MET, needed before Step 16 only.

Rendering: run with `qlmanage` (works). `rsvg-convert` and ImageMagick were not installed (`NOT RUN` for those).
