# Step 16 · Palette

> **Phase 6 · Visual direction** — role: Brand designer
> **Applies to:** A B C — type **B**: do **not** create a new palette; document the existing one and add only missing roles
> **Output:** `03-research/16-palette.md` (+ `03-research/16-palette-options.html` when options are shown)
> **Base prompt** — never edited for a project. Shared rules and the end-of-turn block: `_prompts/README.md`.

---

## Reads

- Everything approved so far: Gate 5 must be `APPROVED` · `04-brand/10-identity.md` (if the module ran) · `02-assets/logo/` · `03-research/08-reference-analysis.md` (colour direction, do-not-copy list) · `03-research/03-brief-analysis.md` (colour mode)

## Stop if

- Gate 5 is not `APPROVED`.
- No logo and no brand colours exist (type A, module off): ask the user for them.

## Do

1. **Type B:** read the existing colours from the page or guideline (state the source); list them with roles; add only roles that are missing (e.g. success, danger, surface tints). Skip to step 4.
2. **Types A and C:** derive **3 palette options** from the logo and the brand directions in Step 10. Each has: name, mood, how it supports the messaging, how it differs from the closest competitor (Step 06), and the full set below. Show them side by side in the options HTML.
3. The user chooses one. Mark it **LOCKED**.
4. **Roles and values** for the chosen palette (hex): primary, primary hover, secondary / accent, page background, panel, title text, body text, muted text, border, success, warning, danger, plus any gradient (if used). Respect the colour mode from the frame lock.
5. **Contrast — computed by code.** Compute WCAG contrast for every text-on-background pair the page will use. Body text ≥ 4.5:1, large text and UI ≥ 3:1. Report the ratio for each pair and the pass count (e.g. `16/16`). Fix failing pairs by adjusting the colour, never by skipping the test.
6. **Usage rules** that enforce the hierarchy: where the primary colour is allowed (e.g. only the main CTA), how many gradient phrases and dark panels the page may have.

## Output — `03-research/16-palette.md`

```
# 16 · Palette
## Source                 (existing page / logo / brand directions)
## Options                (A, C: three; B: n/a)
## Chosen palette — LOCKED  (role · hex · usage)
## Contrast table         (pair · ratio · pass/fail)
## Usage rules
## Assumptions
```

## Check before handing back

- [ ] Contrast was computed for every pair and the pass count is reported.
- [ ] Type B: no new palette invented.
- [ ] Types A, C: exactly one option is marked LOCKED by the user's choice.
- [ ] Usage rules state where the primary colour may appear.

## End of turn

End-of-turn block (Next: Step 17) → stop.
