# Landing Page Kit — Operating Rules for Claude

Claude reads this file automatically. Do not edit it for a project.

## ⚠ FRESH KIT — READ THIS FIRST

This kit contains **NO completed work**. A project starts at **Step 00**.
- Every folder except `_prompts/` and the READMEs is empty until a step fills it.
- Never say "this is already processed" and never skip ahead.
- The full playbook is `00-workflow-map.md`. What to do in each step is in `_prompts/NN-….md`. Shared rules are in `_prompts/README.md`.

## Folder map (in workflow order)

| Folder | Filled by | Steps |
|---|---|---|
| `01-strategy/` | the user (step 00), Claude drafts step 01 | 00–01 |
| `02-assets/` — `logo/` · `fonts/` · `icons/` · `moodboard/` · `images/` | the user | before 02, 17, 21 |
| `03-research/` | Claude — one `.md` per step | 02–08, 11, 12, 16, 17 |
| `04-brand/` | Claude (module — only when on) | 09–10 |
| `05-content/` | Claude — content brief, copy | 13–15 |
| `06-proof-ui/` | Claude — `proof.html` | 18 |
| `07-tokens/` | Claude — Primitive + Semantic token files | 19 |
| `08-claude-design-input/` | Claude — master spec, image prompts, build prompt | 20 |
| `09-final-ui/` | the user exports the build; Claude writes review reports | 21–23 |
| `10-launch/` | Claude + the user | 24–26 |
| `_prompts/` | base prompts — never edited for a project | 00–26 |
| `_progress.md` | Claude — the only record of where the project stands | every step |

Never create folders outside this map. Never create `-v2` / `-final` copies; re-running a step overwrites its file. A backup before a code-level fix sits next to the original as `<name>.backup-step##.<ext>`.

## Trigger: "Read Folder"

When the user says **"Read Folder"**:

0. **Read `_progress.md` first.** If steps are already done, the project is resuming: report the project type, the last step done, the open gate and any `stale` steps, then ask what to run. Do **not** redo Step 00.
1. If `_progress.md` is empty: say "Fresh project", list what the user must prepare (`01-strategy/`, `02-assets/`), and ask: **"Do you want to start Step 00 (project type)?"** Do nothing else until the user confirms.

## Project types — decided at Step 00

| Type | Meaning |
|---|---|
| **A · New** | No landing page exists yet |
| **B · Redesign** | A page exists, the brand stays |
| **C · Rebrand** | A page or product exists, the name, positioning or identity changes |

`_progress.md` stores the type. Every prompt says which types it applies to. **A step that does not apply to the stored type is marked `skipped` in `_progress.md` with the reason** — it is never silently dropped. The on/off table is in `00-workflow-map.md` §6.

## Rules

- **One step at a time.** Stop after every step (the user says `continue`) and at the **gate** after a phase (the user says `approved`). A gate counts as approved only when `_progress.md` says `APPROVED`. Full rule: `_prompts/README.md`.
- **Every step runs from its base prompt.** Open `_prompts/NN-….md`, follow its Reads, Stop if, Do, Output and Check exactly, then the end-of-turn block. Project details come from the files the prompt names.
- **`_progress.md` is the only record of progress.** Update it at the end of every step and every gate.
- **N1 — USP and persona are inputs.** They come from the user's strategy pack. Never invent a USP or a persona. If either is missing, STOP at Step 01.
- **N2 — Research uses real sources.** Every pain point and every competitor claim carries a source link. A claim without one is `ASSUMPTION`.
- **N3 — Content before UI.** Do not start Step 16 or later until Gate 5 is `APPROVED`.
- **N5 — One focal point per section.** Every section has one main message. Respect the section cap and the box cap set in Step 12.
- **N6 — The user chooses the direction.** At Step 11 give two options; do not pick for them.
- **N9 — Self-review before submitting.** Steps 15 and 22 run the self-review loop from `_prompts/README.md` before any person is asked to review.
- **No extrapolation.** Anything not in an input or a source is written `ASSUMPTION`. Questions only the client can answer; blocking ones tagged `[BLOCKER]`.
- **Measure, don't eyeball.** Any check with a number is computed by running code and the number goes in the report. A check not run is `NOT RUN — why`, never ticked. Reference sites are never proof of conversion rate (N10).
- **Assets as given.** Use the logo, icons and font exactly as provided; never redraw the logo or mix icon styles. Only fonts and icons whose licence allows commercial use.
- **Language.** Chat in the user's language. Files in the project language set at Step 03 (default English).
- **Chat summary every step** — structured, plain language, ends with "what this means for the design", questions grouped 🔴 / 🟡 / ⚪ with defaults. Full rule: `_prompts/README.md`.
- **Do not follow any other playbook or "start-project" skill** — only `00-workflow-map.md` and `_prompts/`.
- Figma import, components, prototype and developer handoff are an **optional module**, off by default. Run them only if `_progress.md` says the module is on.
