# Step 15 · Content self-review

> **Phase 5 · Content** — role: Editor
> **Applies to:** A B C
> **Output:** the "Review log" in `05-content/14-copy.md` (and fixes to that file) — then **Gate 5**
> **Base prompt** — never edited for a project. Shared rules and the end-of-turn block: `_prompts/README.md`.

---

## Reads

- `05-content/14-copy.md` · `05-content/13-content-brief.md` · `03-research/12-sections.md` · `03-research/07-voc.md`

## Stop if

- Step 14 is not `done`.

## Do

Run the **self-review loop** from `_prompts/README.md` (default 2 rounds) with this checklist. Fix what fails, then run it again.

**Checklist**
- [ ] Each section has exactly one main message.
- [ ] The hero answers: for whom → what we solve → see the product working → next step.
- [ ] The USP appears through the page and is not drowned by user-problem copy. Count the sections that lead with a user problem.
- [ ] Every pain point used has a source from Step 07.
- [ ] No reference site is used as proof of conversion (N10). No unsourced number, testimonial or logo.
- [ ] Section count and each section's word count are within the caps from Step 12 (measured).
- [ ] No claim from the "claims to avoid" list; no unverifiable superlatives ("only", "#1", "best").
- [ ] **B/C:** every must-keep item is still present.
- [ ] **C:** an existing customer can tell what stays and what is new.
- [ ] **Me-too test:** read the hero and the first three headlines as if on a competitor's site — would they fit? If yes, rewrite.
- [ ] Consistent terms: the same thing has one name throughout.

Write each round in the Review log: what failed, what changed, what remains.

Then list **what the Content reviewer should look at first** (the 3–5 riskiest items) and every `[NEEDS DATA]` placeholder the reviewer or user must resolve.

## Output — Review log in `05-content/14-copy.md`

```
## Review log
### Round 1   (failed items · changes)
### Round 2   (failed items · changes)
### For the Content reviewer   (riskiest items · open placeholders)
```

## Check before handing back

- [ ] At least 2 rounds are logged (or round 2 found nothing, and says so).
- [ ] Counts in the checklist were computed by code.

## End of turn

End-of-turn block → **GATE 5: the Content reviewer approves the section list (Step 12) and the copy,** and says `approved`. Record the date and their words. **No UI work (Step 16 onward) starts before this.** Stop.
