# Step 03 · Brief analysis & frame lock

> **Phase 1 · Intake & audit** — role: Senior product analyst
> **Applies to:** A B C
> **Output:** `03-research/03-brief-analysis.md`
> **Base prompt** — never edited for a project. Shared rules and the end-of-turn block: `_prompts/README.md`.

---

## Reads

- `01-strategy/` (brief + strategy pack + project type) · `03-research/02-intake.md`

## Stop if

- Step 02 is not `done`.

## Do

1. **What the brief says** — goal, audience, constraints, tone, must-haves, deadlines. Quote the brief; do not paraphrase into new requirements.
2. **What the brief does not say** — list the gaps. Every gap becomes a question or an `ASSUMPTION` with a default.
3. **Questions for the client** — numbered, grouped 🔴 / 🟡 / ⚪, each with the default used if unanswered. Only questions the client can answer. Tag blocking ones `[BLOCKER]`.
4. **Frame lock** — decide with the user and record:

   | Item | Options |
   |---|---|
   | Devices | desktop only · mobile only · responsive (desktop 1440 + mobile 375) |
   | Width / orientation | e.g. 1440 px, one long scrolling page |
   | Colour mode | light only · dark only · both |
   | Language | one language, or several with a switch |
   | **Project language (for files)** | default English |
   | Pages | the `P##` list from Step 00 |

5. **Risks** — anything in the brief that conflicts with the strategy pack, or an unverifiable claim in it (e.g. "the only…", "#1…"). Flag each; do not rewrite it.

## Output — `03-research/03-brief-analysis.md`

```
# 03 · Brief analysis
## What the brief says
## Gaps
## Questions for the client   (🔴 / 🟡 / ⚪, defaults, [BLOCKER])
## Frame lock                 (table — LOCKED when the user confirms)
## Risks & unverifiable claims
## Assumptions
```

## Check before handing back

- [ ] Every requirement quotes the brief.
- [ ] Every gap is a question or an `ASSUMPTION`.
- [ ] Frame lock has an entry for every row (or "to confirm" with a default).
- [ ] Unverifiable claims are listed under Risks.

## End of turn

End-of-turn block (Next: Step 04 for B/C, otherwise Step 05) → stop. Ask the user to confirm the frame lock; it is approved at **Gate 1**.
