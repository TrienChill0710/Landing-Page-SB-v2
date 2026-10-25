# 20 · Master spec — ShopBase 2.0 Home (P01·A and P01·B)

Project: ShopBase website redesign · type **C · Rebrand** · page **P01 Home** in two variants (**P01·A** "Find, fix, approve" and **P01·B** "One store, with AI on top") · English · light mode only · responsive, locked frames **1440** and **375** · palette Option 1 LOCKED · Gates 0 to 6 `APPROVED` · Step 19 done · this file is Step 20, **Gate 7 is open** (tokens and spec await the Strategy owner).

This is the single source for the build. The look is `06-proof-ui/proof.html` (Gate 6 APPROVED); where this file and the proof differ on the look, the proof wins and the difference is a bug in this file. Where the proof has no frame (header, footer, S04, S08), this file says so and gives a PROPOSAL built only from existing tokens.

## 0 · How to read this file

| Marker | Meaning |
|---|---|
| `[NEEDS DECISION]` | A person must decide; the default stated next to it is what gets built if nobody answers. |
| `not in the proof, to confirm` | A state or part the proof did not draw. Built only from existing tokens and classes, no new colour. The user judges it at the Step 21 build. |
| `derived` | A number computed from the proof's measured frames (headless Chrome, 1440 and 375) or from tokens; not a design decision. |
| `DO NOT BUILD unless confirmed` | Fenced in a block quote. Not part of the default page. Never built until the user says so in words. |
| `ASSUMPTION` | Carried from earlier steps; nothing proves it. |

- **Where a hex colour may appear in this file:** only in section 2 (design foundation tables) and Appendix A (the `:root` block). Every other section names colours by token or CSS variable. The measured appendix checks this by code.
- **Copy is verbatim.** Every line under "Content" is the APPROVED default copy from `05-content/14-copy.md`, copied by code and re-checked by code (Appendix B). Copy that is CONDITIONAL or ALTERNATE is fenced and is not built.
- **Nothing here is proven.** Every statement about what the AI does is the user's screenshot wording plus "proposed" and "scan" (UNPROVEN as product behaviour). No result number appears anywhere on the page.

## 1 · Product summary

1. **What:** the Home page (P01) of ShopBase 2.0, "ShopBase for the AI era": one independent store product whose headline feature is AI. CR Scan AI finds what stops shoppers and builds a proposed fix; AOV AI recommends offers aimed at order value; the seller approves every change (UNPROVEN as product behaviour).
2. **For whom:** experienced dropshipping and print-on-demand sellers (personas A and B, equal weight), plus existing merchants who also read Home (persona M). The page does not name the audience and says nothing about migration (Step 09 default).
3. **USP:** AI that works on the store, and the seller decides. Shown as a product demonstration (scan, proposed fix, approval) through labelled illustrations; no result numbers, no comparisons.
4. **Frame:** one page in two variants, built as two HTML files: P01·A has 9 sections, P01·B has 7 (8 only if the CONDITIONAL S11 is confirmed). Locked frames 1440 and 375, English only, type C · Rebrand, light mode only (no dark surface exists).
5. **Primary action:** sign up, "Get started for free" → `https://accounts.shopbase.com/sign-up` (referral parameters kept). One secondary button, in the hero only: "Explore CR Scan AI".

## 2 · Design foundation

Names point to `07-tokens/2-semantic.json` (role) and `1-primitive.json` (raw value). The CSS variable names are the ones `proof.html` uses; the full generated block is in Appendix A. **Hex is allowed in this section's tables and in Appendix A only.**

### 2.1 Colour roles (palette Option 1, LOCKED, plus soft fields F1 to F3)

| CSS variable | Token | Value | Use |
|---|---|---|---|
| `--color-primary` | `color.action.primary` | `#4371CD` | Get started buttons and the one approve control only |
| `--color-primary-hover` | `color.action.primary-hover` | `#3A62B2` | Hover of the primary button |
| `--color-on-primary` | `color.text.on-primary` | `#FFFFFF` | Text on the primary button |
| `--color-accent-tint` | `color.surface.accent` | `#E7F3FD` | A found issue, a proposed fix, the approval highlight (inner cards) |
| `--color-page` | `color.surface.page` | `#FFFFFF` | Page and card white |
| `--color-panel` | `color.surface.panel` | `#F4F7FC` | Cool grey panel, pill fill, footer fill, secondary-button hover |
| `--color-title` | `color.text.title` | `#1E222B` | Headlines, secondary-button text |
| `--color-body` | `color.text.body` | `#373B43` | Paragraphs, the Illustration label |
| `--color-muted` | `color.text.muted` | `#596070` | Captions; only on page, panel, F1, F2 |
| `--color-border` | `color.border.default` | `#7F8A9E` | UI outlines (secondary button, pill); page, panel, F1 only |
| `--color-border-field` | `color.border.field` | `#66718A` | UI outline where the edge touches F1 or F2; dashed approve region |
| `--color-divider` | `color.border.divider` | `#DDE3EE` | Decorative hairline (header bottom line) |
| `--color-link` | `color.text.link` | `#3A62B2` | Text links; same value as primary hover; never on F3 |
| `--color-focus` | `color.focus.ring` | `#1E4A9E` | 2px focus ring on every interactive element |
| `--color-canvas` | `color.surface.canvas` | `#DDE3EE` | PROOF ONLY: grey canvas around frames (outer wrapper) |
| `--color-bar` | `color.neutral.200` | `#DDE3EE` | Placeholder bars only |
| `--field-1-a` | `color.field.1.stop-1` | `#F3FAFE` | F1 Mist, stop 1 |
| `--field-1-b` | `color.field.1.stop-2` | `#EDF2FC` | F1 Mist, stop 2 |
| `--field-2-a` | `color.field.2.stop-1` | `#D1EBFB` | F2 Sky, stop 1 |
| `--field-2-b` | `color.field.2.stop-2` | `#D9E4F9` | F2 Sky, stop 2 |
| `--field-3-a` | `color.field.3.stop-1` | `#C5E6FA` | F3 Azure, stop 1 |
| `--field-3-b` | `color.field.3.stop-2` | `#A4BDEF` | F3 Azure, stop 2 |
| `--field-angle` | `field.angle` | `135deg` | Gradient angle for all three fields; never on text |

Rules that go with the colours (from `16-palette.md`, locked): the primary colour appears only on the "Get started for free" buttons and the one approve control drawn inside the S07 illustration; never as a section background, a field, or body text. No gradient on text, ever. Soft fields only behind an illustration card. Muted text and links never sit on F3; the standard border `--color-border` sits on page, panel and F1 only; on F2 use `--color-border-field`; on F3 draw no border. No dark panel exists. No glow, sparkle or "AI magic" cue.

### 2.2 Font and type scale

Font: **Inter** only (`02-assets/fonts/InterVariable.woff2`, weights 100 to 900 in the file; the page uses 400, 500, 600), SIL Open Font License 1.1, keep `02-assets/fonts/LICENSE-Inter.txt` with the font. `@font-face` as in the proof (`font-display: swap`). Scale ratio 1.25 from 1rem, one step down for captions.

| CSS variable | Token | Value | Note |
|---|---|---|---|
| `--font-sans` | `font.family.base` | `"Inter", system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif` | Inter first, then the proof's fallback stack |
| `--fs-n1` | `font.size.n1` | `0.8rem` | Caption step (12.8 px) |
| `--fs-0` | `font.size.0` | `1rem` | Base (16 px) |
| `--fs-1` | `font.size.1` | `1.25rem` | Lead and paragraph on desktop (20 px) |
| `--fs-2` | `font.size.2` | `1.5625rem` | Section headline on mobile (25 px) |
| `--fs-3` | `font.size.3` | `1.953rem` | Hero headline on mobile (31.2 px) |
| `--fs-4` | `font.size.4` | `2.441rem` | Section headline on desktop (39.1 px) |
| `--fs-5` | `font.size.5` | `3.052rem` | Hero headline on desktop (48.8 px) |
| `--fw-regular` | `font.weight.regular` | `400` | Body |
| `--fw-medium` | `font.weight.medium` | `500` | Captions |
| `--fw-semibold` | `font.weight.semibold` | `600` | Headlines, buttons, pill |
| `--lh-tight` | `font.line-height.tight` | `1.1` | Hero headline, button label |
| `--lh-heading` | `font.line-height.snug` | `1.2` | Section headline, pill |
| `--lh-body` | `font.line-height.relaxed` | `1.55` | Paragraphs, captions |
| `--ls-tight` | `font.letter-spacing.tight` | `-0.02em` | Headlines |
| `--ls-label` | `font.letter-spacing.wide` | `0.04em` | Captions, pill, frame meta |
| `--size-hero` | `typography.hero-headline.fontSize` | `3.052rem` | Role: hero headline (mobile: 1.953rem) |
| `--size-h2` | `typography.section-headline.fontSize` | `2.441rem` | Role: section headline (mobile: 1.5625rem) |
| `--size-lead` | `typography.lead.fontSize` | `1.25rem` | Role: lead and paragraph (mobile: 1rem) |
| `--size-body` | `typography.base.fontSize` | `1rem` | Role: button label, document base |
| `--size-caption` | `typography.caption.fontSize` | `0.8rem` | Role: caption, pill |

