# Step 23 · Spec check

> **Phase 8 · Build & review** — role: Design QA
> **Applies to:** A B C
> **Output:** `09-final-ui/23-spec-check.md` — then **Gate 8**
> **Base prompt** — never edited for a project. Shared rules and the end-of-turn block: `_prompts/README.md`.

---

## Reads

- `09-final-ui/final-ui.html` · `09-final-ui/22-self-review.md` · `08-claude-design-input/master-spec.md` · `07-tokens/` · `05-content/14-copy.md`

## Stop if

- Step 22 is not `done`.

## Do

Compare the build with the spec, **one row per item**, and compute what can be computed.

1. **Sections:** every `S##` in the spec is in the build, in order. List missing, extra, reordered.
2. **Copy:** diff each section's text against `14-copy.md`. List every difference (the build tool may have reworded).
3. **Tokens:** every `:root` value equals its token value (primitive/semantic). List drift. Report values used in the build that have no token.
4. **Components:** repeated parts use the same class every time.
5. **Images:** each `IMG##` slot is filled or a labelled placeholder; no slot uses a wrong crop.
6. **Actions:** every link and button goes where the spec says; list dead links (`#`, empty `href`).
7. **Measurement hooks:** each event from Step 05 is attached to its CTA.
8. **Caps:** sections, length, boxes, CTAs per section — measured.
9. **Type B/C:** the must-keep items are present (URLs, keywords, sections). Type C: old-brand name count = 0 (search command output).
10. **Verdict** — `matches` / `minor drift` / `needs rework` per section; a list of fixes ordered by severity.
11. **Re-sync tokens** if the build legitimately changed values and the user accepts them: update `07-tokens/` and say so (this makes nothing before Step 19 stale).

## Output — `09-final-ui/23-spec-check.md`

```
# 23 · Spec check
## Section coverage
## Copy differences
## Token drift
## Components, images, actions, hooks
## Caps                  (measured)
## Types B/C checks
## Verdict & fixes
```

## Check before handing back

- [ ] Every numeric item has a measured value.
- [ ] Every copy difference is listed, not summarised.
- [ ] Dead links are listed with their location.

## End of turn

End-of-turn block → **GATE 8: the Strategy owner reviews the UI** and says `approved`, or gives feedback. Route feedback with the table "Feedback after Gate 8" in `_prompts/README.md`; going back marks later steps `stale`. Record the date and their words. Stop.
