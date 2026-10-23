# Step 19 · Tokens

> **Phase 7 · System & spec** — role: Design-systems engineer
> **Applies to:** A B C — type **B**: map onto the existing tokens first, add only what is missing
> **Output:** `07-tokens/1-primitive.json` · `07-tokens/2-semantic.json` · `07-tokens/token-mapping.md`
> **Base prompt** — never edited for a project. Shared rules and the end-of-turn block: `_prompts/README.md`.

---

## Reads

- `06-proof-ui/proof.html` · `03-research/16-palette.md` · the existing token files, if type B supplied any

## Stop if

- Gate 6 is not `APPROVED`.

## Do

1. **Primitive tokens** (W3C design-token JSON): raw values only — colour scale, font families and sizes, line heights, spacing steps, radii, shadows, border widths, durations and easing. Names are neutral (`color.blue.600`), never roles.
2. **Semantic tokens**: roles that **alias** primitives — `color.action.primary`, `color.text.body`, `color.surface.panel`, `space.section`, `radius.card`… One mode per frame lock (light and/or dark). Every aliased value resolves to a primitive.
3. **Map the proof.** For every CSS variable in `proof.html`'s `:root`, find its token. Produce `token-mapping.md`: variable → token → status (`mapped` / `presentation-only` / `unused`).
4. **Type B:** keep existing token names; map the new palette roles onto them; list additions separately.
5. **Measure** (by code) and report: JSON validity, number of tokens per file, broken aliases (target 0), proof variables mapped vs total, values left over from any sample or earlier project (target 0).
6. Do not create a component tier unless the user asks.

## Output

```
07-tokens/1-primitive.json
07-tokens/2-semantic.json
07-tokens/token-mapping.md
```

## Check before handing back

- [ ] Both files are valid JSON (measured).
- [ ] 0 broken aliases (measured).
- [ ] Every `:root` variable of the proof is mapped, marked presentation-only, or listed unused.
- [ ] No sample values from another project remain.

## End of turn

End-of-turn block (Next: Step 20) → stop. Tokens are approved with the spec at **Gate 7**.
