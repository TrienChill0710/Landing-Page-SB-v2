# 20 · Build prompt — ShopBase 2.0 Home (Step 21)

This file has two parts. **Part A** is the text you paste into Claude Design (or the project's build tool). **Part B** is for you: what to attach, what to load into a design system, how to check the result, and the order of steps.

---

## Part A · The prompt (paste everything between the lines)

----- START OF PROMPT -----

You are building the Home page of ShopBase 2.0 as two separate HTML files. You have no earlier context. Everything you need is in the attached files. **If the answer is not in the spec, ask me. Do not invent.** Ask all your questions **before you build anything**, in one list, and wait for my answers.

**What to build**

1. Read `master-spec.md` completely. It is the single source. Build **every section and every state** it describes, at the locked frames **1440 px and 375 px wide** (responsive between them), each section labelled with an HTML comment in the form `S## · Name` (for example `<!-- S03 · Hero A -->`) and the attribute `data-section-id` holding the code only (for example `data-section-id="S03"`), as section 3.1 and section 7 of the spec say.
2. Export **one HTML file per variant**: `final-ui-A.html` (variant P01·A) and `final-ui-B.html` (variant P01·B). **Build A first**, show it to me, then build B from the same tokens and the same components (B reuses A's header, footer, S07, S08 and S09). Each file is complete and stands alone (one file each: CSS in one `<style>` block in the head, no external stylesheet, no script unless the spec asks for one).
3. Section order: A = S01, S03, S04, S05, S06, S07, S08, S09, S02. B = S01, S10, S12, S08, S07, S09, S02. **Do not build S11.**

**Match the proof exactly**

4. Attached `proof.html` is the approved look (Gate 6). **Match it exactly**: look, spacing, radius, depth, type sizes, colours, the soft fields, the white cards with the soft shadow, the "Illustration" pill, the buttons. Reuse the proof's CSS class names and rules. Where the spec says a part is not in the proof (header, footer, mobile menu, S04, S08, image element, hover/pressed proposals), build it only from the same tokens and classes, and do not add a colour, a font size, a radius or a shadow that the tokens do not have. When in doubt, copy the proof.
5. Do not restyle, modernise or "improve" anything. No gradient on text, no glow, no sparkle, no dark section, no extra animation, no transitions, no carousel, no video.

**Tokens and code rules**

6. Put every design value in CSS variables in `:root`, using the exact `:root` block in Appendix A of `master-spec.md` (including its three `@media` blocks). Copy it unchanged. Use `var(--…)` everywhere.
7. **No hex colour outside `:root`.** **No inline `style=` attributes.** No `!important`. Semantic class names (`.btn-primary`, `.card`, `.field-2`…), never visual ones like `.blue-box`.
8. **No `loading="lazy"`** on any image. Give every image `width` and `height` attributes.
9. The hero headline is the page's **one `<h1>`** (S03 in A, S10 in B). Every other section headline is an `<h2>`. One `<main id="main">`. Include the "Skip to main content" link.
10. Presentation (a device frame, a grey canvas, a shadow around the page) goes on **one outer wrapper only**, never inside a section. By default export a plain full-width page with no wrapper.
11. Respect the caps: at most 10 sections per page (counting header and footer), at most 4 boxes (cards or panels) per section, one primary button per section (the hero also has the one secondary button). Do not add sections, cards, buttons, links, badges or icons that the spec does not list.

**Copy, logo, font, icons, images**

12. Use the copy **verbatim** from `master-spec.md` (it is copied from the approved `14-copy.md`). **Never rewrite, shorten, translate or "tidy" it. Never add a claim, a number, a testimonial or a line of your own.** If a piece of copy does not fit a layout, **ask me**; do not change it. Alt texts are copy too.
13. **Do not build anything the spec fences as `DO NOT BUILD`** (the S11 parts list, the plan line in S09, the link line in S08, the alternate headlines). They are not part of this build, even if they look useful.
14. **Never include:** result numbers or percentages, "built in", the "Free Launch" plan, comparisons or competitor names, "best" or "#1" claims, DMCA or trademark mentions, the old brand names (PrintBase, PlusBase, PrintHub, PlusHub), "Print on demand", "Dropshipping", "Book a demo", any sign-up label other than "Get started for free", country flags or country text, a copyright or legal-entity line the spec marks as undecided.
15. **Logo:** use the attached SVG files exactly as provided. `Logo (6).svg` on the light header and footer, with the clear space in the spec (24/254 of the logo width) and at least 120 px wide. **Never redraw, trace, recolour, outline, rotate or add effects to the logo.** `Logo (1).svg` is not used (no dark surface exists).
16. **Font and icons:** only **Inter** (the attached `InterVariable.woff2`, self-hosted with `@font-face` as in the proof) and **Lucide** outline icons (the attached icon files; same stroke, round caps). No other font, no other icon set, no emoji.
17. **Images** go in their `IMG##` slots exactly as the spec's image table says (six slots, file names `02-assets/images/IMG##-name.png`, shown inside the white card under the "Illustration" pill). **Crop only where the spec says (the hero crop of IMG01); never stretch, never redraw, never regenerate a picture.** A slot whose file is not attached stays the **labelled "Illustration" placeholder** from the proof (pill and neutral bars). Never invent an image.

**Behaviour**

18. The header is sticky (the spec's default, to be confirmed). Sign-up links go to `https://accounts.shopbase.com/sign-up`, Login to `https://accounts.shopbase.com/sign-in`, the hero secondary button to `#s05` (A) or `#s12` (B). Leave links to the sign-up page plain (no parameters added, none removed) and mark them `data-signup-link`; the site's referral script is updated separately to use that marker (not part of this build).
19. Add the measurement data attributes from section 7 of the spec (`data-section-id`, `data-section-type`, `data-variant`, `data-event`, `data-cta-label`). Add no analytics script, no tag, no vendor code (the tool is not chosen).
20. States: build default, hover, focus, pressed and the empty (placeholder) state exactly as the spec describes. Where the spec says "not in the proof, to confirm", build the proposal and list it in your reply so I can judge it. States marked n/a are not built.

**When you finish, reply with:** the two file names; the list of every place you deviated from the spec or the proof (ideally none); every question you had to guess; and the count of sections, buttons, images and placeholders per file.

----- END OF PROMPT -----

---

## Part B · For you (Step 21)

### Files to attach

| Attach | Path | Why |
|---|---|---|
| Master spec | `08-claude-design-input/master-spec.md` | The single source: sections, copy, actions, states, tokens block |
| Proof | `06-proof-ui/proof.html` | The approved look (also needs the font file next to it to render) |
| Logo files | `02-assets/logo/Logo (6).svg`, `Logo (1).svg`, `Logo (3).svg` | As provided; only `Logo (6).svg` shows on the page, `Logo (3).svg` is the favicon |
| Token files | `07-tokens/1-primitive.json`, `07-tokens/2-semantic.json`, `07-tokens/token-mapping.md` | The values behind the `:root` block |
| Font | `02-assets/fonts/InterVariable.woff2` and `02-assets/fonts/LICENSE-Inter.txt` | Inter, self-hosted; keep the licence with the font |
| Icons | `02-assets/icons/arrow-right.svg`, `02-assets/icons/LICENSE-Lucide.txt` (and `menu.svg`, `x.svg` once added from Lucide; every file in `02-assets/icons/`) | Lucide outline icons |
| Images | every `IMG##` file that exists in `02-assets/images/`: `IMG01-scan-card.png`, `IMG02-proposed-fix-card.png`, `IMG03-approval-card.png`, `IMG04-offer-card.png`, `IMG05-store-with-scan-card.png`, `IMG06-finding-and-fix-on-store.png` | Illustrations in their slots. A missing file stays a placeholder. Do not attach `hero-2.0-reference.png` (a reference screenshot, not an asset) |

Do **not** attach `02-assets/moodboard/` (Calendly and other references): the page must not copy them.

### If the tool has a design system, load this

- **Tokens:** the `:root` block from Appendix A of the master spec (colours, fields, type scale, spacing, radius, shadow, sizes, breakpoints), as variables with those exact names.
- **Repeated components** (same class names as the proof): `.frame`, `.frame-inner`, `.btn` with `.btn-primary` and `.btn-secondary`, `.icon`, `.title-hero`, `.title-section`, `.text-lead`, `.text-body`, `.text-caption`, `.hero-stack`, `.button-row`, `.hero-visual`, `.closing-stack`, `.split` and `.split-reverse`, `.field-1` to `.field-3`, `.card` with `.card-inner`, `.pill`, `.card-img`, plus the new header and footer classes of section 5 of the spec.
- **Usage rules:** primary colour only on the "Get started for free" buttons and the drawn approve control; one soft field per illustration section and at most two F3 fields per page; muted text and links never on F3; no gradient on text; the logo never on a field; Inter and Lucide only; no hex outside `:root`; no inline styles; one primary button per section; copy never edited.

### Review checklist you can use against the proof

Open the exported file next to `proof.html` at **1440** and **375** wide.

- **Look:** same white page, same soft blue fields, white cards with the soft shadow and no border, the "Illustration" pill on every illustration, one blue button style, rounded corners in the same steps (field > card > inner card > button). No new colour, no dark area, no glow, no gradient on text.
- **Spacing:** the gap between sections matches the proof's frames; the hero has air above the headline and a clear gap before the card; the text-and-picture rows alternate sides on desktop and stack on mobile (text first); buttons are full width on mobile.
- **Copy exactness:** every headline, line, caption, button label and alt text equals the spec word for word; nothing added; no numbers on the page.
- **Counts:** variant A has **9** sections and variant B has **7**; **3** primary buttons per file (header, hero, closing); **1** secondary button per file (hero); picture placements: **5** in A (IMG01 twice: hero crop and S05, then IMG02, IMG03, IMG04) and **4** in B (IMG05, IMG06, IMG04, IMG03), each with its pill; exactly **1** `<h1>` per file; no S11; no `loading="lazy"`; no `style=`.
- **Links:** sign-up buttons go to the sign-up address; Login goes to sign-in; the hero secondary button jumps to the Scan section (A) or the Scan and fix section (B).
- **Not in the proof, so judge by eye:** the header, the mobile menu, the footer, S04 and S08.

### Order of steps for you (this is Step 21)

1. Generate or draw the images from `image-prompts.md`, save them in `02-assets/images/`, and say **"images done"** or **"skip images"** (Step 20 finishes there, then **Gate 7**: you approve the tokens and the master spec).
2. Open Claude Design, attach the files above, paste Part A.
3. Answer its questions from the spec (it should ask before building). If an answer is not in the spec, stop and bring the question to me: the spec is updated first, nothing is made up during the build.
4. Review variant A against the checklist; ask for fixes; then ask it to build variant B from the same components.
5. Export the two files as `final-ui-A.html` and `final-ui-B.html` into `09-final-ui/` (the font and image paths in the spec assume that folder). Two files instead of the kit's single `final-ui.html` is a default (spec section 10); you can change it, for example build only A now.
6. Say **"build done"**: Step 22 (UI self-review) and Step 23 (spec check) then run on the exported files.
