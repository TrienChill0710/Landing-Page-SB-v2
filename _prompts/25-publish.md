# Step 25 · Publish / handoff

> **Phase 9 · Launch** — role: Release manager
> **Applies to:** A B C
> **Output:** `10-launch/25-publish.md` — then **Gate 9**
> **Base prompt** — never edited for a project. Shared rules and the end-of-turn block: `_prompts/README.md`.

---

## Reads

- `10-launch/24-prelaunch.md` · `09-final-ui/final-ui.html` · `07-tokens/` · `08-claude-design-input/master-spec.md` · `_progress.md` (roles, modules)

## Stop if

- Step 24 has open items that block launch (anything marked 🔴).
- No Publisher is named in `_progress.md`.

## Do

1. **Choose the route** with the user: publish from the build tool, hand the HTML and tokens to developers, or both. If the Figma / handoff module is on, run its steps now (import tokens and screens, build components, prototype, developer handoff) — each as its own step in the optional module.
2. **Handoff package** (when developers build it): the final HTML, the token files, the master spec, the image files with `IMG##` names, the copy file, the events table, the redirect map, the pre-launch checklist and its open items. Nothing the developers need may live only in a chat.
3. **Publish steps for the Publisher:** environment, domain, who flips the switch, how to roll back, who is on call for the first 48 hours.
4. **Smoke test after publish:** sign-up path, primary CTAs, forms, analytics events, redirects (B, C), old-brand scan on the live page (C). Report each result.
5. Update `_progress.md`: launch date, URL, the Publisher, and where results will be read.

## Output — `10-launch/25-publish.md`

```
# 25 · Publish
## Route                  (publish / handoff / both)
## Handoff package        (file list)
## Publish plan           (owner · environment · rollback)
## Smoke test             (item · result)
## Post-launch ownership
```

## Check before handing back

- [ ] A Publisher is named and the rollback is written.
- [ ] The smoke test was run on the live URL (or `NOT RUN — not live yet`).
- [ ] Nothing needed by developers exists only in chat.

## End of turn

End-of-turn block → **GATE 9: the Strategy owner approves the launch** and says `approved`. Record the date and their words. Step 26 runs later, after the reading window set in Step 05. Stop.
