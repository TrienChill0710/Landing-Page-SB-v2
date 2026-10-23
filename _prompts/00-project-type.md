# Step 00 · Project type

> **Phase 0 · Type & strategy** — role: Project lead
> **Applies to:** A B C
> **Output:** `01-strategy/00-project-type.md` · `_progress.md` header filled in
> **Base prompt** — never edited for a project. Shared rules and the end-of-turn block: `_prompts/README.md`.

---

## Reads

- `_progress.md` · everything in `01-strategy/` and `02-assets/` (to see what the user already supplied)

## Stop if

- The user has not confirmed they want to start (see "Read Folder" in `CLAUDE.md`).
- Questions 1 or 2 below are unanswered — ask them and wait.

## Do

Ask the user these five questions in chat (numbered, so they can answer by number). Do not guess answers from the folder.

1. Is there a landing page today? If yes, send the link.
2. Is there a brand today (logo, palette, guideline)? Does it stay, or is it being replaced?
3. If a page exists: current numbers (traffic, conversion rate, scroll depth), feedback received, what **must stay** (URLs, SEO keywords, sections that work)?
4. Scope: one page, or several (Home, sub-pages, legal pages)?
5. Do current customers read this page? If yes, what do they need to hear that a new visitor does not?

**Question 1 and 2 are blocking.** Questions 3–5 have defaults: "no numbers available", "one page", "no existing customers" — mark each default used as `ASSUMPTION`.

Then classify:

| Type | Rule |
|---|---|
| **A · New** | No page exists |
| **B · Redesign** | A page exists and the brand stays |
| **C · Rebrand** | A page or product exists and the name, positioning or identity changes |

Brand module: **on** for C; **on** for A when no logo/palette exists; **off** for B.
List the pages in scope as `P01, P02…` (name + one-line job). Ask who fills the four roles (Strategy owner, Content reviewer, Builder, Publisher).

Fill the `_progress.md` header: project name, type, pages, modules, roles. Mark every step that does not apply to the type as `skipped` with the reason (see `00-workflow-map.md` §6).

## Output — `01-strategy/00-project-type.md`

```
# 00 · Project type
## Type            (A / B / C + one-line reason)
## Answers         (the five questions, with the answers or the default used)
## Pages in scope  (P## · name · job)
## Modules         (Brand on/off + why · Figma/handoff off)
## Roles
## Steps skipped for this type
## Assumptions
```

## Check before handing back

- [ ] Type is one of A, B, C, with a reason from the answers.
- [ ] Every page in scope has a `P##` code.
- [ ] `_progress.md` header filled; non-applicable steps marked `skipped` with a reason.
- [ ] Defaults used are marked `ASSUMPTION`.

## End of turn

End-of-turn block (Next: Step 01) → stop.
