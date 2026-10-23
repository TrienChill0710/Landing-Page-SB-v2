# Step 07 · Voice of customer (VoC)

> **Phase 2 · Research** — role: User researcher
> **Applies to:** A B C
> **Output:** `03-research/07-voc.md`
> **Base prompt** — never edited for a project. Shared rules and the end-of-turn block: `_prompts/README.md`.

---

## Reads

- `01-strategy/01-strategy-pack.md` (personas, USP) · `03-research/06-positioning.md` · `03-research/04-audit.md` (if B/C)

## Stop if

- Step 06 is not `done`.
- Web search is unavailable: say so, do **not** invent quotes, and ask the user to paste material. A VoC file with no real sources is not a VoC file.

## Do

For **each persona** in the strategy pack, find what real people say, in their own words.

1. **Sources** — Reddit threads, app-store and marketplace reviews, YouTube comments, industry forums, and any customer feedback the user supplied. For each source record: link, date if visible, what kind of person.
2. **Pain points** — per persona, the top 5–7, each with: the pain in the person's words (short quote), how often it appears across sources (e.g. "in 4 of 9 threads" — a count of what you read, not a market statistic), the source link(s).
3. **Language** — words and phrases the persona uses for their problem, their goal and the alternatives they use today. These feed the copy.
4. **What they already believe or distrust** — objections to products like ours.
5. **Fit with the USP** — for each pain point: does the USP address it directly, partly, or not? Do not stretch the USP to fit.
6. **B:** add why the existing page did not persuade, if sources say so. **C:** add what existing customers say about the old brand or product.
7. **Limits** — state the sample size and any bias (e.g. complaints are over-represented). **No quantitative claims** such as "most sellers…" from a handful of comments.

## Output — `03-research/07-voc.md`

```
# 07 · Voice of customer
## Sources read           (link · type · date)
## Persona: <name>
   ### Pain points        (rank · quote · frequency in read sources · links)
   ### Their language
   ### Beliefs & objections
   ### Fit with the USP   (direct / partial / none)
## (repeat per persona)
## Type B / C extras
## Limits & bias
## Assumptions
```

## Check before handing back

- [ ] Every pain point has at least one source link and a short real quote.
- [ ] Frequencies describe the sources read, not the market.
- [ ] No persona was added or dropped.
- [ ] Pain points that the USP does not answer are marked, not hidden.

## End of turn

End-of-turn block (Next: Step 08) → stop.
