# Step 05 · Measurement

> **Phase 1 · Intake & audit** — role: Growth analyst
> **Applies to:** A B C
> **Output:** `03-research/05-measurement.md` — then **Gate 1**
> **Base prompt** — never edited for a project. Shared rules and the end-of-turn block: `_prompts/README.md`.

---

## Reads

- `01-strategy/01-strategy-pack.md` (North Star) · `03-research/03-brief-analysis.md` · `03-research/04-audit.md` (if B/C)

## Stop if

- Step 03 is not `done`, or (B/C) Step 04 is not `done`.

## Do

1. **North Star** — restate the one metric and how it is calculated (numerator, denominator, time window).
2. **Baseline.**
   - **B, C:** the current value, from the user's numbers. If none: `NOT AVAILABLE` — list how to get it (analytics tool, date range) as a 🔴 question. Never estimate.
   - **A:** there is no baseline; say so.
3. **Events to track** — one row per event: page / section, trigger, event name, why. Minimum: primary CTA click per section, form submit, scroll depth milestones, outbound links to the sign-up flow.
4. **Target** — only if the user gave one. If not, write "no target set" and add a question. Do not invent a target.
5. **When to read the result** — how many days or how many visitors before comparing with the baseline (propose; mark `ASSUMPTION`). Step 26 uses this.

## Output — `03-research/05-measurement.md`

```
# 05 · Measurement
## North Star & formula
## Baseline               (value + source, or NOT AVAILABLE)
## Events to track        (table)
## Target                 (as given, or "not set")
## Reading window
## Assumptions
```

## Check before handing back

- [ ] North Star has an explicit formula.
- [ ] No baseline or target was invented.
- [ ] Every primary CTA appears in the events table.

## End of turn

End-of-turn block → **GATE 1: the Strategy owner approves the frame lock (Step 03) and the audit (Step 04)** and says `approved`. Record the date and their words. Stop.
