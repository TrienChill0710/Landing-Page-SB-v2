# Step 13 · Content brief

> **Phase 5 · Content** — role: Content strategist
> **Applies to:** A B C
> **Output:** `05-content/13-content-brief.md`
> **Base prompt** — never edited for a project. Shared rules and the end-of-turn block: `_prompts/README.md`.

---

## Reads

- `03-research/12-sections.md` · `03-research/07-voc.md` · `01-strategy/01-strategy-pack.md` · `04-brand/09-messaging.md` (if the module ran) · `03-research/04-audit.md` (B/C)

## Stop if

- Step 12 is not `done`, or Gate 4 is not `APPROVED`.

## Do

For **every section** `S##` write a brief the copywriter (Step 14) can follow without guessing:

| Field | Content |
|---|---|
| Message | The one main message, as a plain sentence |
| For whom | Persona; what they believe at this point on the page |
| Pain point used | From Step 07, with its source link — or "none: this section is about the USP" |
| Proof | What backs the message (a feature, a demo, a number, a quote). Each item names its source. No proof → `UNPROVEN`, and say what to supply |
| CTA | Label and destination (`P##` / `/signup`) |
| Tone | From the voice rules in Step 09, or the strategy pack |
| Length | Maximum words for headline / body / supporting items |
| Must include / must avoid | Legal wording, claims to avoid, keywords to keep (B/C: from the must-keep list) |

Rules:
- The **USP is the thread** through the page (N4). Pain points are material to pick a message; they do not become the page. Count how many sections lead with a user problem; if it is more than one, justify each or fix.
- The hero brief answers: for whom → what we solve → see the product working → next step.
- **Type C:** include where the old → new change is explained, and which sections reassure existing customers.
- **Numbers and statistics** are never invented. A number needs a source from the user or Step 07; otherwise it is a placeholder marked `NEEDS DATA`.

## Output — `05-content/13-content-brief.md`

```
# 13 · Content brief
## Page-level notes       (thread, tone, keywords)
## S01 · <name>           (table of the fields above)
## S02 · …
## Data the user must supply   (every NEEDS DATA / UNPROVEN item)
## Assumptions
```

## Check before handing back

- [ ] Every `S##` from Step 12 has a brief; none added or dropped here.
- [ ] Every pain point cited has a source link.
- [ ] Every number is sourced or marked `NEEDS DATA`.
- [ ] No more than one section leads with a user problem, or each exception is justified.

## End of turn

End-of-turn block (Next: Step 14) → stop.
