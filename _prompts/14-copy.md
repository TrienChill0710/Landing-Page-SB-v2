# Step 14 · Copy

> **Phase 5 · Content** — role: Senior copywriter
> **Applies to:** A B C
> **Output:** `05-content/14-copy.md`
> **Base prompt** — never edited for a project. Shared rules and the end-of-turn block: `_prompts/README.md`.

---

## Reads

- `05-content/13-content-brief.md` · `04-brand/09-messaging.md` (if the module ran) · `03-research/07-voc.md` (language) · `03-research/04-audit.md` (SEO snapshot, B/C)

## Stop if

- Step 13 is not `done`.

## Do

Write the real copy for every section, in the **project language** (Step 03), following the content brief. No lorem ipsum.

1. **Per section** `S##`: headline, supporting line, body or item copy (cards, steps, FAQ), CTA label, alt text for each visual, and a one-line **visual note** (what the visual must show — a product UI, a photo, a diagram — not the style).
2. **Words from the audience.** Use the phrases collected in Step 07 where they fit; do not quote a real person without their source and permission.
3. **One message per section.** If a section drifts to two, shorten it.
4. **Proof.** Use only claims that have a source in the brief. Items marked `NEEDS DATA` stay as visible placeholders `[NEEDS DATA: …]` — never fill in a number. Do not write testimonials, logos or statistics that do not exist.
5. **SEO per page:** title (≤ 60 characters), meta description (≤ 155), H1, and the main keywords. **B/C:** keep the keywords and URLs on the must-keep list.
6. **Legal and microcopy:** form labels, error messages, empty states, cookie and consent wording where the page needs them.
7. **Word count per section** against the brief's maximum — computed by code, reported.

## Output — `05-content/14-copy.md`

```
# 14 · Copy
## P01 · SEO              (title · meta · H1 · keywords)
## S01 · <name>           (headline · support · body · CTA · alt text · visual note)
## S02 · …
## Microcopy & legal
## Placeholders           (every [NEEDS DATA])
## Review log             (filled in Step 15)
## Assumptions
```

## Check before handing back

- [ ] Every `S##` has copy; word counts are within the brief (measured).
- [ ] No invented numbers, testimonials or logos; placeholders are visible.
- [ ] Title and meta lengths are within the limits (measured).
- [ ] B/C: must-keep keywords and URLs are present.

## End of turn

End-of-turn block (Next: Step 15) → stop.
