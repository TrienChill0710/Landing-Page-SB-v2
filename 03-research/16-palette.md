# 16 · Palette

Project: ShopBase website redesign · type **C · Rebrand** · page P01 Home (variants P01·A and P01·B) · English · Gate 5 `APPROVED` (2026-10-25) · light mode only (frame lock) · responsive 1440 + 375.

> **LOCKED: Option 1 · Logo-true Blue, primary `#4371CD`.** The user chose it on 2026-10-25 ("Phương án 1", `_progress.md` Decisions log). Options 2 and 3 stay in this file as **not chosen** (kept for the record, not used from here on). The full role table, contrast table and usage rules of the locked palette are in "Chosen palette — LOCKED" below. A later user decision (2026-10-25) changed the earlier "no gradient" default; see "Amendment: Calendly-style visual direction" (its field tints are an ASSUMPTION until the user sees the Step 18 proof).
> Preview for the user's eyes (shows all three options as derived, before the choice): `03-research/16-palette-options.html` (local file; open in a browser; all ratios on it come from the script below).

## Source

- **Logo colours (measured, Step 10):** blue `#497BDF`, sky `#8BCDF6`, wordmark dark `#373B43`, white. Logo files used as supplied, never edited: `02-assets/logo/Logo (6).svg` (dark wordmark, light surfaces), `Logo (1).svg` (white wordmark, dark surfaces), `Logo (3).svg` (icon only).
- **Brand directions (Step 10):** 1 logo-true blue · 2 blue-violet like the hero screenshot · 3 ink and soft colour fields (Calendly direction). One option per direction.
- **Hero screenshot, sampled (Step 03, re-read here):** button `#3B59F6`, headline gradient `#4454D0` to `#6A63DE`. **`#0096ED`** is a chat-only scale blue, unverifiable (intake W9).
- **Competitor colour facts: almost none were measured.** Step 06 measured no colours for Shopify, BigCommerce, Printify or the others: **not measured**. Step 08 counted hex values in inline CSS only (rendered colours NOT VERIFIED): Intelligems `#2962FF` (7), Shoplift `#4D65FF` (1, too few to say anything), Clarity `#6A5AE0` (12) and `#0078D4` (11), Cursor `#F7F7F4`, `#26251E` (warm neutrals; Cursor is a Step 08 reference, not a Step 06 competitor). Differences below are limited to these counts.
- **Style reference:** `style-ref-01-calendly-fullpage.png`, viewed in 5 slices. Seen: warm off-white page, dark navy buttons, serif and sans headlines, white cards on saturated blue, lilac and pink fields, a dark footer. I could not sample pixel values (no image library in this environment), so Option 3's off-white `#FBFAF7` is **my choice by eye, not a measured Calendly value**.
- **Messaging (Step 09/10):** calm, plain, seller in charge, AI that proposes; no result numbers; no "AI magic" look: Step 08's colour direction (accepted with the research at Gate 2) advises against a gradient or glow that signals "magic AI". This is a recommendation the user accepted, not a separate user decision on gradients.
- **Type face:** Inter (assumed; open question 3 in Step 10). The preview loads it from Google Fonts with a normal fallback stack.

## Options

All three keep the logo blue recognisable: the logo is always shown unchanged, and the logo blue `#497BDF` passes 3:1 as a graphic on every option's page and panel backgrounds. The light sky strip at the base of the icon (`#8BCDF6`, 1.73:1 on white) is thin on any light surface; it is part of the supplied logo and is not counted in the pass counts.

