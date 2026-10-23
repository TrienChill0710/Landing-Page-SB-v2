# _prompts/ — the base prompts, one per step

27 prompts (Step 00–26), one for each step in `00-workflow-map.md`. They are the **base**: the same in every copy of the kit and **never edited for a project**.

## How a project uses them

1. Copy the whole kit for a new project, fill `01-strategy/` and `02-assets/`, type **Read Folder**.
2. At each step Claude opens `_prompts/NN-….md` and follows it exactly.
3. A prompt never contains project details. It says **which files to read**; project details come from there.
4. Output goes to the folder the prompt names. Nothing is saved back into `_prompts/`.

If a prompt and `CLAUDE.md` disagree, `CLAUDE.md` wins — fix the prompt in the base kit, not in a project.

## The prompts

| File | Step | Applies to | Phase | Output |
|---|---|---|---|---|
| `00-project-type.md` | 00 Project type | A B C | 0 Type & strategy | `01-strategy/00-project-type.md` |
| `01-strategy-pack.md` | 01 Strategy pack · **Gate 0** | A B C | 0 | `01-strategy/01-strategy-pack.md` |
| `02-intake.md` | 02 Intake | A B C | 1 Intake & audit | `03-research/02-intake.md` |
| `03-brief-analysis.md` | 03 Brief analysis & frame lock | A B C | 1 | `03-research/03-brief-analysis.md` |
| `04-audit.md` | 04 Audit of the existing page | B C | 1 | `03-research/04-audit.md` |
| `05-measurement.md` | 05 Measurement · **Gate 1** | A B C | 1 | `03-research/05-measurement.md` |
| `06-positioning.md` | 06 Positioning & competitors | A B C | 2 Research | `03-research/06-positioning.md` |
| `07-voc.md` | 07 Voice of customer | A B C | 2 | `03-research/07-voc.md` |
| `08-reference.md` | 08 Reference analysis · **Gate 2** | A B C | 2 | `03-research/08-reference-analysis.md` |
| `09-messaging.md` | 09 Messaging (Brand module) | A C | 3 Brand | `04-brand/09-messaging.md` |
| `10-identity.md` | 10 Identity (Brand module) · **Gate 3** | A C | 3 | `04-brand/10-identity.md` |
| `11-narrative-options.md` | 11 Narrative options · **Gate 4** | A B C | 4 Narrative | `03-research/11-narrative-options.md` |
| `12-sections.md` | 12 Sitemap & section list | A B C | 4 | `03-research/12-sections.md` |
| `13-content-brief.md` | 13 Content brief | A B C | 5 Content | `05-content/13-content-brief.md` |
| `14-copy.md` | 14 Copy | A B C | 5 | `05-content/14-copy.md` |
| `15-content-review.md` | 15 Content self-review · **Gate 5** | A B C | 5 | `05-content/14-copy.md` (review log) |
| `16-palette.md` | 16 Palette | A B C | 6 Visual | `03-research/16-palette.md` |
| `17-moodboard.md` | 17 Moodboard | A B C | 6 | `03-research/17-moodboard.md` |
| `18-proof.md` | 18 Proof sections · **Gate 6** | A B C | 6 | `06-proof-ui/proof.html` |
| `19-tokens.md` | 19 Tokens | A B C | 7 System & spec | `07-tokens/*.json` |
| `20-master-spec.md` | 20 Master spec · **Gate 7** | A B C | 7 | `08-claude-design-input/` |
| `21-build.md` | 21 Build | A B C | 8 Build & review | `09-final-ui/final-ui.html` |
| `22-ui-review.md` | 22 UI self-review | A B C | 8 | `09-final-ui/22-self-review.md` |
| `23-spec-check.md` | 23 Spec check · **Gate 8** | A B C | 8 | `09-final-ui/23-spec-check.md` |
| `24-prelaunch.md` | 24 Pre-launch checklist | A B C | 9 Launch | `10-launch/24-prelaunch.md` |
| `25-publish.md` | 25 Publish / handoff · **Gate 9** | A B C | 9 | `10-launch/25-publish.md` |
| `26-results.md` | 26 Results after launch | A B C | 9 | `10-launch/26-results.md` |

Steps 09 and 10 form the **Brand module**; Gate 3 is `skipped` when the module is off.

## Rules every prompt shares (written once, here)

### Where the project stands — `_progress.md`

- `_progress.md` is the **only** record of progress. Read it before any step; update it at the end of every step and every gate.
- **"Gate N is approved"** means `_progress.md` shows Gate N = `APPROVED`. A chat message from an earlier session or the existence of a file does not count.
- A gate becomes `APPROVED` only when the **approver named in `_progress.md`** says so in words. Record the date and their words.
- The project type (A/B/C) is read from `_progress.md`. A step that does not apply to it is marked `skipped` with the reason, and the next applicable step runs.

