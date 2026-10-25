# 19 · Token mapping

Project: ShopBase website redesign · type **C · Rebrand** · page P01 Home (variants P01·A and P01·B) · light mode only (frame lock) · Gate 6 `APPROVED` (2026-10-25).
Files: `07-tokens/1-primitive.json` (raw values, neutral names) · `07-tokens/2-semantic.json` (roles that alias primitives, `{path}` syntax) · this file. Tokens are approved with the spec at Gate 7.

Sources: every primitive value comes from `06-proof-ui/proof.html` `:root` (base block and the three media-query blocks) or from `03-research/16-palette.md` (locked Option 1 role table and the Amendment). The proof was not changed. Format: W3C design tokens (`$type`, `$value`, `$description`); dimensions are strings with a unit; non-standard on purpose (values kept equal to the proof): the angle is typed `dimension` (DTCG has no angle type), the grid templates `string` (not a DTCG type), letter spacing is in `em` (DTCG dimension allows px and rem only) and the shadows write a unitless `0`; the logo ratio uses `number`, which is standard. The semantic file has one mode (light). Typography roles are DTCG composites (family, size, weight, line height, letter spacing). There is **no component tier** and **no duration or easing token**: the proof has no `transition` or `animation`.

## 1. Every `:root` variable of the proof

Parsed by code (`tokens19_check.py`) from the first `:root` block (83 variables). Status: `mapped` = has a token and the proof uses it on the page; `presentation-only` = used only by the proof's own chrome (canvas, legend, wrapper, placeholder bars); `unused` = declared and never referenced anywhere. **For `mapped` and `presentation-only` rows that have a token, the token's resolved value was compared with the variable's computed value: 77 comparisons, 0 differences.** "Refs" = direct `var(--x)` uses outside `:root`; 5 variables have 0 direct uses but are reached through other variables, so none is `unused`.

