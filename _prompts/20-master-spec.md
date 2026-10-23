# Step 20 · Master spec

> **Phase 7 · System & spec** — role: Product designer (Cowork writes, Claude Design builds)
> **Applies to:** A B C
> **Output:** `08-claude-design-input/master-spec.md` · `image-prompts.md` · `build-prompt.md` — then **Gate 7**
> **Base prompt** — never edited for a project. Shared rules and the end-of-turn block: `_prompts/README.md`.

---

## Reads

- Everything in `03-research/` · `04-brand/` · `05-content/14-copy.md` · `06-proof-ui/proof.html` · `07-tokens/` · `02-assets/`

## Stop if

- Gate 6 is not `APPROVED`, or Step 19 is not `done`.

## Part 1 — `master-spec.md` (the single source for the build)

1. **Product summary** — 5 lines: what, for whom, USP, frame, modes, language, project type.
2. **Design foundation** — locked palette (roles + hex), font and type scale, spacing, radius, shadows, icon library, logo usage (which file on light / dark surfaces). Point to token names. Appendix: the `:root` block generated from `07-tokens/`.
3. **Page structure and global behaviour** — header, sticky behaviour, footer, scroll, responsive rules, caps (sections, length, boxes, CTAs).
4. **Every section**, in `S##` order, per page `P##`:
   ```
   S## · Name            page · flows (FL##) · focal point
   Purpose
   Layout                top → bottom (from the Step 17 pattern)
   Content               the APPROVED copy from Step 14, verbatim
   Visuals               what each image / mock / diagram must show
   Actions               every link and button → where it goes (P## / S## / URL)
   States                default · hover · focus · loading · empty · error · success · disabled — each described or "n/a — why"
   Notes                 anything special (sticky, motion, carousel)
   ```
5. **Shared components** — repeated parts (button, card, section header, CTA block…), with variants and states in words. Use the same class every time.
6. **Coverage** — every `S##` and `FL##` appears; every page has a way in and a next step. List any that do not, with why.
7. **Measurement hooks** — the events from Step 05, attached to the right CTAs.
8. **Image, video and motion slots** — one row each:

   | IMG## · name | Sections | What it shows | Ratio · export size | File in `02-assets/images/` |
   |---|---|---|---|---|

   Codes `IMG##` are permanent. Reuse an image where the content is the same.
9. **Type C:** a list of every place the new name and brand must appear, and every old-brand item that must not.

## Part 1b — `image-prompts.md`

One ready-to-paste prompt per image slot, for an image generator: subject and composition (and where empty space stays for text), aspect ratio and size, look (the locked palette by hex, lighting, finish), **one shared style line repeated in every prompt**, exclusions (no text, no logos, no watermarks, no real people's faces unless needed), and the file name `02-assets/images/IMG##-name.png`. Then tell the user: generate → save with that name → say **"images done"**, or **"skip images"** (slots stay labelled placeholders). **STOP and wait.**

## Part 2 — `build-prompt.md`

The prompt for the build tool (Claude Design or the project's tool). It must say:
- Build **every section and state** in `master-spec.md` at the locked frame, labelled `S## · Name`.
- **Match the proof exactly** — look, spacing, depth.
- Tokens as CSS variables in `:root`; semantic class names; **no inline styles**; no hex outside `:root`.
- Use the real copy, the logo as provided, only the locked icon library and font.
- Use the images in their `IMG##` slots (cropped, never redrawn); missing ones stay placeholders. **No `loading="lazy"`.**
- Presentation (device frame, canvas background) on an outer wrapper only.
- Respect the caps; export **one HTML file**; ask questions before building if anything is unclear.
- List the files to attach: master spec, proof, logo, token files, every image.

If the build tool supports a **design system**, also list what to load into it (tokens, repeated components, usage rules) so repeated parts do not get reinvented.

## Check before handing back

- [ ] Every `S##` and state is in the spec; copy is verbatim from Step 14.
- [ ] Foundation matches `07-tokens/` exactly.
- [ ] Caps and measurement hooks are in the spec.
- [ ] Every image slot has a code, a size, a prompt and a file name.
- [ ] The build prompt demands the proof look, `:root` variables, no inline styles, one HTML file.

## End of turn

Part 1b: ask for the images and stop. After "images done" / "skip images": end-of-turn block → **GATE 7: the Strategy owner approves tokens and spec** and says `approved`. Record the date and their words. Stop.
