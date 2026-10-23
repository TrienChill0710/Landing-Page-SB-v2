# Step 02 · Intake & input check

> **Phase 1 · Intake & audit** — role: Project coordinator
> **Applies to:** A B C
> **Output:** `03-research/02-intake.md`
> **Base prompt** — never edited for a project. Shared rules and the end-of-turn block: `_prompts/README.md`.

---

## Reads

- `_progress.md` · `01-strategy/` · every sub-folder of `02-assets/`

## Stop if

- Gate 0 is not `APPROVED` in `_progress.md`.

## Do

1. **Run the input checklist** and show it as a table (✅ found / ⚠ missing):

   | Input | Where | Required |
   |---|---|---|
   | Strategy pack | `01-strategy/01-strategy-pack.md` | Yes — Gate 0 |
   | Brief (client brief or 5–10 lines) | `01-strategy/` | Yes — without it, STOP |
   | Logo (SVG/PNG) | `02-assets/logo/` | B, C: yes · A: if a brand exists. Brand module on → comes from Step 10 |
   | Logo for dark surfaces | `02-assets/logo/` | Only if dark mode or dark headers are planned |
   | Font — files or `font-name.txt` | `02-assets/fonts/` | Before Step 16 |
   | Icons — SVG or `icon-library.txt` | `02-assets/icons/` | Before Step 16 |
   | Moodboard, 2–4 images | `02-assets/moodboard/` | Recommended |
   | Existing page link + numbers + feedback | `01-strategy/` | B, C — yes |

2. **For every missing item:** show a ⚠ WARNING saying what is missing, where to put it, and 1–2 concrete options. Flag licence risks: system fonts that cannot be redistributed, icons from other apps or paid packs, a logo that is only a screenshot, a low-resolution logo (state its pixel size).
3. You may continue to Step 06 while visual assets are missing, but **STOP before Step 16** until logo (or Step 10 output), font and icons exist.
4. **Echo back 3–5 lines:** project name, type, product in one line, main brand colour if a logo exists, the primary persona and the USP — so the user can correct you.
5. Ask: "I understand this. Shall I continue?" Do not start Step 03 on your own.

## Output — `03-research/02-intake.md`

```
# 02 · Intake
## Input checklist        (table)
## Warnings               (missing items, licence and resolution risks)
## What I understood      (3–5 lines)
## Assumptions
```

## Check before handing back

- [ ] Every row of the checklist has a status.
- [ ] Every ⚠ has a location and at least one option.
- [ ] Logo resolution and licence risks were checked, not assumed.

## End of turn

End-of-turn block (Next: Step 03) → stop.
