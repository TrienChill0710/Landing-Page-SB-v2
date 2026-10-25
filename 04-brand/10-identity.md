# 10 · Identity

Project: ShopBase website redesign · type **C · Rebrand** · page **P01 Home** · files in English · Gates 0 to 2 `APPROVED` (2026-10-24) · Brand module on · Gate 3 `open`.
Inputs read: `CLAUDE.md`, `_prompts/README.md`, `_prompts/10-identity.md`, `_progress.md` (Decisions log), `04-brand/09-messaging.md`, `03-research/02-intake.md`, `03-research/03-brief-analysis.md`, `03-research/04-audit.md`, `03-research/06-positioning.md` (me-too points only), `03-research/08-reference-analysis.md`, `02-assets/` (listed below), the user's hero screenshot, and the Calendly full-page reference (1920 x 14305 px, cut with Python PIL into 8 slices in the scratchpad; the original is untouched. The draft was written from 6 of the 8 slices; at review all 8 were viewed and the description below was corrected to match).

> **Read this first.**
> - **The user decided the name, logo and colours stay.** This step records them, measures the logo, and keeps everything else as a question or a proposal. It does **not** choose the final palette (Step 16).
> - **No logo was drawn, traced or edited.** The three SVGs were only read and measured.
> - **Everything marked PROPOSAL is mine, not a ShopBase brand rule.** No brand guideline was supplied (see "Brand guideline check").
> - The legal entity, the support email and the 2021 dates are **the user's decisions only** (Migration list rows 12 to 14).

---

## Status of each asset

| Asset | Status | What exists | What is missing |
|---|---|---|---|
| Logo (full, light surface) | **provided** | `02-assets/logo/Logo (6).svg` | Written usage rules (none supplied) |
| Logo (full, dark surface) | **provided** | `02-assets/logo/Logo (1).svg` (white wordmark, no background) | Whether any dark surface is planned (intake Q4, default: no) |
| Logo (icon only) | **provided** | `02-assets/logo/Logo (3).svg` | Where it is allowed (favicon, app icon) is not stated |
| Name | **provided** (stays) | "ShopBase" (user decision) | |
| Colour | **partly provided, to choose** | Logo colours (measured). A colour scale and the hero screenshot's blues (observed). | Which blue is the brand primary (open question 1). Final palette is Step 16 |
| Font | **not provided; to choose** | Nothing in `02-assets/`. The live site loads Inter today (observed) | Confirmation from the user (open question 3) |
| Icon style | **not provided; to choose** | Nothing in `02-assets/` (no `icons/` folder) | One library (proposed) |
| Imagery / illustration style | **to create**; direction given | The user will supply illustrations of the product demo (Decisions log, Step 09 Q2). Calendly reference saved | The illustrations themselves (Steps 17 and 18) |

`02-assets/` today: `README.md`, `logo/` (3 SVG), `images/hero-2.0-reference.png`, `moodboard/style-ref-01-calendly-fullpage.png`. There is **no** `fonts/` and **no** `icons/` folder.

---

## Logo

### As provided (measured by code, `python3 -I`, files untouched)

| File | Use | viewBox | Aspect | Paths | Fills |
|---|---|---|---|---|---|
| `Logo (6).svg` | full logo, **light** surfaces | `0 0 254 48` | 5.29 : 1 | 11 | wordmark `#373B43` (8 paths), icon `#497BDF`, `#8BCDF6`, smile white |
| `Logo (1).svg` | full logo, **dark** surfaces | `0 0 254 48` | 5.29 : 1 | 11 | wordmark white (8 paths), icon `#497BDF`, `#8BCDF6`, smile white. No background shape: on white only the icon shows and the wordmark disappears |
| `Logo (3).svg` | icon only | `0 0 48 48` | 1 : 1 | 3 | `#497BDF`, `#8BCDF6`, white |

All three are vector (only `<svg>` and `<path>`, no raster). The files carry no licence note; that the user owns them is an `ASSUMPTION` (intake W8).

Geometry from the path coordinates (bounding boxes computed from the exact extremes of each curve, `python3 -I`, re-run at review; the draft used control points, which gave values up to about 0.2 units wider):