| CSS variable | Proof value | Semantic token | Primitive it resolves to | Status | Refs | Note |
|---|---|---|---|---|---|---|
| `--color-primary` | `#4371CD` | `color.action.primary` | `color.blue.600` | mapped | 2 |  |
| `--color-primary-hover` | `#3A62B2` | `color.action.primary-hover` | `color.blue.700` | mapped | 2 |  |
| `--color-on-primary` | `#FFFFFF` | `color.text.on-primary` | `color.white` | mapped | 1 |  |
| `--color-accent-tint` | `#E7F3FD` | `color.surface.accent` | `color.sky.100` | mapped | 1 |  |
| `--color-page` | `#FFFFFF` | `color.surface.page` | `color.white` | mapped | 7 |  |
| `--color-panel` | `#F4F7FC` | `color.surface.panel` | `color.neutral.50` | mapped | 2 |  |
| `--color-title` | `#1E222B` | `color.text.title` | `color.neutral.900` | mapped | 10 |  |
| `--color-body` | `#373B43` | `color.text.body` | `color.neutral.800` | mapped | 9 |  |
| `--color-muted` | `#596070` | `color.text.muted` | `color.neutral.700` | mapped | 2 |  |
| `--color-border` | `#7F8A9E` | `color.border.default` | `color.neutral.500` | mapped | 2 |  |
| `--color-border-field` | `#66718A` | `color.border.field` | `color.neutral.600` | mapped | 1 |  |
| `--color-divider` | `#DDE3EE` | `color.border.divider` | `color.neutral.200` | mapped | 2 |  |
| `--color-link` | `#3A62B2` | `color.text.link` | `color.blue.700` | mapped | 1 |  |
| `--color-focus` | `#1E4A9E` | `color.focus.ring` | `color.blue.800` | mapped | 2 |  |
| `--color-canvas` | `#DDE3EE` | `color.surface.canvas` | `color.neutral.200` | presentation-only | 1 | grey canvas around the frames; proof chrome, not a page surface |
| `--color-bar` | `#DDE3EE` | (none) | `color.neutral.200` | presentation-only | 1 | fill of the placeholder illustration bars; no semantic token on purpose (aliases the divider colour) |
| `--field-1-a` | `#F3FAFE` | `color.field.1.stop-1` | `color.sky.50` | mapped | 1 |  |
| `--field-1-b` | `#EDF2FC` | `color.field.1.stop-2` | `color.blue.50` | mapped | 1 |  |
| `--field-2-a` | `#D1EBFB` | `color.field.2.stop-1` | `color.sky.200` | mapped | 1 |  |
| `--field-2-b` | `#D9E4F9` | `color.field.2.stop-2` | `color.blue.100` | mapped | 1 |  |
| `--field-3-a` | `#C5E6FA` | `color.field.3.stop-1` | `color.sky.300` | mapped | 1 |  |
| `--field-3-b` | `#A4BDEF` | `color.field.3.stop-2` | `color.blue.300` | mapped | 1 |  |
| `--field-angle` | `135deg` | `field.angle` | `angle.135` | mapped | 3 |  |
| `--shadow-card` | `0 0.5rem 2rem rgba(30, 34, 43, 0.10)` | `shadow.card` | `shadow.soft` | mapped | 1 |  |
| `--shadow-device` | `0 0.75rem 2.5rem rgba(30, 34, 43, 0.16)` | `shadow.device` | `shadow.lifted` | presentation-only | 1 | shadow of the outer proof wrapper (.frame-device) only; the token exists because the brief asks for it |
| `--font-sans` | `"Inter", system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif` | `font.family.base` | `font.family.sans` | mapped | 1 |  |
| `--fs-n1` | `0.8rem` | (none) | `font.size.n1` | mapped | 0 | scale step; reached through typography.caption |
| `--fs-0` | `1rem` | (none) | `font.size.0` | mapped | 1 | scale step; reached through typography.base, lead-mobile, paragraph-mobile |
| `--fs-1` | `1.25rem` | (none) | `font.size.1` | mapped | 2 | scale step; reached through typography.lead, body |
| `--fs-2` | `1.5625rem` | (none) | `font.size.2` | mapped | 0 | scale step; reached through typography.section-headline-mobile |
| `--fs-3` | `1.953rem` | (none) | `font.size.3` | mapped | 1 | scale step; reached through typography.hero-headline-mobile |
| `--fs-4` | `2.441rem` | (none) | `font.size.4` | mapped | 0 | scale step; reached through typography.section-headline |
| `--fs-5` | `3.052rem` | (none) | `font.size.5` | mapped | 0 | scale step; reached through typography.hero-headline |
| `--fw-regular` | `400` | (none) | `font.weight.regular` | mapped | 1 | reached through typography.* |
| `--fw-medium` | `500` | (none) | `font.weight.medium` | mapped | 1 | reached through typography.caption |
| `--fw-semibold` | `600` | (none) | `font.weight.semibold` | mapped | 12 | reached through typography.hero-headline, section-headline |
| `--lh-tight` | `1.1` | (none) | `font.line-height.tight` | mapped | 2 | reached through typography.hero-headline |
| `--lh-heading` | `1.2` | (none) | `font.line-height.snug` | mapped | 4 | reached through typography.section-headline |
| `--lh-body` | `1.55` | (none) | `font.line-height.relaxed` | mapped | 4 | reached through typography.lead, body, base, caption |
| `--ls-tight` | `-0.02em` | (none) | `font.letter-spacing.tight` | mapped | 3 | reached through typography headlines |
| `--ls-label` | `0.04em` | (none) | `font.letter-spacing.wide` | mapped | 3 | reached through typography.caption |
| `--size-hero` | `3.052rem` | `typography.hero-headline.fontSize` | `font.size.5` | mapped | 1 |  |
| `--size-h2` | `2.441rem` | `typography.section-headline.fontSize` | `font.size.4` | mapped | 1 |  |
| `--size-lead` | `1.25rem` | `typography.lead.fontSize` | `font.size.1` | mapped | 2 |  |
| `--size-body` | `1rem` | `typography.base.fontSize` | `font.size.0` | mapped | 4 | paragraph text in the frames uses --size-lead instead (see typography.paragraph) |
| `--size-caption` | `0.8rem` | `typography.caption.fontSize` | `font.size.n1` | mapped | 7 |  |
| `--space-1` | `0.25rem` | `space.stack.xs` | `space.1` | mapped | 2 |  |
| `--space-2` | `0.5rem` | `space.stack.sm` | `space.2` | mapped | 5 |  |
| `--space-3` | `1rem` | `space.stack.md` | `space.3` | mapped | 12 |  |
| `--space-4` | `1.5rem` | `space.stack.lg` | `space.4` | mapped | 12 |  |
| `--space-5` | `2.5rem` | `space.stack.xl` | `space.5` | mapped | 5 |  |
| `--space-6` | `4rem` | `space.stack.2xl` | `space.6` | mapped | 5 |  |
| `--space-7` | `6rem` | (none) | `space.7` | mapped | 0 | top step; reached through space.section |
| `--section-gap` | `6rem` | `space.section` | `space.7` | mapped | 1 |  |
| `--gutter` | `2.5rem` | `space.gutter` | `space.5` | mapped | 4 |  |
| `--field-pad` | `4rem` | `space.field-pad` | `space.6` | mapped | 1 |  |
| `--container` | `75rem` | `layout.container.base` | `size.1200` | mapped | 3 | declared 75rem does not apply at any whole-pixel width (the two media queries leave only widths strictly between 1439px and 1440px); compact and wide tokens carry the real values |
| `--legend-col` | `14rem` | (none) | (none) | presentation-only | 1 | min width of the label column in the intro frame index (proof chrome); no token on purpose |
| `--frame-max` | `90rem` | `layout.page.frame-max` | `size.1440` | presentation-only | 1 | width of the proof's device wrapper (1440 frame) |
| `--text-measure` | `38rem` | `layout.measure.text` | `size.608` | mapped | 2 |  |
| `--hero-text-measure` | `54rem` | `layout.measure.hero` | `size.864` | mapped | 2 |  |
| `--card-min-h` | `18rem` | `layout.card.min-height` | `size.288` | mapped | 1 |  |
| `--card-max-w` | `46rem` | `layout.card.max-width` | `size.736` | mapped | 1 |  |
| `--control-h` | `3.25rem` | `size.control-height` | `size.52` | mapped | 1 |  |
| `--icon` | `1.25rem` | `size.icon` | `size.20` | mapped | 2 |  |
| `--bar-h` | `0.75rem` | (none) | (none) | presentation-only | 1 | height of placeholder illustration bars; no token on purpose |
| `--bar-short` | `40%` | (none) | (none) | presentation-only | 1 | width of a placeholder bar (40%); no token on purpose |
| `--bar-mid` | `70%` | (none) | (none) | presentation-only | 1 | width of a placeholder bar (70%); no token on purpose |
| `--bar-long` | `100%` | (none) | (none) | presentation-only | 1 | width of a placeholder bar (100%); no token on purpose |
| `--split-cols` | `5fr 7fr` | `layout.split.columns` | `grid.columns.5-7` | mapped | 1 |  |
| `--split-cols-reverse` | `7fr 5fr` | `layout.split.columns-reverse` | `grid.columns.7-5` | mapped | 1 |  |
| `--line` | `1px` | `border.width.default` | `border.width.1` | mapped | 4 |  |
| `--line-dashed` | `2px` | `border.width.strong` | `border.width.2` | mapped | 1 |  |
| `--focus-w` | `2px` | `focus.ring.width` | `outline.width` | mapped | 2 |  |
| `--focus-offset` | `2px` | `focus.ring.offset` | `outline.offset` | mapped | 2 |  |
| `--logo-w` | `7.5rem` | `layout.logo.min-width` | `size.120` | presentation-only | 1 | width of the logo in the proof legend (frames hold no logo); equals the identity minimum, token kept for later steps |
| `--logo-clear` | `calc(7.5rem * 0.0945)` | `layout.logo.clear-space-ratio` | `ratio.0945` | presentation-only | 1 | legend only; proof computes calc(logo-w * 0.0945); the token holds the ratio |
| `--radius-field` | `2rem` | `radius.field` | `radius.32` | mapped | 1 |  |
| `--radius-card` | `1.5rem` | `radius.card` | `radius.24` | mapped | 2 |  |
| `--radius-inner` | `1rem` | `radius.inner` | `radius.16` | mapped | 3 |  |
| `--radius-control` | `0.75rem` | `radius.control` | `radius.12` | mapped | 3 | same value as radius.button |
| `--radius-pill` | `62rem` | `radius.pill` | `radius.992` | mapped | 1 |  |
| `--radius-bar` | `0.375rem` | (none) | (none) | presentation-only | 1 | radius of placeholder bars; no token on purpose (0.375rem is not in the primitive file) |

