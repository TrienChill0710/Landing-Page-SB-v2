# Step 08 · Reference analysis

> **Phase 2 · Research** — role: Senior designer
> **Applies to:** A B C
> **Output:** `03-research/08-reference-analysis.md` — then **Gate 2**
> **Base prompt** — never edited for a project. Shared rules and the end-of-turn block: `_prompts/README.md`.

---

## Reads

- `01-strategy/01-strategy-pack.md` (USP) · `03-research/06-positioning.md` · `03-research/07-voc.md`

## Stop if

- Step 07 is not `done`.

## Do

Pick references **to learn something specific for our USP** — never to copy. Ask the user for any reference sites they want included. Otherwise choose 5–8 pages and give a link for each.

1. **Analyse each reference by aspect.** One row per aspect; say what we can learn, or "nothing — not relevant":

   | Aspect | Question |
   |---|---|
   | Positioning | How is the main value stated? Is it shown with the real product UI? |
   | Information order | Section order; where proof sits relative to the CTA |
   | Trust | Use cases, results, testimonials, security / privacy pages — how presented |
   | Colour | What gives a trustworthy feel; does it separate them from competitors? |
   | Difference | Would copying this make us look like a competitor? |

   Add Layout and Motion only if the project needs them.
2. **Evidence rule (N10).** There is no public data that a reference converts well unless the source shows it. State "no conversion evidence" for each reference; never use one as a reason to choose a design.
3. **Pattern table** — for each section type the page will need (hero, proof, pricing, FAQ…): the best pattern seen, which reference, and why it suits our USP and personas.
4. **Do-not-copy list** — patterns that would make us look like a competitor (from the me-too test in Step 06).
5. **Colour direction** — 2–3 sentences on colour feel to aim for; no hex values yet (Step 16).

## Output — `03-research/08-reference-analysis.md`

```
# 08 · Reference analysis
## References             (link · why chosen)
## Analysis by aspect     (table per reference)
## Pattern table          (section type · pattern · source · why)
## Do-not-copy list
## Colour direction
## Assumptions
```

## Check before handing back

- [ ] Every reference has a link and a stated reason.
- [ ] No reference is called "high converting" without a source.
- [ ] The do-not-copy list exists and ties back to Step 06.
- [ ] Every pattern ties to the USP or a persona pain point.

## End of turn

End-of-turn block → **GATE 2: the Strategy owner reviews the positioning (06), the pain points (07) and the references (08), confirms nothing drifts from the USP,** and says `approved`. Record the date and their words. Stop.
