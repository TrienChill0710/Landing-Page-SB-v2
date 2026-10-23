# Step 04 · Audit of the existing page

> **Phase 1 · Intake & audit** — role: Conversion analyst
> **Applies to:** **B C only** — type A: mark `skipped` ("no existing page") and go to Step 05
> **Output:** `03-research/04-audit.md`
> **Base prompt** — never edited for a project. Shared rules and the end-of-turn block: `_prompts/README.md`.

---

## Reads

- `01-strategy/` (existing page link, numbers, feedback, must-keep list) · `03-research/03-brief-analysis.md`

## Stop if

- Step 03 is not `done`.
- Project type is A (skip, do not run).
- No link to the existing page and no screenshots of it: ask for one and wait.

## Do

1. **Inventory the page, section by section.** For each: name, purpose, headline, main message, CTA, visuals. Give each a temporary code `OLD-01, OLD-02…` (they map to `S##` in Step 12).
2. **What works, what does not.** Use numbers if the user gave them; otherwise judge against the strategy pack and say so (`ASSUMPTION — no analytics`). Do not invent metrics.
3. **Feedback received** — summarise the user's feedback (from stakeholders, customers, tests), each item with its source.
4. **Must-keep list** — URLs, SEO keywords and meta, sections that perform, legal text, tracking tags, integrations. Anything the user listed is mandatory; flag anything you suspect should also stay.
5. **SEO snapshot** — URL, title, meta description, H1, main keywords for each page in scope. If you cannot fetch them, mark `NOT AVAILABLE`.
6. **Type C only — brand assets and old-name inventory:** every place the old name, logo, domain, legal entity, support email and product names appear (page copy, legal pages, forms, meta, images). This list drives Step 24.
7. **Verdict per section:** `keep` · `rework` · `drop` — a first view only; Step 12 decides.

## Output — `03-research/04-audit.md`

```
# 04 · Audit
## Section inventory      (OLD-## · purpose · message · CTA · verdict)
## What works / what does not
## Feedback received      (with sources)
## Must-keep list
## SEO snapshot
## Old-brand inventory    (type C only)
## Assumptions
```

## Check before handing back

- [ ] Every section of the existing page is in the inventory.
- [ ] No metric appears without a source from the user.
- [ ] The must-keep list includes everything the user named.
- [ ] Type C: the old-brand inventory has entries (or says "none found" with how it was searched).

## End of turn

End-of-turn block (Next: Step 05) → stop.
