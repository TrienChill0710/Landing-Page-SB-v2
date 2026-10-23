# Step 11 · Narrative options

> **Phase 4 · Narrative** — role: Product marketing lead
> **Applies to:** A B C
> **Output:** `03-research/11-narrative-options.md` — then **Gate 4 (decision)**
> **Base prompt** — never edited for a project. Shared rules and the end-of-turn block: `_prompts/README.md`.

---

## Reads

- `01-strategy/01-strategy-pack.md` · `03-research/06-positioning.md` · `03-research/07-voc.md` · `03-research/08-reference-analysis.md` · `04-brand/09-messaging.md` (if the module ran) · `03-research/04-audit.md` (if B/C)

## Stop if

- Gate 2 is not `APPROVED`, or (Brand module on) Gate 3 is not `APPROVED` / `skipped`.

## Do

The user will **choose** the direction. Give exactly **two** options that are genuinely different stories, not two variants of one. Examples of a real difference: lead with the USP vs lead with the whole platform; speak to people who know the category vs to newcomers.

For each option:

1. **Name and one-line idea.**
2. **Message order** — the page as 5–8 beats in sequence, each beat one message (not sections yet).
3. **Hero promise** — one headline-level sentence and what the reader should see first.
4. **Flow per persona** — what each persona sees and does from arrival to the CTA (3–5 steps each).
5. **Best for** — which audience state it fits (new to the category / already knows it / existing customers). For type C, say how it serves both existing customers and new ones.
6. **Pros** — 3 points, each tied to a finding from Steps 06–08.
7. **Cons / risks** — 2–3 points, and how the page would handle each.
8. **What it costs** — rough section count and page length.

Then a **comparison table** (reader fit, USP depth, clarity for each persona, length, risk) and **your recommendation with the reason**. State it as a recommendation; do not decide for the user (N6).

## Output — `03-research/11-narrative-options.md`

```
# 11 · Narrative options
## Option A — <name>      (idea · beats · hero promise · flow per persona · best for · pros · cons · cost)
## Option B — <name>
## Comparison
## Recommendation & why
## Assumptions
```

## Check before handing back

- [ ] The two options differ in story, not just in order.
- [ ] Every pro and con cites a finding.
- [ ] Each persona has a flow in each option.
- [ ] The recommendation is labelled a recommendation.

## End of turn

End-of-turn block → **GATE 4 (decision): the Strategy owner chooses an option in words** (or asks for a change). Record the chosen option, the date and their words in `_progress.md` (header "Chosen narrative option" and Decisions log). **Do not run Step 12 until an option is chosen.** Stop.