**Counts:** 83 variables · 71 mapped · 12 presentation-only · 0 unused. Variables reached only through another variable (0 direct uses): `--fs-n1`, `--fs-2`, `--fs-4`, `--fs-5` (through the `--size-*` role variables) and `--space-7` (through `--section-gap`).

### Responsive values (the proof re-points variables in three media-query `:root` blocks)

Each re-pointed value was resolved with the CSS cascade (base, then the max-width 1439 block, then the max-width 767 block) and compared with its token.

| Where | Variable | Computed value | Token | Match |
|---|---|---|---|---|
| mobile | `--size-hero` | `1.953rem` | `typography.hero-headline-mobile.fontSize` | yes |
| mobile | `--size-h2` | `1.5625rem` | `typography.section-headline-mobile.fontSize` | yes |
| mobile | `--size-lead` | `1rem` | `typography.lead-mobile.fontSize` | yes |
| mobile | `--size-lead` | `1rem` | `typography.paragraph-mobile.fontSize` | yes |
| mobile | `--size-body` | `1rem` | `typography.base.fontSize` | yes |
| mobile | `--section-gap` | `4rem` | `space.section-mobile` | yes |
| mobile | `--gutter` | `1.5rem` | `space.gutter-mobile` | yes |
| mobile | `--field-pad` | `1rem` | `space.field-pad-mobile` | yes |
| mobile | `--radius-field` | `1rem` | `radius.field-mobile` | yes |
| mobile | `--radius-card` | `1rem` | `radius.card-mobile` | yes |
| mobile | `--card-min-h` | `15rem` | `layout.card.min-height-mobile` | yes |
| mobile | `--space-4` | `1.5rem` | `space.card-pad-mobile` | yes |
| compact (max 1439) | `--container` | `68rem` | `layout.container.compact` | yes |
| compact (max 1439) | `--gutter` | `2.5rem` | `space.gutter` | yes |
| wide (min 1440) | `--container` | `80rem` | `layout.container.wide` | yes |
| desktop base | `--size-lead` | `1.25rem` | `typography.paragraph.fontSize` | yes |
| desktop base | `--space-5` | `2.5rem` | `space.card-pad` | yes |
| desktop base | `--size-hero` | `3.052rem` | `typography.hero-headline.fontSize` | yes |

