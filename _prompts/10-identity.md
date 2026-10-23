# Step 10 · Identity (Brand module)

> **Phase 3 · Brand** — role: Brand designer
> **Applies to:** **A C** (Brand module on) — otherwise `skipped`
> **Output:** `04-brand/10-identity.md` — then **Gate 3**
> **Base prompt** — never edited for a project. Shared rules and the end-of-turn block: `_prompts/README.md`.

---

## Reads

- `04-brand/09-messaging.md` · `03-research/08-reference-analysis.md` · `02-assets/` (logo, fonts, icons — whatever the user has)

## Stop if

- Step 09 is not `done`.
- The Brand module is off.

## Do

1. **What exists and what must be created.** For each of logo, colour, font, icon style, imagery style: `provided` / `to create` / `to choose`.
2. **Logo.** **Never draw or redraw a logo.** If one must be created, say it is for a designer or the user to supply; you may write a brief for it (meaning, tone, constraints, usage). If a logo is provided, record its format, pixel size, clear space, minimum size, and whether a dark-surface version exists.
3. **Colour foundation** — if the user supplied brand colours, list them with roles. If not, give 2–3 directions (name, mood, why it fits the messaging and stands apart from competitors) with approximate hue families, **no final hex** — Step 16 produces and tests the palette.
4. **Typography** — one heading font and one body font, each open-source with a commercial-use licence (state the licence), or the user's own. Hierarchy in words (not px yet).
5. **Icon style and imagery style** — one icon library (licence stated) and 3–5 rules for photos or illustrations (subject, light, crop, what to avoid).
6. **Type C only — migration list:** each old brand asset from the audit's old-brand inventory → replace / keep / retire, with owner.

## Output — `04-brand/10-identity.md`

```
# 10 · Identity
## Status of each asset   (provided / to create / to choose)
## Logo                   (as provided, or the brief)
## Colour directions
## Typography             (fonts + licences)
## Icons & imagery
## Migration list         (type C)
## Assumptions
```

## Check before handing back

- [ ] No logo was drawn by the AI.
- [ ] Every font and icon library has a stated commercial-use licence.
- [ ] Colour directions are tied to the messaging and to the me-too test.
- [ ] Type C: every old asset has a decision.

## End of turn

End-of-turn block → **GATE 3: the Strategy owner approves messaging and identity** and says `approved`. Record the date and their words. Stop.