### Option 1 · Logo-true Blue (31/31) · CHOSEN, LOCKED 2026-10-25
- **Mood:** calm, plain, checkable. White page, cool grey panels, one blue.
- **Supports the messaging:** one familiar blue and no glow says "describe, don't dazzle" and keeps the seller in charge; the approval control can be the one saturated element. Soft sky fields (from the logo's `#8BCDF6`) sit behind the illustrations only.
- **How it differs from the closest measured competitor colour:** the closest measured value is Clarity's violet `#6A5AE0` (distance 49.1 of 441.7); then Shoplift `#4D65FF` (52.4, one use only), Intelligems `#2962FF` (58.3) and Clarity `#0078D4` (67.7). The primary keeps the logo hue (220) where those are more saturated or more violet, but these are all blues and the gap is modest. It is a **blue on white like those pages**; colour alone does not set ShopBase apart (consistent with Step 10: the me-too risk is in wording). Shopify and the rest: not measured.
- **Primary** `#4371CD` is the logo blue scaled to 92% brightness (same hue, 220), because white on the logo blue itself is 4.05:1 and fails 4.5:1 for button text.
| Role | Hex |
|---|---|
| Primary | `#4371CD` |
| Primary hover | `#3A62B2` |
| Secondary / accent | `#8BCDF6` |
| Accent tint (approval highlight bg) | `#E7F3FD` |
| Page background | `#FFFFFF` |
| Panel | `#F4F7FC` |
| Title text | `#1E222B` |
| Body text | `#373B43` |
| Muted text | `#596070` |
| Border (UI, 3:1) | `#7F8A9E` |
| Divider (decorative only, carries no UI meaning) | `#DDE3EE` |
| Link | `#3A62B2` |
| Focus ring | `#1E4A9E` |
| Success | `#1B7A47` |
| Success tint | `#E6F4EC` |
| Warning | `#8A5300` |
| Warning tint | `#FFF3D6` |
| Danger | `#B3261E` |
| Danger tint | `#FDECEA` |
| Dark panel (optional) | `#1F2430` |
| Muted text on dark panel | `#B9C0D0` |
| Gradient | none (soft field fill `#E7F3FD` to `#8BCDF6` behind illustrations only, no text on it) |

- **Distance, primary to:** logo blue 21.4 (hue diff 0) · hero button `#3B59F6` 48.2 · gradient start `#4454D0` 29.2 · gradient end `#6A63DE` 44.8 · `#0096ED` 83.0 (chat-only).
- **Thin margins:** white on primary 4.69:1 (needs 4.5), success text 4.72:1; fine, but do not lighten either.

### Option 2 · Blue-Violet (34/34) · NOT CHOSEN
- **Mood:** modern, energetic, indigo-leaning. It is the user's own hero blue, so the page and the hero screenshot agree.
- **Supports the messaging:** "new generation" fits the AI-era story; it is the weakest fit for "calm and plain", and its gradient is the "magic" cue Step 08 warned against.
- **How it differs from the closest measured competitor colour:** it is the **closest to the measured pages**: primary `#3B59F6` is 22.0 from Intelligems `#2962FF` and 23.4 from Shoplift `#4D65FF` (RGB, max 441.7; Shoplift is one use only), and 51.9 from Clarity violet. It would look like an AI-tool page. Competitors in Step 06: not measured.
- **Conflicts with "colours stay"** unless the user counts the screenshot blue as the brand blue (Step 03 R4).
| Role | Hex |
|---|---|
| Primary | `#3B59F6` |
| Primary hover | `#2F47D6` |
| Secondary / accent | `#5B54D4` |
| Accent tint (approval highlight bg) | `#EEF0FE` |
| Page background | `#FFFFFF` |
| Panel | `#F5F6FD` |
| Title text | `#14161F` |
| Body text | `#3A3D4D` |
| Muted text | `#5A5E72` |
| Border (UI, 3:1) | `#868BA5` |
| Divider (decorative only, carries no UI meaning) | `#E0E2F2` |
| Link | `#3B59F6` |
| Focus ring | `#2F47D6` |
| Success | `#1B7A47` |
| Success tint | `#E6F4EC` |
| Warning | `#8A5300` |
| Warning tint | `#FFF3D6` |
| Danger | `#B3261E` |
| Danger tint | `#FDECEA` |
| Dark panel (optional) | `#1A1D3A` |
| Muted text on dark panel | `#BCC0DA` |
| Gradient (optional) | `#4454D0` to `#6A63DE`, text only, max 1 phrase (ASSUMPTION, measured from the screenshot) |

- **Distance, primary to:** logo blue 43.4 (hue diff 10.4) · hero button 0.0 · gradient start 39.4 · gradient end 53.7 · `#0096ED` 85.3 (chat-only).
- **Thin margins:** link on accent tint 4.70:1, gradient end text 4.72:1, border on panel 3.12:1.

### Option 3 · Ink and Soft Fields (34/34) · NOT CHOSEN
- **Mood:** warm, friendly, grown-up. Buttons and titles are navy ink; blue appears in links, the approval step, and soft fields behind illustrations.
- **Supports the messaging:** quiet buttons and colour in the illustrations make the product demo the colourful thing and the claims calm; it follows the user's Calendly style direction most closely.
- **How it differs from the closest measured competitor colour:** the action colour is not blue, so primary `#1F2A44` is 195.5 from Intelligems and 201.4 from Shoplift. Its accent blue `#2A57B8` is 60.3 from Clarity `#0078D4` and 71.9 from Intelligems. **But** the ink and warm off-white are near Cursor's measured warm neutrals (primary 39.0 from `#26251E`; page 5.8 from `#F7F7F4`): Cursor is a reference, not a Step 06 competitor, and the counts are inline-CSS only. Shopify and the rest: not measured.
- **Risk:** the brand blue is weaker in the first screen; the logo is then the main blue. Warm off-white adds a second neutral (the panel is white).
- **Blue in use** is the accent `#2A57B8` (logo hue, darker, passes 4.5:1 as text), not the primary.
| Role | Hex |
|---|---|
| Primary | `#1F2A44` |
| Primary hover | `#121A2E` |
| Secondary / accent | `#2A57B8` |
| Accent tint (approval highlight bg) | `#E3EDFB` |
| Page background | `#FBFAF7` |
| Panel | `#FFFFFF` |
| Title text | `#1B2236` |
| Body text | `#373B43` |
| Muted text | `#5E6470` |
| Border (UI, 3:1) | `#8A8F9A` |
| Divider (decorative only, carries no UI meaning) | `#E6E3DC` |
| Link | `#2A57B8` |
| Focus ring | `#2A57B8` |
| Success | `#1B7A47` |
| Success tint | `#E6F4EC` |
| Warning | `#8A5300` |
| Warning tint | `#FFF3D6` |
| Danger | `#B3261E` |
| Danger tint | `#FDECEA` |
| Dark panel (optional) | `#1F2A44` |
| Muted text on dark panel | `#B9C0D0` |
| Gradient (optional) | soft field `#DCEBFB` to `#8BCDF6`, background only, no text on it, no text gradient |

- **Thin margin:** border on the off-white page 3.11:1 (needs 3); do not lighten it.
- **Distance, accent blue to:** logo blue 61.5 · hero button 64.3 · gradient start 35.5 · gradient end 75.4 · `#0096ED` 92.4 (chat-only). Ink primary to logo blue: 179.9 (not a blue).

### Recommendation (given before the choice; the user then chose Option 1, 2026-10-25)

**Option 1 · Logo-true Blue.** Reasons: it follows "name, logo, colours stay" and the Step 10 default; it keeps the logo blue the most recognisable (primary is 21.4 from it); it is the calmest and uses no gradient; and its soft sky fields borrow the Calendly fields idea at no cost. Honest trade-off: blue on white is also what the measured AI pages use, so the page's difference rests on wording and layout, not colour. If the user wants the Calendly feel strongest, Option 3 is the better pick. Option 2 is the least suited to the "calm, no magic" direction (Step 08, accepted at Gate 2) and sits closest to measured AI pages.

## Chosen palette — LOCKED

**LOCKED: Option 1 · Logo-true Blue.** Chosen by the user on 2026-10-25 ("Phương án 1"). Steps 17 and 18 may now use it. Options 2 and 3 above are **not chosen**. Hex values below are copied unchanged from the Option 1 table; the one added row is the soft-field set from the Amendment (ASSUMPTION until the Step 18 proof).

**Mood:** calm, plain, checkable. White page, cool grey panels, one blue. **Primary** `#4371CD` is the logo blue (`#497BDF`) scaled to 92% brightness, same hue (220), because white on the logo blue itself is 4.05:1 and fails 4.5:1 for button text. It is not a ShopBase-supplied colour (ASSUMPTION 3).

### Role table (LOCKED)

| Role | Hex | Usage |
|---|---|---|
| Primary | `#4371CD` | "Get started for free" buttons (header, hero, closing band) and the one approve control in the approval step. Never a section background, never body text |
| Primary hover | `#3A62B2` | Hover of the primary button; also the link colour |
| Secondary / accent | `#8BCDF6` | The logo's sky. Fields (tinted, see Amendment) and small markers; never text |
| Accent tint (approval highlight bg) | `#E7F3FD` | A found issue, a proposed fix, the approval-step highlight (title text on it, neutral) |
| Page background | `#FFFFFF` | Page |
| Panel | `#F4F7FC` | Cool grey panels, "Illustration" pill fill, footer fill (default, light) |
| Title text | `#1E222B` | Headlines, secondary-button text |
| Body text | `#373B43` | Paragraphs, the "Illustration" label, dark logo wordmark colour (as supplied) |
| Muted text | `#596070` | Captions, small lines. Never on a field stronger than F2 (see Amendment) |
| Border (UI, 3:1) | `#7F8A9E` | Inputs, secondary button outline. On page, panel and field F1 only |
| Divider (decorative only) | `#DDE3EE` | Hairlines that carry no UI meaning |
| Link | `#3A62B2` | Text links (same as primary hover) |
| Focus ring | `#1E4A9E` | 2px ring plus 2px offset on every interactive element |
| Success | `#1B7A47` | Only a state the seller caused (approved) |
| Success tint | `#E6F4EC` | Background of that state label |
| Warning | `#8A5300` | "Needs your decision" |
| Warning tint | `#FFF3D6` | Background of that label |
| Danger | `#B3261E` | Errors and destructive actions only |
| Danger tint | `#FDECEA` | Background of that label |
| Dark panel (optional) | `#1F2430` | Only if the user allows a dark surface (default no); on-dark button, focus and link colours are untested (rule 7) |
| Muted text on dark panel | `#B9C0D0` | Only on the dark panel |
| Soft fields | F1 Mist, F2 Sky, F3 Azure (hexes in the Amendment) | Behind illustrations and product cards only; supersedes the original "gradient: none" row |

Distance, primary to: logo blue 21.4 (hue diff 0) · hero button `#3B59F6` 48.2 · gradient start `#4454D0` 29.2 · gradient end `#6A63DE` 44.8 · `#0096ED` 83.0 (chat-only). Thin margins: white on primary 4.69:1 (needs 4.5), success text 4.72:1; do not lighten either.

### Contrast table (LOCKED palette) · 31/31 pass

Recomputed at the lock by a separate script (`lock16.py`, `python3 -I`, run from `/tmp`; WCAG 2.x relative luminance): it parsed the 31 Option 1 rows from this file, recomputed each ratio from the two hex values and compared with the printed number. **Result: 31 rows, 31 pass, 0 differences from the printed ratios (to 2 decimals).** The same 31 rows are printed again under "Contrast table → Option 1" below; the pass count is unchanged.

| Pair | Colours | Ratio | Need | Result |
|---|---|---|---|---|
| Title text on page | `#1E222B` on `#FFFFFF` | 15.92:1 | 4.5 | pass |
| Body text on page | `#373B43` on `#FFFFFF` | 11.24:1 | 4.5 | pass |
| Muted text on page | `#596070` on `#FFFFFF` | 6.30:1 | 4.5 | pass |
| Title text on panel | `#1E222B` on `#F4F7FC` | 14.83:1 | 4.5 | pass |
| Body text on panel | `#373B43` on `#F4F7FC` | 10.46:1 | 4.5 | pass |
| Muted text on panel | `#596070` on `#F4F7FC` | 5.87:1 | 4.5 | pass |
| White text on primary button | `#FFFFFF` on `#4371CD` | 4.69:1 | 4.5 | pass |
| White text on primary hover | `#FFFFFF` on `#3A62B2` | 5.88:1 | 4.5 | pass |
| Secondary button text (title colour) on page | `#1E222B` on `#FFFFFF` | 15.92:1 | 4.5 | pass |
| Link on page | `#3A62B2` on `#FFFFFF` | 5.88:1 | 4.5 | pass |
| Link on panel | `#3A62B2` on `#F4F7FC` | 5.48:1 | 4.5 | pass |
| Title text on accent tint (approval highlight) | `#1E222B` on `#E7F3FD` | 14.13:1 | 4.5 | pass |
| Link on accent tint | `#3A62B2` on `#E7F3FD` | 5.22:1 | 4.5 | pass |
| "Illustration" label (body colour) on its panel pill | `#373B43` on `#F4F7FC` | 10.46:1 | 4.5 | pass |
| Success text on success tint | `#1B7A47` on `#E6F4EC` | 4.72:1 | 4.5 | pass |
| Warning text on warning tint | `#8A5300` on `#FFF3D6` | 5.74:1 | 4.5 | pass |
| Danger text on danger tint | `#B3261E` on `#FDECEA` | 5.72:1 | 4.5 | pass |
| Border on page (UI) | `#7F8A9E` on `#FFFFFF` | 3.48:1 | 3 | pass |
| Border on panel (UI) | `#7F8A9E` on `#F4F7FC` | 3.24:1 | 3 | pass |
| Focus ring on page (UI) | `#1E4A9E` on `#FFFFFF` | 8.31:1 | 3 | pass |
| Focus ring on panel (UI) | `#1E4A9E` on `#F4F7FC` | 7.73:1 | 3 | pass |
| Primary button fill on page (UI boundary) | `#4371CD` on `#FFFFFF` | 4.69:1 | 3 | pass |
| Logo dark wordmark #373B43 on page | `#373B43` on `#FFFFFF` | 11.24:1 | 4.5 | pass |
| Logo dark wordmark #373B43 on panel | `#373B43` on `#F4F7FC` | 10.46:1 | 4.5 | pass |
| Logo icon blue #497BDF on page (graphic) | `#497BDF` on `#FFFFFF` | 4.05:1 | 3 | pass |
| Logo icon blue #497BDF on panel (graphic) | `#497BDF` on `#F4F7FC` | 3.77:1 | 3 | pass |
| Logo white wordmark on dark panel | `#FFFFFF` on `#1F2430` | 15.52:1 | 4.5 | pass |
| Logo icon blue #497BDF on dark panel (graphic) | `#497BDF` on `#1F2430` | 3.83:1 | 3 | pass |
| Logo icon sky #8BCDF6 on dark panel (graphic) | `#8BCDF6` on `#1F2430` | 8.99:1 | 3 | pass |
| Muted-on-dark text on dark panel | `#B9C0D0` on `#1F2430` | 8.51:1 | 4.5 | pass |
| Title text on sky accent fill #8BCDF6 | `#1E222B` on `#8BCDF6` | 9.22:1 | 4.5 | pass |

The 23 field pairs added by the Amendment are counted separately (23/23, below). The dark-panel rows pass as logo and text pairs only; the button, focus ring and link on the dark panel are still untested or fail (see "Pairs not in the table" and rule 7).

### Usage rules (LOCKED, Option 1)

Numbers are PROPOSALS (ASSUMPTION), not ShopBase rules.

| Rule | Locked value |
|---|---|
| Where the primary colour `#4371CD` may appear | Only the "Get started for free" buttons (header, hero, closing band) and the one approve control in the approval step. Links use the hover shade `#3A62B2`. Never as a section background, a field, or on body text |
| Secondary button | White fill, 1px border `#7F8A9E`, title-colour text ("Explore CR Scan AI"). On a field: only F1 with this border; on F2 use the field border `#66718A` (Amendment) |
| Maximum gradient phrases (text gradients) | **0**. No gradient on any text, ever |
| Soft colour fields (changed by the Amendment) | One field per illustration section, behind the illustration or product card only, built from the blue family, 2 stops (hexes in the Amendment). Replaces the earlier "no gradient anywhere" |
| Maximum dark panels | **0** by default. The footer may be dark **only if the user allows it** (Step 10 Q6, default no); the on-dark button, focus ring and link colours are untested and must be added and tested at Step 19 first |
| Page text | Title, body, muted as in the table. Muted text never on F3; only on page, panel, F1 and F2 |

Rules for every use of the palette:
1. **Proposed fix and approved states, without implying results.** A found issue and a proposed fix use the accent tint with title text (neutral), or the warning pair for "needs your decision". Success green appears only on a state the seller caused (the change was approved), as a state label, never beside a metric, score or percentage, never on a scan result, never on a button. Danger red is only for errors and destructive actions, not for "issues found". No colour carries a number; the page has none.
2. **"Illustration" label stays legible.** It sits in a solid pill (panel fill `#F4F7FC`, body-colour text `#373B43`, 12px or larger, weight 600, 1px border) that never sits directly on a gradient; the pill pair passes 10.46:1. If the pill touches a field, its border is the field border `#66718A` (tested on F1 and F2 in the Amendment). No opacity below 1 on the label.
3. **Logo.** `Logo (6).svg` on page and panel backgrounds, `Logo (1).svg` only on the dark panel, never the reverse; the logo is not recoloured. The logo never sits on a field (the sky strip of the icon is 1.35:1 to 1.64:1 on F1 and F2, computed).
4. **One saturated element per card** (the approve control), and at most one primary button per section (hero has the extra secondary button).
5. Focus ring: 2px ring plus 2px offset in `#1E4A9E` on every interactive element; never removed.
6. Border colour `#7F8A9E` is for UI outlines (inputs, secondary button); the decorative divider is not used where an edge must be visible.
7. **Dark panel needs its own colours before it is used.** On Option 1 the focus ring (1.87:1) and the link colour (2.64:1) fail on the dark panel (see "Pairs not in the table"). If the user allows a dark footer or closing band, Step 19 must add and test an on-dark focus ring and link colour first; until then no focus ring or link sits on a dark panel.
8. **The UI border `#7F8A9E` sits on page, panel and F1 only**; on F2 use `#66718A`, on F3 no border is drawn. Muted text and links never sit on F3.

## Contrast table

Computed by code, WCAG 2.x. Text pairs need 4.5:1 (body, button labels, links, chip text, the "Illustration" label); UI and graphic pairs need 3:1. Pass counts: **Option 1 31/31 · Option 2 34/34 · Option 3 34/34**. No pair was dropped; two values were adjusted during the run (Option 2 border `#8A8FA8` gave 2.96:1 on its panel and was changed to `#868BA5`; Option 1 border `#8590A3` gave exactly 3.00:1 on its panel and was changed to `#7F8A9E` for margin). Scripts (scratchpad, `python3 -I`, run from `/tmp`): `palette16_data.py` (colours and maths), `palette16_build.py` (writes both files and prints the report below). Path: `/private/tmp/claude-501/-Users-nguyentoan-Documents-SB-v2-LD/fb8c2ff0-4f7d-46ed-a2f8-aeb17aa0cde3/scratchpad/`.

### Option 1 (31/31)
| Pair | Colours | Ratio | Need | Result |
|---|---|---|---|---|
| Title text on page | `#1E222B` on `#FFFFFF` | 15.92:1 | 4.5 | pass |
| Body text on page | `#373B43` on `#FFFFFF` | 11.24:1 | 4.5 | pass |
| Muted text on page | `#596070` on `#FFFFFF` | 6.30:1 | 4.5 | pass |
| Title text on panel | `#1E222B` on `#F4F7FC` | 14.83:1 | 4.5 | pass |
| Body text on panel | `#373B43` on `#F4F7FC` | 10.46:1 | 4.5 | pass |
| Muted text on panel | `#596070` on `#F4F7FC` | 5.87:1 | 4.5 | pass |
| White text on primary button | `#FFFFFF` on `#4371CD` | 4.69:1 | 4.5 | pass |
| White text on primary hover | `#FFFFFF` on `#3A62B2` | 5.88:1 | 4.5 | pass |
| Secondary button text (title colour) on page | `#1E222B` on `#FFFFFF` | 15.92:1 | 4.5 | pass |
| Link on page | `#3A62B2` on `#FFFFFF` | 5.88:1 | 4.5 | pass |
| Link on panel | `#3A62B2` on `#F4F7FC` | 5.48:1 | 4.5 | pass |
| Title text on accent tint (approval highlight) | `#1E222B` on `#E7F3FD` | 14.13:1 | 4.5 | pass |
| Link on accent tint | `#3A62B2` on `#E7F3FD` | 5.22:1 | 4.5 | pass |
| "Illustration" label (body colour) on its panel pill | `#373B43` on `#F4F7FC` | 10.46:1 | 4.5 | pass |
| Success text on success tint | `#1B7A47` on `#E6F4EC` | 4.72:1 | 4.5 | pass |
| Warning text on warning tint | `#8A5300` on `#FFF3D6` | 5.74:1 | 4.5 | pass |
| Danger text on danger tint | `#B3261E` on `#FDECEA` | 5.72:1 | 4.5 | pass |
| Border on page (UI) | `#7F8A9E` on `#FFFFFF` | 3.48:1 | 3 | pass |
| Border on panel (UI) | `#7F8A9E` on `#F4F7FC` | 3.24:1 | 3 | pass |
| Focus ring on page (UI) | `#1E4A9E` on `#FFFFFF` | 8.31:1 | 3 | pass |
| Focus ring on panel (UI) | `#1E4A9E` on `#F4F7FC` | 7.73:1 | 3 | pass |
| Primary button fill on page (UI boundary) | `#4371CD` on `#FFFFFF` | 4.69:1 | 3 | pass |
| Logo dark wordmark #373B43 on page | `#373B43` on `#FFFFFF` | 11.24:1 | 4.5 | pass |
| Logo dark wordmark #373B43 on panel | `#373B43` on `#F4F7FC` | 10.46:1 | 4.5 | pass |
| Logo icon blue #497BDF on page (graphic) | `#497BDF` on `#FFFFFF` | 4.05:1 | 3 | pass |
| Logo icon blue #497BDF on panel (graphic) | `#497BDF` on `#F4F7FC` | 3.77:1 | 3 | pass |
| Logo white wordmark on dark panel | `#FFFFFF` on `#1F2430` | 15.52:1 | 4.5 | pass |
| Logo icon blue #497BDF on dark panel (graphic) | `#497BDF` on `#1F2430` | 3.83:1 | 3 | pass |
| Logo icon sky #8BCDF6 on dark panel (graphic) | `#8BCDF6` on `#1F2430` | 8.99:1 | 3 | pass |
| Muted-on-dark text on dark panel | `#B9C0D0` on `#1F2430` | 8.51:1 | 4.5 | pass |
| Title text on sky accent fill #8BCDF6 | `#1E222B` on `#8BCDF6` | 9.22:1 | 4.5 | pass |

### Option 2 (34/34)
| Pair | Colours | Ratio | Need | Result |
|---|---|---|---|---|
| Title text on page | `#14161F` on `#FFFFFF` | 18.04:1 | 4.5 | pass |
| Body text on page | `#3A3D4D` on `#FFFFFF` | 10.74:1 | 4.5 | pass |
| Muted text on page | `#5A5E72` on `#FFFFFF` | 6.40:1 | 4.5 | pass |
| Title text on panel | `#14161F` on `#F5F6FD` | 16.73:1 | 4.5 | pass |
| Body text on panel | `#3A3D4D` on `#F5F6FD` | 9.97:1 | 4.5 | pass |
| Muted text on panel | `#5A5E72` on `#F5F6FD` | 5.94:1 | 4.5 | pass |
| White text on primary button | `#FFFFFF` on `#3B59F6` | 5.32:1 | 4.5 | pass |
| White text on primary hover | `#FFFFFF` on `#2F47D6` | 7.02:1 | 4.5 | pass |
| Secondary button text (title colour) on page | `#14161F` on `#FFFFFF` | 18.04:1 | 4.5 | pass |
| Link on page | `#3B59F6` on `#FFFFFF` | 5.32:1 | 4.5 | pass |
| Link on panel | `#3B59F6` on `#F5F6FD` | 4.94:1 | 4.5 | pass |
| Title text on accent tint (approval highlight) | `#14161F` on `#EEF0FE` | 15.92:1 | 4.5 | pass |
| Link on accent tint | `#3B59F6` on `#EEF0FE` | 4.70:1 | 4.5 | pass |
| "Illustration" label (body colour) on its panel pill | `#3A3D4D` on `#F5F6FD` | 9.97:1 | 4.5 | pass |
| Success text on success tint | `#1B7A47` on `#E6F4EC` | 4.72:1 | 4.5 | pass |
| Warning text on warning tint | `#8A5300` on `#FFF3D6` | 5.74:1 | 4.5 | pass |
| Danger text on danger tint | `#B3261E` on `#FDECEA` | 5.72:1 | 4.5 | pass |
| Border on page (UI) | `#868BA5` on `#FFFFFF` | 3.36:1 | 3 | pass |
| Border on panel (UI) | `#868BA5` on `#F5F6FD` | 3.12:1 | 3 | pass |
| Focus ring on page (UI) | `#2F47D6` on `#FFFFFF` | 7.02:1 | 3 | pass |
| Focus ring on panel (UI) | `#2F47D6` on `#F5F6FD` | 6.51:1 | 3 | pass |
| Primary button fill on page (UI boundary) | `#3B59F6` on `#FFFFFF` | 5.32:1 | 3 | pass |
| Logo dark wordmark #373B43 on page | `#373B43` on `#FFFFFF` | 11.24:1 | 4.5 | pass |
| Logo dark wordmark #373B43 on panel | `#373B43` on `#F5F6FD` | 10.42:1 | 4.5 | pass |
| Logo icon blue #497BDF on page (graphic) | `#497BDF` on `#FFFFFF` | 4.05:1 | 3 | pass |
| Logo icon blue #497BDF on panel (graphic) | `#497BDF` on `#F5F6FD` | 3.76:1 | 3 | pass |
| Logo white wordmark on dark panel | `#FFFFFF` on `#1A1D3A` | 16.40:1 | 4.5 | pass |
| Logo icon blue #497BDF on dark panel (graphic) | `#497BDF` on `#1A1D3A` | 4.05:1 | 3 | pass |
| Logo icon sky #8BCDF6 on dark panel (graphic) | `#8BCDF6` on `#1A1D3A` | 9.50:1 | 3 | pass |
| Muted-on-dark text on dark panel | `#BCC0DA` on `#1A1D3A` | 9.13:1 | 4.5 | pass |
| White text on violet accent | `#FFFFFF` on `#5B54D4` | 5.73:1 | 4.5 | pass |
| Violet accent text on page | `#5B54D4` on `#FFFFFF` | 5.73:1 | 4.5 | pass |
| Gradient start #4454D0 text on page (if used) | `#4454D0` on `#FFFFFF` | 6.13:1 | 4.5 | pass |
| Gradient end #6A63DE text on page (if used) | `#6A63DE` on `#FFFFFF` | 4.72:1 | 4.5 | pass |

### Option 3 (34/34)
| Pair | Colours | Ratio | Need | Result |
|---|---|---|---|---|
| Title text on page | `#1B2236` on `#FBFAF7` | 15.14:1 | 4.5 | pass |
| Body text on page | `#373B43` on `#FBFAF7` | 10.76:1 | 4.5 | pass |
| Muted text on page | `#5E6470` on `#FBFAF7` | 5.70:1 | 4.5 | pass |
| Title text on panel | `#1B2236` on `#FFFFFF` | 15.81:1 | 4.5 | pass |
| Body text on panel | `#373B43` on `#FFFFFF` | 11.24:1 | 4.5 | pass |
| Muted text on panel | `#5E6470` on `#FFFFFF` | 5.94:1 | 4.5 | pass |
| White text on primary button | `#FFFFFF` on `#1F2A44` | 14.26:1 | 4.5 | pass |
| White text on primary hover | `#FFFFFF` on `#121A2E` | 17.31:1 | 4.5 | pass |
| Secondary button text (title colour) on page | `#1B2236` on `#FBFAF7` | 15.14:1 | 4.5 | pass |
| Link on page | `#2A57B8` on `#FBFAF7` | 6.38:1 | 4.5 | pass |
| Link on panel | `#2A57B8` on `#FFFFFF` | 6.66:1 | 4.5 | pass |
| Title text on accent tint (approval highlight) | `#1B2236` on `#E3EDFB` | 13.38:1 | 4.5 | pass |
| Link on accent tint | `#2A57B8` on `#E3EDFB` | 5.64:1 | 4.5 | pass |
| "Illustration" label (body colour) on its panel pill | `#373B43` on `#FFFFFF` | 11.24:1 | 4.5 | pass |
| Success text on success tint | `#1B7A47` on `#E6F4EC` | 4.72:1 | 4.5 | pass |
| Warning text on warning tint | `#8A5300` on `#FFF3D6` | 5.74:1 | 4.5 | pass |
| Danger text on danger tint | `#B3261E` on `#FDECEA` | 5.72:1 | 4.5 | pass |
| Border on page (UI) | `#8A8F9A` on `#FBFAF7` | 3.11:1 | 3 | pass |
| Border on panel (UI) | `#8A8F9A` on `#FFFFFF` | 3.24:1 | 3 | pass |
| Focus ring on page (UI) | `#2A57B8` on `#FBFAF7` | 6.38:1 | 3 | pass |
| Focus ring on panel (UI) | `#2A57B8` on `#FFFFFF` | 6.66:1 | 3 | pass |
| Primary button fill on page (UI boundary) | `#1F2A44` on `#FBFAF7` | 13.66:1 | 3 | pass |
| Logo dark wordmark #373B43 on page | `#373B43` on `#FBFAF7` | 10.76:1 | 4.5 | pass |
| Logo dark wordmark #373B43 on panel | `#373B43` on `#FFFFFF` | 11.24:1 | 4.5 | pass |
| Logo icon blue #497BDF on page (graphic) | `#497BDF` on `#FBFAF7` | 3.88:1 | 3 | pass |
| Logo icon blue #497BDF on panel (graphic) | `#497BDF` on `#FFFFFF` | 4.05:1 | 3 | pass |
| Logo white wordmark on dark panel | `#FFFFFF` on `#1F2A44` | 14.26:1 | 4.5 | pass |
| Logo icon blue #497BDF on dark panel (graphic) | `#497BDF` on `#1F2A44` | 3.52:1 | 3 | pass |
| Logo icon sky #8BCDF6 on dark panel (graphic) | `#8BCDF6` on `#1F2A44` | 8.26:1 | 3 | pass |
| Muted-on-dark text on dark panel | `#B9C0D0` on `#1F2A44` | 7.82:1 | 4.5 | pass |
| White text on accent blue (approve control) | `#FFFFFF` on `#2A57B8` | 6.66:1 | 4.5 | pass |
| Title text on soft field A #DCEBFB | `#1B2236` on `#DCEBFB` | 13.04:1 | 4.5 | pass |
| Title text on soft field B #8BCDF6 | `#1B2236` on `#8BCDF6` | 9.15:1 | 4.5 | pass |
| Accent blue on page (UI / text) | `#2A57B8` on `#FBFAF7` | 6.38:1 | 4.5 | pass |

### Pairs not in the table (computed at review, independent script, `python3 -I`)

These are not counted in the pass counts above, which cover the default page (light, no dark panel). They limit how some roles may be used (see Usage rules 7 and 8).

| Pair | Option 1 | Option 2 | Option 3 | Need |
|---|---|---|---|---|
| Primary button fill on the dark panel (UI boundary) | 3.31 pass | 3.08 pass (thin) | **1.00 fail** (button and dark panel are the same ink `#1F2A44`) | 3 |
| Focus ring on the dark panel (UI) | **1.87 fail** | **2.34 fail** | **2.14 fail** | 3 |
| Link colour on the dark panel (text) | **2.64 fail** | **3.08 fail** | **2.14 fail** | 4.5 |
| White title text on the dark panel | 15.52 pass | 16.40 pass | 14.26 pass | 4.5 |
| Border colour on the accent tint (UI) | 3.09 pass (thin) | **2.96 fail** | **2.74 fail** | 3 |
| Muted text on the accent tint | 5.59 pass | 5.65 pass | 5.03 pass | 4.5 |
| Body text on the accent tint | 9.97 pass | 9.48 pass | 9.51 pass | 4.5 |
| Primary button fill on panel (UI) | 4.36 pass | 4.94 pass | 14.26 pass | 3 |
| Muted text on the strongest soft-field colour (`#8BCDF6`; Option 2: `#F5F6FD`) | **3.65 fail** | 5.94 pass | **3.44 fail** | 4.5 |
| Option 2 gradient middle `#565CD7` on page | | 5.37 pass | | 4.5 |
| Option 3 accent approve control on accent tint / on `#8BCDF6` field (UI) | | | 5.64 / 3.86 pass | 3 |

Small text (12 to 14 px: the "Illustration" pill, chips, muted lines) is already tested at the full 4.5:1 level in the tables above. Disabled states: none; the default copy has no form and its button states are default, hover, focus-visible and pressed only (`14-copy.md`, Microcopy). The pressed state has no colour yet (Step 19).

### Script output (pasted, unedited)

```
script: palette16_check via palette16_build.py (python3 -I; WCAG 2.x relative luminance; Euclidean RGB distance, max 441.7)

== Option 1 Logo-true Blue: 31/31 pass
  PASS   15.92:1  (need 4.5)  #1E222B on #FFFFFF  Title text on page
  PASS   11.24:1  (need 4.5)  #373B43 on #FFFFFF  Body text on page
  PASS    6.30:1  (need 4.5)  #596070 on #FFFFFF  Muted text on page
  PASS   14.83:1  (need 4.5)  #1E222B on #F4F7FC  Title text on panel
  PASS   10.46:1  (need 4.5)  #373B43 on #F4F7FC  Body text on panel
  PASS    5.87:1  (need 4.5)  #596070 on #F4F7FC  Muted text on panel
  PASS    4.69:1  (need 4.5)  #FFFFFF on #4371CD  White text on primary button
  PASS    5.88:1  (need 4.5)  #FFFFFF on #3A62B2  White text on primary hover
  PASS   15.92:1  (need 4.5)  #1E222B on #FFFFFF  Secondary button text (title colour) on page
  PASS    5.88:1  (need 4.5)  #3A62B2 on #FFFFFF  Link on page
  PASS    5.48:1  (need 4.5)  #3A62B2 on #F4F7FC  Link on panel
  PASS   14.13:1  (need 4.5)  #1E222B on #E7F3FD  Title text on accent tint (approval highlight)
  PASS    5.22:1  (need 4.5)  #3A62B2 on #E7F3FD  Link on accent tint
  PASS   10.46:1  (need 4.5)  #373B43 on #F4F7FC  "Illustration" label (body colour) on its panel pill
  PASS    4.72:1  (need 4.5)  #1B7A47 on #E6F4EC  Success text on success tint
  PASS    5.74:1  (need 4.5)  #8A5300 on #FFF3D6  Warning text on warning tint
  PASS    5.72:1  (need 4.5)  #B3261E on #FDECEA  Danger text on danger tint
  PASS    3.48:1  (need 3.0)  #7F8A9E on #FFFFFF  Border on page (UI)
  PASS    3.24:1  (need 3.0)  #7F8A9E on #F4F7FC  Border on panel (UI)
  PASS    8.31:1  (need 3.0)  #1E4A9E on #FFFFFF  Focus ring on page (UI)
  PASS    7.73:1  (need 3.0)  #1E4A9E on #F4F7FC  Focus ring on panel (UI)
  PASS    4.69:1  (need 3.0)  #4371CD on #FFFFFF  Primary button fill on page (UI boundary)
  PASS   11.24:1  (need 4.5)  #373B43 on #FFFFFF  Logo dark wordmark #373B43 on page
  PASS   10.46:1  (need 4.5)  #373B43 on #F4F7FC  Logo dark wordmark #373B43 on panel
  PASS    4.05:1  (need 3.0)  #497BDF on #FFFFFF  Logo icon blue #497BDF on page (graphic)
  PASS    3.77:1  (need 3.0)  #497BDF on #F4F7FC  Logo icon blue #497BDF on panel (graphic)
  PASS   15.52:1  (need 4.5)  #FFFFFF on #1F2430  Logo white wordmark on dark panel
  PASS    3.83:1  (need 3.0)  #497BDF on #1F2430  Logo icon blue #497BDF on dark panel (graphic)
  PASS    8.99:1  (need 3.0)  #8BCDF6 on #1F2430  Logo icon sky #8BCDF6 on dark panel (graphic)
  PASS    8.51:1  (need 4.5)  #B9C0D0 on #1F2430  Muted-on-dark text on dark panel
  PASS    9.22:1  (need 4.5)  #1E222B on #8BCDF6  Title text on sky accent fill #8BCDF6

== Option 2 Blue-Violet: 34/34 pass
  PASS   18.04:1  (need 4.5)  #14161F on #FFFFFF  Title text on page
  PASS   10.74:1  (need 4.5)  #3A3D4D on #FFFFFF  Body text on page
  PASS    6.40:1  (need 4.5)  #5A5E72 on #FFFFFF  Muted text on page
  PASS   16.73:1  (need 4.5)  #14161F on #F5F6FD  Title text on panel
  PASS    9.97:1  (need 4.5)  #3A3D4D on #F5F6FD  Body text on panel
  PASS    5.94:1  (need 4.5)  #5A5E72 on #F5F6FD  Muted text on panel
  PASS    5.32:1  (need 4.5)  #FFFFFF on #3B59F6  White text on primary button
  PASS    7.02:1  (need 4.5)  #FFFFFF on #2F47D6  White text on primary hover
  PASS   18.04:1  (need 4.5)  #14161F on #FFFFFF  Secondary button text (title colour) on page
  PASS    5.32:1  (need 4.5)  #3B59F6 on #FFFFFF  Link on page
  PASS    4.94:1  (need 4.5)  #3B59F6 on #F5F6FD  Link on panel
  PASS   15.92:1  (need 4.5)  #14161F on #EEF0FE  Title text on accent tint (approval highlight)
  PASS    4.70:1  (need 4.5)  #3B59F6 on #EEF0FE  Link on accent tint
  PASS    9.97:1  (need 4.5)  #3A3D4D on #F5F6FD  "Illustration" label (body colour) on its panel pill
  PASS    4.72:1  (need 4.5)  #1B7A47 on #E6F4EC  Success text on success tint
  PASS    5.74:1  (need 4.5)  #8A5300 on #FFF3D6  Warning text on warning tint
  PASS    5.72:1  (need 4.5)  #B3261E on #FDECEA  Danger text on danger tint
  PASS    3.36:1  (need 3.0)  #868BA5 on #FFFFFF  Border on page (UI)
  PASS    3.12:1  (need 3.0)  #868BA5 on #F5F6FD  Border on panel (UI)
  PASS    7.02:1  (need 3.0)  #2F47D6 on #FFFFFF  Focus ring on page (UI)
  PASS    6.51:1  (need 3.0)  #2F47D6 on #F5F6FD  Focus ring on panel (UI)
  PASS    5.32:1  (need 3.0)  #3B59F6 on #FFFFFF  Primary button fill on page (UI boundary)
  PASS   11.24:1  (need 4.5)  #373B43 on #FFFFFF  Logo dark wordmark #373B43 on page
  PASS   10.42:1  (need 4.5)  #373B43 on #F5F6FD  Logo dark wordmark #373B43 on panel
  PASS    4.05:1  (need 3.0)  #497BDF on #FFFFFF  Logo icon blue #497BDF on page (graphic)
  PASS    3.76:1  (need 3.0)  #497BDF on #F5F6FD  Logo icon blue #497BDF on panel (graphic)
  PASS   16.40:1  (need 4.5)  #FFFFFF on #1A1D3A  Logo white wordmark on dark panel
  PASS    4.05:1  (need 3.0)  #497BDF on #1A1D3A  Logo icon blue #497BDF on dark panel (graphic)
  PASS    9.50:1  (need 3.0)  #8BCDF6 on #1A1D3A  Logo icon sky #8BCDF6 on dark panel (graphic)
  PASS    9.13:1  (need 4.5)  #BCC0DA on #1A1D3A  Muted-on-dark text on dark panel
  PASS    5.73:1  (need 4.5)  #FFFFFF on #5B54D4  White text on violet accent
  PASS    5.73:1  (need 4.5)  #5B54D4 on #FFFFFF  Violet accent text on page
  PASS    6.13:1  (need 4.5)  #4454D0 on #FFFFFF  Gradient start #4454D0 text on page (if used)
  PASS    4.72:1  (need 4.5)  #6A63DE on #FFFFFF  Gradient end #6A63DE text on page (if used)

== Option 3 Ink and Soft Fields: 34/34 pass
  PASS   15.14:1  (need 4.5)  #1B2236 on #FBFAF7  Title text on page
  PASS   10.76:1  (need 4.5)  #373B43 on #FBFAF7  Body text on page
  PASS    5.70:1  (need 4.5)  #5E6470 on #FBFAF7  Muted text on page
  PASS   15.81:1  (need 4.5)  #1B2236 on #FFFFFF  Title text on panel
  PASS   11.24:1  (need 4.5)  #373B43 on #FFFFFF  Body text on panel
  PASS    5.94:1  (need 4.5)  #5E6470 on #FFFFFF  Muted text on panel
  PASS   14.26:1  (need 4.5)  #FFFFFF on #1F2A44  White text on primary button
  PASS   17.31:1  (need 4.5)  #FFFFFF on #121A2E  White text on primary hover
  PASS   15.14:1  (need 4.5)  #1B2236 on #FBFAF7  Secondary button text (title colour) on page
  PASS    6.38:1  (need 4.5)  #2A57B8 on #FBFAF7  Link on page
  PASS    6.66:1  (need 4.5)  #2A57B8 on #FFFFFF  Link on panel
  PASS   13.38:1  (need 4.5)  #1B2236 on #E3EDFB  Title text on accent tint (approval highlight)
  PASS    5.64:1  (need 4.5)  #2A57B8 on #E3EDFB  Link on accent tint
  PASS   11.24:1  (need 4.5)  #373B43 on #FFFFFF  "Illustration" label (body colour) on its panel pill
  PASS    4.72:1  (need 4.5)  #1B7A47 on #E6F4EC  Success text on success tint
  PASS    5.74:1  (need 4.5)  #8A5300 on #FFF3D6  Warning text on warning tint
  PASS    5.72:1  (need 4.5)  #B3261E on #FDECEA  Danger text on danger tint
  PASS    3.11:1  (need 3.0)  #8A8F9A on #FBFAF7  Border on page (UI)
  PASS    3.24:1  (need 3.0)  #8A8F9A on #FFFFFF  Border on panel (UI)
  PASS    6.38:1  (need 3.0)  #2A57B8 on #FBFAF7  Focus ring on page (UI)
  PASS    6.66:1  (need 3.0)  #2A57B8 on #FFFFFF  Focus ring on panel (UI)
  PASS   13.66:1  (need 3.0)  #1F2A44 on #FBFAF7  Primary button fill on page (UI boundary)
  PASS   10.76:1  (need 4.5)  #373B43 on #FBFAF7  Logo dark wordmark #373B43 on page
  PASS   11.24:1  (need 4.5)  #373B43 on #FFFFFF  Logo dark wordmark #373B43 on panel
  PASS    3.88:1  (need 3.0)  #497BDF on #FBFAF7  Logo icon blue #497BDF on page (graphic)
  PASS    4.05:1  (need 3.0)  #497BDF on #FFFFFF  Logo icon blue #497BDF on panel (graphic)
  PASS   14.26:1  (need 4.5)  #FFFFFF on #1F2A44  Logo white wordmark on dark panel
  PASS    3.52:1  (need 3.0)  #497BDF on #1F2A44  Logo icon blue #497BDF on dark panel (graphic)
  PASS    8.26:1  (need 3.0)  #8BCDF6 on #1F2A44  Logo icon sky #8BCDF6 on dark panel (graphic)
  PASS    7.82:1  (need 4.5)  #B9C0D0 on #1F2A44  Muted-on-dark text on dark panel
  PASS    6.66:1  (need 4.5)  #FFFFFF on #2A57B8  White text on accent blue (approve control)
  PASS   13.04:1  (need 4.5)  #1B2236 on #DCEBFB  Title text on soft field A #DCEBFB
  PASS    9.15:1  (need 4.5)  #1B2236 on #8BCDF6  Title text on soft field B #8BCDF6
  PASS    6.38:1  (need 4.5)  #2A57B8 on #FBFAF7  Accent blue on page (UI / text)

== Distances (RGB Euclidean, hue difference in degrees)
Option 1 blue in use = #4371CD (primary), hue 220; primary = #4371CD, hue 220
    #4371CD vs logo blue #497BDF:  21.4 ( 4.9% of max), hue diff  0.0
    #4371CD vs hero button #3B59F6:  48.2 (10.9% of max), hue diff 10.4
    #4371CD vs hero gradient start #4454D0:  29.2 ( 6.6% of max), hue diff 13.1
    #4371CD vs hero gradient end #6A63DE:  44.8 (10.1% of max), hue diff 23.4
    #4371CD vs scale blue #0096ED (chat-only):  83.0 (18.8% of max), hue diff 18.0
Option 2 blue in use = #3B59F6 (primary), hue 230; primary = #3B59F6, hue 230
    #3B59F6 vs logo blue #497BDF:  43.4 ( 9.8% of max), hue diff 10.4
    #3B59F6 vs hero button #3B59F6:   0.0 ( 0.0% of max), hue diff  0.0
    #3B59F6 vs hero gradient start #4454D0:  39.4 ( 8.9% of max), hue diff  2.8
    #3B59F6 vs hero gradient end #6A63DE:  53.7 (12.2% of max), hue diff 13.0
    #3B59F6 vs scale blue #0096ED (chat-only):  85.3 (19.3% of max), hue diff 28.3
Option 3 blue in use = #2A57B8 (accent), hue 221; primary = #1F2A44, hue 222
    #2A57B8 vs logo blue #497BDF:  61.5 (13.9% of max), hue diff  1.0
    #2A57B8 vs hero button #3B59F6:  64.3 (14.6% of max), hue diff  9.4
    #2A57B8 vs hero gradient start #4454D0:  35.5 ( 8.0% of max), hue diff 12.2
    #2A57B8 vs hero gradient end #6A63DE:  75.4 (17.1% of max), hue diff 22.4
    #2A57B8 vs scale blue #0096ED (chat-only):  92.4 (20.9% of max), hue diff 19.0
    (ink primary #1F2A44 vs logo blue: 179.9)

== Distances to measured reference-site colours (Step 08, inline-CSS counts only, rendered NOT VERIFIED)
Option 1 primary #4371CD vs Intelligems #2962FF (R3, 7 uses in inline CSS):  58.3
Option 1 primary #4371CD vs Shoplift #4D65FF (R4, 1 use: too few to say anything):  52.4
Option 1 primary #4371CD vs Clarity violet #6A5AE0 (R5, 12 uses):  49.1
Option 1 primary #4371CD vs Clarity blue #0078D4 (R5, 11 uses):  67.7
Option 1 primary #4371CD vs Cursor ink #26251E (R1, 4 uses): 193.0
Option 1 page #FFFFFF vs Cursor warm off-white #F7F7F4 (R1, 2 uses):  15.8
Option 2 primary #3B59F6 vs Intelligems #2962FF (R3, 7 uses in inline CSS):  22.0
Option 2 primary #3B59F6 vs Shoplift #4D65FF (R4, 1 use: too few to say anything):  23.4
Option 2 primary #3B59F6 vs Clarity violet #6A5AE0 (R5, 12 uses):  51.9
Option 2 primary #3B59F6 vs Clarity blue #0078D4 (R5, 11 uses):  74.8
Option 2 primary #3B59F6 vs Cursor ink #26251E (R1, 4 uses): 223.2
Option 2 page #FFFFFF vs Cursor warm off-white #F7F7F4 (R1, 2 uses):  15.8
Option 3 primary #1F2A44 vs Intelligems #2962FF (R3, 7 uses in inline CSS): 195.5
Option 3 primary #1F2A44 vs Shoplift #4D65FF (R4, 1 use: too few to say anything): 201.4
Option 3 primary #1F2A44 vs Clarity violet #6A5AE0 (R5, 12 uses): 179.6
Option 3 primary #1F2A44 vs Clarity blue #0078D4 (R5, 11 uses): 166.7
Option 3 primary #1F2A44 vs Cursor ink #26251E (R1, 4 uses):  39.0
Option 3 page #FBFAF7 vs Cursor warm off-white #F7F7F4 (R1, 2 uses):   5.8
Option 3 accent #2A57B8 vs Intelligems #2962FF (R3, 7 uses in inline CSS):  71.9
Option 3 accent #2A57B8 vs Shoplift #4D65FF (R4, 1 use: too few to say anything):  80.4
Option 3 accent #2A57B8 vs Clarity violet #6A5AE0 (R5, 12 uses):  75.5
Option 3 accent #2A57B8 vs Clarity blue #0078D4 (R5, 11 uses):  60.3
Option 3 accent #2A57B8 vs Cursor ink #26251E (R1, 4 uses): 162.0
```

## Usage rules

> **Superseded for the build:** the locked rules are in "Chosen palette — LOCKED → Usage rules (LOCKED, Option 1)" and the Amendment below. The three-option comparison table that follows is kept for the record; Options 2 and 3 are not chosen.

Rules apply to the chosen option. Numbers below are PROPOSALS (ASSUMPTION), not ShopBase rules.

| Rule | Option 1 · Logo-true Blue | Option 2 · Blue-Violet | Option 3 · Ink and Soft Fields |
|---|---|---|---|
| Where the primary colour may appear | `#4371CD` only: the "Get started for free" buttons (header, hero, closing band), and the one approve control in the approval step. Links use the hover shade `#3A62B2`. Never as a section background or on body text | `#3B59F6` only: the "Get started for free" buttons and the one approve control; links same blue. Violet accent `#5B54D4` only as a small tag or marker, never a button | Ink `#1F2A44` for every button and the dark panel. Blue (`#2A57B8`) only for links, the approval-step highlight and the approve control. Never for body text |
| Secondary button | White fill, 1px border `#7F8A9E`, title-colour text ("Explore CR Scan AI") | White fill, 1px border `#868BA5`, title-colour text | Off-white fill, 1px border `#8A8F9A`, title-colour text |
| Maximum gradient phrases | **0** (no gradient) | **1** at most (hero second line, ASSUMPTION), recommended **0** because Step 08's accepted colour direction advises against a "magic AI" gradient | **0** text gradients; soft field gradient behind illustration cards only, no text on it |
| Maximum dark panels | 0 by default; 1 at most (footer or closing band) only if the user allows dark surfaces (Step 10 Q6, default no) | same | 1 at most (footer or closing band), same condition |
| Soft fields | one per illustration card, decorative | one per illustration card, plain tint only | one per illustration card; the strongest colour inside a card is the approve control |
| Page text | title, body, muted as in the table; muted text never on a field | same | same |

Rules for all options:
1. **Proposed fix and approved states, without implying results.** A found issue and a proposed fix use the **accent tint with title text** (neutral), or the warning pair for "needs your decision". **Success green appears only on a state the seller caused** (the change was approved), as a state label, never beside a metric, score or percentage, never on a scan result, never on a button. **Danger red is only for errors and destructive actions**, not for "issues found". No colour carries a number; the page has none.
2. **"Illustration" label stays legible.** It sits in a solid pill (panel fill, body-colour text, 12px or larger, weight 600, 1px border) and never sits directly on a field or gradient; the pill pair passes 10.46:1 (Option 1), 9.97:1 (Option 2), 11.24:1 (Option 3). No opacity below 1 on the label.
3. **Logo.** `Logo (6).svg` on page and panel backgrounds, `Logo (1).svg` only on the dark panel, never the reverse; the logo is not recoloured.
4. **One saturated element per card**, and at most one primary button per section (hero has the extra secondary button).
5. Focus ring: 2px ring plus 2px offset in the focus colour on every interactive element; never removed.
6. Border colour is for UI outlines (inputs, secondary button); the decorative divider is not used where an edge must be visible.
7. **Dark panel needs its own colours before it is used.** On every option the focus ring and the link colour fail on the dark panel, and in Option 3 the ink button is invisible on the ink dark panel (1.00:1; see "Pairs not in the table"). If the user allows a dark footer or closing band, Step 19 must add and test an on-dark button, focus ring and link colour first; until then no button or link sits on a dark panel.
8. **The UI border colour sits on page and panel only**, never on the accent tint (Option 2 2.96:1, Option 3 2.74:1 fail there). Muted text never sits on a soft field (fails in Options 1 and 3).

## Amendment: Calendly-style visual direction (user decision 2026-10-25)

**Decision (`_progress.md`, Decisions log, 2026-10-25):** the page follows Calendly's visual approach closely (layout rhythm, card system, spacing, type hierarchy, treatment of colour fields behind product cards) while its content differs so that it foregrounds the USP. We reproduce the approach, never Calendly's assets, illustrations, wording or exact artwork. **What this changes in this file:** the earlier default "no gradient" (Step 08 colour direction, accepted at Gate 2) no longer bans soft colour fields behind illustrations and product cards. **What it does not change:** no gradient on text, no "AI magic" look (no glow, sparkle, neon), Option 1's hexes, the primary-colour rule, the "Illustration" label rule, the no-numbers rule.

**Status of everything below: ASSUMPTION until the user sees the Step 18 proof.** The tint hexes are mine, derived by mixing white with the logo's own colours (`#497BDF`, `#8BCDF6`); they are not ShopBase-supplied values.

### The three soft fields

Each field is a flat tint or a 2-stop soft gradient (linear or radial, plain, no pattern, no noise). Stops are mixes of white with the logo blue `#497BDF` or the logo sky `#8BCDF6`. Contrast was computed at **both stops** (the worst stop is the one that counts).

| Field | Stop 1 | Stop 2 | Derived as | Lightest to darkest luminance | Where it may sit |
|---|---|---|---|---|---|
| F1 Mist | `#F3FAFE` | `#EDF2FC` | white + 10% sky; white + 10% logo blue | 0.946 to 0.885 | Behind any illustration or product card; text may sit directly on it (for example the hero and S07). S09 has no illustration and stays on a plain band (`14-copy.md`), so it gets no field |
| F2 Sky | `#D1EBFB` | `#D9E4F9` | white + 40% sky; white + about 20% logo blue, rounded by hand (an exact 20% mix would be `#DBE5F9`; the hex used and tested is `#D9E4F9`) | 0.799 to 0.771 | Behind illustration cards; text may sit directly on it (title, body, muted, link) |
| F3 Azure | `#C5E6FA` | `#A4BDEF` | white + 50% sky; white + 50% logo blue | 0.754 to 0.505 | Behind illustration cards only; the strongest, **text-free** except title and body (cards cover the content) |

New role, needed because the standard border `#7F8A9E` fails on F2: **Field border `#66718A`** (same cool-grey family as the border and muted text: hue about 222, between `#7F8A9E` and `#596070` in lightness). It is for the outline of a card, the secondary button or the "Illustration" pill when it touches F1 or F2 (on F1 the standard border also passes). Where the same pill or button also meets the page or panel, the field border still passes there (review, independent script: 4.89:1 on page `#FFFFFF`, 4.55:1 on panel `#F4F7FC`, 4.34:1 on accent tint `#E7F3FD`; need 3).

### Contrast on the fields (computed by code)

Script: `fields16_check2.py` (`python3 -I`, run from `/tmp`, WCAG 2.x). Text pairs need 4.5:1, UI and graphic pairs 3:1. Ratios are shown as `stop 1 / stop 2`; the pair passes only if both do. Scratchpad: `/private/tmp/claude-501/-Users-nguyentoan-Documents-SB-v2-LD/fb8c2ff0-4f7d-46ed-a2f8-aeb17aa0cde3/scratchpad/`.

| Pair (colour on field) | Hex | F1 Mist | F2 Sky | F3 Azure | Need |
|---|---|---|---|---|---|
| Title text | `#1E222B` | 15.10 / 14.18 pass | 12.88 / 12.45 pass | 12.19 / 8.42 pass | 4.5 |
| Body text | `#373B43` | 10.66 / 10.01 pass | 9.09 / 8.78 pass | 8.60 / 5.94 pass | 4.5 |
| Muted text | `#596070` | 5.98 / 5.61 pass | 5.10 / 4.93 pass | 4.82 / **3.33 fail** | 4.5 |
| Link | `#3A62B2` | 5.58 / 5.24 pass | 4.76 / 4.60 pass (thin) | 4.50 / **3.11 fail** | 4.5 |
| Logo dark wordmark (text) | `#373B43` | 10.66 / 10.01 pass | 9.09 / 8.78 pass | 8.60 / 5.94 pass | 4.5 |
| UI border, standard | `#7F8A9E` | 3.30 / 3.10 pass | **2.82 / 2.72 fail** | **2.66 / 1.84 fail** | 3 |
| Field border (new) | `#66718A` | 4.64 / 4.36 pass | 3.96 / 3.82 pass | **3.74 / 2.59 fail** | 3 |
| Primary button fill (UI) | `#4371CD` | 4.44 / 4.17 pass | 3.79 / 3.66 pass | **3.59 / 2.48 fail** | 3 |
| Focus ring | `#1E4A9E` | 7.88 / 7.40 pass | 6.72 / 6.49 pass | 6.36 / 4.39 pass | 3 |
| Logo icon blue (graphic) | `#497BDF` | 3.84 / 3.61 pass | 3.28 / 3.17 pass | **3.10 / 2.14 fail** | 3 |
| Logo icon sky strip (graphic, thin, not counted as in the main table) | `#8BCDF6` | 1.64 / 1.54 | 1.40 / 1.35 | 1.32 / 1.10 | 3 |
| White wordmark (`Logo (1).svg`) | `#FFFFFF` | 1.05 / 1.12 | 1.24 / 1.28 | 1.31 / 1.89 | 4.5 |
| White card edge vs field (information only, a card is not a control) | `#FFFFFF` | 1.05 / 1.12 | 1.24 / 1.28 | 1.31 / 1.89 | n/a |

**What is allowed to touch each field, and the count.** Allowed means the pair passes at both stops; the fails above are the reason a pair is **not allowed**, not a pair that was dropped to hide a failure.
- **F1 Mist: 10 allowed pairs, 10/10 pass** (title, body, muted, link, dark wordmark text, standard border, field border, primary button fill, focus ring, logo icon blue).
- **F2 Sky: 9 allowed pairs, 9/9 pass** (the same list without the standard border, which failed at 2.82 / 2.72: fixed by the field border `#66718A`, 3.96 / 3.82).
- **F3 Azure: 4 allowed pairs, 4/4 pass** (title, body, dark wordmark text, focus ring). Muted text, link, both borders, the primary button and the logo icon fail on it, so **nothing but title text, body text and the focus ring may touch F3**; cards sit on it without a border, and any button sits inside a white card.
- **Total 23/23 allowed field pairs pass.** The white logo wordmark fails on all three fields (1.05 to 1.89:1), so `Logo (1).svg` never sits on a field.
- **The logo pairs pass but do not put the logo on a field.** The dark wordmark and the logo icon blue are in the count because they were tested; rule 3 still keeps the whole logo off every field, because its sky strip is 1.10 to 1.64:1 on F1 to F3.

**Fixes made by adjusting the tint, as the step requires.** First draft tints (F1 `#EEF8FE`/`#E4EBFA`, F2 `#DCF0FC`/`#C8D7F5`) failed: F1 border 2.91:1 at its darker stop; F2 muted text 4.35, link 4.06, border 2.40 and logo icon 2.80. The tints were lightened to the values above (F1 now passes the standard border; F2 passes muted, link and logo icon). F2 could not pass the standard border without becoming almost white, so for F2 the **colour** was adjusted instead (new field border `#66718A`); this is a judgment call and is flagged in the report.

**Two cautions.** (1) F2's link margin is thin (4.60:1 at stop 2, needs 4.5): do not darken F2's second stop. (2) A field's pattern or noise would change these numbers: the fields stay plain; if the user later wants a pattern (own shapes, Step 17), the tests must run again.

### Rules for fields (these update the usage rules)

| Rule | Value |
|---|---|
| Source of colour | Only Option 1's blue family: logo blue `#497BDF` / primary `#4371CD`, logo sky `#8BCDF6`, and their tints F1, F2, F3. No lilac, pink, teal, yellow or any other hue |
| Gradient on text | **0**. Never |
| Gradient (field) count | One field per illustration section, behind its illustration or product card. Page maximum: one per illustration section (P01·A: S03, S05, S06, S07, S08; P01·B: S10, S12, S08, S07); F3 on at most 2 sections per page (ASSUMPTION) |
| "AI magic" cues | None: no glow, sparkle, neon edge, animated shimmer, particles. A field is a still, soft wash |
| Text on a field | Only the pairs listed above as allowed; any other colour needs a new test first. Headlines and body text on F1 or F2 are allowed; on F3 only title and body, and by default the content sits inside a white card instead |
| Cards on a field | White card, large radius, soft shadow; the card border is none, or `#7F8A9E` on F1, or `#66718A` on F2, never on F3 |
| "Illustration" label | Stays in its solid panel pill (`#373B43` on `#F4F7FC`, 10.46:1); the pill sits on the white card by default; if it touches F1 or F2 its border is `#66718A`; never directly on F3 |
| Dark panels | Still **0 by default**. The footer may be dark **only if the user allows it**; the on-dark focus ring and link colour are untested (1.87:1 and 2.64:1 on `#1F2430`, rule 7) and must be added and tested at Step 19 first. The default footer is `#F4F7FC` with body and muted text (tested on panel) |
| Primary colour | Unchanged: buttons and the one approve control; never a field |

### What of Calendly's colour use Option 1 cannot reproduce

Seen in the slices of `02-assets/moodboard/style-ref-01-calendly-fullpage.png` (hero and the following blocks, the "Built for" block, the alternating feature rows, the customer-stories band, the integrations grid, the closing call to action and the dark footer; colours judged by eye, I did not sample pixel values, so every colour statement below is an observation by eye, not a measurement).

| Calendly (seen) | With Option 1 |
|---|---|
| **Warm off-white page** and warm beige-grey rounded containers behind the hero and the four-card band | **Not reproducible.** Option 1 keeps a white page `#FFFFFF` and cool grey panels `#F4F7FC` (Option 3's warm `#FBFAF7` was not chosen) |
| **Several hue families on the fields**: blue to lilac to pink (hero edge, recaps, stories band), teal to green to yellow (assistant field, payments field), deep navy at the bottom of some fields | **Not reproducible.** Only the blue family: pale cyan-to-periwinkle at most (F1 to F3). No lilac, pink, teal, green or yellow, and no deep navy base on a field (a field that dark would need white text or be text-free, and was not tested) |
| **Navy buttons and navy headings** (a near-black navy) | **Not reproducible.** Buttons are the logo-blue primary `#4371CD`; titles are the cool near-black `#1E222B` |
| **A full-width saturated band** (customer stories: blue to lilac to pink, white title on it) | **Not reproducible.** No full-bleed saturated band: no tested white-on-blue background exists besides the primary button, and the section itself (customer stories) is not ours |
| **Serif headlines** in the feature rows | Not a colour issue, but not reproducible by default: the font is Inter only (Step 10, Q3); a serif is the user's call |
| **Dark navy rounded footer panel** | Not by default: footer is light unless the user allows a dark footer (and then on-dark colours must be tested first) |
| **Contour-line wavy field pattern, notched card row, tinted glows around cards** | Not reproduced: own shapes at Step 17 (identity imagery rule 5); plain soft fields only |
| **Colour from photos** (portraits, customer logos, partner logos in colour) | None of these exist on our page (identity imagery rules 2 and 3) |

**So Option 1 keeps a white or near-white cool page and the blue family only. The result will resemble Calendly's structure (rounded containers, white cards on soft colour fields, alternating rows, one clear button) but not its colours; Calendly's warmth, multi-hue fields and navy are the part that does not carry over. That is the user's choice** (Option 1 chosen 2026-10-25 together with the Calendly-style direction; Option 3 would have been closer to Calendly's colours and was not chosen).

## Assumptions

1. Light mode only; dark panels are optional and default to none until the user answers Step 10 Q6 (ASSUMPTION).
2. Inter is the type face (unconfirmed, Step 10 Q3).
3. Primary `#4371CD` (Option 1) is a darkened logo blue chosen to pass 4.5:1 with white; it is not a ShopBase-supplied colour. The same holds for every hex that is not a logo or screenshot value (neutrals, tints, status colours, accent `#5B54D4`, ink `#1F2A44`, accent blue `#2A57B8`): all are mine (ASSUMPTION).
4. Option 3's warm off-white `#FBFAF7` is my choice by eye; Calendly's value was not sampled.
5. Hero screenshot blues are sampled from an image and may differ from the source CSS; `#0096ED` is chat-only.
6. Competitor colour comparisons use only the Step 08 inline-CSS counts (rendered colours not verified); Step 06 competitors' colours were not measured.
7. Status colours and tints are shared across the three options (same hexes); only neutrals, blues and dark panels differ.
8. Contrast was measured on flat colours; text over images or soft-field gradients is not used (labels sit in solid pills). The headline gradient in Option 2 is tested at both end colours only.
9. The mock uses only copy from `14-copy.md`'s default page (hero A headline and sub-line, button labels, the S07 headline, body and caption, the header link label "Login" and the "Illustration" label); the chip words "Success / Warning / Danger" and the demo labels ("Primary hover", "Focus ring", "Panel surface, …", "Approval step highlight:") are palette labels, not page copy.
10. The preview was checked in headless Chrome at 1440 px and at exactly 375 px (a 375 px iframe, because the headless window will not go below 500 px), with Inter loaded and with Google Fonts blocked (fallback font): no element wider than the viewport, all logo images load. Not checked on a real phone.
11. Not used here: Calendly's wavy field pattern and notched cards (Step 10 rule: own shapes at Step 17).
12. (Lock, 2026-10-25) Option 1 is chosen; Options 2 and 3 are kept as "not chosen" and are not used. Their numbers stay unchanged.
13. (Amendment) The field tints F1, F2, F3, the field border `#66718A` and every rule in the Amendment are my derivations, ASSUMPTION until the user sees the Step 18 proof. They were tested on flat stops; a field is a plain 2-stop wash, and any pattern or noise needs a new test.
14. (Amendment) Calendly's colours in the slices are judged by eye, not sampled.
15. (Amendment) "Maximum fields per page" and "F3 on at most 2 sections" are proposals, not ShopBase rules.
16. (Amendment) A dark footer stays off unless the user allows it; its on-dark focus ring and link colours are untested.

## Open questions

### 🔴 Must answer
1. ~~Which option (1, 2 or 3)?~~ **Answered 2026-10-25: Option 1 ("Phương án 1"), LOCKED.** None open.

### 🟡 Should answer
2. Allow a dark panel (footer or closing band)? *Default: no; `Logo (1).svg` stays unused.*
3. ~~If Option 2: keep the one gradient phrase?~~ Not applicable (Option 2 not chosen). Text gradient stays 0.
3b. Do you accept the field tints F1 Mist, F2 Sky, F3 Azure and the field border `#66718A`? *Default: used as an ASSUMPTION; you see them on the Step 18 proof and can change them then.*
4. Confirm Inter. *Default: Inter.*

### ⚪ Nice to have
5. Supply the `#0096ED` colour scale as a file so it can be cited. *Default: it stays chat-only and unverified.*

## Check before handing back

- [x] Contrast was computed for every pair and the pass count is reported (Option 1 31/31, Option 2 34/34, Option 3 34/34).
- [x] Type C: exactly three options were derived; one recommendation was labelled (before the choice).
- [x] Types A, C: exactly one option is marked LOCKED by the user's choice: Option 1 · Logo-true Blue (user, 2026-10-25); Options 2 and 3 marked "not chosen".
- [x] The locked option's contrast was recomputed by code at the lock: 31/31, no difference from the printed ratios; the Amendment's field pairs: 23/23 allowed pairs pass.
- [x] Usage rules state where the primary colour may appear.
- [x] Light mode only; logo tested in both dark-wordmark and white-wordmark forms on each option's backgrounds.
- [x] Preview checked at 375 px wide (headless Chrome, 375 px iframe, with and without Inter): no horizontal overflow; the "PASS" labels were breaking mid-word and were fixed at review.
- [ ] Preview verified on a real phone. NOT RUN: no device.
