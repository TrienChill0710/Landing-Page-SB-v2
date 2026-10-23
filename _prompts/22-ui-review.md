# Step 22 · UI self-review

> **Phase 8 · Build & review** — role: Design QA
> **Applies to:** A B C
> **Output:** `09-final-ui/22-self-review.md` (and fixes, applied to the build prompt or `final-ui.html` as the user decides)
> **Base prompt** — never edited for a project. Shared rules and the end-of-turn block: `_prompts/README.md`.

---

## Reads

- `09-final-ui/final-ui.html` · `08-claude-design-input/master-spec.md` · `06-proof-ui/proof.html` · `03-research/12-sections.md` (caps) · `03-research/06-positioning.md` (me-too test)

## Stop if

- `final-ui.html` does not exist.

## Do

Run the **self-review loop** from `_prompts/README.md` (default 2 rounds). Where the result can be measured, **measure it with code** and report the number; where it needs a look, render the page and screenshot each section (if you cannot render, say `NOT RUN — no browser` and review the HTML structure only).

**Checklist**
- [ ] **Boxes:** count boxes (cards/panels) per section from the DOM; each ≤ the cap.
- [ ] **Focal point:** per section, one main heading and ≤ the CTA cap; the main message is the first thing seen.
- [ ] **Length:** total page height ≤ the cap (desktop and mobile if responsive).
- [ ] **Sections:** count equals the section list; order matches Step 12.
- [ ] **Header and logo:** logo as provided, enough clear space, header not crowded.
- [ ] **Colour use:** the primary colour only where the usage rules allow; images fit the colour mode (e.g. no dark photos jammed on a light page).
- [ ] **Hygiene:** hex outside `:root` = 0, inline `style=` = 0, `loading="lazy"` = 0, distinct font sizes vs the type scale.
- [ ] **Contrast:** every text pair passes.
- [ ] **Copy:** matches the approved copy; no placeholder text, no sample testimonials or numbers left; type C: no old-brand names.
- [ ] **Me-too test:** squint at the page — could it be a competitor's? If yes, say what to change.
- [ ] **Responsive:** each device in the frame lock is covered.

Write each round: what failed (with the measured number), what was changed, what remains. End with **what the Strategy owner should look at first**.

## Output — `09-final-ui/22-self-review.md`

```
# 22 · UI self-review
## Round 1    (measured numbers · failures · fixes)
## Round 2
## Remaining issues
## For the Strategy owner   (look at first)
```

## Check before handing back

- [ ] 2 rounds logged (or round 2 found nothing, and says so).
- [ ] Every numeric check has a measured value or `NOT RUN — why`.

## End of turn

End-of-turn block (Next: Step 23) → stop.
