# Step 24 · Pre-launch checklist

> **Phase 9 · Launch** — role: Launch manager
> **Applies to:** A B C — the checks differ by type (below)
> **Output:** `10-launch/24-prelaunch.md`
> **Base prompt** — never edited for a project. Shared rules and the end-of-turn block: `_prompts/README.md`.

---

## Reads

- `_progress.md` · `09-final-ui/` · `03-research/04-audit.md` (B/C) · `03-research/05-measurement.md` · `05-content/14-copy.md` (SEO)

## Stop if

- Gate 8 is not `APPROVED`.

## Do

Build the checklist from the table. Run every check you can with code or search and report the result; mark the rest `OWNER: <name>` with a question for the user. Nothing here is assumed done.

**All types (A, B, C)**
- [ ] Legal pages exist (terms, privacy, any required notice) with the **correct legal entity, governing law, date**. Placeholders like `[date]` are gone.
- [ ] Support email and contact details are real and monitored.
- [ ] Where form data is stored, who owns it, and whether it is shared with another product or entity.
- [ ] Cookie / consent behaviour matches the markets served.
- [ ] Per page: title, meta description, H1, canonical, social image.
- [ ] Analytics and the events from Step 05 fire (test each CTA).
- [ ] Every link works (no `#`, no 404); forms submit; sign-up path works end to end.
- [ ] No placeholder content, sample testimonials, fake numbers or stock names left.
- [ ] Every claim on the page has its source or approval.

**B and C — also**
- [ ] Redirect map: each old URL → new URL. Every URL on the must-keep list resolves.
- [ ] SEO keywords and meta from the audit are preserved; sitemap and robots updated.

**C — also**
- [ ] **Old-brand scan.** Search the build, legal pages, forms, meta, image alt text and file names for every old name, domain, product name, legal entity and support email from the audit's old-brand inventory. **The count must be 0.** Report the exact command and its output.
- [ ] Legal pages and counter-notice / report forms use the new brand and a form owned by the new brand.
- [ ] Existing customers have a way to learn about the change (page section, banner, email) if Step 09 planned one.

## Output — `10-launch/24-prelaunch.md`

```
# 24 · Pre-launch checklist
## Checks run             (item · result · evidence)
## Open items             (owner · question)
## Old-brand scan         (type C: command + count)
## Redirect map           (types B, C)
```

## Check before handing back

- [ ] Every checklist line has a result or an owner.
- [ ] Type C: the old-brand scan was run and its count is reported.
- [ ] Types B, C: the redirect map covers every old URL.

## End of turn

End-of-turn block (Next: Step 25) → stop.
