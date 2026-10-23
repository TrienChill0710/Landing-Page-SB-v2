# Step 12 · Sitemap & section list

> **Phase 4 · Narrative** — role: Information architect
> **Applies to:** A B C
> **Output:** `03-research/12-sections.md`
> **Base prompt** — never edited for a project. Shared rules and the end-of-turn block: `_prompts/README.md`.

---

## Reads

- `03-research/11-narrative-options.md` (the chosen option) · `01-strategy/` · `03-research/04-audit.md` (B/C) · `03-research/07-voc.md` · `03-research/05-measurement.md`

## Stop if

- Gate 4 is not `APPROVED` (no option chosen).

## Do

1. **Pages.** Confirm the `P##` list from Step 00. More than one page: the sitemap first (page, job, who links to it, what it links to, primary CTA). Every page needs a way in and a next step; list any dead end.
2. **Caps — set them now, with the user.** Propose: **maximum sections per page**, **maximum page length** (desktop px and mobile px if responsive), **maximum boxes (cards/panels) per section**, **maximum CTAs per section**. Defaults if the user has no view: 10 sections · 9,000 px desktop · 4 boxes · 1 CTA. Mark defaults `ASSUMPTION`. Record the caps in `_progress.md`.
3. **Section list per page, following the chosen option's message order.** One row per section:

   | S## | Name | Purpose | The ONE message (focal point) | Persona served | Pain point it answers (from Step 07) | CTA |

   Each section has exactly one focal point (N5). A section with two messages is split or one is cut.
4. **Types B and C — keep / rework / drop table** for every `OLD-##` section from the audit: decision + reason, and the `S##` it becomes (or "dropped"). Anything on the must-keep list stays.
5. **Check against the caps.** Count sections and estimate length; if over a cap, cut or merge and say what.
6. **Flows** — `FL##`: arrive → read → click CTA, for each persona and each entry source.
7. **Open decisions** — anything the user must settle.

## Output — `03-research/12-sections.md`

```
# 12 · Sitemap & sections
## Caps                   (sections · length · boxes · CTAs)
## Pages                  (P## table)
## Section list           (per page, S## table)
## Keep / rework / drop   (types B, C)
## Flows                  (FL##)
## Cap check              (measured counts)
## Open decisions
## Assumptions
```

## Check before handing back

- [ ] Section list follows the chosen option, not the other one.
- [ ] Every section has one focal point and a persona.
- [ ] Section count ≤ cap (counted by code, not by eye).
- [ ] B/C: every `OLD-##` has a decision; every must-keep item survives.
- [ ] `S##`, `P##`, `FL##` codes assigned once.

## End of turn

End-of-turn block (Next: Step 13) → stop. This step is approved with the copy at **Gate 5**.
