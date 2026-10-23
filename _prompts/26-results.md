# Step 26 · Results after launch

> **Phase 9 · Launch** — role: Growth analyst
> **Applies to:** A B C — run after the reading window from Step 05 has passed; optional if the user does not want it
> **Output:** `10-launch/26-results.md`
> **Base prompt** — never edited for a project. Shared rules and the end-of-turn block: `_prompts/README.md`.

---

## Reads

- `03-research/05-measurement.md` (North Star, baseline, events, reading window) · `10-launch/25-publish.md` · the analytics export or numbers the user supplies

## Stop if

- Gate 9 is not `APPROVED`.
- The reading window has not passed: say how many days or visitors remain, and stop.
- The user supplies no analytics data. Do not estimate results.

## Do

1. **Result against the North Star** — the new value, the period, the visitor count. **B, C:** compare with the baseline from Step 05 and state the difference. **A:** compare with the target if one was set; otherwise report the value as a first baseline.
2. **Funnel** — per section or event: how many reached it, how many clicked. Find where people leave.
3. **By persona or source** — only if the data is split that way.
4. **Reliability** — sample size, period length, anything else that changed in the same period (campaigns, seasonality, pricing). Say plainly when the data is too thin to conclude; do not declare a win or a loss from noise.
5. **What the numbers suggest** — 3–5 hypotheses, each tied to a section and a finding from the research (Steps 07–08). Label them hypotheses.
6. **Next actions** — what to test or change, ordered by expected value, each saying which step it would re-open (use the stale table in `_prompts/README.md`).

## Output — `10-launch/26-results.md`

```
# 26 · Results
## North Star result      (value · period · vs baseline or target)
## Funnel
## Reliability & caveats
## Hypotheses
## Next actions           (and the step each re-opens)
```

## Check before handing back

- [ ] Every figure comes from the user's data; none estimated.
- [ ] Sample size and caveats are stated.
- [ ] Hypotheses are labelled as hypotheses.

## End of turn

End-of-turn block → stop. The project is complete unless the user re-opens a step.