Roles (classes from the proof): `.title-hero` (hero headline: `--size-hero`, `--lh-tight`, `--ls-tight`, `--fw-semibold`, `--color-title`) · `.title-section` (`--size-h2`, `--lh-heading`, `--ls-tight`, `--fw-semibold`, `--color-title`) · `.text-lead` and `.text-body` (both `--size-lead`, `--lh-body`, `--color-body`; the proof's `.text-body` uses the lead size, not `--size-body`) · `.text-caption` (`--size-caption`, `--fw-medium`, `--ls-label`, `--color-muted`). Button labels use `--size-body` at `--fw-semibold`.

### 2.3 Spacing and sizes

| CSS variable | Token | Value | Note |
|---|---|---|---|
| `--space-1` | `space.stack.xs` | `0.25rem` (4 px) | inner gaps |
| `--space-2` | `space.stack.sm` | `0.5rem` (8 px) | hero button-row top, small gaps |
| `--space-3` | `space.stack.md` | `1rem` (16 px) | gaps in a button row and card list |
| `--space-4` | `space.stack.lg` | `1.5rem` (24 px) | stack gaps, inner-card padding |
| `--space-5` | `space.stack.xl` | `2.5rem` (40 px) | card padding, gutter |
| `--space-6` | `space.stack.2xl` | `4rem` (64 px) | field padding, hero visual top margin, split gap |
| `--space-7` | `space.7` | `6rem` (96 px) | top step: the section gap, used nowhere else |
| `--section-gap` | `space.section` | `6rem` (96 px) | vertical padding of a section (mobile 4rem) |
| `--gutter` | `space.gutter` | `2.5rem` (40 px) | inline padding of a section (mobile 1.5rem) |
| `--field-pad` | `space.field-pad` | `4rem` (64 px) | padding inside a soft field (mobile 1rem) |
| `--container` | `layout.container.base` | `75rem` (1200 px) | content width: 80rem from 1440, 68rem below (declared 75rem never applies) |
| `--legend-col` | not a token (copied from the proof) | `14rem` (224 px) | proof chrome only |
| `--frame-max` | `layout.page.frame-max` | `90rem` (1440 px) | PROOF wrapper width (1440 frame) |
| `--text-measure` | `layout.measure.text` | `38rem` (608 px) | max width of lead and body text |
| `--hero-text-measure` | `layout.measure.hero` | `54rem` (864 px) | max width of the hero headline |
| `--card-min-h` | `layout.card.min-height` | `18rem` (288 px) | card min height (mobile 15rem) |
| `--card-max-w` | `layout.card.max-width` | `46rem` (736 px) | card max width |
| `--control-h` | `size.control-height` | `3.25rem` (52 px) | button min height |
| `--icon` | `size.icon` | `1.25rem` (20 px) | Lucide icon size |
| `--bar-h` | not a token (copied from the proof) | `0.75rem` (12 px) | placeholder bar height |
| `--bar-short` | not a token (copied from the proof) | `40%` | placeholder bar width |
| `--bar-mid` | not a token (copied from the proof) | `70%` | placeholder bar width |
| `--bar-long` | not a token (copied from the proof) | `100%` | placeholder bar width |
| `--split-cols` | `layout.split.columns` | `5fr 7fr` | text then visual |
| `--split-cols-reverse` | `layout.split.columns-reverse` | `7fr 5fr` | visual then text |
| `--line` | `border.width.default` | `1px` | hairline width |
| `--line-dashed` | `border.width.strong` | `2px` | dashed region outline width |
| `--focus-w` | `focus.ring.width` | `2px` | focus ring width |
| `--focus-offset` | `focus.ring.offset` | `2px` | focus ring offset |
| `--logo-w` | `layout.logo.min-width` | `7.5rem` (120 px) | logo width in the proof legend = the 120 px minimum |
| `--logo-clear` | `layout.logo.clear-space-ratio` | `calc(var(--logo-w) * 0.0945)` | clear space = logo width x 24/254 |

### 2.4 Radius, shadow, border, focus

| CSS variable | Token | Value | Note |
|---|---|---|---|
| `--shadow-card` | `shadow.card` | `0 0.5rem 2rem rgba(30, 34, 43, 0.10)` | white card on a field only |
| `--shadow-device` | `shadow.device` | `0 0.75rem 2.5rem rgba(30, 34, 43, 0.16)` | PROOF outer wrapper only |
| `--radius-field` | `radius.field` | `2rem` | large container behind a card (mobile 1rem as the proof renders) |
| `--radius-card` | `radius.card` | `1.5rem` | white card (mobile 1rem) |
| `--radius-inner` | `radius.inner` | `1rem` | inner card |
| `--radius-control` | `radius.control` | `0.75rem` | buttons and chips |
| `--radius-pill` | `radius.pill` | `62rem` | Illustration pill |
| `--radius-bar` | not a token (copied from the proof) | `0.375rem` | placeholder bars (not a token) |

Radius family: container (`--radius-field`) > card (`--radius-card`) > inner card (`--radius-inner`) > control (`--radius-control`). Pill: `--radius-pill`. Shadow: one soft shadow on a white card sitting on a field (`--shadow-card`); inner cards and cards on the plain page have none; the device shadow belongs to the outer presentation wrapper only. **No transitions and no animations exist in the proof, so none are specified: motion = none.**

### 2.5 Icons

**Lucide** only (ISC licence, `02-assets/icons/LICENSE-Lucide.txt`; Feather-derived icons are MIT). One style: 24 × 24 grid, outline stroke 2, round caps and joins, `currentColor`, shown at `--icon` (1.25rem). Only `02-assets/icons/arrow-right.svg` exists today. Two more are needed for the mobile menu: Lucide `menu` and `x` `[NEEDS DECISION]` (default: add those two files from the official Lucide set to `02-assets/icons/`, unchanged, and use them; if not added, the menu button shows the words "Open menu" and "Close menu" only; with the icons, those words stay as the button's accessible name). Decorative icons carry `aria-hidden="true"`. No second icon library, no emoji, no coloured icon tiles, no wand or sparkle icons.

### 2.6 Logo usage (as provided, never redrawn, never recoloured)

| File | Use | Rule |
|---|---|---|
| `02-assets/logo/Logo (6).svg` | Header and footer, on the light surfaces `--color-page` and `--color-panel` | The only logo file used on the page. Dark wordmark on transparent. Alt text `ShopBase` (S01 copy). |
| `02-assets/logo/Logo (1).svg` | Dark surfaces only | **Not used: no dark surface exists** in P01. White wordmark; invisible on white. |
| `02-assets/logo/Logo (3).svg` | Icon only (favicon) | Favicon `[NEEDS DECISION]`: the user has not said where the icon may be used; default: used unchanged as the favicon. Never beside the full logo. |

Clear space: **24 / 254 of the logo width on all four sides** (about 9.4%; in the proof `--logo-clear` = `--logo-w` × 0.0945). Minimum size: **120 px wide** for the full logo (`--logo-w`, 7.5rem), **24 px** for the icon alone. These come from Step 10 and are PROPOSALS (no brand guideline exists), to be confirmed by the user at Gate 7. The logo never sits on a soft field. Files have no built-in margin; the page adds the clear space. Use the file's own `width` and `height` attributes (254 × 48) for aspect ratio; set the displayed width with `--logo-w`.

## 3 · Page structure and global behaviour

### 3.1 Document

- `<html lang="en">`, one `<main id="main">`, sections as `<section class="frame" id="s##">` in the order of section 4.0, header and footer outside `<main>`. Each section carries `data-section-id="S##"` and an HTML comment `<!-- S## · Name -->`; its heading is the section's accessible name (`aria-labelledby`).
- **Exactly one `<h1>`: the hero headline** (S03 in A, S10 in B), still styled with `.title-hero`. The proof renders the hero headline as an `<h2>` because its frames stand alone; the build must make it the `<h1>`. All other section headlines are `<h2>`. The header and footer have no headings.
- `<head>`: title, meta description, Open Graph title and description from the SEO draft below (per variant, verbatim); `meta viewport`; favicon; one canonical `https://www.shopbase.com/` `[NEEDS DECISION]` (how the two variants go live is open, Step 12 decision 2; default: each file carries its own variant's title and meta, one canonical for Home). No structured data in the build by default (K16: added at Step 21/24 if the user confirms).
- Paths from `09-final-ui/`: `../02-assets/fonts/InterVariable.woff2`, `../02-assets/logo/Logo%20(6).svg`, `../02-assets/images/IMG##-name.png`, `../02-assets/icons/arrow-right.svg` (inline SVG as in the proof).
- Presentation (canvas background, device frame, shadow) goes on an **outer wrapper only** (`.canvas` > `.frame-device`, as in the proof), never inside a section. Default for the export: a plain full-width page with no wrapper; add the wrapper only if the build tool needs a 1440 or 375 frame to show it.

### 3.1b Head text per variant (SEO draft, verbatim from `14-copy.md`; DRAFT until the user confirms; Open Graph and Twitter title and description = the title and meta description, as the copy file says)

**P01·A**
- Title: ShopBase 2.0: AI that finds what stops shoppers
- Meta description: ShopBase 2.0 has CR Scan AI, which finds what stops shoppers on your store and builds a proposed fix. Get started for free.

**P01·B**
- Title: ShopBase 2.0: one store platform, with AI on top
- Meta description: ShopBase 2.0 is one store platform with CR Scan AI, which finds what stops shoppers and builds a proposed fix. Get started for free.

### 3.2 Header (S01) and footer (S02)

Specified in section 4 (the proof did not cover them). Summary: header = logo, optional Pricing link `[NEEDS DECISION]`, Login text link, one primary button; footer = logo, two link columns, no claims.

### 3.3 Sticky behaviour

**The header stays visible while the page scrolls** (`position: sticky; top: 0` on a white `--color-page` bar with a `--color-divider` bottom hairline, above the content). This is the **Step 12 default (assumption 9), to confirm at Gate 7**. Why: S05 to S08 carry no button, so the sticky header is the only primary button between the hero and S09 (FL11, FL12). If the user rejects it, add a primary button after S07 instead (Step 12 decision 9); that change takes a new section code. Anchor targets (`#s05`, `#s12`) get `scroll-margin-top` equal to the header height (`--control-h` + 2 × `--space-3`, derived) so the section's headline is not hidden under the bar. On mobile the sticky header holds the logo and the menu button; the primary button then sits inside the opened menu (see S01), so on a phone the mid-page button is one tap away rather than always visible `[NEEDS DECISION]` (alternative: keep a primary button in the mobile bar; it does not fit at 375 next to the logo with the proof's button size).

### 3.4 Scroll and motion

Plain browser scroll. **No smooth-scroll, no scroll-triggered animation, no parallax, no carousel, no video, no transitions: none exists in the proof and none is added.** The secondary hero button jumps to its anchor. `scroll_depth` and `section_view` are measured passively (section 7).

### 3.5 Responsive rules (breakpoints from `layout.breakpoint.*`)

| Context | Rule (tokens) | Effect |
|---|---|---|
| Wide: viewport ≥ **1440px** (`layout.breakpoint.wide-min`) | `--container` = `layout.container.wide` (80rem) | Content column 1280px, centred; side gutter `--gutter` (2.5rem) |
| Compact: **768px to 1439px** (up to `layout.breakpoint.compact-max`, above mobile) | `--container` = `layout.container.compact` (68rem), `--gutter` 2.5rem | Same layout as desktop on a narrower column. **Not a locked frame: not drawn and not measured in the proof; check it at Step 22, to confirm.** |
| Mobile: viewport ≤ **767px** (`layout.breakpoint.mobile-max`) | `--size-hero` → hero-headline-mobile, `--size-h2` → section-headline-mobile, `--size-lead` → lead-mobile (1rem), `--section-gap` → `space.section-mobile` (4rem), `--gutter` → `space.gutter-mobile` (1.5rem), `--field-pad` → `space.field-pad-mobile` (1rem), `--radius-field` and `--radius-card` → 1rem, `--card-min-h` → 15rem | Locked frame **375**. `.split` and `.split-reverse` become one column (text first, then the visual) with gap `--space-5`; `.card` padding and gap shrink (`--space-4`, `--space-3`); `.hero-visual` margin-top `--space-5`; `.button-row` becomes a full-width column and each `.btn` is full width. |

The mobile field radius is an open decision (section 11, item 1): the default keeps what the proof renders (1rem for field and card).

### 3.6 Caps (Step 12, all ASSUMPTION until the user says otherwise)

| Cap | Value | P01·A | P01·B (default, S11 not built) |
|---|---|---|---|
| Sections per page, counting header and footer | 10 | 9 | 7 |
| Page length, desktop 1440 | 9,000 px | 4,864 px (derived estimate) | 3,903 px (derived estimate) |
| Page length, mobile 375 | 16,000 px | 4,943 px (derived estimate) | 3,944 px (derived estimate) |
| Boxes (cards, panels) per section | 4 | max 4 (S07: 2 cards + 1 region + 1 field; S06 and S08: 3) | max 4 (S07; S10 and S12: 3) |
| Primary CTAs per section | 1 (the hero has one extra secondary button) | S01, S03, S09 → 1 each | S01, S10, S09 → 1 each |

Length estimate method: the frame heights **measured on the proof** in headless Chrome (1440 and 375: S03, S10, S05, S06, S12, S07, S09) plus the Step 12 estimates for the parts the proof did not draw (S01 80 / 64 px, S02 450 / 900 px, S04 480 / 600 px) and S08 taken equal to the S06 frame. Real heights depend on the user's images (the images are 3:1 and may be taller or shorter than the proof's placeholder cards) and on the header and footer as built; measure again at Step 22.

## 4 · Sections

### 4.0 Page order per variant

| Position | P01·A (9 sections) | P01·B (7 sections, S11 not built) |
|---|---|---|
| 1 | S01 · Header | S01 · Header |
| 2 | S03 · Hero A | S10 · Hero B |
| 3 | S04 · The unseen problem | S12 · Scan and fix |
| 4 | S05 · Scan | S08 · AOV AI |
| 5 | S06 · Fix | S07 · Approve |
| 6 | S07 · Approve | S09 · Closing call to action |
| 7 | S08 · AOV AI | S02 · Footer |
| 8 | S09 · Closing call to action | - |
| 9 | S02 · Footer | - |

Section order inside each variant follows that variant's own narrative (Step 12). S11 is not in either default order. Groups below: SHARED (both variants), A only, B only; inside a group by S## code.

Field and layout pattern per illustration section (Step 17 patterns, proof frames): hero = centred stack, then one field with one card · S05 / S12 / S07 = text left, field right (`.split`) · S06 / S08 = field left, text right (`.split.split-reverse`) · S09 = centred stack on the plain page, no field. Field use: F2 S03, S10, S06 · F1 S05, S08 · F3 S12, S07 (F3 appears on at most two sections of a page: S07 only in A, S12 and S07 in B). S08's F1 and S04's layout are **not in the proof, to confirm**.

### 4.1 SHARED sections (both variants)

#### S01 · Header
Page P01·A and P01·B · flows FL01 to FL12 (first section of every flow; FL03 and FL06 use the Login link; FL07 and FL08 start from a referral link) · focal point: ShopBase, and where to start or sign in.

**Purpose.** Orient the reader and give the way in (sign up) and the way back in (log in). Page chrome, not a story beat. For existing merchants the Login link is the only element built for them.

**Layout (top → bottom; not in the proof, to confirm).** One bar, sticky (section 3.3), full width on `--color-page`, bottom hairline `--color-divider`, inner row in `.frame-inner` width, height = `--control-h` + 2 × `--space-3` (derived 84px). Skip link first in the DOM. Desktop: logo (`Logo (6).svg` at `--logo-w`, with clear space; links to the top of the page) on the left; on the right, in order: Pricing link (only if confirmed), Login (text link), primary button with the arrow icon; gap `--space-4`. Mobile (≤767px): logo left; menu button right (`<details class="menu">` with a `<summary>`, no script); the opened panel is a column under the bar on `--color-page` holding Pricing (if confirmed), Login, then the primary button at full width. Classes (new, built only from tokens): `.skip-link`, `.site-header`, `.site-header-inner`, `.logo-link`, `.nav`, `.nav-link`, `.menu`, `.menu-toggle`, `.menu-panel`; the button is `.btn.btn-primary` as in the proof.

**Content (verbatim, APPROVED default).**
- Headline: none (page chrome)
- Login label: Login
- CTA label: Get started for free
- Alt text, logo: ShopBase
- Skip link: Skip to main content
- Menu button (mobile): Open menu / Close menu
- Nav item, only if confirmed: Pricing `[NEEDS DECISION]`. Default: **not built.** The approved copy says to drop the item if K1 is not confirmed; Step 12 decision 3 had it in the default header. If the user confirms `/pricing` (K1, SUSPECTED), build one `.nav-link` labelled `Pricing` → `https://www.shopbase.com/pricing`.

**Visuals.** The logo file as provided; the arrow icon (Lucide `arrow-right`, `aria-hidden`) in the button. No other image, no second logo file, no flag, no announcement bar.

**Actions.**
- Logo → top of P01 (`#main`, or `/`).
- Login → `https://accounts.shopbase.com/sign-in` (navigation, not a CTA).
- Primary button "Get started for free" → `https://accounts.shopbase.com/sign-up` with the referral parameters `fpr`, `fpt`, `clickId`, `invite_trial` kept (K12 SUSPECTED, strong, to confirm; see section 7).
- Pricing (only if confirmed) → `https://www.shopbase.com/pricing`.
- Menu button (mobile) → opens and closes the menu panel.
- No "Book a demo", no "Print on demand", no "Dropshipping" item (Step 12 decision 3).

**States.**
- default: as in Layout.
- hover: primary button as the proof (`.btn-primary:hover`: background and border → `--color-primary-hover`). Login and Pricing: text colour `--color-link` (the proof's `a` rule), no underline by default, underline on hover (text colour unchanged) — **not in the proof, to confirm**. Menu button: as `.btn-secondary:hover` (background → `--color-panel`) — not in the proof, to confirm.
- pressed: not in the proof, to confirm: same colours as hover; no darker colour exists in the tokens and none is invented; no movement or scale.
- focus: every link, the button and the menu button show `outline: var(--focus-w) solid var(--color-focus); outline-offset: var(--focus-offset)` (the proof's focus-visible rule); never removed.
- loading: n/a — links only; no data is fetched.
- empty: n/a — the header always has the logo, Login and the button.
- error: n/a — no input or request on this page.
- success: n/a — nothing is submitted.
- disabled: n/a — no control is ever disabled.

**Notes.** Sticky (section 3.3, Step 12 default, to confirm). Cap: header counts as one of the 10 sections; one primary button. Desktop shows Login and the button in the bar; at 375 they move into the menu. The old live header (two logos, product tabs, two "Book a demo" items, flag by country) is not carried (section 9).

#### S02 · Footer
Page P01·A and P01·B · flows: end of page for every flow (no flow ends here by design; FL03 and FL06 may use its help and legal links) · focal point: legal and help links stay reachable.

**Purpose.** Navigate, legal, help. Nothing else: no claims, no taglines, no numbers.

**Layout (top → bottom; not in the proof, to confirm).** A band on `--color-panel` (the palette's default light footer), padding `--section-gap` block, `--gutter` inline, content in `.frame-inner` width. Top: logo (`Logo (6).svg`, `--logo-w`, with clear space). Below: two link columns, each a `.footer-title` over a `.footer-list` of `.footer-link` items; on mobile the columns stack in one column. Bottom: a legal row. Classes (new, tokens only): `.site-footer`, `.footer-grid`, `.footer-title`, `.footer-list`, `.footer-link`, `.footer-legal`. Footer links are not boxes (Step 12).

**Content (verbatim, APPROVED default; every link label is SUSPECTED, the user confirms).**
- Column titles: Help · Legal
- Link labels (all SUSPECTED, user confirms): Help center · Blog · Developers · Updates · Templates · Status · App Store · Google Play · Terms of service · Privacy policy · ShopBase Payments terms · Marketplace payments terms
- Alt text, logo: ShopBase
- Copyright and legal entity line: **not built** `[NEEDS DECISION]`: the legal entity name and the year are the user's decision only (identity migration rows 12 to 14). Default: no copyright line is drawn until the user supplies the text; nothing is invented.
- Cookie and consent text: **not built** `[NEEDS DECISION]` (NEEDS LEGAL TEXT from the legal owner). Default: none.

**Footer link set, K3 to K6 `[NEEDS DECISION]`** (all SUSPECTED). Default: the twelve labels above are built as links to the live destinations below; K3 (`/features/*`) and K4 (company and partner pages) links are not built; the sign-up and sign-in links live in S01.

**Column set `[NEEDS DECISION]`.** Default arrangement: **Help** = Help center, Blog, Developers, Updates, Templates, Status, App Store, Google Play; **Legal** = Terms of service, Privacy policy, ShopBase Payments terms, Marketplace payments terms. The split of the first eight labels under "Help" is this file's reading of the approved column titles; the user may regroup. No feature or company links by default (K3, K4 not confirmed).

**Visuals.** Logo only. No illustration, no social icons, no app-store badges (the labels are text links).

**Actions (destinations are the live ones from the audit, all SUSPECTED; verify before publishing).**
- Help center → `https://help.shopbase.com/` · Blog → `https://blog.shopbase.com/` · Developers → `https://developers.shopbase.com/` · Updates → `https://updates.shopbase.com/` · Templates → `https://templates.shopbase.com/` · Status → `https://www.shopbasestatus.com/`
- App Store, Google Play → `[NEEDS DECISION]` exact store URLs (the audit names `apps.apple.com` and `play.google.com` without the full address; default: the two labels are built as links only once the user gives the URLs, otherwise they are left off).
- Terms of service → `https://www.shopbase.com/terms-of-service` · Privacy policy → `https://www.shopbase.com/privacy-policy` · ShopBase Payments terms → `https://www.shopbase.com/shopbase-payments-terms` · Marketplace payments terms → `https://www.shopbase.com/shopbase-marketplace-payments-terms`
- Logo → top of P01.
- **Not drawn by default:** the `/dmcareport` DMCA link `[NEEDS DECISION]` (the user's rule says no DMCA mention on Home; the live footer links it, K5b; dropping a DMCA contact link may have a legal consequence, ask the person who owns it; flagged for Step 24), PrintBase, PlusBase, PrintHub, "Dropshipping Zone" and the country Facebook groups (K13).

**States.**
- default: as in Layout.
- hover: no underline by default, underline on hover — not in the proof, to confirm. Link text colour `--color-body` (on `--color-panel`; pair measured at Step 19), title text `--color-title`.
- pressed: not in the proof, to confirm: same as hover.
- focus: the proof's focus-visible ring on every link (`--color-focus`, `--focus-w`, `--focus-offset`).
- loading: n/a — links only.
- empty: a column with no confirmed link is left out; a footer with no links at all is not allowed (legal links must stay reachable).
- error: n/a — no input.
- success: n/a — nothing is submitted.
- disabled: n/a — no control.

**Notes.** No dark footer (no dark surface is allowed; on-dark colours are untested). The legal entity name "OpenCommerce Group, Inc" and `support@shopbase.com` live on the legal pages and are not on Home; the page must not promise a support channel (E7 unknown). "ShopBase Payments terms" and "Marketplace payments terms" are legal link labels carried from the approved copy; they are the only places an old product name could show, and they stay `[NEEDS DECISION]` with the default of the approved copy (shown, SUSPECTED).

#### S07 · Approve
Page P01·A and P01·B · flows FL01 to FL06, FL11, FL12 (step 3 of the loop in A; after S08 in B) · focal point: the seller decides: "You approve every change" is the caption under the approval illustration, not a block (UNPROVEN as product behaviour).

**Purpose.** Show the approval step: who decides.

**Layout (top → bottom; proof frame S07).** `.frame` > `.frame-inner` > `.split` (5fr 7fr): left `.split-text` (`h2.title-section`, `p.text-body`), right `.split-visual` holding `.field.field-3` > `figure.card` (the "Illustration" `.pill`, then IMG03 in place of the placeholder), then the caption `p.text-caption.visual-caption` **under the field** (outside it). Placeholder state (no image): the card holds the pill, one `.card.card-inner.card-small` with two bars, and one `.region` ("Approve control: part of the illustration", dashed `--line-dashed` outline in `--color-border-field`). Measured on the proof: frame 653 px at 1440 (field 709 × 425, card 581 × 297, inner card 501 × 88, region 501 × 56) and 606 px at 375 (card 295 × 269). Mobile: one column, text first, caption under the field.

**Content (verbatim, APPROVED default; identical in both variants).**
- Headline: A proposal, then your decision.
- Body: The AI proposes. You decide.
- Caption: You approve every change
- Alt text, Illustration 3: Illustration of a proposed change on a card with one approve button.
- Visual label: Illustration

**Visuals.** IMG03 (section 8): one small card showing a proposed change and a single approve control; no number, no real store domain. The approve control is **drawn inside the illustration**, it is not a live button on the page (S07 has no CTA in the plan). It is the only element on the page's mid-section that may use the primary colour. No "undo", no control block, no "nothing changes until" line.

**Actions.** None: no link or button in this section (the approve control is part of the picture).

**States.**
- default: as in Layout.
- hover: n/a — no interactive element (the drawn approve control is not live).
- pressed: n/a — same reason.
- focus: n/a — nothing takes keyboard focus.
- loading: n/a — static; the figure keeps `--card-min-h` while IMG03 loads.
- empty: the labelled placeholder with the dashed region (proof frame S07) is the state when `IMG03` is missing.
- error: n/a — if IMG03 fails to load its `alt` text shows; no error UI.
- success: n/a — no approval happens on the page; no success state is drawn.
- disabled: n/a.

**Notes.** F3 on this section; the pill sits on the white card, never on the field. S07 is SHARED: same words, same picture, same structure in both variants; only its position differs (A: 6th; B: 5th of 7).

#### S08 · AOV AI
Page P01·A and P01·B · flows FL01, FL02, FL04, FL05, FL06 (and FL11, FL12 onward) · focal point: AOV AI recommends offers aimed at order value.

**Purpose.** Show the second AI tool. It has no matching voice-of-customer pain; it is a feature description only. The Content reviewer may cut it without breaking the story.

**Layout (top → bottom; not in the proof, to confirm).** Same pattern as the proof's S06 frame: `.frame` > `.frame-inner` > `.split.split-reverse` (visual left, text right): `.split-visual` with `.field.field-1` > `figure.card` (the pill, IMG04), and `.split-text` (`h2.title-section`, `p.text-body`). F1 is this file's choice (F3 is capped at two sections; F2 would sit next to F2/F3 neighbours): to confirm. Placeholder state: the pill, one `.card.card-inner.card-small` with three bars and two plain bars (same structure as S06). Expected height: about the S06 frame (629 px at 1440, 557 px at 375), derived.

**Content (verbatim, APPROVED default; identical in both variants).**
- Headline: AOV AI recommends offers aimed at order value.
- Body: AOV stands for average order value.
- CTA label: none
- Alt text, Illustration 4: Illustration of one offer shown on a card.
- Visual label: Illustration

> **DO NOT BUILD unless confirmed (A only; needs data item 8: every AOV AI offer waits for the seller's approval; default: not shown).** Optional link line under the body in A:
> - Link line (A, conditional): Like the fix, an offer is a proposal for you to approve.

> **DO NOT BUILD (ALTERNATE, needs Gate 5 sign-off; unproven outcome wording).** Alternate headline for S08 using the word "raise". Default: not built; the headline above stands.

**Visuals.** IMG04 (section 8): one generic offer on one card with generic labels; no number or percentage; no real product; **no specific offer type** (no bundle, discount or upsell) until the user says what AOV AI recommends.

**Actions.** None.

**States.** 
- default: as in Layout.
- hover: n/a — no link or button in this section.
- pressed: n/a — same reason.
- focus: n/a — nothing in this section can take keyboard focus (the picture is not a control).
- loading: n/a — nothing is fetched. While an IMG file loads the figure keeps the card's `min-height` (`--card-min-h`), so the layout does not jump.
- empty: the labelled placeholder (the proof's frame: pill and neutral bars) is the empty state, used for every IMG## whose file is missing.
- error: n/a — no input, no request. If an image file fails to load its `alt` text shows; no error UI is designed.
- success: n/a — nothing is submitted.
- disabled: n/a — nothing can be switched off.

**Notes.** SHARED: identical in A and B; position differs (A: 7th; B: 4th of 7). The expansion "average order value" is the standard meaning of AOV, not a product claim; the user confirms it (Step 14 assumption 2).

#### S09 · Closing call to action
Page P01·A and P01·B · flows FL01 to FL08, FL11, FL12 (the closing button; FL03 and FL06 end here or at Login; FL11 and FL12 end here or at the sticky header button) · focal point: the same primary action as the hero.

**Purpose.** Last push to the same action. No new claim may appear here.

**Layout (top → bottom; proof frame S09).** `.frame` > `.frame-inner` > `.closing-stack` (centred, gap `--space-4`): `h2.title-section`, one optional line `p.text-body`, `.button-row` (margin-top `--space-3`) with one `.btn.btn-primary` and the arrow icon. **Plain page: no field, no card, no illustration.** Measured on the proof: 386 px at 1440, 299 px at 375 (button full width on mobile). The line is capped at `--text-measure` (not in the proof, harmless for a one-line text).

**Content (verbatim, APPROVED default).**
- Headline: Start with ShopBase 2.0.
- Support (A): ShopBase 2.0 is one product.
- Support (B): none — empty by default (the button stands alone in B)
- CTA label: Get started for free

> **DO NOT BUILD unless confirmed (B only; default: empty).** Support (B, conditional): a plan line. It needs the user to confirm the plan exists, what it includes, for how long, and whether it replaces the trial. The wording is in `14-copy.md` and is not repeated here.

**Visuals.** None.

**Actions.** Primary button → `https://accounts.shopbase.com/sign-up` with the referral parameters kept (K12 SUSPECTED, to confirm). No secondary button, no other link.

**States.**
- default: as in Layout.
- hover: as the proof (`.btn-primary:hover`).
- pressed: not in the proof, to confirm: same colours as hover; nothing invented.
- focus: the proof's focus-visible ring (`--color-focus`).
- loading: n/a — a link; the destination page loads.
- empty: in B the support line is empty and the block shows headline and button only.
- error: n/a — no request on this page.
- success: n/a — nothing is submitted here.
- disabled: n/a.

**Notes.** SHARED: only the optional line differs by variant (A "one product" line; B empty). Position: A 8th, B 6th of 7. One primary button, no secondary (cap).

### 4.2 A-only sections (P01·A "Find, fix, approve")

#### S03 · Hero A
Page P01·A · flows FL01, FL02, FL03, FL07, FL09, FL11 · focal point: ShopBase 2.0 has AI that finds what stops shoppers and builds the fix (a card under the buttons shows what the scan found).

**Purpose.** State the promise and show the thing first. The primary button must sit above the first scroll (FL09 paid visitors).

**Layout (top → bottom; proof frame S03, Step 17 K1).** `.frame` (padding-block `--section-gap`) > `.frame-inner` > `.hero-stack` (centred stack, gap `--space-4`): `h1.title-hero` (max `--hero-text-measure`), `p.text-lead` (max `--text-measure`), `.button-row` (margin-top `--space-2`: primary then secondary, gap `--space-3`); then `.hero-visual` (margin-top `--space-6`; mobile `--space-5`) > `.field.field-2` (padding `--field-pad`) > `figure.card` (max `--card-max-w`, centred): the pill, then IMG01 as a top crop. Measured on the proof: frame 949 px at 1440 (stack 1280 × 277, field 1280 × 416, card 736 × 288, primary button 225 × 52, secondary 197 × 52) and 794 px at 375 (field 327 × 272, card 295 × 240, buttons full width). The headline is the page's one `<h1>`.

**Content (verbatim, APPROVED default).**
- Headline: AI that finds what stops shoppers on your store and builds the fix.
- Support: CR Scan AI finds what stops shoppers and builds a proposed fix. You approve every change.
- CTA label (primary): Get started for free
- CTA label (secondary): Explore CR Scan AI
- Alt text, Illustration 1 (small crop): Illustration of a scan result: a card listing what the scan found on a store.
- Visual label: Illustration

> **DO NOT BUILD (ALTERNATE, needs Gate 5 sign-off).** The screenshot's outcome headline is not part of the build. Default headline is the one above. (Decision recorded at Gate 5: the fenced headlines stay fenced.)

**Visuals.** IMG01 (section 8), the same picture as S05, shown as a **smaller top crop**: the figure's image box keeps the proof's hero card content area (about 656 × 159 px at 1440, derived) with `object-fit: cover; object-position: top`. The box keeps that same proportion (656 : 159, about 4.1 : 1) at every width, so the crop is always the full width and the top ~73% of IMG01 (at 375 about 247 × 60 px, derived); it never crops the sides. Never stretched, never redrawn. If IMG01 does not exist: the proof's placeholder (pill, four bars).

**Actions.**
- "Get started for free" → `https://accounts.shopbase.com/sign-up` with the referral parameters kept (K12 SUSPECTED, to confirm).
- "Explore CR Scan AI" → on-page anchor **`#s05`** (S05 · Scan). ASSUMPTION from the copy file; no other page.

**States.**
- default: as in Layout.
- hover: primary as the proof (`--color-primary-hover` on background and border); secondary as the proof (`.btn-secondary:hover`: background → `--color-panel`).
- pressed: not in the proof, to confirm: primary same as hover; secondary: background `--color-panel` plus border `--color-border-field`; no new colour.
- focus: the proof's ring on both buttons.
- loading: n/a — plain links. The figure keeps `--card-min-h` while IMG01 loads.
- empty: the labelled placeholder (pill + four bars) when IMG01 is missing.
- error: n/a — no request; a failed image shows its `alt`.
- success: n/a.
- disabled: n/a — buttons are never disabled.

**Notes.** One extra secondary button is the allowed cap exception. Boxes: 1 card + 1 field (2 of 4). No logo row, no tabs, no stat strip, no second line under the buttons.

#### S04 · The unseen problem
Page P01·A · flows FL01, FL02 · focal point: a store can lose shoppers for reasons that are hard to see (framing only; UNPROVEN, the Content reviewer may cut it).

**Purpose.** Frame why a scan is needed. The only problem-led section on the page.

**Layout (top → bottom; not in the proof, to confirm).** A statement band: `.frame` > `.frame-inner` > `.closing-stack` reused without the button row (centred stack on the plain page, gap `--space-4`): `h2.title-section`, `p.text-body` capped at `--text-measure`. No field, no card, no image. Expected height 350 to 480 px at 1440 (Step 12 estimate 480 px), derived.

**Content (verbatim, APPROVED default).**
- Headline: Shoppers can leave without explanation.
- Body: A store can have shoppers and still lose them for reasons that are hard to see. That is what the scan is for.
- CTA label: none
- Alt text: none (no image)

**Visuals.** None. Text only.

**Actions.** None.

**States.** 
- default: as in Layout.
- hover: n/a — no link or button in this section.
- pressed: n/a — same reason.
- focus: n/a — nothing in this section can take keyboard focus (text only).
- loading: n/a — text only, nothing is fetched, no image.
- empty: n/a — the headline and body are always present (if the user cuts S04, the section is removed, not left empty).
- error: n/a — no input, no request, no image.
- success: n/a — nothing is submitted.
- disabled: n/a — nothing can be switched off.

**Notes.** Approved at Gate 5 as written; the recommended cut was not requested, so it stays. If the user cuts it later the A page has 8 sections; codes are never renumbered.

#### S05 · Scan
Page P01·A · flows FL01, FL02, FL11 · focal point: CR Scan AI scans the store and lists what it found (target of the hero secondary button).

**Purpose.** Show step 1 of the loop.

**Layout (top → bottom; proof frame S05, Step 17 K2).** `.frame` > `.frame-inner` > `.split` (5fr 7fr, gap `--space-6`, items centred): left `.split-text` (`h2.title-section`, `p.text-body`, max `--text-measure`); right `.split-visual` > `.field.field-1` > `figure.card` with the pill and IMG01 in full. Placeholder: pill + five bars. Measured on the proof: 608 px at 1440 (field 709 × 416, card 581 × 288) and 566 px at 375 (card 295 × 240). Mobile: one column, text first. The section carries `id="s05"`.

**Content (verbatim, APPROVED default).**
- Headline: CR Scan AI shows you what it finds.
- Body: It scans your store and lists what may be stopping shoppers.
- CTA label: none
- Alt text, Illustration 1: Illustration of a scan result: a card listing what the scan found on a store.
- Visual label: Illustration

**Visuals.** IMG01: the full scan card with generic labels and short reasons; no number, no store domain. The found issues may use the accent tint (`--color-accent-tint`) inside the picture; no primary colour inside.

**Actions.** None. (It is the landing point of "Explore CR Scan AI".)

**States.** 
- default: as in Layout.
- hover: n/a — no link or button in this section.
- pressed: n/a — same reason.
- focus: n/a — nothing in this section can take keyboard focus (the picture is not a control).
- loading: n/a — nothing is fetched. While an IMG file loads the figure keeps the card's `min-height` (`--card-min-h`), so the layout does not jump.
- empty: the labelled placeholder (the proof's frame: pill and neutral bars) is the empty state, used for every IMG## whose file is missing.
- error: n/a — no input, no request. If an image file fails to load its `alt` text shows; no error UI is designed.
- success: n/a — nothing is submitted.
- disabled: n/a — nothing can be switched off.

**Notes.** F1. Boxes: 1 card + 1 field (2 of 4). Event `cta_secondary_target_view` fires when this section becomes visible after the hero secondary click (section 7).

#### S06 · Fix
Page P01·A · flows FL01, FL02, FL11 · focal point: CR Scan AI builds a proposed fix for what it found.

**Purpose.** Show step 2 of the loop.

**Layout (top → bottom; proof frame S06, Step 17 K3).** `.frame` > `.frame-inner` > `.split.split-reverse` (7fr 5fr: visual left, text right on desktop; text first on mobile): `.split-visual` > `.field.field-2` > `figure.card` with the pill and IMG02; `.split-text` with `h2.title-section` and `p.text-body`. Placeholder: pill, one `.card.card-inner.card-small` (three bars), then two bars. Measured on the proof: 629 px at 1440 (field 709 × 437, card 581 × 309, inner card 501 × 116) and 557 px at 375.

**Content (verbatim, APPROVED default).**
- Headline: Then it builds a proposed fix.
- Body: For what it found, CR Scan AI builds a proposed fix.
- CTA label: none
- Alt text, Illustration 2: Illustration of one proposed fix shown on a card.
- Visual label: Illustration

**Visuals.** IMG02: one proposed fix on one card: a title line, a one-line reason, a small status marker, a change row, the proposal highlight on the accent tint; no number; do not show what changes inside the store; no approve button here (that belongs to S07).

**Actions.** None.

**States.** 
- default: as in Layout.
- hover: n/a — no link or button in this section.
- pressed: n/a — same reason.
- focus: n/a — nothing in this section can take keyboard focus (the picture is not a control).
- loading: n/a — nothing is fetched. While an IMG file loads the figure keeps the card's `min-height` (`--card-min-h`), so the layout does not jump.
- empty: the labelled placeholder (the proof's frame: pill and neutral bars) is the empty state, used for every IMG## whose file is missing.
- error: n/a — no input, no request. If an image file fails to load its `alt` text shows; no error UI is designed.
- success: n/a — nothing is submitted.
- disabled: n/a — nothing can be switched off.

**Notes.** F2. Boxes: 2 cards + 1 field (3 of 4).

### 4.3 B-only sections (P01·B "One store, with AI on top")

#### S10 · Hero B
Page P01·B · flows FL04, FL05, FL06, FL08, FL10, FL12 · focal point: ShopBase 2.0 is one store platform, with AI that finds what stops shoppers and builds the fix (a store with the scan card on top of it).

**Purpose.** State the promise as a store platform with AI on top. Primary button above the first scroll (FL10).

**Layout (top → bottom; proof frame S10, Step 17 K1).** Same structure as S03: `.hero-stack` (`h1.title-hero`, `p.text-lead`, `.button-row`), then `.hero-visual` > `.field.field-2` > `figure.card` with the pill and IMG05 **in full** (not cropped). Placeholder: pill, three bars (short, tall, mid) and one `.card.card-inner.card-small` (two bars). Measured on the proof: 1076 px at 1440 (field 1280 × 489, card 736 × 361, inner 656 × 88) and 936 px at 375 (card 295 × 313). The headline is the page's one `<h1>`.

**Content (verbatim, APPROVED default).**
- Headline: ShopBase 2.0: one store platform, with AI that finds what stops shoppers and builds the fix.
- Support: On your store, CR Scan AI finds what stops shoppers and builds a proposed fix. You approve every change.
- CTA label (primary): Get started for free
- CTA label (secondary): Explore CR Scan AI
- Alt text, hero illustration: Illustration of a store page with a scan card on top of it.
- Visual label: Illustration

> **DO NOT BUILD (ALTERNATE, needs Gate 5 sign-off).** The screenshot's outcome headline is not part of the build.

**Visuals.** IMG05: one store with the scan card on top of it; no number, no real domain. No confirmed part names as labels (S11 is not confirmed).

**Actions.**
- "Get started for free" → `https://accounts.shopbase.com/sign-up` with the referral parameters kept (K12 SUSPECTED, to confirm).
- "Explore CR Scan AI" → on-page anchor **`#s12`** (S12 · Scan and fix), per the copy file (drop the button if S11 is ever built and grows).

**States.** Same as S03: default as in Layout, hover (proof), pressed (not in the proof, to confirm: as S03), focus (proof's ring), loading n/a (links), empty = the placeholder when IMG05 is missing, error n/a, success n/a, disabled n/a.

**Notes.** One extra secondary button is the cap exception. Boxes: 2 cards + 1 field (3 of 4).

#### S11 · One product: the parts list (B only, CONDITIONAL)
Page P01·B · flows FL04, FL05, FL06, only if confirmed · focal point: ShopBase 2.0 is one independent product for running a store, listing only the parts the user confirms.

> **DO NOT BUILD unless confirmed. Default: this section is NOT BUILT and has no markup.** P01·B has 7 sections without it; the "one product" statement stays only in the S10 headline.
> - It needs the user to say which parts really ship in ShopBase 2.0 (store, catalog, payments, fulfillment, support), whether "built in" is true, one plain sentence per part, and an alt text if a parts visual is supplied. None is confirmed.
> - If confirmed it follows the copy in `14-copy.md` (S11 block), at most 4 boxes (five parts must merge to four or become labels), no old brand names, no speed, cost, reliability or "built in" claim. The secondary hero button may then need to be dropped.
> - If built, the page needs its own `S11 · One product: the parts list` markup, spec rows for states and actions, and the B events add `s11_present: true`. Do that as a spec change, not in the build.

#### S12 · Scan and fix
Page P01·B · flows FL04, FL05, FL06, FL12 · focal point: CR Scan AI finds what stops shoppers on this store and builds the fix (target of the hero secondary button).

**Purpose.** Show the AI layer on this store: K2 and K3 in one section.

**Layout (top → bottom; proof frame S12, Step 17 K2 and K3).** `.frame` > `.frame-inner` > `.split` (5fr 7fr): left `.split-text` (`h2.title-section`, `p.text-body`); right `.split-visual` > `.field.field-3` > `figure.card` with the pill and IMG06. Placeholder: pill, two bars, one `.card.card-inner.card-small` (three bars). Measured on the proof: 629 px at 1440 (field 709 × 437, card 581 × 309) and 582 px at 375. The section carries `id="s12"`.

**Content (verbatim, APPROVED default).**
- Headline: A scan, then a proposed fix.
- Body: On your store, CR Scan AI finds what may be stopping shoppers. For what it found, it builds a proposed fix.
- CTA label: none
- Alt text, illustration: Illustration of a finding and its proposed fix shown on a store.
- Visual label: Illustration

**Visuals.** IMG06: the finding and its proposed fix shown on a store, one image (two images is the user's call and a change to the Step 12 plan; default one); no number.

**Actions.** None (landing point of "Explore CR Scan AI").

**States.** 
- default: as in Layout.
- hover: n/a — no link or button in this section.
- pressed: n/a — same reason.
- focus: n/a — nothing in this section can take keyboard focus (the picture is not a control).
- loading: n/a — nothing is fetched. While an IMG file loads the figure keeps the card's `min-height` (`--card-min-h`), so the layout does not jump.
- empty: the labelled placeholder (the proof's frame: pill and neutral bars) is the empty state, used for every IMG## whose file is missing.
- error: n/a — no input, no request. If an image file fails to load its `alt` text shows; no error UI is designed.
- success: n/a — nothing is submitted.
- disabled: n/a — nothing can be switched off.

**Notes.** F3 (one of at most two F3 sections in B, with S07). Boxes: 2 cards + 1 field (3 of 4). Event `cta_secondary_target_view` fires here.

## 5 · Shared components (same class names as `proof.html`)

Classes marked **new** are not in the proof (header, footer, mobile menu, image); they use tokens only.

| Component | Class names | Variants | States (in words) |
|---|---|---|---|
| Section frame | `.frame`, `.frame-inner` | one | Padding-block `--section-gap`, inline `--gutter`; content max `--container`, centred. Stacked frames add their paddings: the gap between two sections' content is two section gaps (12rem desktop, 8rem mobile), as in the proof frames. |
| Primary button | `.btn.btn-primary` | with arrow icon (always, label "Get started for free"); full width on mobile | default fill `--color-primary`, text `--color-on-primary`; hover fill and border `--color-primary-hover` (proof); focus ring `--color-focus`; pressed = hover (not in the proof, to confirm); loading, disabled: n/a (a link). |
| Secondary button | `.btn.btn-secondary` | hero only | default white fill, 1px `--color-border` outline, text `--color-title`; hover fill `--color-panel` (proof); pressed adds the `--color-border-field` outline (not in the proof, to confirm); focus ring. |
| Icon | `.icon` (inline Lucide SVG) | arrow-right; menu and x for the mobile menu | `currentColor`, `--icon` size, `aria-hidden`. |
| Headlines and text | `.title-hero`, `.title-section`, `.text-lead`, `.text-body`, `.text-caption` | mobile sizes by variable re-pointing | text only; no states. |
| Hero stack | `.hero-stack`, `.button-row`, `.hero-visual` | S03, S10 | button row centred, wraps; full-width column at ≤767px. |
| Closing stack | `.closing-stack` | S09; reused for S04 (not in the proof, to confirm) | centred on the plain page. |
| Split row | `.split`, `.split-reverse`, `.split-text`, `.split-visual`, `.visual-caption` | text left or text right | one column at ≤767px, text first. |
| Soft field | `.field`, `.field-1`, `.field-2`, `.field-3` | F1 Mist, F2 Sky, F3 Azure | two-stop gradient at `--field-angle`; padding `--field-pad`; never behind text except as allowed (section 2.1). |
| Card | `.card`, `.card-small`, `.card-inner` | outer card on a field (white, soft shadow, no border); inner card (accent tint, no shadow); at most one inner card per card | static; not a control. |
| Illustration pill | `.pill` ("Illustration") | one per illustration | solid panel fill, body text, 1px `--color-border`; sits on the white card, never directly on F3; always visible. |
| Image in a card | `.card-img` (**new**) | S05, S06, S07, S08, S10, S12 (full); S03 (top crop) | `width: 100%`, `height: auto`, keeps the file's ratio; `alt` from the copy file; no `loading="lazy"`; with `width`/`height` attributes set to the export size. |
| Placeholder bars | `.bars`, `.bar`, `.bar-short`, `.bar-mid`, `.bar-long`, `.bar-tall` | placeholder state only | neutral `--color-bar`; white inside an inner card. Used only until the user's image exists. |
| Approve region | `.region` | S07 placeholder state only | dashed outline, text "Approve control: part of the illustration"; not live UI. |
| Header | `.skip-link`, `.site-header`, `.site-header-inner`, `.logo-link`, `.nav`, `.nav-link`, `.menu`, `.menu-toggle`, `.menu-panel` (**new**) | desktop bar; mobile menu | see S01. |
| Footer link list | `.site-footer`, `.footer-grid`, `.footer-title`, `.footer-list`, `.footer-link`, `.footer-legal` (**new**) | two columns; stacked on mobile | see S02. |
| Focus ring | `a:focus-visible`, `summary:focus-visible`, `.btn:focus-visible` | all interactive elements | `--focus-w` ring, `--focus-offset`, `--color-focus`; never removed. |

Proof-only parts that must **not** be built into the page: `.legend-card`, `.proof-*`, `.frame-legend`, `.frame-label`, `.frame-meta`, `.frame-supply`, `.frame-index`, `.report-*`, `.logo-legend*`. The canvas and `.frame-device` are an outer wrapper only.

## 6 · Coverage

**Sections.** All 12 codes S01 to S12 appear once as a section heading in section 4 (checked by code, Appendix B); none is dropped, none renumbered.

| S## | Name | Group | Pos in A | Pos in B | Built by default | Section heading in this file |
|---|---|---|---|---|---|---|
| S01 | Header | SHARED | 1 | 1 | yes | 4.1 |
| S02 | Footer | SHARED | 9 | 7 | yes | 4.1 |
| S03 | Hero A | A only | 2 | - | yes | 4.2 |
| S04 | The unseen problem | A only | 3 | - | yes | 4.2 |
| S05 | Scan | A only | 4 | - | yes | 4.2 |
| S06 | Fix | A only | 5 | - | yes | 4.2 |
| S07 | Approve | SHARED | 6 | 5 | yes | 4.1 |
| S08 | AOV AI | SHARED | 7 | 4 | yes | 4.1 |
| S09 | Closing call to action | SHARED | 8 | 6 | yes | 4.1 |
| S10 | Hero B | B only | - | 2 | yes | 4.3 |
| S11 | One product: the parts list (CONDITIONAL, not built) | B only, CONDITIONAL | - | - | no (CONDITIONAL, fenced) | 4.3 |
| S12 | Scan and fix | B only | - | 3 | yes | 4.3 |

**Flows.** All 12 flows FL01 to FL12 from Step 12 are covered: every section in every flow's path is built by default, except S11, which appears in FL04 to FL06 only if confirmed (without it the path skips it, as Step 12 says).

| FL## | Variant | Persona | Path (Step 12) | Entry source | Ends at (Step 12) | Spec: way in and next step |
|---|---|---|---|---|---|---|
| FL01 | A | A dropshipper | S01 → S03 → S04 → S05 → S06 → S07 → S08 → S09 | unknown, no analytics | Click [P] in S03 or S09 → sign-up page (outside P01) | way in: Home URL; next step: sign-up button |
| FL02 | A | B POD seller | S01 → S03 → S04 → S05 → S06 → S07 → S08 → S09 | unknown, no analytics | Same | way in: Home URL; next step: sign-up button |
| FL03 | A | M existing merchant | S01 (Login link) or S01 → S03 → S07 → S09 | unknown (they read Home and log in, `brief.md` §2; how they arrive is not stated) | Login (S01) or sign-up | way in: Home URL; next step: Login (S01) or sign-up button |
| FL04 | B | A dropshipper | S01 → S10 → S11 (if confirmed) → S12 → S08 → S07 → S09 | unknown, no analytics | Click [P] in S10 or S09 → sign-up page | way in: Home URL; S11 only if confirmed; next step: sign-up button |
| FL05 | B | B POD seller | Same as FL04 | unknown, no analytics | Same | way in: Home URL; next step: sign-up button |
| FL06 | B | M existing merchant | S01 (Login link) or S01 → S10 → S11 (if confirmed) → S12 → S08 → S07 → S09 (`11` option B merchant flow: beats 3 to 5) | unknown (they read Home and log in, `brief.md` §2; how they arrive is not stated) | Login or sign-up | way in: Home URL; S11 only if confirmed; next step: Login (S01) or sign-up button |
| FL07 | A | A and B (same path) | S01 → S03 → S09 | Referral or affiliate link with `fpr` etc. (exists in the live script; volume unknown) | Click [P] with parameters kept → sign-up | way in: Home URL via a referral link (parameters kept); next step: sign-up button |
| FL08 | B | A and B (same path) | S01 → S10 → S09 | Referral or affiliate link | Same | way in: Home URL via a referral link (parameters kept); next step: sign-up button |
| FL09 | A | A and B | S03 (first screen) → [P] | Paid ad click (tags exist; whether campaigns land on Home is unknown) | Sign-up | way in: Home URL via a paid ad (hero above the first scroll); next step: sign-up button |
| FL10 | B | A and B | S10 (first screen) → [P] | Paid ad click (same note) | Sign-up | way in: Home URL via a paid ad (hero above the first scroll); next step: sign-up button |
| FL11 | A | A and B | S03 → [S] Explore CR Scan AI → S05 → S06 → S07 → ... | Any source, via the hero secondary button | Primary button only in S09, or in S01 if the header stays visible while scrolling | way in: Home URL via the hero secondary button; next step: sign-up button |
| FL12 | B | A and B | S10 → [S] Explore CR Scan AI → S12 (skips S11) → S08 → S07 → ... | Any source, via the hero secondary button | Same as FL11 | way in: Home URL via the hero secondary button; next step: sign-up button |

**Every page has a way in and a next step.** P01 is the only page. Way in: the Home URL; inbound sources are unknown (no analytics): referral links with `fpr`, paid ads, organic search, returning merchants (Login). Next step: the sign-up page (three primary buttons: S01, hero, S09), Login (S01), and the footer links (S02). No dead end on the page itself. One risk, handled by the sticky header: S05 to S08 and S12 carry no button (FL11, FL12; section 3.3).

## 7 · Measurement hooks

Tooling is **undecided**: no analytics tool is chosen and no test-splitting tool is known (Step 05 Q3, Step 12 decision 2). The build therefore adds **markup hooks only** (data attributes, no script, no vendor tag) and keeps the existing tags unchanged; a tool's code is added at Step 21/24 once chosen `[NEEDS DECISION]`.

**Every event carries `variant` = `A` or `B`** (Step 12 note 1), plus `section_id` (the S## code) and `position` (place in that variant's order, section 4.0). For P01·B also `s11_present` = `false` (S11 not built). Parameter names are tool-neutral `snake_case` from Step 05.

Hook convention on each element: `data-section-id="S03"`, `data-section-type="hero"`, `data-variant="A"`, and on clickables `data-event="…"` and `data-cta-label="…"`. Section types: `header`, `hero`, `feature` (S04 to S08, S12), `closing`, `footer`.

| Step 05 event | Name | Fires on | Parameters (all with `variant`, `section_id`, `position`; B also `s11_present`) |
|---|---|---|---|
| E01 | `home_view` | Whole page load | `device`, `source`, `has_referral_params`, `variant` |
| E02 | `cta_primary_click` | The primary button: S01 (header), S03 (A) or S10 (B), S09 | `section_type` (`header`, `hero`, `closing`), `section_id`, `cta_label` ("Get started for free"), `destination`, `variant`, `position` |
| E03 | `cta_secondary_click` | Hero secondary button: S03 (A, target `#s05`) or S10 (B, target `#s12`) | `section_type` (`hero`), `section_id`, `cta_label` ("Explore CR Scan AI"), `destination`, `variant` |
| E04 | `cta_secondary_target_view` | S05 (A) or S12 (B) becoming visible after an E03 click | `section_id`, `variant` |
| E05 | `signup_outbound_click` | Any link to `accounts.shopbase.com/sign-up`: S01, S03 / S10, S09 (catch-all by destination) | `section_type`, `section_id`, `cta_label`, `has_referral_params`, `destination`, `variant` |
| E06 | `signup_form_submit` | **none**: the email-first form is not carried, so no form exists | n/a |
| E07 | `scroll_depth` | Whole page at 25, 50, 75, 100 % | `percent`, `device`, `variant`; not comparable across variants (page heights differ): also record the pixel depth |
| E08 | `section_view` | Every built section, at least half in view: A = S01, S03, S04, S05, S06, S07, S08, S09, S02; B = S01, S10, S12, S08, S07, S09, S02 | `section_id`, `section_type`, `position` (section 4.0), `variant` |
| E09 | `signin_click` | Login link in S01 | `section_type` (`header`), `destination`, `variant` |
| E10 | `demo_link_click` | **none**: "Book a demo" is not carried | n/a |
| E11 to E13 | `signup_start`, `signup_complete`, `store_create_complete` | Outside P01 (`accounts.shopbase.com` and the app) | `entry_page`, `source`, and **`variant`, which cannot be carried today** (see the constraint below) |

**Referral-parameter constraint (K12 SUSPECTED, strong).** The live page's script reads `fpr`, `fpt`, `clickId`, `invite_trial` and appends them to some sign-up links. Rules for the build: (1) each of the three primary sign-up buttons is a plain `https://accounts.shopbase.com/sign-up` link marked `data-signup-link`, so the referral script (or its replacement) can find and rewrite it; the build never strips or renames the parameters or their cookies; (2) click events read the destination **at click time**, not at load, because the script rewrites links after load; (3) `has_referral_params` is logged as true or false only, never the values; (4) adding a `variant` parameter to the sign-up URL, so E11 to E13 on `accounts.shopbase.com` can be split by variant, is **not done by default** `[NEEDS DECISION]`: it must not alter the referral parameters. The default means the North Star cannot be split by variant until the user decides how the variant travels to sign-up. **Stated plainly: the live script will not rewrite any of the new buttons as built.** Per the audit (K12) it rewrites only links whose `href` already contains `sign-up?` or `sign-in?`, the two old header buttons (selector `.navigation-right .button-navigation`) and forms; the new plain `sign-up` links (no `?`) and the new header classes match none of these. So the referral script must be updated (or replaced) to target `data-signup-link` before publishing, or referral credit is lost on all three buttons. That is a Step 24 item (with the K12 confirmation), not a build item; the build only adds the marker.

## 8 · Image, video and motion slots

**Scope of an image (decision of this step, to confirm).** Each IMG## is the picture that sits **inside the white `.card`, under the "Illustration" pill**. The page draws the soft field, the white card, its radius and shadow, and the pill from tokens; the picture is a flat illustration on a pure white background that merges into the card. This keeps every colour and edge identical to the proof. The alternative (a card on a pale field drawn inside the image) cannot be cropped to both the 1440 and 375 field shapes and its colours would not match the tokens; it is listed in section 11.

**Export size and ratio (derived).** The proof's placeholder cards leave an image area of about 656 × 159 (S03), 501 × 159 (S05), 501 × 180 (S06, S12, S08), 501 × 168 (S07) and 656 × 232 px (S10) at 1440 (ratios 4.1, 3.2, 2.8, 3.0, 2.8). One shared ratio of **3:1** is the closest single fit, so every slot is exported **1200 × 400 px** (wide enough for the widest slot, 656 px, at 1.8×; the 501 px slots get 2.4×). At 375 the card is 295 px wide (image width 247 px, height 82 px): the card keeps its `--card-min-h`, so the picture sits at the top with empty white card below it; if that looks wrong at Step 22, a taller mobile crop is a review item.

| IMG## · name | Sections | What it shows | Ratio · export size | File in `02-assets/images/` |
|---|---|---|---|---|
| IMG01 · scan-card | S05 (full), S03 (hero, top crop) | A scan result card: a short list of what the scan found, generic bars, one highlighted row; no number, no domain | 3:1 · 1200 × 400 px (derived) | `02-assets/images/IMG01-scan-card.png` |
| IMG02 · proposed-fix-card | S06 (A) | One proposed fix on one card: title, one-line reason, status marker, a change row, accent-tint highlight; no number; nothing shown changing in a store; no button | 3:1 · 1200 × 400 px (derived) | `02-assets/images/IMG02-proposed-fix-card.png` |
| IMG03 · approval-card | S07 (A and B) | One small card with a proposed change and a single approve control (the only primary-colour element); no number, no domain; the control is part of the picture, not live UI | 3:1 · 1200 × 400 px (derived) | `02-assets/images/IMG03-approval-card.png` |
| IMG04 · offer-card | S08 (A and B) | One generic offer on one card with generic labels; no number or percentage; no real product; no specific offer type | 3:1 · 1200 × 400 px (derived) | `02-assets/images/IMG04-offer-card.png` |
| IMG05 · store-with-scan-card | S10 (B hero) | One store page with the scan card on top of it; no number, no real domain | 3:1 · 1200 × 400 px (derived) | `02-assets/images/IMG05-store-with-scan-card.png` |
| IMG06 · finding-and-fix-on-store | S12 (B) | A finding and its proposed fix shown on a store, one image; no number | 3:1 · 1200 × 400 px (derived) | `02-assets/images/IMG06-finding-and-fix-on-store.png` |

Derivation (px; `derived` from the proof frames measured in headless Chrome: card padding 40 px desktop / 24 px mobile, card gap 24 / 16, pill height 25.34):

| Placement | Card at 1440 | Image area at 1440 (w × h) | Ratio | Card at 375 | Image width at 375 | Height at 3:1 |
|---|---|---|---|---|---|---|
| S03 (IMG01 crop) | 736 × 288 | 656 × 158.7 | 4.13 | 295 × 240 | 247 | 82.3 |
| S05 (IMG01) | 581.34 × 288 | 501.34 × 158.7 | 3.16 | 295 × 240 | 247 | 82.3 |
| S06 (IMG02; S08 assumed equal) | 581.33 × 309.34 | 501.33 × 180 | 2.79 | 295 × 261.34 | 247 | 82.3 |
| S07 (IMG03) | 581.34 × 297.17 | 501.34 × 167.8 | 2.99 | 295 × 269 | 247 | 82.3 |
| S10 (IMG05) | 736 × 361.34 | 656 × 232 | 2.83 | 295 × 313.34 | 247 | 82.3 |
| S12 (IMG06) | 581.34 × 309.34 | 501.34 × 180 | 2.79 | 295 × 261.34 | 247 | 82.3 |

Reuse rule: where two places show the same content they share one file (IMG01: the hero's crop and the S05 card). S03 shows the **top ~73%** of IMG01 (the proof's hero card area), so IMG01's most important rows go in the upper part. S07's approve control (primary colour) is drawn inside IMG03.

**Video: none. Motion: none.** The proof has no video, no animation, no transition, no carousel; none is added. No Open Graph image is specified (not in the copy brief; `[NEEDS DECISION]`, default: none).

**Status of the images:** none of the six exists yet (they are the user's "Illustration" pieces). Until a file exists its slot stays the labelled placeholder from the proof; the page labels every one "Illustration" and never presents it as real product UI. An image generator will not produce an accurate product interface; see `image-prompts.md`.

## 9 · Type C: new name in, old brand out

### 9.1 Where the new name and brand must appear

| Place | What | Variant |
|---|---|---|
| `<title>`, meta description, Open Graph title and description | "ShopBase 2.0" (SEO draft in section 3.1) | A and B (own text each) |
| Hero headline (`<h1>`) | "ShopBase 2.0: one store platform, …" | B (A's headline does not carry the name) |
| Closing call to action headline | "Start with ShopBase 2.0." | A and B |
| Closing line | "ShopBase 2.0 is one product." | A only |
| Hero support and body lines | The 2.0 tool names "CR Scan AI" (hero support, S05, S06 / S10, S12) and "AOV AI" (S08), each with a plain-word description of what it does | A and B |
| Header and footer logo | `Logo (6).svg`, as provided, with clear space; alt text `ShopBase` | A and B |
| Favicon | `Logo (3).svg` as provided `[NEEDS DECISION]` | A and B |
| Footer legal labels | "Terms of service", "Privacy policy" and the two payments terms labels (SUSPECTED) | A and B |
| Brand colours | Option 1 blue family only; logo files unchanged | A and B |

Counts of "ShopBase 2.0" in the default copy lines of this file: P01·A 2, P01·B 2 (headlines, lines, captions and alt text only; the title and meta description add more).

### 9.2 Old-brand items that must NOT appear (identity migration list and audit inventory)

| Old item | Rule |
|---|---|
| PrintBase (text, footer link to `printbase.com`), PlusBase (footer link, `PlusBase Logo Dark Color.png`), PrintHub, PlusHub (integrations-strip logos, footer link text) | Retire. No link, no logo, no text. |
| "Print on demand", "Print-On-Demand", "Dropshipping" as nav items, tabs, headings, the typing headline, "Dropshipping Zone" | Not carried (nothing in the page's copy uses them; the audience is addressed without the product split). |
| Per-model tabs (E-commerce brands, Dropshipping, Print-On-Demand) | Dropped (OLD-04). |
| Old promise "Build a profitable E-commerce business in a few clicks with ShopBase", "in a few clicks", "all-in-one", "app mazes", "No more money waste for third-party apps", "best eCommerce platform", "free for 14 days" | Not carried, in the page or the meta tags. |
| "100% Happiness Guarantee", "Award-winning Support Team", "24/7 live chat", "$700 Millions+", "365,500+ merchants", "90,000+ stores" | Not carried (no source, no number allowed). |
| "Book a demo" (text link and the mislabelled button), "Start Free Trial", "Start 14-Day Free Trial", "Join us", "Find out more" and any other sign-up spelling | Only "Get started for free" exists. No email-first hero form. |
| Old logo files `Logo full.svg`, `ShopBase-Logo Light@1x.svg`, `sb smilde.svg` and any second header logo | Replaced by the three supplied SVGs (only `Logo (6).svg` on the page). |
| "ShopBase Hero", "ShopBase Network", "ShopBase Marketplace", "Made in ShopBase" tiles, template showcase, partner-logo strip, stats ("$700 Millions+" and the others), testimonials, service-commitment block | Not carried (open decision of the user, default none). The only exception is the two payments-terms legal labels in the footer (S02). |
| Country logic: flag, "from Bangladesh" / "from India" in the headline, footer Facebook groups by country, `loc.beeketing.com` | Dropped by default (K13). |
| Legal entity name ("OpenCommerce Group, Inc", legal pages only), `support@shopbase.com`, the copyright line (live Home: "© ShopBase" with a script-set year; legal pages: © 2021), DMCA link | Not on Home by default; the user decides (identity rows 12 to 14, K5b). Dropping the live Home's copyright line is part of that decision. |
| Any numbers, result claims, comparisons, "built in", "Free Launch", "automatic", Vietnam-specific text | Not on the page. |

## 10 · Two variants: how to build

**DEFAULT: two separate HTML outputs, `09-final-ui/final-ui-A.html` (P01·A) and `09-final-ui/final-ui-B.html` (P01·B)**, each a complete page (a default the user can change, section 11 item 15; the kit's base prompts name one `final-ui.html`, so Steps 22 and 23 then run once per file), both built from the same `:root` tokens (Appendix A) and the same shared components (section 5). **Build A first**: it has 9 sections and no CONDITIONAL part in its default; B has CONDITIONAL parts (S11, the plan line), which stay unbuilt, and B reuses A's header, footer, S07, S08, S09 and component CSS unchanged. Shared sections are identical between files (same markup, same text) except the stated variant differences: the `data-variant` value, the title and meta, the hero, the secondary button anchor (`#s05` in A, `#s12` in B), the S08 order, and S09's optional line (A shows it, B leaves it empty).

How the two go live (one URL with a split, two URLs, one in reserve) is **not decided** (Step 12 decision 2, a BLOCKER at Step 21 for publishing, not for building). The build adds no splitting logic.

## 11 · Open decisions

| # | Decision | Default used |
|---|---|---|
| 1 | **Mobile field radius.** The proof renders field and card both at 1rem on mobile (`--radius-field` points at `--radius-card`, which is also re-pointed). "Inner smaller than parent" suggests the field should be 1.5rem on mobile. | **Keep the proof's value (1rem).** To change: in the mobile block of Appendix A set `--radius-field` to the value of token `radius.24` (1.5rem). One line. |
| 2 | **Card shadow exception.** The Step 18 rule was "shadows go on an outer wrapper"; the proof puts one soft shadow inside the frames on white cards on a field. | Keep as the proof: `--shadow-card` on `.card` on a field only; none on inner cards or cards on the plain page. |
| 3 | **Hero field width.** The hero field fills the content column (1280 px at 1440, 89% of the viewport). | Keep as the proof. |
| 4 | **Hero headline element.** The proof draws it as `<h2>`. | The build makes the hero headline the one `<h1>` (S03, S10). |
| 5 | **Hero "Explore CR Scan AI" target.** | `#s05` in A, `#s12` in B (copy file). |
| 6 | **Header: Pricing link (K1).** Approved copy says drop it if not confirmed; Step 12 had it in the default header. | Not built; confirm to add (`https://www.shopbase.com/pricing`). |
| 7 | **Footer:** column set and arrangement, K3 to K6 links, store URLs, `/dmcareport` (default off), legal entity and year (default: no line), cookie text (default: none), "ShopBase Payments terms" and "Marketplace payments terms" labels (default: shown). | As stated in S02. |
| 8 | **Sticky header** (Step 12 default) and the mobile menu holding the primary button. | Sticky, button inside the mobile menu. |
| 9 | **Header and footer, S04 and S08 visuals** are not in the proof. | Built as proposed in section 4; judged at Step 21/22. |
| 10 | **Image scope** (picture inside the card, not card-on-field) and ratio 3:1. | As section 8. |
| 11 | **Two extra Lucide icons** (`menu`, `x`) for the mobile menu. | Add the two files, unchanged. |
| 12 | **S11, the plan line, the S08 link line and the ALTERNATE headlines.** | All unbuilt. |
| 13 | **How the variants go live; variant passed to sign-up; analytics tool; canonical; structured data; Open Graph image; favicon use.** | Not decided; the build adds nothing for them. |
| 14 | **Gate 7** (the Strategy owner approves tokens and this spec). | Open. |
| 15 | **Two output files, A first** (`final-ui-A.html`, then `final-ui-B.html`). | Two files, A built and reviewed first; the user may change it (for example build only A now, or B first). |
| 16 | **Must-keep tags and scripts** (K7 to K12, K14: Google Ads, Facebook Pixels, Sender, verification metas, referral script, status widget; Step 12 decision 1). | Not part of the design build; kept unchanged and wired in at Step 24 with the user's yes. The referral script must be updated to target `data-signup-link` (section 7). |
| 17 | **Logo clear space and minimum size** (Step 10 proposals: 24/254 of the logo width, 120 px full logo, 24 px icon). | Used as proposed (section 2.6). |

## 12 · Check before handing back (Step 20)

- [x] Every `S##` and state is in the spec, and the copy is verbatim from Step 14 (measured: 12 of 12 section headings; 50 strings checked, 0 mismatches).
- [x] Foundation matches `07-tokens/` exactly (measured: 83 of 83 `:root` variables and the responsive blocks resolve to the proof's values at 375, 1000 and 1440 px, 0 mismatches).
- [x] Caps and measurement hooks (with `variant` on every event) are in the spec (sections 3.6 and 7).
- [x] Every image slot has a code, a size, a prompt and a file name (6 of 6, cross-checked in the spec, `image-prompts.md` and `build-prompt.md`).
- [x] The build prompt demands the proof look, `:root` variables, no inline styles, no hex outside `:root`, one HTML file per variant (21 of 21 required demands present).
- [x] Hex appears only in section 2 and Appendix A of this file (0 elsewhere); the build prompt has none.
- [x] No CONDITIONAL or ALTERNATE copy is in a buildable section, the image prompts or the build prompt (all fenced, default not built).
- [ ] **Not met, stated plainly:** the six images do not exist yet (slots stay labelled placeholders until the user says "images done" or "skip images"); the header, footer, S04, S08, the mobile menu and the hover / pressed proposals are **not in the proof and were never rendered** (NOT RUN: judged at Step 21/22); page length is a derived estimate, not a rendered page; the 768 to 1439 px range is not a locked frame; every must-keep (K1 to K16) is still SUSPECTED; **Gate 7 is not approved**.


## Appendix A · `:root` block (generated by code from `07-tokens/`)

Generated by `step20_gen_root.py` from `2-semantic.json` and `1-primitive.json` (names and the 83 variables are the proof's; each value is resolved from the token named in the comment). Six variables are not tokens (placeholder bars, proof chrome): they are copied from the proof and marked. The `@media` blocks use the breakpoints of `layout.breakpoint.*`. Copy it unchanged into the build. This appendix is the **only place besides section 2 where hex may appear.**

```css
:root {
  --color-primary: #4371CD; /* color.action.primary */
  --color-primary-hover: #3A62B2; /* color.action.primary-hover */
  --color-on-primary: #FFFFFF; /* color.text.on-primary */
  --color-accent-tint: #E7F3FD; /* color.surface.accent */
  --color-page: #FFFFFF; /* color.surface.page */
  --color-panel: #F4F7FC; /* color.surface.panel */
  --color-title: #1E222B; /* color.text.title */
  --color-body: #373B43; /* color.text.body */
  --color-muted: #596070; /* color.text.muted */
  --color-border: #7F8A9E; /* color.border.default */
  --color-border-field: #66718A; /* color.border.field */
  --color-divider: #DDE3EE; /* color.border.divider */
  --color-link: #3A62B2; /* color.text.link */
  --color-focus: #1E4A9E; /* color.focus.ring */
  --color-canvas: #DDE3EE; /* color.surface.canvas */
  --color-bar: #DDE3EE; /* color.neutral.200 */
  --field-1-a: #F3FAFE; /* color.field.1.stop-1 */
  --field-1-b: #EDF2FC; /* color.field.1.stop-2 */
  --field-2-a: #D1EBFB; /* color.field.2.stop-1 */
  --field-2-b: #D9E4F9; /* color.field.2.stop-2 */
  --field-3-a: #C5E6FA; /* color.field.3.stop-1 */
  --field-3-b: #A4BDEF; /* color.field.3.stop-2 */
  --field-angle: 135deg; /* field.angle */
  --shadow-card: 0 0.5rem 2rem rgba(30, 34, 43, 0.10); /* shadow.card */
  --shadow-device: 0 0.75rem 2.5rem rgba(30, 34, 43, 0.16); /* shadow.device */
  --font-sans: "Inter", system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* font.family.base */
  --fs-n1: 0.8rem; /* font.size.n1 */
  --fs-0: 1rem; /* font.size.0 */
  --fs-1: 1.25rem; /* font.size.1 */
  --fs-2: 1.5625rem; /* font.size.2 */
  --fs-3: 1.953rem; /* font.size.3 */
  --fs-4: 2.441rem; /* font.size.4 */
  --fs-5: 3.052rem; /* font.size.5 */
  --fw-regular: 400; /* font.weight.regular */
  --fw-medium: 500; /* font.weight.medium */
  --fw-semibold: 600; /* font.weight.semibold */
  --lh-tight: 1.1; /* font.line-height.tight */
  --lh-heading: 1.2; /* font.line-height.snug */
  --lh-body: 1.55; /* font.line-height.relaxed */
  --ls-tight: -0.02em; /* font.letter-spacing.tight */
  --ls-label: 0.04em; /* font.letter-spacing.wide */
  --size-hero: 3.052rem; /* typography.hero-headline.fontSize */
  --size-h2: 2.441rem; /* typography.section-headline.fontSize */
  --size-lead: 1.25rem; /* typography.lead.fontSize */
  --size-body: 1rem; /* typography.base.fontSize */
  --size-caption: 0.8rem; /* typography.caption.fontSize */
  --space-1: 0.25rem; /* space.stack.xs */
  --space-2: 0.5rem; /* space.stack.sm */
  --space-3: 1rem; /* space.stack.md */
  --space-4: 1.5rem; /* space.stack.lg */
  --space-5: 2.5rem; /* space.stack.xl */
  --space-6: 4rem; /* space.stack.2xl */
  --space-7: 6rem; /* space.7 */
  --section-gap: 6rem; /* space.section */
  --gutter: 2.5rem; /* space.gutter */
  --field-pad: 4rem; /* space.field-pad */
  --container: 75rem; /* layout.container.base */
  --legend-col: 14rem; /* NOT IN TOKENS (copied from the proof; placeholder bars / proof chrome) */
  --frame-max: 90rem; /* layout.page.frame-max */
  --text-measure: 38rem; /* layout.measure.text */
  --hero-text-measure: 54rem; /* layout.measure.hero */
  --card-min-h: 18rem; /* layout.card.min-height */
  --card-max-w: 46rem; /* layout.card.max-width */
  --control-h: 3.25rem; /* size.control-height */
  --icon: 1.25rem; /* size.icon */
  --bar-h: 0.75rem; /* NOT IN TOKENS (copied from the proof; placeholder bars / proof chrome) */
  --bar-short: 40%; /* NOT IN TOKENS (copied from the proof; placeholder bars / proof chrome) */
  --bar-mid: 70%; /* NOT IN TOKENS (copied from the proof; placeholder bars / proof chrome) */
  --bar-long: 100%; /* NOT IN TOKENS (copied from the proof; placeholder bars / proof chrome) */
  --split-cols: 5fr 7fr; /* layout.split.columns */
  --split-cols-reverse: 7fr 5fr; /* layout.split.columns-reverse */
  --line: 1px; /* border.width.default */
  --line-dashed: 2px; /* border.width.strong */
  --focus-w: 2px; /* focus.ring.width */
  --focus-offset: 2px; /* focus.ring.offset */
  --logo-w: 7.5rem; /* layout.logo.min-width */
  --logo-clear: calc(var(--logo-w) * 0.0945); /* layout.logo.clear-space-ratio */
  --radius-field: 2rem; /* radius.field */
  --radius-card: 1.5rem; /* radius.card */
  --radius-inner: 1rem; /* radius.inner */
  --radius-control: 0.75rem; /* radius.control */
  --radius-pill: 62rem; /* radius.pill */
  --radius-bar: 0.375rem; /* NOT IN TOKENS (copied from the proof; placeholder bars / proof chrome) */
}

@media (max-width: 1439px) {
  :root {
    --container: 68rem; /* layout.container.compact */
    --gutter: 2.5rem; /* space.gutter */
  }
}

@media (min-width: 1440px) {
  :root {
    --container: 80rem; /* layout.container.wide */
  }
}

@media (max-width: 767px) {
  :root {
    --size-hero: 1.953rem; /* typography.hero-headline-mobile.fontSize */
    --size-h2: 1.5625rem; /* typography.section-headline-mobile.fontSize */
    --size-lead: 1rem; /* typography.lead-mobile.fontSize */
    --section-gap: 4rem; /* space.section-mobile */
    --gutter: 1.5rem; /* space.gutter-mobile */
    --field-pad: 1rem; /* space.field-pad-mobile */
    --radius-field: 1rem; /* radius.field-mobile */
    --radius-card: 1rem; /* radius.card-mobile */
    --card-min-h: 15rem; /* layout.card.min-height-mobile */
  }
}
```

## Appendix B · Measured

All numbers below were computed by code and pasted unedited. Scripts (run with `python3 -I` from a folder outside the project; kept in the scratchpad `/private/tmp/claude-501/-Users-nguyentoan-Documents-SB-v2-LD/fb8c2ff0-4f7d-46ed-a2f8-aeb17aa0cde3/scratchpad/s20/`):

- `step20_gen_root.py`: generates Appendix A from `07-tokens/` and compares it with the proof's `:root`.
- `step20_build.py`: assembles this file from its template; copy strings, tables and positions are generated by code.
- `step20_check.py`: re-reads this file, `image-prompts.md` and `build-prompt.md` from disk and runs every check below (it excludes this Appendix B from its own checks).
- `step20_measure_mk.py` and `step20_measure_mk2.py`: copy the proof to a test file with a measuring script (the proof itself is untouched) and measure it in headless Chrome at 1440 (window) and 375 (an iframe of that width).

**`step20_gen_root.py` output**

```
proof base :root variables: 83 | generated base variables: 83
generated from a token: 77 | not in tokens (copied from proof): 6
literal text identical to the proof (before resolving var()): 73 of 83
width 375: variables compared 83 (proof) / 83 (generated) | mismatches after resolving var() and the media cascade: 0 []
width 1000: variables compared 83 (proof) / 83 (generated) | mismatches after resolving var() and the media cascade: 0 []
width 1440: variables compared 83 (proof) / 83 (generated) | mismatches after resolving var() and the media cascade: 0 []
media blocks: proof ['max-width: 1439px', 'max-width: 767px', 'min-width: 1440px'] | generated ['max-width: 1439px', 'max-width: 767px', 'min-width: 1440px']
TOTAL mismatches over 3 widths: 0
```

**`step20_check.py` output**

```
S01 to S12 as section headings: 12 headings, each of the 12 codes exactly once: True | order in file (groups SHARED, A only, B only): S01 S02 S07 S08 S09 S03 S04 S05 S06 S10 S11 S12
FL01 to FL12 referenced in section 4: 12 of 12 (missing: []) | in the coverage table (section 6): 12 of 12 (missing: [])
Verbatim copy check against 14-copy.md: strings checked 50 (44 section fields, 2 microcopy, 4 SEO) | mismatches 0 []
Appendix A :root vs proof :root (resolved values, 3 widths): proof variables 83, spec variables 83, same name set: True | 375 px: 83 vars, 0 mismatches; 1000 px: 83 vars, 0 mismatches; 1440 px: 83 vars, 0 mismatches | total mismatches 0
IMG slots: spec table 6 (IMG01,IMG02,IMG03,IMG04,IMG05,IMG06) | prompts in image-prompts.md 6 | slots missing a code, size, prompt, file name or build-prompt entry: 0 [] | shared style line occurrences: 7 (1 definition + 6 prompts)
CONDITIONAL / ALTERNATE copy strings (from 14-copy.md fenced blocks): 7 unique lines | found outside a fenced block quote in master-spec, in image-prompts or in build-prompt: 0 [] | (kept inside a DO NOT BUILD block quote: 1)
Hex colours in master-spec: 44 total | outside section 2 and Appendix A: 0 [] | inside the two allowed places: 44 | build-prompt.md hex: 0 (image-prompts.md may carry hex: palette and style line)
Old-brand / banned-claim scan of 55 content lines: 0 hits [] | digits other than the name 'ShopBase 2.0': 0 []
build-prompt.md required demands present: 21 of 21 (missing: [])
Caps table and measurement hooks (with variant) present in master-spec: True
```

**Proof frames measured in headless Chrome (px)** (the proof's own report gives the same heights: 949 / 1076 / 608 / 629 / 629 / 653 / 386 at 1440 and 794 / 936 / 566 / 557 / 582 / 606 / 299 at 375; the iframe at 375 had a 16 px field radius, which confirms the open decision about the mobile field radius):

| Frame | Height at 1440 | Height at 375 | Card at 1440 | Card at 375 |
|---|---|---|---|---|
| S03 | 949.41 | 793.52 | 736 × 288 | 295 × 240 |
| S10 | 1076.45 | 935.61 | 736 × 361.34 | 295 × 313.34 |
| S05 | 608 | 565.59 | 581.34 × 288 | 295 × 240 |
| S06 | 629.34 | 556.94 | 581.33 × 309.34 | 295 × 261.34 |
| S12 | 629.34 | 581.73 | 581.34 × 309.34 | 295 × 261.34 |
| S07 | 653 | 605.63 | 581.34 × 297.17 | 295 × 269 |
| S09 | 385.88 | 298.8 | none | none |

Page-length figures in section 3.6 are sums of these heights plus the stated Step 12 estimates for header, footer and S04 (derived, not a rendered page).

