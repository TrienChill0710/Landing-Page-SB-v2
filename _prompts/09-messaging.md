# Step 09 · Messaging (Brand module)

> **Phase 3 · Brand** — role: Brand strategist
> **Applies to:** **A C** — type B: mark `skipped` ("brand stays; Brand module off") and go to Step 11. Type A with an existing brand: skip as well.
> **Output:** `04-brand/09-messaging.md`
> **Base prompt** — never edited for a project. Shared rules and the end-of-turn block: `_prompts/README.md`.

---

## Reads

- `01-strategy/01-strategy-pack.md` · `03-research/06-positioning.md` · `03-research/07-voc.md` · `03-research/04-audit.md` (type C)

## Stop if

- Gate 2 is not `APPROVED`.
- The Brand module is off in `_progress.md`.

## Do

1. **Positioning statement** — "For [persona] who [need], [name] is a [category] that [key benefit]. Unlike [alternative], [differentiator]." Use only the USP and its proof from the strategy pack.
2. **Message hierarchy** — one primary message; three supporting messages; the proof behind each. Each ties to a pain point in Step 07.
3. **Voice** — 3–4 attributes with a "we say / we don't say" example each. Based on the personas' own language from Step 07.
4. **Naming and taglines** (only if the user asked) — propose 3–5 options with the reason; the user chooses. Check for obvious conflicts with competitors' names.
5. **Type C only — the change message for existing customers:** what is changing, why, what stays the same, what they must do (if anything). Plain, no spin. List the questions an existing customer will ask first.
6. **What we must not claim** — claims that are unproven (from Step 01 `UNPROVEN`), superlatives, legally risky wording.

## Output — `04-brand/09-messaging.md`

```
# 09 · Messaging
## Positioning statement
## Message hierarchy       (primary · 3 supporting · proof for each)
## Voice                   (attributes + we say / we don't say)
## Names & taglines        (only if asked)
## Change message          (type C)
## Claims to avoid
## Assumptions
```

## Check before handing back

- [ ] The positioning statement uses only the strategy pack's USP.
- [ ] Every supporting message has a proof source or is marked `UNPROVEN`.
- [ ] Type C: the change message answers what changes and what stays.

## End of turn

End-of-turn block (Next: Step 10) → stop.