- Icon: 48 x 48 units. The `#497BDF` shape fills y 0 to 40; the `#8BCDF6` base fills y 40 to 48. The white smile spans x 8.0 to 40.0 and y 12.0 to 24.45 (about 12.45 units tall).
- Wordmark: starts at x 62.12 and ends at x 253.17. Gap between icon and wordmark: 62.12 - 48 = **about 14.1 units** (about 0.29 of the icon height; the draft's control-point estimate was 13.95). Capital height about 32.4 units (y 8.0 to 40.44); lower-case x-height about 23.6 units (y 16.88 to 40.44); the "p" descends to y 47.91.
- Content width is 253.17 of 254, content height 48 of 48: the artwork touches the edge of the viewBox, so **the files carry no built-in margin**. All clear space must be added by the page.

### Clear space and minimum size: PROPOSAL (not a ShopBase rule)

No brand guideline was supplied, so these are derived from the geometry only. The user (Strategy owner) confirms or changes them.

| Item | Proposal | How it was derived |
|---|---|---|
| Clear space, all four sides | **24 units = half the icon height** (that is half the logo height, and 9.4% of the full logo's width: 24 / 254) | Half the icon height is larger than the icon-to-wordmark gap (about 14.1), so the space around the logo is clearly larger than the space inside it. At a header logo of 40 px tall this is 20 px |
| Minimum size, full logo | **120 px wide** (height 22.7 px) | At 120 px the logo is 120 x 48 / 254 = 22.7 px tall (so is the icon) and the wordmark x-height is 11.1 px (23.6 / 48 x 22.7). Proposed floor chosen so the x-height stays above 10 px. Not tested on real screens. `ASSUMPTION` |
| Minimum size, icon only | **24 px** | At 24 px the smile is about 6.2 px tall (12.45 / 48 x 24). Below this the smile stops reading. Not tested. `ASSUMPTION` |
| Print | Not proposed | Home is a web page only |

### Surfaces (measured contrast, WCAG 2.x formula)

Dark sample surface: `#121212`, the hero screenshot's near-black text colour, used only as a test value (no dark surface is chosen).

| Logo part | On white | On `#121212` | Note |
|---|---|---|---|
| Icon blue `#497BDF` | 4.05 : 1 | 4.62 : 1 | Icon is a graphic, not text; the 3 : 1 level for graphics is met on both |
| Icon light blue `#8BCDF6` | 1.73 : 1 | 10.85 : 1 | Thin on white; it is the base strip of the icon, and the icon blue carries the shape |
| Wordmark `#373B43` | 11.24 : 1 | n/a | Use `Logo (6).svg` on light surfaces only |

Rules proposed: `Logo (6).svg` on light surfaces, `Logo (1).svg` on dark surfaces, never the reverse, no change of colour, no rotation, no effects. **Whether a dark surface exists on Home is not decided** (the Calendly reference ends in a dark footer; our default is still "light only", so `Logo (1).svg` stays unused until the user says otherwise).

### Brand guideline check

`https://www.shopbase.com/brand-guideline` and `https://www.shopbase.com/brand-asset` are both listed in the live `sitemap.xml`. Fetched politely with `curl` on 2026-10-24 (re-checked at review with a browser User-Agent into a new folder: a `GET` returns **404**; `curl -I`, a `HEAD` request, returns 405 from the server, which is not a page): **both return HTTP 404**, and the body is the site's own "ShopBase - Page Not Found" page (25,183 bytes; so did `/brand`, `/brand-guidelines`). **There is no brand guideline to quote.** Nothing in this file is taken from a guideline. If ShopBase has one elsewhere (a PDF, a Figma file, a design-system site), the user should supply it; it would replace every PROPOSAL above and might make Steps 16 and 17 stale. Saved copies are in the scratchpad (outside the project).

---

## Colour directions

### What the colours are today, with the source of each (not a palette)

| Colour | Hex | Role (as provided or observed) | Source | Status |
|---|---|---|---|---|
| Logo blue | `#497BDF` | Logo icon body. "Brand colour" by the user's decision (colours stay) | Measured from `Logo (3).svg` | **provided** |
| Logo light blue | `#8BCDF6` | Logo icon base strip | Measured from the SVG | **provided** |
| Logo wordmark dark | `#373B43` | Wordmark on light surfaces | Measured from `Logo (6).svg` | **provided** |
| White | `#FFFFFF` | Smile; wordmark on dark surfaces | Measured | **provided** |
| Blue (Primary) 500 | `#0096ED` | "Primary" in a colour scale the user showed in chat | Chat screenshot, **not stored in the project**, not verifiable (intake W9) | **provided in chat only** |
| Hero button fill | `#3B59F6` | Primary button ("Get started for free") | Sampled from `hero-2.0-reference.png`; re-sampled at review: a solid fill (3,464 of 3,465 pixels in a patch beside the label), with a lighter bottom edge about `#6083F7` | **observed** |
| Hero headline gradient | `#4454D0` (left) to about `#6A63DE` (right end), via `#565CD7` (re-sampled at review with PIL; the draft's end value `#6862DD` was taken slightly before the end of the line) | Second headline line | Sampled from the same screenshot | **observed** |
| Hero text colours | about `#121212` (headline, secondary button text), about `#676767` (sub-line) | Text | Sampled, approximate | **observed** |
| Live site body text grey | `#606b74` | Paragraph colour on today's site | Live site CSS (observed; untrusted data) | **observed** |

Measured gaps (from intake and Step 03, recomputed here only for the contrast figures above): logo blue `#497BDF` has hue 220 degrees; `#0096ED` has hue 202 degrees; the screenshot's blues have hue 230 to 243 degrees. They are **three different blues**. White text on `#497BDF` is 4.05 : 1 (fails the 4.5 : 1 level for normal text); on `#3B59F6` it is 5.32 : 1 (passes); on `#0096ED` it is 3.19 : 1 (fails).

### Open question: which blue is the brand primary

The user said "colours stay". The files supply one blue (`#497BDF`); the chat scale supplies another; the hero screenshot (which the user supplied as the 2.0 hero) uses a third, more violet one. Three directions, hue families only, **no final hex** (Step 16 produces and tests the palette):

| # | Direction | Mood | Hue family | Why it fits the messaging | How it stands apart | Risk |
|---|---|---|---|---|---|---|
| 1 | **Logo-true blue** (default) | Calm, plain, checkable | The logo's blue family (about 220 degrees) with its lighter sky blue for soft fields, on cool neutrals | Voice is plain, calm, no hype, seller in charge (09 voice 1 to 3). One familiar blue with no glow says "describe, don't dazzle". It matches the user's rule that logo and colours stay. The approve control can be the one saturated element | Step 06's me-too finding is about **wording** (4 of 5 competitors claim AI); colour alone cannot fix it. This direction avoids adding the "magic AI" look (08 colour direction). Competitor colours were **not measured** in Step 06, so no claim is made that blue is rare in the category | Plain blue is common in software generally. Normal-size white text on the logo blue fails 4.5 : 1, so Step 16 must darken the action colour or use dark text |
| 2 | **Blue-violet, as in the hero screenshot** | Modern, AI-era, energetic | About 230 to 245 degrees (indigo-leaning), gradient allowed on one line | It continues the user's own 2.0 hero, so the page and the product screenshot agree. Reads "new generation", which suits the "AI era" story | It moves the brand off the old ShopBase blue, which helps signal the rebrand. But in the reference CSS (Step 08) AI product pages already use blue and violet (`#6a5ae0` on Clarity, `#4d65ff` on Shoplift, `#2962ff` on Intelligems; inline CSS counts only), so this sits **inside** the AI-tool look, closest to the me-too risk. Step 08 also warned against gradient or glow that signals "magic" | Conflicts with "colours stay" unless the user counts the screenshot's blue as the brand colour (Step 03 R4). The gradient works against the calm, approve-every-change tone |
| 3 | **Ink and soft colour fields** (the Calendly direction) | Warm, friendly, grown-up | Near-black navy for actions and text; the logo's blue and sky-blue families appear only inside soft illustration fields; warm off-white page | The user chose Calendly as the style direction (Decisions log). Calendly's own page, as seen in the slices, uses a dark navy button, a warm off-white page and blue-to-lilac-to-pink fields behind the product cards, so colour comes from the illustrations and the buttons stay quiet. That makes the product demo (user-supplied illustrations) the colourful thing and the claims calm | The action colour is **not** blue, so the page does not look like the blue-button AI pages we sampled. The brand blue remains in the logo and the illustration fields | Dark buttons are less "ShopBase blue", so the brand reads weaker in the first screen. Warm off-white adds a second neutral for Step 16 to test. Pastel gradients near the Calendly look can drift toward copying, so Step 17 must use ShopBase's own shapes |

Default if the user does not answer: **Direction 1** (it is the intake's Q2 default and follows "colours stay"); Step 16 may borrow the fields idea from direction 3. This is a proposal, not a choice. The user chooses.

---

## Typography

### Observed on the live site today

Read from the homepage HTML and its stylesheet (`shopbase-landing.webflow.shared…min.css`, 665,296 bytes), downloaded into a new scratchpad folder and parsed with `python3 -I`:

- `body` and paragraphs use **`Inter`, then `sans-serif`** (Inter is the first family in 333 of the stylesheet's 427 `font-family` declarations, far more than any other; re-counted at review from a fresh download). The page loads **Inter 300, 400, 500, 600, 700** through the Google WebFont loader.
- The same loader also lists Oswald, Merriweather, PT Sans, Open Sans, Lato, PT Serif and Changa One, and the CSS names other families first in a few rules (PT Sans 21, DM Sans 16, Lato 12, Oswald 10, Open Sans 4, PT Serif 2, plus system stacks). DM Sans is **not** in the loader list and has no `@font-face`, so those rules would fall back to another font. These look like leftovers from the page builder; whether any is visible on Home was **not checked in a browser** (`NOT VERIFIED`).
- Observed styling: headings use tight tracking (`letter-spacing: -.03em` on the `h2` rule), medium weight; paragraphs 16 px with a 1.5 line height in grey `#606b74`.
- The user's typography scale (h1 28/36 … small 12/16, shown in chat only) names no family. The hero screenshot's lettering looks like a tight, heavy grotesque of the same kind. **That is only my reading of a picture, not an identification.**

### Proposal (not a ShopBase rule)

| Role | Font | Licence | Why |
|---|---|---|---|
| Heading | **Inter**, semibold to bold, tight tracking | **SIL Open Font License 1.1** | Already used by the live site; the hero screenshot looks consistent with it; one family keeps the page quiet and fast |
| Body | **Inter**, regular and medium | same | Same reasons. Two roles, one family on purpose; a second family is an option only if the user wants a serif voice like Calendly's (it sets its feature-section headlines and its customer quote in a serif, and its centred section headings in a sans) |

**Licence, verified from the official source:** the Inter repository's `LICENSE.txt` (`https://github.com/rsms/inter/blob/master/LICENSE.txt`, fetched as raw text on 2026-10-24) reads "Copyright (c) 2016 The Inter Project Authors" and "licensed under the SIL Open Font License, Version 1.1". Its permission clause reads: "Permission is hereby granted, free of charge, to any person obtaining a copy of the Font Software, to use, study, copy, merge, embed, modify, redistribute, and sell modified and unmodified copies of the Font Software, subject to the following conditions", among them that the font may not be sold by itself and that the licence text travels with copies. The licence text also contains the OFL's "Reserved Font Name" condition (modified versions may not reuse a reserved name); Inter's copyright line names no Reserved Font Name. For a web page this allows commercial use. **Not legal advice**; the Publisher must keep the licence text with any self-hosted font files. Using the font from Google Fonts is a separate licence question I did not check.

**Hierarchy in words (no sizes yet; sizes come at Step 19):** one large, bold, tightly tracked display line for the hero headline; a clearly smaller, semibold heading for section titles; a medium subheading for card titles; regular body text in a softer grey than the headings; a small, medium-weight, all-caps eyebrow label above section titles (Calendly shows this); small regular text for ticks and footnotes. The user's chat scale (28 down to 12) is the starting set of steps and is confirmed or revised at Step 19.

---

## Icons & imagery

### Icons

- **Live site today (observed):** the page has 25 references to `.svg` files, plus the page builder's own icon font (`webflow-icons`) for dropdown arrows and the menu button. It has no single icon family I could identify; whether the SVGs are icons or illustrations was not checked.
- **Proposal: Lucide** (one style: 24 x 24 grid, outline strokes, rounded ends). **Licence, verified from the official source:** the repository `LICENSE` (`https://github.com/lucide-icons/lucide/blob/main/LICENSE`, fetched as raw text on 2026-10-24) states "ISC License ... Permission to use, copy, modify, and/or distribute this software for any purpose with or without fee is hereby granted, provided that the above copyright notice and this permission notice appear in all copies." A listed subset of icons derived from Feather carries the MIT License (Cole Bemis), which also allows commercial use with the notice. The notices must be kept in the shipped code. This lets all page icons come from one outline style, which also matches the tick and arrow icons visible in the hero screenshot and Calendly's outline icons in the slices.
- The user has supplied no icons. One style only; never mix libraries.

### Imagery rules (PROPOSAL; they follow the user's decisions)

What the Calendly slices show (all 8 viewed at review; only what is visible; not copied): a warm off-white page with generous space between sections; two headline styles: large dark navy **sans** headlines **centred** under a small all-caps label for section intros ("AI MEETING MANAGEMENT", "GET STARTED"), and **serif** headlines **left-aligned** under a small product badge for feature sections ("Meet Callie, your AI assistant"); dark navy buttons ("Start for free"); big rounded containers; white cards with rounded corners and soft shadows sitting on **saturated colour fields** (blue, lilac and pink bands; teal to green to yellow bands); product cards that show a small piece of interface (a calendar, an availability panel, an email reply, a payment toggle) rather than a whole screen; feature lists as stacked rows with a small outline icon each, one row open; a row of four cards (Book, Prep, Capture, Follow up) with a notch cut between them; photos of people inside some product cards (avatars, a video call); a "Real customers. Real results." carousel with a portrait photo, a serif quote, a named person, a customer logo and a result figure; a grid of third-party integration logos; a dark rounded footer panel with a link grid. The last four (people photos, customer story with a figure, customer logo, partner-logo grid) are things this page **cannot** use under imagery rules 2 and 3 and the Step 09 claims list.

1. **The product demo is shown as illustrations, and labelled as illustrations.** User decision: scan, then proposal, then approval, supplied by the user. Show one small, clear piece of interface per image (a found issue, a proposed fix, an approve control), in the Calendly manner of a white card on a colour field. A caption such as "Illustration" sits with each; none is presented as real product UI unless the user says so.
2. **No numbers in any image.** No "+30%", no percentage, no "confident" score, no revenue figure, no order count (Decisions log: no result numbers). Placeholder values inside a mock card must be words or neutral dummies the Content reviewer approves.
3. **No real store, no real person.** No real store domains or logos of customers, no photos of people presented as sellers or customers, no implied testimonials. Name fields in a card use obviously generic labels. Faces, if any appear at all, are illustrated and not tied to a quote.
4. **Rounded shapes, one idea per card, colour in the field not the text.** Large corner radius, white card, soft shadow, colour from the field behind it (blues from the logo family first, per the chosen colour direction). Only the approve control is allowed to be the strongest colour inside a card.
5. **Own shapes, not Calendly's.** The wavy contour-line fields and the notched card row are Calendly's look; do not reproduce them. Step 17 defines ShopBase's own field pattern. Avoid glow, sparkle and "magic" cues (Step 08 do-not-copy 1, 2 and 5), and avoid stock-photo scenes of laptops and handshakes.

---

## Migration list

Type C. Source: the audit's old-brand inventory (`03-research/04-audit.md`) and the legal-page findings. "Step" is where the item is handled (24 or earlier). Roles are from `_progress.md`: Strategy owner and Content reviewer = the user; Builder default = Claude runs, user exports; Publisher = the user. **Decision** is my proposal unless the item is marked as the user's.

| # | Old item (where found) | Decision | Owner | Step | Notes |
|---|---|---|---|---|---|
| 1 | **PrintBase**: POD tab sentence in desktop and mobile copy (2 visible mentions; the audit's third is the footer link, row 2) | **Retire** | Content reviewer (confirms), Builder | 14 (copy), 21 | PrintBase no longer exists as a brand (user decision) |
| 2 | **PrintBase** footer link to `printbase.com` | **Retire** | Strategy owner decides, Publisher | 12 (footer scope), 24 | Link to a brand that no longer exists |
| 3 | **PlusBase** footer link to `plusbase.com` | **Retire** | Strategy owner decides, Publisher | 12, 24 | Same reason |
| 4 | **PlusBase** header logo file `PlusBase Logo Dark Color.png` (second header logo) | **Retire**; replace with the logo from `02-assets/logo/` | Builder | 21 | Which logo it shows was `NOT VERIFIED` in the audit; the logo comes from the supplied SVGs either way |
| 5 | **PlusHub** and **PrintHub** logos in the integrations strip (`Plushub.png`, `Printhub.png`, alt text empty) | **Retire** (the whole strip is dropped in the audit verdict) | Strategy owner, Builder | 12, 21 | Do not carry the two dead-brand logos into any new integrations section |
| 6 | **PrintHub** footer link on the two legal pages, not on Home (its target is `/privacy-policy`, probably a mistake) | **Retire** | Publisher | 24 | `ASSUMPTION` that the target is a mistake |
| 7 | "**Print on demand**" and "**Dropshipping**" top-level nav items and their pages (`/print-on-demand`) | **Open: keep or retire** is the user's call (pack Q8). Proposed: do not carry them into the Home header unless the user keeps those products | Strategy owner | 12 | Audience still includes dropshipping and POD sellers (user decision), so retiring the nav does not remove them from the page's story |
| 8 | **Per-model tabs** (E-commerce brands, Dropshipping, Print-On-Demand, with their "Print-on-demand products" copy) and the typing headline; also the meta description, `og:description` and `twitter:description` ("Dropshipping, Print-on-Demand, Online Brand, Content Creator") | **Retire** (meta: **Replace** with 2.0 wording) | Strategy owner, Content reviewer, Publisher (meta) | 12, 14, 24 | Proposed in Steps 06 and 09. The footer community link "Dropshipping Zone" is a Facebook group name, handled with row 16 and the audit's country-logic item (K13) |
| 9 | **Old promise**: "Build a profitable E-commerce business in a few clicks with ShopBase" (H1, `<title>`, `og:title`, `twitter:title`, testimonial text) | **Replace** with the 2.0 positioning | Content reviewer (wording), Builder, Publisher (meta) | 14, 21, 24 | Meta tags carry the old promise too, not only the page body |
| 10 | Other old-promise wording: "in a few clicks", "all-in-one", "app mazes", "No more money waste for third-party apps" | **Retire** (no replacement unless the user confirms what is truly built in) | Content reviewer | 14 | "No apps to stitch together" in the screenshot is itself unconfirmed |
| 11 | Old service promises: "100% Happiness Guarantee", "Award-winning Support Team", "24/7 live chat" | **Open**: keep only if the user confirms each is still true | Strategy owner, Content reviewer | 13, 14 | Not in any input as current fact |
| 12 | **Legal entity** "OpenCommerce Group, Inc" (Terms and Privacy pages, not on Home) | **Keep for now; DECISION ONLY THE USER CAN MAKE** | Strategy owner (and whoever handles legal text) | 24 | Not changed by a Home redesign; I will not suggest a replacement name. Default: unchanged, flagged |
| 13 | **`support@shopbase.com`** (legal pages; the 2.0 support route is unknown, 09 question E7) | **Keep for now; DECISION ONLY THE USER CAN MAKE** | Strategy owner | 24 | Home must not promise a support channel until confirmed |
| 14 | **© ShopBase 2021** (two footers on legal pages) and "Copyright 2021 OpenCommerce Group, Inc." | **Keep for now; DECISION ONLY THE USER CAN MAKE.** Proposed: update the year only after the legal decision in row 12 | Strategy owner, Publisher | 24 | The Home footer's year is rewritten by a script; the legal pages are out of scope (P01 only) |
| 15 | **External domains**: `www.printbase.com`, `www.plusbase.com` | **Retire** (see rows 2 and 3) | Publisher | 24 | |
| 16 | **External domains kept**: `accounts.shopbase.com`, `templates.shopbase.com`, `blog.shopbase.com`, `help.shopbase.com`, `developers.`, `updates.`, `network.`, `www.shopbasestatus.com`, app-store links, Facebook community links | **Keep** by default; each link checked to still exist and still fit 2.0 | Publisher, Builder | 24 | Audit default; the sign-up target stays as the primary CTA |
| 17 | Old logo file names (`Logo full.svg`, `ShopBase-Logo Light@1x.svg`, `sb smilde.svg`) | **Replace** with the three supplied SVGs | Builder | 21 | The old files were not opened in the audit |
| 18 | The **ShopBase name, logo, colours** | **Keep** (user decision) | Strategy owner | 16 (which blue), 21 | Blue choice is the open question above |
| 19 | **Other old product names** on Home: "ShopBase Payments" (POD tab, footer), "ShopBase Marketplace" (footer), "ShopBase Hero" and "ShopBase Network" (nav), "Made in ShopBase" (12 template tiles) | **Open: keep or retire is the user's call** (not on the user's removed list). Proposed: carry none into new Home copy until confirmed as 2.0 parts | Strategy owner, Content reviewer | 12, 14 | Audit old-brand inventory, "Old product names (other)"; added at review so every inventory line has a decision |

Anything not listed here (tracking tags, country cookie, the 12 template tiles) belongs to the audit's must-keep and rework lists and is handled at Steps 12, 21 and 24, not here.

---

## Assumptions

1. The user owns the three logo SVGs; no licence note exists (`ASSUMPTION`, intake W8).
2. `Logo (1).svg` is the dark-surface file and `Logo (6).svg` the light-surface file; read from the fills, not labelled by the user.
3. Clear space and minimum sizes are my proposals from geometry, not tested on screens and not ShopBase rules. Path bounding boxes come from the exact curve extremes (recomputed at review).
4. `#0096ED` and the typography scale come from the user's chat only; they are not stored in the project.
5. Hero screenshot colours are sampled from an image and may differ from the source CSS.
6. Inter is proposed because the live site loads it and the screenshot looks consistent with it; I did not identify the screenshot's font. Whether the 2.0 font is Inter is the user's to confirm.
7. Competitor and reference colours were not measured as rendered; Step 08 read inline CSS counts only (`NOT VERIFIED` visually). Direction claims about "standing apart" are therefore limited to the findings stated.
8. The Calendly reference is a style direction, not a brand voice (09 attribute 4 stays `ASSUMPTION`).
9. Home is light-only (default). The live site's other fonts and icon files were not checked in a browser.
10. Font and icon licences were read from the official repositories on 2026-10-24; a later licence change would not be seen.

---

## Open questions

### 🔴 Must answer
1. **Which blue is the brand primary** (logo `#497BDF`, the chat scale's `#0096ED`, or the hero screenshot's violet-leaning blue)? *Blocks Step 16. Default: direction 1, logo-true blue; the screenshot's violet is not adopted until you say so.*
2. **Legal entity and support email** ("OpenCommerce Group, Inc", `support@shopbase.com`, the 2021 dates): keep or change? Only you can decide this. *Blocks Step 24 only. Default: unchanged and flagged; nothing on Home names either.*

### 🟡 Should answer
3. **Font:** is Inter (what the live site loads) the 2.0 font, or is there a licensed brand font? *Default: Inter, as in the proposal; needed before Step 16.*
4. **Brand guideline:** the sitemap lists `/brand-guideline` and `/brand-asset` but both return 404. Is there a guideline elsewhere? *Default: none; the PROPOSAL items stand.*
5. **Clear space and minimum size:** accept the proposal (24 units; 120 px full logo; 24 px icon)? *Default: accepted as proposals until you say otherwise.*
6. **Dark surfaces:** will Home have a dark header or footer? *Default: no; `Logo (1).svg` unused.*
7. **Nav items "Print on demand" and "Dropshipping":** keep or retire (pack Q8)? And the other old product names (ShopBase Payments, ShopBase Marketplace, ShopBase Hero, ShopBase Network, "Made in ShopBase"): still 2.0 parts? *Default: not carried into the Home header or new copy.*
8. **Old service promises** (happiness guarantee, award-winning support, 24/7 chat): still true? *Default: not used.*

### ⚪ Nice to have
9. Paste the chat colour scale and typography scale into a file (`01-strategy/`) so later steps can cite them. *Default: re-send at Step 16.*
10. Confirm ShopBase owns the logo files. *Default: yes.*
11. Is there a favicon or app icon rule for the icon-only logo? *Default: the icon-only file may be used for the favicon, as a proposal.*

---

## Check before handing back

- [x] No logo was drawn by the AI. The three SVGs were only read and measured; none was edited or traced.
- [x] Every font and icon library has a stated commercial-use licence, **verified** from the official source on 2026-10-24: Inter (SIL OFL 1.1, `https://github.com/rsms/inter/blob/master/LICENSE.txt`) and Lucide (ISC, with an MIT subset, `https://github.com/lucide-icons/lucide/blob/main/LICENSE`). Google Fonts hosting terms were not checked.
- [x] Colour directions are tied to the messaging (calm, plain, seller in charge) and to the me-too test (Step 06: the me-too risk is in wording, so colour cannot solve it alone; direction 2 sits closest to the AI-tool look). The competitor-colour part is limited by what was measured.
- [x] Type C: every old asset has a decision, an owner and a step (19 rows; row 19 and the meta-description part of row 8 added at review). Rows 7, 11, 12, 13, 14 and 19 are open decisions for the user, not silent.
- [ ] A brand guideline was found and quoted. NOT MET: the page returns 404; reported as such.
- [ ] Final palette chosen. NOT DONE on purpose (Step 16).