## 2. Open decisions the tokens fix (approved as shown at Gate 6, may be refined at Step 20/21)

The Gate 6 line in `_progress.md` names three visual judgement calls (hero field width, card shadow exception, amount of blue) but no file defines them in detail. The readings below are mine, taken from what `proof.html` shows; the values are exact.

| Call | Exact values fixed as tokens | Status |
|---|---|---|
| Hero field width | Measured at review: at 1440 the hero field is 1280px wide (= the 80rem container, 89% of the viewport; Calendly's is about 79%) and the hero card 736px; at 375 the field fills the content width and the card is the field minus 2 × 16px. The hero field (F2) fills the full content width: `layout.container.compact` 68rem below 1440, `layout.container.wide` 80rem from 1440 (both = `size.1088` / `size.1280`); padding inside the field `space.field-pad` 4rem (mobile 1rem); the card inside is centred, `layout.card.max-width` 46rem; field radius `radius.field` 2rem (mobile 1rem). The hero headline measure is `layout.measure.hero` 54rem, the lead `layout.measure.text` 38rem | approved as shown, may be refined at Step 20/21 |
| Card shadow exception | Reading: the exception is to the Step 18 rule "shadows go on an outer wrapper, never inside the section frame"; the proof puts one shadow inside the frames, on white cards on a field (measured at 1440 and 375: the only box-shadow inside any frame is `.card`, 0 8px 32px rgba(30,34,43,0.1); inner cards none; no card border). White cards on a field have the soft shadow and no border: `shadow.card` = 0 0.5rem 2rem at #1E222B 10%. An inner card inside a card has no shadow (the proof sets `box-shadow: none`). The only other shadow, `shadow.device` = 0 0.75rem 2.5rem at #1E222B 16%, belongs to the proof's outer wrapper and is not part of the page. Cards on the plain page get no shadow in this proof (there are none); the moodboard rule "hairline border or panel fill, no shadow" for them is not tokenised | approved as shown, may be refined at Step 20/21 |
| Amount of blue | `color.action.primary` #4371CD only on the Get started buttons; `color.text.link` and hover #3A62B2; `color.focus.ring` #1E4A9E; blue inside the soft fields only: F1 #F3FAFE to #EDF2FC, F2 #D1EBFB to #D9E4F9, F3 #C5E6FA to #A4BDEF at `field.angle` 135deg; accent tint #E7F3FD inside inner cards. Page and cards stay white, panel #F4F7FC. Fields used in the proof: F2 in S03, S10, S06; F1 in S05; F3 in S12, S07 | approved as shown, may be refined at Step 20/21 |

## 3. Tokens that exist but the proof does not use (for later steps)

Semantic tokens with no proof variable behind them:

- `color.accent.sky`: palette secondary/accent (logo sky); small markers, never text; the proof draws none
- `color.status.success.text`: status colour pair from the locked palette; the proof has no status label
- `color.status.success.tint`: status colour pair from the locked palette; the proof has no status label
- `color.status.warning.text`: status colour pair from the locked palette; the proof has no status label
- `color.status.warning.tint`: status colour pair from the locked palette; the proof has no status label
- `color.status.danger.text`: status colour pair from the locked palette; the proof has no status label
- `color.status.danger.tint`: status colour pair from the locked palette; the proof has no status label
- `radius.button`: same value as `radius.control`; the proof's buttons use `--radius-control`
- `layout.breakpoint.mobile-max`: mirrors a media query of the proof (the proof writes the number inside `@media`, not in a variable)
- `layout.breakpoint.compact-max`: mirrors a media query of the proof (the proof writes the number inside `@media`, not in a variable)
- `layout.breakpoint.wide-min`: mirrors a media query of the proof (the proof writes the number inside `@media`, not in a variable)
- `layout.viewport.mobile-design`: mirrors a media query of the proof (the proof writes the number inside `@media`, not in a variable)

Primitives not referenced by any semantic token: `font.ratio.scale` (documents the 1.25 ratio; each step is stored as a rem value). Every other primitive is aliased by at least one semantic token. Also tokenised but used only by presentation-only variables: `layout.page.frame-max`, `layout.logo.min-width`, `layout.logo.clear-space-ratio`, `color.surface.canvas`, `shadow.device`.

Deliberately **not** tokenised: the dark panel colours (`#1F2430`, `#B9C0D0`: dark surfaces are off by default and their on-dark focus ring and link are untested, palette rule 7), the logo colours (assets, used as supplied), the placeholder-bar sizes and radius (`--bar-*`, `--radius-bar`) and `--legend-col` (proof chrome only), the pressed state of the button (palette notes it has no colour yet; the proof draws none).

## 4. Things found while tokenising (report, not silently fixed)

1. **Palette and proof agree on every colour.** All 16 colour variables compared with the locked role table and Amendment (12 roles, 3 fields with 2 stops each counted as 3 pairs, the field border): 0 disagreements.
2. **`--container: 75rem` never applies in practice.** The two media queries (max-width 1439 and min-width 1440) cover every whole-pixel width (only a fractional width strictly between 1439px and 1440px, for example under browser zoom, would fall through), so the content width is 68rem or 80rem. Both are tokens (`layout.container.compact`, `.wide`); `layout.container.base` keeps the declared 75rem.
3. **Mobile radius.** In the 767 block `--radius-field: var(--radius-card)` while `--radius-card` is also re-pointed to `--radius-inner`; custom properties resolve at the computed value, so both are 1rem on mobile, not 1.5rem for the field. Tokens `radius.field-mobile` and `radius.card-mobile` hold 1rem. **Confirmed at review by rendering the proof at 375 (headless Chrome, 375 px iframe):** field, white card and inner card all have a 16px corner in every frame, so on mobile the "inner smaller than parent" radius family does not hold (the field and card corners look concentric-equal). The token reading is right; the proof's 767 block most likely meant field 1.5rem, card 1rem. Open for Step 20/21: if 1.5rem is wanted, change `radius.field-mobile` to `{radius.24}` there; the proof is not edited.
4. **Body text size.** In the frames, paragraph text (`.text-body`) uses `--size-lead` (1.25rem, 1rem on mobile), not `--size-body` (1rem). So `typography.paragraph` equals `typography.lead`, and `--size-body` maps to `typography.base` (page base and button label size). Naming quirk of the proof; values are as rendered. (Renamed at review from `typography.body`/`body-mobile` to `typography.paragraph`/`paragraph-mobile`, so Step 20 does not read "body" as the proof's 1rem `--size-body`.)
5. **Colours that exist only in the palette, not in the proof's `:root`:** `color.sky.400` (#8BCDF6) and the six status colours and tints. They match the locked role table.
6. **Breakpoints and 375.** `breakpoint.767/1439/1440` come from the proof's media queries and `viewport.375` from its "Mobile (375)" comment, not from `:root` variables; this is the one place the "values only from `:root`" rule is relaxed, as the brief asked for breakpoints.
7. **Logo clear space.** The proof's `calc(var(--logo-w) * 0.0945)` equals 24/254 from `04-brand/10-identity.md` (0.0945); `size.120` (7.5rem) equals the 120px minimum full-logo width in that file. Both are identity proposals, not ShopBase rules.
8. **Type scale.** 7 steps (n1, 0 to 5), ratio 1.25 from 1rem; rem values are the proof's rounded numbers (for example 1.953rem, 2.441rem, 3.052rem), not recomputed.

## 5. Measured (by code)

Script: `tokens19_check.py` (`python3 -I`, run from the scratchpad folder outside the project, scratchpad `/private/tmp/claude-501/-Users-nguyentoan-Documents-SB-v2-LD/fb8c2ff0-4f7d-46ed-a2f8-aeb17aa0cde3/scratchpad/`). It checks JSON validity and duplicate keys, counts tokens, resolves every alias recursively, detects cycles and raw values in the semantic file, parses the proof's `:root` blocks, compares token values with the proof's computed values, finds unused variables, checks leftovers against the proof and the locked palette, compares the proof with the palette tables, and computes contrast from the token values. Output pasted unedited:

```
JSON valid (no duplicate keys): 1-primitive.json
JSON valid (no duplicate keys): 2-semantic.json
Tokens: primitive = 80 | semantic = 87 | total = 167
Tokens without a $type (own or inherited): 0 []
Aliases inside primitive file: 0 []
Semantic alias references: 122
Broken aliases: 0 []
Cycles: 0 []
Raw (non-alias) values in semantic file: 0 []
Proof :root variables (base block): 83 | media :root blocks: ['max-width: 1439px', 'min-width: 1440px', 'max-width: 767px']
Variables with no direct var() use outside :root: ['--fs-n1', '--fs-2', '--fs-4', '--fs-5', '--space-7']
Variables never reached (unused, incl. via other root vars): []
Variable -> token value checks run: 77 | value differences: 0 []
Status counts: mapped = 71 | presentation-only = 12 | unused = 0 | total = 83
Responsive/derived value checks: 18 | differences: 0 []
    mobile --size-hero = 1.953rem -> typography.hero-headline-mobile.fontSize OK
    mobile --size-h2 = 1.5625rem -> typography.section-headline-mobile.fontSize OK
    mobile --size-lead = 1rem -> typography.lead-mobile.fontSize OK
    mobile --size-lead = 1rem -> typography.body-mobile.fontSize OK
    mobile --size-body = 1rem -> typography.base.fontSize OK
    mobile --section-gap = 4rem -> space.section-mobile OK
    mobile --gutter = 1.5rem -> space.gutter-mobile OK
    mobile --field-pad = 1rem -> space.field-pad-mobile OK
    mobile --radius-field = 1rem -> radius.field-mobile OK
    mobile --radius-card = 1rem -> radius.card-mobile OK
    mobile --card-min-h = 15rem -> layout.card.min-height-mobile OK
    mobile --space-4 = 1.5rem -> space.card-pad-mobile OK
    compact (max 1439) --container = 68rem -> layout.container.compact OK
    compact (max 1439) --gutter = 2.5rem -> space.gutter OK
    wide (min 1440) --container = 80rem -> layout.container.wide OK
    desktop base --size-lead = 1.25rem -> typography.body.fontSize OK
    desktop base --space-5 = 2.5rem -> space.card-pad OK
    desktop base --size-hero = 3.052rem -> typography.hero-headline.fontSize OK
Typography composite parts checked against .title-hero/.title-section/.text-lead/.text-caption CSS: 8 OK
Dimension/number primitives that equal no resolved :root variable value: 2 [('font.ratio.scale', 1.25), ('ratio.logo-clear', 0.0945)]
Primitive values from a sample or earlier project / not traceable: 0 []
Primitive values traceable only outside :root variables (listed, not leftovers): 1
    ('viewport.375', '375px', "proof CSS comment 'Mobile (375)' and frame width; not a :root variable")
Colour primitives not in proof :root (traced to 16-palette LOCKED only): ['color.sky.400', 'color.green.50', 'color.green.700', 'color.amber.50', 'color.amber.700', 'color.red.50', 'color.red.700']
Earlier-project / reference-site names found in token files: []
Proof :root colour variables compared with palette role table: 16 | disagreements: 0 []
Palette status/extra roles in role table: {'Secondary / accent': '#8BCDF6', 'Success': '#1B7A47', 'Success tint': '#E6F4EC', 'Warning': '#8A5300', 'Warning tint': '#FFF3D6', 'Danger': '#B3261E', 'Danger tint': '#FDECEA', 'Dark panel (optional)': '#1F2430', 'Muted text on dark panel': '#B9C0D0'}
Status colours and accent sky equal palette role table: OK (7 values)
Logo clear ratio: 24/254 = 0.0945 | token 0.0945
Transitions / animations / easing in proof: 0 (none, so no duration/easing tokens)
Contrast pairs computed from token values: 62 | pass: 62 | fail: 0
Pairs that also appear in 16-palette LOCKED table: 20 | ratio differences >0.006: 0 []
   lowest: 3.09:1 (need 3) color.border.default on color.surface.accent  #7F8A9E on #E7F3FD
   lowest: 3.10:1 (need 3) color.border.default on color.field.1.stop-2  #7F8A9E on #EDF2FC
   lowest: 3.24:1 (need 3) color.border.default on color.surface.panel  #7F8A9E on #F4F7FC
   lowest: 3.30:1 (need 3) color.border.default on color.field.1.stop-1  #7F8A9E on #F3FAFE
   lowest: 3.48:1 (need 3) color.border.default on color.surface.page  #7F8A9E on #FFFFFF
   lowest: 3.66:1 (need 3) color.action.primary on color.field.2.stop-2  #4371CD on #D9E4F9
```

### Contrast of the text and UI roles against the surfaces they are meant for

Recomputed from resolved token values (WCAG 2.x). 62 pairs, 62 pass. 20 of them also appear in the locked contrast table of `16-palette.md` and match its printed ratios to 2 decimals (reference: that table, rows with the same two hexes). Rules from the palette are applied: muted text and links are not paired with F3; the standard border is not paired with F2 or F3; the field border is not paired with F3; the primary fill is not paired with F3. Field pairs list the weaker of the two stops. Thin margins: border on F1 stop 2 3.10, link on F2 stop 2 4.60 (palette caution: do not darken F2 stop 2).

**Review correction (independent script):** two rows below are **not palette-allowed pairs** and are kept for information only: muted text on the accent tint (5.59) and the UI border `#7F8A9E` on the accent tint (3.09). The locked role table and usage rules put muted text only on page, panel, F1 and F2, and the UI border only on page, panel and F1. Two allowed pairs were missing and are added at the end: title text on the logo sky `#8BCDF6` (9.22, locked table) and the primary fill on the panel (4.36, palette "pairs not in the table"). **Palette-allowed set: 62 pairs (per stop), 62 pass; thinnest 3.10 (UI border on F1 stop 2), then link on F2 stop 2 4.60.** The semantic file's descriptions already state these limits (`color.text.muted`, `color.border.default`, and now `color.surface.accent`).

| Foreground token | Background token(s) | Colours | Lowest ratio | Need | Result |
|---|---|---|---|---|---|
| `color.text.title` | `color.surface.page` | #1E222B on #FFFFFF | 15.92 | 4.5 | pass |
| `color.text.title` | `color.surface.panel` | #1E222B on #F4F7FC | 14.83 | 4.5 | pass |
| `color.text.title` | `color.surface.accent` | #1E222B on #E7F3FD | 14.13 | 4.5 | pass |
| `color.text.title` | `color.field.1` | #1E222B on #EDF2FC | 14.18 | 4.5 | pass |
| `color.text.title` | `color.field.2` | #1E222B on #D9E4F9 | 12.45 | 4.5 | pass |
| `color.text.title` | `color.field.3` | #1E222B on #A4BDEF | 8.42 | 4.5 | pass |
| `color.text.body` | `color.surface.page` | #373B43 on #FFFFFF | 11.24 | 4.5 | pass |
| `color.text.body` | `color.surface.panel` | #373B43 on #F4F7FC | 10.46 | 4.5 | pass |
| `color.text.body` | `color.surface.accent` | #373B43 on #E7F3FD | 9.97 | 4.5 | pass |
| `color.text.body` | `color.field.1` | #373B43 on #EDF2FC | 10.01 | 4.5 | pass |
| `color.text.body` | `color.field.2` | #373B43 on #D9E4F9 | 8.78 | 4.5 | pass |
| `color.text.body` | `color.field.3` | #373B43 on #A4BDEF | 5.94 | 4.5 | pass |
| `color.text.muted` | `color.surface.page` | #596070 on #FFFFFF | 6.30 | 4.5 | pass |
| `color.text.muted` | `color.surface.panel` | #596070 on #F4F7FC | 5.87 | 4.5 | pass |
| `color.text.muted` | `color.surface.accent` | #596070 on #E7F3FD | 5.59 | 4.5 | pass, but NOT an allowed pair (information only) |
| `color.text.muted` | `color.field.1` | #596070 on #EDF2FC | 5.61 | 4.5 | pass |
| `color.text.muted` | `color.field.2` | #596070 on #D9E4F9 | 4.93 | 4.5 | pass |
| `color.text.link` | `color.surface.page` | #3A62B2 on #FFFFFF | 5.88 | 4.5 | pass |
| `color.text.link` | `color.surface.panel` | #3A62B2 on #F4F7FC | 5.48 | 4.5 | pass |
| `color.text.link` | `color.surface.accent` | #3A62B2 on #E7F3FD | 5.22 | 4.5 | pass |
| `color.text.link` | `color.field.1` | #3A62B2 on #EDF2FC | 5.24 | 4.5 | pass |
| `color.text.link` | `color.field.2` | #3A62B2 on #D9E4F9 | 4.60 | 4.5 | pass |
| `color.text.on-primary` | `color.action.primary` | #FFFFFF on #4371CD | 4.69 | 4.5 | pass |
| `color.text.on-primary` | `color.action.primary-hover` | #FFFFFF on #3A62B2 | 5.88 | 4.5 | pass |
| `color.status.success.text` | `color.status.success.tint` | #1B7A47 on #E6F4EC | 4.72 | 4.5 | pass |
| `color.status.warning.text` | `color.status.warning.tint` | #8A5300 on #FFF3D6 | 5.74 | 4.5 | pass |
| `color.status.danger.text` | `color.status.danger.tint` | #B3261E on #FDECEA | 5.72 | 4.5 | pass |
| `color.border.default` | `color.surface.page` | #7F8A9E on #FFFFFF | 3.48 | 3 | pass |
| `color.border.default` | `color.surface.panel` | #7F8A9E on #F4F7FC | 3.24 | 3 | pass |
| `color.border.default` | `color.surface.accent` | #7F8A9E on #E7F3FD | 3.09 | 3 | pass, but NOT an allowed pair (information only) |
| `color.border.default` | `color.field.1` | #7F8A9E on #EDF2FC | 3.10 | 3 | pass |
| `color.border.field` | `color.surface.page` | #66718A on #FFFFFF | 4.89 | 3 | pass |
| `color.border.field` | `color.surface.panel` | #66718A on #F4F7FC | 4.55 | 3 | pass |
| `color.border.field` | `color.surface.accent` | #66718A on #E7F3FD | 4.34 | 3 | pass |
| `color.border.field` | `color.field.1` | #66718A on #EDF2FC | 4.36 | 3 | pass |
| `color.border.field` | `color.field.2` | #66718A on #D9E4F9 | 3.82 | 3 | pass |
| `color.focus.ring` | `color.surface.page` | #1E4A9E on #FFFFFF | 8.31 | 3 | pass |
| `color.focus.ring` | `color.surface.panel` | #1E4A9E on #F4F7FC | 7.73 | 3 | pass |
| `color.focus.ring` | `color.field.1` | #1E4A9E on #EDF2FC | 7.40 | 3 | pass |
| `color.focus.ring` | `color.field.2` | #1E4A9E on #D9E4F9 | 6.49 | 3 | pass |
| `color.focus.ring` | `color.field.3` | #1E4A9E on #A4BDEF | 4.39 | 3 | pass |
| `color.action.primary` | `color.surface.page` | #4371CD on #FFFFFF | 4.69 | 3 | pass |
| `color.action.primary` | `color.field.1` | #4371CD on #EDF2FC | 4.17 | 3 | pass |
| `color.action.primary` | `color.field.2` | #4371CD on #D9E4F9 | 3.66 | 3 | pass |
| `color.text.title` | `color.accent.sky` | #1E222B on #8BCDF6 | 9.22 | 4.5 | pass (added at review) |
| `color.action.primary` | `color.surface.panel` | #4371CD on #F4F7FC | 4.36 | 3 | pass (added at review) |

### Review (independent re-check, `rev19_check.py` in the scratchpad `rev19/` folder, `python3 -I`)

Re-measured from scratch: both files parse with duplicate keys rejected; 80 primitive and 87 semantic tokens; 122 alias references, 0 broken, 0 cycles, 0 raw values in the semantic file, no path collision between the two files; 83 proof variables, 77 value comparisons and 12 responsive comparisons, 0 mismatches; 71 / 12 / 0; contrast as corrected above. Renamed at review, so the pasted output above shows the old names: `ratio.logo-clear` is now `ratio.0945` (a primitive must not carry a role name) and `typography.body` / `body-mobile` are now `typography.paragraph` / `paragraph-mobile`. The two DTCG notes now also name the non-standard em letter spacing and the unitless 0 in the shadows.

## Check before handing back

- [x] Both files are valid JSON (measured: no duplicate keys either).
- [x] 0 broken aliases, 0 cycles, 0 raw values in the semantic file (measured).
- [x] Every `:root` variable of the proof is mapped, marked presentation-only, or listed unused (83 of 83: 71 mapped, 12 presentation-only, 0 unused).
- [x] No sample values from another project remain (measured: 0 leftovers; the only values outside `:root` variables are the 3 breakpoints, matched to the proof's media queries by the script, and 375, traced to a CSS comment).
- [ ] Tokens approved: not yet. They are approved with the spec at Gate 7.
