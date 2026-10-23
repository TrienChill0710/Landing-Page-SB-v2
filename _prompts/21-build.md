# Step 21 · Build

> **Phase 8 · Build & review** — role: Builder (the user drives the build tool; Claude guides)
> **Applies to:** A B C
> **Output:** `09-final-ui/final-ui.html` (exported by the user)
> **Base prompt** — never edited for a project. Shared rules and the end-of-turn block: `_prompts/README.md`.

---

## Reads

- `08-claude-design-input/` (spec, build prompt, image prompts) · `02-assets/images/`

## Stop if

- Gate 7 is not `APPROVED`.
- Images are neither saved in `02-assets/images/` nor explicitly skipped.

## Do

Guide the user step by step, then **STOP and wait**:

1. Open the build tool (Claude Design, or the tool the project uses).
2. If it supports a design system, load the tokens, repeated components and usage rules from the spec first.
3. Attach the files listed in `build-prompt.md`, including every image.
4. Paste the build prompt. Answer the tool's questions from the spec — if the answer is not in the spec, say so and stop; do not make it up.
5. Let it build. Review in the browser against the proof.
6. Export **one HTML file** and save it as `09-final-ui/final-ui.html`.
7. Tell Claude: **"build done"**.

While waiting, do nothing else. If the user reports the tool misses something, point to the exact spec section and suggest the correction to the prompt — do not edit the spec silently.

## Check before handing back

- [ ] The user has the file list and the prompt.
- [ ] `final-ui.html` exists in `09-final-ui/` before Step 22 starts.

## End of turn

Tell the user to export and say "build done" → stop. Next: Step 22.
