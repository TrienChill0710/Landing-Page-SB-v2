# Step 01 · Strategy pack

> **Phase 0 · Type & strategy** — role: Product strategist
> **Applies to:** A B C
> **Output:** `01-strategy/01-strategy-pack.md` — then **Gate 0**
> **Base prompt** — never edited for a project. Shared rules and the end-of-turn block: `_prompts/README.md`.

---

## Reads

- `01-strategy/00-project-type.md` · everything else in `01-strategy/` (the user's strategy pack, Business Model Canvas, brief)

## Stop if

- Step 00 is not `done` in `_progress.md`.
- **The user's materials contain no USP, or no target persona.** Say which is missing and give the template `01-strategy/strategy-pack-template.md`. **Never invent a USP or a persona** (N1). Stop here until the user supplies them.

## Do

Consolidate the user's materials into one strategy pack. Your job is to organise and test it, not to author it.

1. **Goal of the page** — one sentence, plus the **North Star metric** (e.g. sign-up rate). If the user gave none, propose one and mark it `ASSUMPTION`.
2. **USP** — one sentence the user wrote, plus the proof they have for it (feature, data, quote). Mark any USP claim with no proof as `UNPROVEN`.
3. **Personas** — primary and secondary: who, situation, the job they want done, what they believe today. Copy from the user's pack; do not add personas.
4. **Business model** — from the Business Model Canvas or the user's summary, in one paragraph: who pays, for what, how.
5. **Audience state** — what the reader already knows: new to the category, or already uses something similar. For types **B and C**, also: what existing customers know about the old product or brand.
6. **Type C only — positioning change:** what is changing (name, promise, audience), why, and what stays the same.
7. **Gaps** — what you need that the pack does not contain, as questions: 🔴 / 🟡 / ⚪ with defaults.

Do not research the market yet (Step 06–07).

## Output — `01-strategy/01-strategy-pack.md`

```
# 01 · Strategy pack
## Goal & North Star
## USP & proof            (UNPROVEN where no proof)
## Personas               (primary · secondary)
## Business model
## Audience state         (+ existing-customer view for B, C)
## Positioning change     (type C only)
## Open questions
## Assumptions
```

## Check before handing back

- [ ] USP and every persona trace to the user's materials (quote the source file).
- [ ] No persona or USP was invented.
- [ ] North Star is one measurable metric.
- [ ] Type C: the positioning change is stated.
- [ ] Open questions are grouped 🔴 / 🟡 / ⚪ with defaults.

## End of turn

End-of-turn block → **GATE 0: the Strategy owner confirms the type and the strategy pack** and says `approved`. Record the date and their words. Stop.
