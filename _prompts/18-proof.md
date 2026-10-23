# Step 18 · Proof sections

> **Phase 6 · Visual direction** — role: Senior product designer
> **Applies to:** A B C
> **Output:** `06-proof-ui/proof.html` — then **Gate 6**
> **Base prompt** — never edited for a project. Shared rules and the end-of-turn block: `_prompts/README.md`.

---

## Reads

- `05-content/14-copy.md` (approved copy) · `03-research/12-sections.md` (caps, focal points) · `03-research/16-palette.md` · `03-research/17-moodboard.md` · `02-assets/` (logo, fonts, icons)

## Stop if

- Step 17 is not `done`, or Gate 5 is not `APPROVED`.
- Logo, font or icons are missing.

## Do

Build **about 5 key sections** (those chosen in Step 17) as one HTML file, at the locked frame (width, devices, colour mode). Use the **approved copy exactly** — do not rewrite it here. If copy does not fit, report it and go back to Step 14.

1. Follow the moodboard patterns, with our palette, font and icon library only.
2. **Hard rules**
   - Every colour, size and spacing value is a CSS variable in `:root`. **No hex outside `:root`.** **No inline `style=`.** Semantic class names.
   - One focal point per section; box and CTA counts within the Step 12 caps.
   - The primary colour only where the usage rules in Step 16 allow.
   - Logo as provided, never redrawn. Icons from the one locked library.
   - No `loading="lazy"` on images. Device mockups, shadows and canvas backgrounds go on an outer wrapper, never inside the section frame.
   - Images that do not exist yet are labelled placeholders at the right size.
3. **Measure** (by code) and report: hex outside `:root` (target 0), inline `style=` count (target 0), distinct font sizes vs the type scale, contrast of every text pair used (all pass), boxes and CTAs per section vs the caps, section heights.
4. Show the user how to open it, and which sections it covers.

## Output — `06-proof-ui/proof.html`

One self-contained HTML file, one frame per key section labelled `S## · Name`.

## Check before handing back

- [ ] Copy is the approved copy, unchanged.
- [ ] Hex outside `:root` = 0; inline `style=` = 0 (measured).
- [ ] Contrast: all text pairs pass (measured).
- [ ] Boxes / CTAs per section within caps (measured).
- [ ] No lazy-loaded images; logo and icons as provided.

## End of turn

End-of-turn block → **GATE 6: the Strategy owner approves the visual direction** and says `approved`. Iterating Steps 16–18 before this gate is normal and does not make later steps stale; nothing after them exists yet. Record the date and their words. Stop.