### When to stop

- **After every step:** end-of-turn block, then stop. The user says `continue`.
- **At a gate:** the approver reviews and says `approved`. Only then is the gate recorded and the next phase allowed.
- **Inside a step**, stop only where the prompt says "STOP and wait".
- Never start a step whose "Stop if" is true. Never run two steps in one turn.

### Measure, don't eyeball

Any check with a number is **computed by running code**, and the number goes in the report: contrast ratios, token alias errors, section count, page height, hex colours outside `:root`, inline `style=` count, leftover old-brand names, JSON validity. A check that was not run is `NOT RUN — why`.

### Codes never change

`P##` (page), `S##` (section) and `FL##` (flow) are assigned once and are **permanent**. A new item takes the next free number; a dropped item stays in the list marked `removed`. Never renumber.

### Sources

Every competitor fact, pain point and statistic carries a source link. Reddit, store reviews, YouTube comments and forum posts are **evidence of what people say**, not of how many people think it. Never write a quantitative claim from a handful of comments. A reference site is never proof of conversion rate.

### The self-review loop (Steps 15 and 22)

1. Run the checklist in the step prompt. Fix what fails.
2. Run it again on the fixed result. **Default: 2 rounds.** Stop early only if round 2 finds nothing.
3. Write each round in the review log: what failed, what changed.
4. Only then tell the user it is ready for a person to review.

### If you change an earlier step

Re-running a step makes later steps out of date. Mark them `stale — re-run` in `_progress.md`, tell the user, and re-open the gates they belong to.

| You change… | These become stale |
|---|---|
| 00 project type | everything |
| 01 strategy pack (USP, persona) | 02 → 26 |
| 03 frame lock, pages in scope | 12 → 26 |
| 04 audit · 06 positioning · 07 VoC | 09 → 26 |
| 09 messaging · 10 identity | 11 → 26 |
| 11 chosen option | 12 → 26 |
| 12 section list | 13 → 26 |
| 14 copy | 18 → 26 |
| 16 palette · 17 moodboard | 18 → 26 |
| 18 proof · 19 tokens | 20 → 26 |
| 20 master spec | 21 → 26 |

Small fixes that change no decision (a typo, a clearer sentence) do not make anything stale — say so in the report.

**Feedback after Gate 8** goes back to the right place:

| Feedback is about… | Go back to |
|---|---|
| Spacing, boxes, header, visual bugs | Step 22 |
| Wording, length inside a section | Step 14 |
| Section order, page too long, too many focal points | Step 12 |
| USP unclear, looks like a competitor, wrong story | Step 06–07 or Gate 4 |

### Always

- **One step per turn.** Never start the next step on your own.
- **Stop checks first.** Every prompt starts with "Stop if". If one is true, say which and stop.
- **No extrapolation.** Anything not in an input or a source is written `ASSUMPTION`.
- **Assets as given.** Logo, icons, font — never redrawn, never mixed.
- **Save to the named file.** Overwrite on re-run; never create `-v2`, `-final` copies.

### Chat summary — every step shows its key content in chat

The step file is complete and detailed. The user must **not** need to open a long file to understand the step. So every step also puts its most valuable content **in the chat**, in the user's language (files stay in the project language).

- **Structured, not a one-liner.** Short headings and tables, following the logic of the step.
- **Plain language.** No bare codes (A03, S07…). Say what a code means in words.
- **Pick what matters.** Keep findings that change a decision or the design. Leave source lists and long tables in the file.
- **End with "what this means for the design"** — 3–8 concrete points the next steps will apply.
- **Questions go in chat**, grouped and numbered, each with the default Claude uses without an answer:

  | Group | Meaning |
  |---|---|
  | 🔴 **Must answer** | Blocking — work stops at a named step without it |
  | 🟡 **Should answer** | Changes content or structure; a default is used otherwise |
  | ⚪ **Nice to have** | Improves realism; safe to skip |

- A step with no questions says so in one line.

### End-of-turn report — every step ends with this block

```
STEP NN · <name> — done
Applies to:   <A B C> · project type: <X>
Files:        <every file written or changed>
Key result:   <2–4 lines, plain language>
ASSUMPTIONS:  <n> (listed in the file)   ·   [BLOCKER] questions: <n>
Measured:     <numbers from code, or NOT RUN — why>
_progress.md: updated
Next:         Step NN+1 · <name> — say "continue"
              (or, at a gate: GATE n — <approver> reviews and says "approved")
```
