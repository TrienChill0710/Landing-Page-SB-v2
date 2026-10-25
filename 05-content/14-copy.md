# 14 · Copy

Project: ShopBase website redesign · type C · Rebrand · page P01 Home in two variants (P01·A "Find, fix, approve"; P01·B "One store, with AI on top") · English · Gate 4 APPROVED (both options) · Step 13 done. Source of truth: `05-content/13-content-brief.md`.

> How to read this file
> - SHARED sections (S01, S02, S07, S08, S09) are written once; where the brief allows a variant difference, lines are labelled (A) or (B).
> - A-only: S03–S06. B-only: S10, S11 (CONDITIONAL, default not built), S12.
> - Lines inside a block quote that start with `CONDITIONAL — do not publish unless confirmed` or `ALTERNATE — needs Gate 5 sign-off` are NOT part of the default page. The word-count script skips them.
> - Nothing here is cleared for publication. Every description of the AI uses the screenshot's own words, plus "proposed" and "scan" from the brief (UNPROVEN as product behaviour). No numbers appear on the page.
> - Field names (Headline, Support, Body, Link line, Caption) are read by the word-count script; do not rename them.

---

## P01 · SEO (DRAFT)

The brief proposes no keywords and no analytics exist (audit: no search volumes). Title and meta are written only from the hero promise in `11` (descriptive, flagged; not approved until Gate 5). Old claims ("best eCommerce platform", "free for 14 days", "in a few clicks", the dropshipping / print-on-demand split) are not carried. K15 (old title/meta, SUSPECTED) is therefore deliberately replaced; the user confirms. K16: canonical and structured data (absent today, audit) to be added at Step 21; the existing Open Graph and Twitter tags (4 OG tags today) are rewritten to match the new title and meta. Whether the variants share one URL is open (data item 19); give the page the title of the variant it shows.

### Variant A (DRAFT)
- Title: ShopBase 2.0: AI that finds what stops shoppers
- Meta description: ShopBase 2.0 has CR Scan AI, which finds what stops shoppers on your store and builds a proposed fix. Get started for free.
- H1: AI that finds what stops shoppers on your store and builds the fix. (same as S03 Headline)
- Open Graph title / description: same as Title / Meta description (DRAFT).

### Variant B (DRAFT)
- Title: ShopBase 2.0: one store platform, with AI on top
- Meta description: ShopBase 2.0 is one store platform with CR Scan AI, which finds what stops shoppers and builds a proposed fix. Get started for free.
- H1: ShopBase 2.0: one store platform, with AI that finds what stops shoppers and builds the fix. (same as S10 Headline)
- Open Graph title / description: same as Title / Meta description (DRAFT).

### Main keywords (DRAFT, ASSUMPTION: no search data)
ShopBase · ShopBase 2.0 · CR Scan AI · AOV AI · store platform (Claude's category word, ASSUMPTION from Step 09) · AI · store. Must-keep keywords: none confirmed (audit: user named nothing; K15 SUSPECTED). Lengths of title and meta are measured below.

---

# Part 1 · SHARED sections

## S01 · Header (SHARED)

- Headline: none (page chrome)
- Nav items (labels only, at most 4 including Login and the button): Pricing `[NEEDS DATA: confirm K1 /pricing; drop this item if not confirmed]` · Login · button
- Login label: Login (plain text link to accounts.shopbase.com/sign-in; navigation, not a CTA)
- CTA label: Get started for free (destination accounts.shopbase.com/sign-up, referral parameters fpr, fpt, clickId, invite_trial kept; K12 SUSPECTED)
- Alt text, logo: ShopBase (logo file used exactly as provided; no second logo file)
- Visual note: the existing ShopBase logo at left, text links and one button at right; stays visible on scroll (Step 12 assumption, Step 20 decides). No "Print on demand", "Dropshipping" or "Book a demo" items.

## S07 · Approve (SHARED, same wording in both variants)

- Headline: A proposal, then your decision.
- Body: The AI proposes. You decide.
- Caption: You approve every change
- Alt text, Illustration 3: Illustration of a proposed change on a card with one approve button.
- Visual label: Illustration (visible next to the image)
- Visual note: one small card showing a proposed change and a single approve control; no number, no real store domain. NEEDS ILLUSTRATION (user-supplied). The caption is the screenshot sentence only; no control block, no "undo", no "nothing changes until".
- Words from the audience: none used (the VoC fear of changes "without my consent", S14, is a theme, not borrowed wording).
- Pain source (Step 07, interim): Persona B rank 5 "changes made without consent" (B5; S14) and the Step 07 section "AI that changes the store" (S7, S22, S23); used as a trust condition only. "AI-1" is a label from Steps 09/13, not an id in `07-voc.md`.

## S08 · AOV AI (SHARED)

- Headline: AOV AI recommends offers aimed at order value.
- Body: AOV stands for average order value.
- CTA label: none
- Alt text, Illustration 4: Illustration of one offer shown on a card.
- Visual label: Illustration
- Visual note: one generic offer on one card with generic labels, no number or percentage, no real product. No input says what kind of offer AOV AI recommends, so the card must not show a specific offer type (bundle, discount, upsell) until the user says. NEEDS ILLUSTRATION.
- Softening: "aimed at order value" is the default until the user accepts "raise" (data item 10). The expansion "average order value" is the standard meaning of AOV, not a product claim; the user confirms it.
- Default wording is identical in A and B. A's optional link line (allowed by the brief) is fenced below because it states that AOV AI offers wait for approval, which is unconfirmed (data item 8).

> CONDITIONAL — do not publish unless confirmed (A only; needs data item 8: every AOV AI offer waits for the seller's approval; default: not shown):
> - Link line (A, conditional): Like the fix, an offer is a proposal for you to approve.

> ALTERNATE — needs Gate 5 sign-off (outcome wording as in the screenshot; unproven):
> - Headline (alt): AOV AI recommends offers that raise order value.

## S09 · Closing call to action (SHARED)

- Headline: Start with ShopBase 2.0.
- Support (A): ShopBase 2.0 is one product.
- Support (B): empty by default (see the conditional line below).
- CTA label: Get started for free (accounts.shopbase.com/sign-up, referral parameters kept; K12 SUSPECTED)
- Alt text: none (no visual)
- Visual note: headline, optional line and one button on a plain band; no secondary button.
- Words from the audience: none.

> CONDITIONAL — do not publish unless confirmed (B only; default: empty, the button stands alone):
> - Support (B, conditional): Start on the Free Launch plan. [NEEDS DATA: the user confirms the plan exists, what it includes, for how long, whether it replaces the 14-day trial, whether CR Scan AI and AOV AI are included]
> - If confirmed as its own section it takes the next free code S13 and needs plan facts first.

## S02 · Footer (SHARED)

- Headline: none
- Column titles: Help · Legal `[NEEDS DATA: confirm column set and any feature/company links, K3 K4 SUSPECTED]`
- Link labels (all SUSPECTED, user confirms): Help center · Blog · Developers · Updates · Templates · Status · App Store · Google Play · Terms of service · Privacy policy · ShopBase Payments terms · Marketplace payments terms
- Not drawn by default: DMCA link (K5b conflict, data item 17, legal owner decides), PrintBase, PlusBase, community Facebook links.
- Copyright line: `[NEEDS DATA: legal entity name and year]`
- Alt text, logo: ShopBase
- Visual note: logo, two or three plain link columns, legal row; no claims, no taglines, no numbers.

---

# Part 2 · P01·A-only sections (Find, fix, approve)

## S03 · Hero A (A only)

- Headline: AI that finds what stops shoppers on your store and builds the fix.
- Support: CR Scan AI finds what stops shoppers and builds a proposed fix. You approve every change.
- CTA label (primary): Get started for free
- CTA label (secondary): Explore CR Scan AI (on-page anchor to S05; ASSUMPTION)
- Alt text, Illustration 1 (small crop): Illustration of a scan result: a card listing what the scan found on a store.
- Visual label: Illustration
- Visual note: a smaller crop of the S05 scan card directly under the two buttons; no number, no real domain. NEEDS ILLUSTRATION.
- Words from the audience: none (hero describes the capability).
- Pain source (Step 07, interim): Persona A rank 6 "traffic or ad spend without sales" (A6; S8, S9), thin; message driver only, the hero does not state it. Trust condition for the approval sentence: see section S07.

> ALTERNATE — needs Gate 5 sign-off (the screenshot's outcome headline; unproven outcome claim):
> - Headline (alt): AI that turns visitors into buyers, and every order into a bigger one.

## S04 · The unseen problem (A only; the Content reviewer may cut it, UNPROVEN)

- Headline: Shoppers can leave without explanation.
- Body: A store can have shoppers and still lose them for reasons that are hard to see. That is what the scan is for.
- CTA label: none
- Alt text: none (no image)
- Visual note: a half-screen statement band, text only.
- Pain source (Step 07, interim): none as a finding. Framing only; nearest are A6 (S8, S9) and the "without explanations" language list (S6, S11, S12, S20).
- Words from the audience: "without explanation" echoes the VoC language list (bans and holds described "without explanations", S6, S11, S12, S20; interim, not a quote and about platforms, not shoppers; ASSUMPTION that the echo fits).

## S05 · Scan (A only)

- Headline: CR Scan AI shows you what it finds.
- Body: It scans your store and lists what may be stopping shoppers.
- CTA label: none
- Alt text, Illustration 1: Illustration of a scan result: a card listing what the scan found on a store.
- Visual label: Illustration
- Pain source (Step 07, interim): A6 (S8, S9), partial; the section describes the feature and does not state the pain.
- Visual note: the full scan card with generic labels, no number, no store domain; target of the hero's "Explore CR Scan AI". NEEDS ILLUSTRATION.

## S06 · Fix (A only)

- Headline: Then it builds a proposed fix.
- Body: For what it found, CR Scan AI builds a proposed fix.
- CTA label: none
- Alt text, Illustration 2: Illustration of one proposed fix shown on a card.
- Visual label: Illustration
- Pain source (Step 07, interim): A6 (S8, S9), partial; trust condition: see section S07.
- Visual note: one proposed fix on one card; no number; do not show what changes inside the store. NEEDS ILLUSTRATION.

---

# Part 3 · P01·B-only sections (One store, with AI on top)

## S10 · Hero B (B only)

- Headline: ShopBase 2.0: one store platform, with AI that finds what stops shoppers and builds the fix.
- Support: On your store, CR Scan AI finds what stops shoppers and builds a proposed fix. You approve every change.
- CTA label (primary): Get started for free
- CTA label (secondary): Explore CR Scan AI (on-page anchor to S12; drop it if S11 grows)
- Alt text, hero illustration: Illustration of a store page with a scan card on top of it.
- Visual label: Illustration
- Visual note: one store with the scan card on top; if S11 is confirmed, only confirmed part names may sit as small labels. No number, no real domain. NEEDS ILLUSTRATION.
- Words from the audience: none.
- Pain source (Step 07, interim): A6 (S8, S9), partial, message driver only; "one" rests on the one-product decision, not on a pain. Trust condition: see section S07.

> ALTERNATE — needs Gate 5 sign-off (the screenshot's outcome headline; unproven outcome claim):
> - Headline (alt): AI that turns visitors into buyers, and every order into a bigger one.

## S11 · One product: the parts list (B only, CONDITIONAL)

Default: NOT BUILT. P01·B has 7 sections and the "one product" statement stays only in S10. The copy below exists only so it can be used the moment the user confirms parts.

> CONDITIONAL — do not publish unless confirmed (the user must say which parts ship in ShopBase 2.0; default: section not built, empty):
> - Headline: One product for running a store.
> - Box labels (only confirmed parts; at most 4 boxes): Store · Catalog · Payments · Fulfillment · Support, each `[NEEDS DATA: ships in 2.0, yes or no]`
> - Box descriptions: `[NEEDS DATA: one plain sentence per confirmed part, up to 12 words; no speed, cost, reliability or "built in" claim]`
> - Alt text: none or `[NEEDS DATA]` if a parts visual is supplied
> - Visual note: confirmed names as plain labels or boxes; no old brand names.

## S12 · Scan and fix (B only)

- Headline: A scan, then a proposed fix.
- Body: On your store, CR Scan AI finds what may be stopping shoppers. For what it found, it builds a proposed fix.
- CTA label: none
- Alt text, illustration: Illustration of a finding and its proposed fix shown on a store.
- Visual label: Illustration
- Pain source (Step 07, interim): A6 (S8, S9), partial; message driver only.
- Visual note: the finding and its proposed fix on a store, same illustration set as A's S05 and S06 (one image or two is the user's call); no number. NEEDS ILLUSTRATION. Target of the hero secondary button.

---

## Microcopy & legal

- Primary button label everywhere: Get started for free (decorative arrow icon, aria-hidden).
- Secondary button (hero only): Explore CR Scan AI.
- Login label: Login.
- Skip link: Skip to main content.
- Menu button (mobile): Open menu / Close menu.
- Illustration label (visible next to every demo image): Illustration.
- Button states: default, hover, focus-visible, pressed; no loading or error state needed (plain links to sign-up; the old email-first form is not carried, so no form labels, errors or empty states exist on this page).
- Footer legal link labels: Terms of service · Privacy policy · ShopBase Payments terms · Marketplace payments terms (SUSPECTED, user confirms).
- Cookie and consent wording: `[NEEDS LEGAL TEXT]` (the legal owner supplies it; none is invented here).
- Copyright and legal entity line: the S02 placeholder `[NEEDS DATA: legal entity name and year]` (one item, not two).

## Measured checks

Script: `/private/tmp/claude-501/-Users-nguyentoan-Documents-SB-v2-LD/fb8c2ff0-4f7d-46ed-a2f8-aeb17aa0cde3/scratchpad/step14_check.py` (run with `python3 -I` on this file; skips fenced CONDITIONAL / ALTERNATE blocks).

| Field | Words | Max (brief) |
|---|---|---|
| S03 Headline / Support | 13 / 16 | 16 / 30 |
| S04 Headline / Body | 5 / 23 | 12 / 25 |
| S05 Headline / Body | 8 / 11 | 10 / 25 |
| S06 Headline / Body | 6 / 11 | 10 / 25 |
| S07 Headline / Body / Caption | 5 / 5 / 4 | 10 / 25 / 4 |
| S08 Headline / Body (A and B) | 8 / 6 (17 in A if the conditional link line is confirmed) | 10 / 25 |
| S09 Headline / Support A | 4 / 5 | 8 / 15 |
| S10 Headline / Support | 16 / 19 | 16 / 30 |
| S12 Headline / Body | 6 / 21 | 10 / 30 |

Result: over = 0. S11 (conditional) not counted. S01 and S02 are labels only. Recounted in Step 15 after the review edits by `/private/tmp/claude-501/-Users-nguyentoan-Documents-SB-v2-LD/fb8c2ff0-4f7d-46ed-a2f8-aeb17aa0cde3/scratchpad/step15_review.py` (`python3 -I`); its output per round is summarised in the Review log.

SEO lengths (characters, after Step 15 edits): Variant A title 47 (max 60), meta 123 (max 155). Variant B title 48, meta 132.

Banned-term scan of non-fenced text (re-run in Step 15 on copy fields only): 0 hits in copy lines for "stitch", "#1", "fastest", "all-in-one", "automatic", Vietnam, "%", digits other than the name "ShopBase 2.0". The few hits ("built in", "best", "undo", "DMCA", PrintBase, PlusBase, "nothing changes") are inside notes that say the term is not used or not drawn.

## Placeholders

| # | Placeholder | Where |
|---|---|---|
| 1 | NEEDS ILLUSTRATION 1 to 4, the B hero and S12 illustrations, and the optional S11 parts visual (data items 1 to 7) | S03, S05, S06, S07, S08, S10, S12, S11 |
| 2 | UNPROVEN: confirmation of "You approve every change", including for every AOV AI offer (item 8) | S07, S03, S10, S08 A conditional link line (the two meta descriptions no longer carry it) |
| 3 | UNPROVEN: proof of what CR Scan AI and AOV AI do (item 9) | S03 to S08, S10, S12 |
| 4 | UNPROVEN: accept "aimed at order value" or sign off "raise" (item 10); confirm the expansion "average order value" | S08 |
| 5 | UNPROVEN: Content reviewer decision on the outcome headline (item 11) | S03, S10 |
| 6 | UNPROVEN: confirm S04 sentence or cut it (item 12) | S04 |
| 7 | NEEDS DATA: parts that ship, "built in" truth, box descriptions, parts visual alt text (item 13) | S11 |
| 8 | NEEDS DATA: Free Launch plan facts (item 14) | S09 B |
| 9 | NEEDS DATA: confirm "one product" line in A (item 15; default yes) | S09 A |
| 10 | NEEDS DATA: K1 Pricing link, footer column set and links K3 to K6 (item 16) | S01, S02 |
| 11 | NEEDS DATA: DMCA link decision (item 17) | S02 |
| 12 | NEEDS DATA: legal entity name and year; NEEDS LEGAL TEXT: cookie and consent | S02, microcopy |
| 13 | NEEDS DATA: how variants go live, title and meta per variant (item 19) | SEO |
| 14 | NEEDS DATA: target keywords or "none" (item 20) | SEO |

Brief item 18 (support route, answers to E1 to E8) has no placeholder on purpose: by default the page says nothing on it.

## Review log

Script for every computed item: `/private/tmp/claude-501/-Users-nguyentoan-Documents-SB-v2-LD/fb8c2ff0-4f7d-46ed-a2f8-aeb17aa0cde3/scratchpad/step15_review.py` (`python3 -I`, run from `/private/tmp/claude-501/x15`, outputs saved there as r1.txt, r2.txt, r3.txt). It computes: section count, words per field, problem-led count, banned-term / number / superlative scan over default (non-fenced) copy fields, fence integrity, term table, pain-source ids against `07-voc.md`, footer labels, placeholder tokens. Both variants are checked separately; fenced CONDITIONAL / ALTERNATE lines are excluded from the default page and checked to stay fenced (6 fence openers, 0 fenced lines found in default copy).

### Computed results (final text)

| Item | P01·A | P01·B (default, S11 not built) |
|---|---|---|
| Sections vs cap 10 | 9 | 7 (8 if S11 is confirmed) |
| Fields over the brief maximum | 0 | 0 |
| Longest fields vs max | S03 Headline 13/16, Support 16/30; S04 Body 23/25; S07 Caption 4/4 | S10 Headline 16/16, Support 19/30; S12 Body 21/30; S07 Caption 4/4 |
| Title / meta characters (max 60 / 155) | 47 / 123 | 48 / 132 |
| Sections leading with a user problem | 1 (S04) | 0 |
| Copy fields scanned | 40 | 34 (the script's 35 wrongly included A's S09 line "ShopBase 2.0 is one product."; corrected at final check) |
| Banned-term scan (outcome words, comparatives, "only", "built in", stitch, Free Launch, undo/rollback, nothing changes, DMCA/trademark, old brands, Vietnam, automatic, %, "-est" superlatives) | 0 hits | 0 hits |
| "price" scan | 1 hit: S01 nav label "Pricing" (a link label for K1, `[NEEDS DATA]`; not a price or fee claim; dropped if K1 is not confirmed) | same |
| Digits in copy fields | 0 other than the name "ShopBase 2.0" (4 uses) | 0 other than "ShopBase 2.0" (5 uses) |
| "You approve every change" | S03 Support, S07 Caption (2) | S10 Support, S07 Caption (2) |
| Primary CTA label | "Get started for free" only | same |

### Term-consistency table (default copy fields; counts A / B)

| Thing | Names found (count A / B) | Verdict |
|---|---|---|
| The scan tool | "CR Scan AI" 6 / 5; bare "CR Scan" 0 / 0; plain-word "the scan / a scan / scans" 6 / 2, alt text included (the script's 12 / 6 also counted the "Scan" inside "CR Scan AI") | one name; the plain-word form is the brief's rule (name once, then say what it does); kept |
| The offers tool | "AOV AI" 1 / 1; bare "AOV" 1 / 1 (only inside "AOV stands for average order value") | one name |
| The product | "ShopBase 2.0" 4 / 5; bare "ShopBase" 2 / 2 (logo alt text, footer legal labels only) | one name |
| The product, as a noun | A: "one product" (S09); B: "one store platform" (S10 and meta); each variant uses one noun, but the two differ. "Product" rests on a user decision; "store platform" is Claude's category word | kept, flagged (risk 4) |
| Where it works | "store / stores" 7 / 8, plus the footer label "App Store" in both; "shop / site / website" 0 / 0 | one name |
| The people who leave | "shoppers" 8 / 5; "visitors / buyers / customers" 0 / 0 (was 1 in S04 body) | unified in round 1 |
| The reader | "you / your" 9 / 6; "seller" 0 / 0; "merchant" 0 / 0 | one voice; "seller" appears only in notes and the fenced screenshot lines, not in default copy |
| What the scan gives | "proposed fix" 5 / 5; "the fix" 2 / 2 (hero headline and H1, the brief's reference phrase) | unified in round 1 except the two hero headlines (risk 5) |
| The generic approval step | "proposal" 1 / 1 (S07 headline); "proposes" 1 / 1 (S07 body, was "suggests"); "recommends" 1 / 1 (S08, the screenshot verb for AOV AI); "change" 2 / 2 (S07 caption "every change", S07 alt text "a proposed change") | S07 verb aligned in round 1; "recommends" kept because it is the screenshot's word for offers; "change" kept as the generic word for a fix or an offer, because S07 covers both tools |
| Generic AI | "the AI" 1 / 1 (S07, covers both tools); "AI that" 3 / 2 (hero) | kept: S07 is shared and approves changes from both tools |
| Sign-up / sign-in | "Get started for free" 5 / 5; "Login" 4 / 4; "Sign in" 0 / 0 | one name each |
| Label of the demo images | "Illustration" 7 / 6 | one name |

### Round 1  (failed items, then changes)

Failed (11):
1. **Claims (N: "claims to avoid" 13).** Both meta descriptions stated "You approve every change" as a fact in a search snippet, which is neither the caption nor the sub-line the brief allows, and said "builds the fix" with no "proposed".
2. **Consistent terms.** S04 body said "visitors", the rest of the page "shoppers".
3. **Consistent terms.** One act had four verbs: S07 "suggests", S07 "proposal", S06 and S12 "proposed fix", S08 "recommends".
4. **Consistent terms.** Hero sub-lines and meta said "builds the fix", later sections "a proposed fix" (reads as the AI applying the fix before the approval line).
5. **One message / Me-too.** S12 body repeated S10's sub-line almost word for word ("On your store, CR Scan AI finds what stops shoppers and builds a proposed fix").
6. **Pain sources.** The copy file named no Step 07 id for the pains behind S03, S05, S06, S10, S12; S07 cited "AI-1" as if it were a Step 07 id, but `07-voc.md` has no such id (it is a Step 09/13 label for the section "AI that changes the store").
7. **Must-keep (B/C).** The brief's S02 list includes the K6 app-store links; the footer labels left them out.
8. **Copy quality.** S08 alt text said "with no numbers" (an instruction, not a description).
9. **Type C: existing customer.** FAIL, not fixable here (see the Type C paragraph below).
10. **Me-too test.** FAIL, not fixable by wording (see the Me-too paragraph below).
11. **Hero check.** "For whom" is implied only ("your store"), and "see the product working" depends on illustrations that do not exist (NEEDS ILLUSTRATION). Both are by the brief's default; reported, not changed.

Changes (items 1 to 8): meta A now "...finds what stops shoppers on your store and builds a proposed fix. Get started for free." (123 characters), meta B likewise (132); "You approve every change" kept only in hero sub-line and S07 caption (decision: drop it from the two meta descriptions; justification is in Assumption 3; the brief allows the sentence only as a caption or sub-line sentence, so dropping it from the meta is what the rule asks; it is also safer because a snippet cannot carry the Illustration label or the surrounding context, and the sentence is still on the page). S04 body "visitors" to "shoppers". S07 body "The AI suggests." to "The AI proposes." S03 and S10 sub-lines "builds the fix" to "builds a proposed fix" (headlines keep the brief's reference phrase). S12 body rewritten: "On your store, CR Scan AI finds what may be stopping shoppers. For what it found, it builds a proposed fix." (21 words, still has "on your store", "finds", "builds ... proposed fix"). A "Pain source (Step 07, interim)" line added to S03, S04, S05, S06, S07, S10, S12 with persona rank and source ids (A6: S8, S9; B5: S14; section "AI that changes the store": S7, S22, S23; S04 echo: S6, S11, S12, S20); "AI-1" now explained as not an id. Footer labels "App Store" and "Google Play" added (SUSPECTED, K6). S08 alt text now "Illustration of one offer shown on a card." The statements elsewhere in the file that these edits made stale were not all updated in round 1; round 2 found and fixed them (see below).

What remains after round 1: items 9, 10, 11 (open by design), plus whatever round 2 finds.

### Round 2  (failed items, then changes)

Re-ran the full checklist and the script on the fixed text, both variants. Computed items all pass (table above). New failures found: **5**, all stale statements created by the round 1 edits, not copy problems: (a) Measured-checks table still showed old word counts for S03, S10, S12; (b) SEO lengths still said A 142 / B 151; (c) Assumption 3 still described the meta sentence and "suggests"; (d) placeholder row 2 still listed "meta A/B"; (e) the closing checklist line still quoted 142 / 151. All five fixed (and a sixth wording line in the "How to read" note updated to say "plus 'proposed' and 'scan' from the brief"). Items 9, 10, 11 are carried unchanged (see below). A third run of the script (r3.txt) is byte-identical to the round 2 output, and a text search finds no remaining "suggests", "142", "151" or "meta A/B".

Round 2 found no new copy failure after those fixes. It did not find "nothing": the stale-statement fixes were needed, and three items remain open because only the user can close them.

Final check (independent script `/private/tmp/claude-501/-Users-nguyentoan-Documents-SB-v2-LD/fb8c2ff0-4f7d-46ed-a2f8-aeb17aa0cde3/scratchpad/final15_check.py`, `python3 -I`, run outside the project): section counts, every word count, SEO lengths (A 47 / 123, B 48 / 132), the banned-term and digit scan, the fences and the pain-source ids all reproduce. No copy line was changed. Corrected in the log only: variant B counts (the review script read A's S09 line into B: fields 34, "ShopBase 2.0" 5); the plain-word "scan" count (6 / 2; the script also counted "CR Scan AI"); "store" counts (the footer label "App Store" was counted); "change" added to the term table; the round 1 note on the meta sentence (the brief allows it only as caption or sub-line, so dropping it is required, not optional); the round 1 / round 2 contradiction on stale statements; B's me-too check now covers three headlines after the hero (adds S07); the hero sub-line note (no longer the screenshot sentence word for word); "see S07" in pain-source lines now reads "see section S07" so it is not mistaken for source S7.

### Checklist result, per item (final text)

| Checklist item | P01·A | P01·B |
|---|---|---|
| One main message per section | pass. S09 pairs a headline with the optional "one product" line; read as one message (start) | pass |
| Hero: for whom, what we solve, see it working, next step | for whom: implied ("your store"; the brief's default is not to name the audience), partial. What we solve: yes ("finds what stops shoppers and builds the fix"). See it working: a small scan card under the buttons, NEEDS ILLUSTRATION, so not yet. Next step: yes, two buttons | for whom: implied, partial. What we solve: yes. See it working: one store with the scan card on top, NEEDS ILLUSTRATION, not yet. Next step: yes |
| USP through the page, not drowned by problem copy | pass. CR Scan AI or AOV AI is named in S03, S05, S06, S08; the one problem-led section is S04 (1, justified in the brief, may be cut) | pass. 0 problem-led; S10, S12, S08 carry the USP |
| Every pain used has a Step 07 source | pass: ids A6, B5 and the "AI that changes the store" section, with sources S8, S9, S14, S7, S22, S23, S6, S11, S12, S20, all present in the `07-voc.md` source table (checked by script); interim, none quoted | pass, same ids |
| No reference-site proof, no unsourced number, testimonial or logo | pass | pass |
| Section count and word caps (measured) | pass: 9 of 10; 0 fields over | pass: 7 of 10; 0 fields over |
| No avoided claim, no unverifiable superlative | pass (scan above); "Pricing" nav label noted | pass |
| B/C must-keep still present | present as SUSPECTED: sign-up with K12 parameters, Login, legal labels, K6 help/blog/developers/updates/templates/status/app-store labels, K1 Pricing as `[NEEDS DATA]`; deliberately not carried: K15 old title/meta, K2, K3/K4 pages, K13 Facebook links, DMCA (data item 17) | same |
| C: existing customer can tell what stays and new | see paragraph below: not met | see paragraph below: not met |
| Me-too test | see paragraph below | see paragraph below |
| Consistent terms | pass (table above); two noted residuals: "the fix" vs "a proposed fix" in the hero headlines, and "one product" (A) vs "one store platform" (B) | same |

**Type C check (what a merchant can and cannot tell from the page alone).** The page is silent on migration by the Step 09 default and nothing was added. A current merchant can tell: the product is now named "ShopBase 2.0"; its headline feature is AI (CR Scan AI, AOV AI) with an approval sentence; a Login link still exists (S01); the old tabs, brand names, Book a demo and "Print on demand / Dropshipping" are gone (by absence only, nothing says this is on purpose); in A the closing line says "ShopBase 2.0 is one product", in B the hero says "one store platform". A current merchant cannot tell: whether their store and apps keep working (E1), whether their plan or price changes (E2), what became of PrintBase / PlusBase (E3), whether the AI is included or extra (E4), what "one product" means for the old services (E6; A's S09 and B's S10 may even prompt the question), where to get help (E7), or what is removed (E8). No reassurance was added because none is confirmed. Item stays open until the user answers E1 to E8 (data item 18) or accepts the silence.

**Me-too test (hero and first three headlines, read as if on a competitor's site).**
- P01·A. Hero "AI that finds what stops shoppers on your store and builds the fix." Against Shopify "Spot opportunities for growth and automate tedious tasks with Sidekick" and BigCommerce "an AI assistant that ... surfaces insights, and handles operations for you": it would fit on either site with no edit. The scan-then-fix wording is more specific than "Your very own commerce AI", but the difference is wording only and unproven; the one line no competitor homepage carries (per `06-positioning.md`, no "approve" on five pages) is "You approve every change", which sits in the sub-line. Headlines 2 and 3: S04 "Shoppers can leave without explanation." would fit any competitor (the section is flagged and cuttable); S05 "CR Scan AI shows you what it finds." and S06 "Then it builds a proposed fix." are anchored only by the tool name and the word "proposed". Verdict: yes, A's hero and S04 would fit a competitor; no rewrite, because no honest differentiator exists beyond the tool names and the approval sentence, and the hard rules bar inventing or moving them.
- P01·B. Hero "ShopBase 2.0: one store platform, with AI that finds what stops shoppers and builds the fix." The first half is the same shape as Wix "one AI-powered eCommerce platform" and Zendrop "a free AI-built store"; it would fit on Wix with the name swapped. The second half is the same promise as A and shares its weakness. The next three headlines (S12 "A scan, then a proposed fix.", S08 "AOV AI recommends offers aimed at order value.", S07 "A proposal, then your decision."): S12 is anchored by "proposed"; S08 is close to Wix "Increase your average order value with related products sections" once the tool name is removed, softened but not different in kind; S07 is the one headline whose idea (the seller decides) appears on none of the five competitor homepages, but it is unproven as product behaviour (data item 8). Verdict: yes for the hero's front half and for S08; reordering the headline to lead with the scan would only make B read like A (the user chose two distinct narratives), so no rewrite. The only honest difference is wording, and it stays unproven.

Note on repetition: in both heroes the sub-line restates the headline ("finds what stops shoppers and builds a proposed fix"); the sub-line adds the tool name and the approval sentence only. Kept because the brief bases the sub-line on the screenshot sentence. Since Step 15 the sub-line is no longer that sentence word for word: "builds the fix" became "builds a proposed fix" (term unification; it adds no claim beyond "You approve every change", which follows it). If the reviewer wants the exact screenshot sentence back, the cost is the "the fix" / "proposed fix" mismatch inside the hero; the reviewer may also want a different sub-line.

### For the Content reviewer

Riskiest items, with the exact lines:
1. **Hero headlines and the me-too finding.** A: "AI that finds what stops shoppers on your store and builds the fix." B: "ShopBase 2.0: one store platform, with AI that finds what stops shoppers and builds the fix." Both would fit a competitor; the only difference is wording and no product proof exists. Also decide the fenced ALTERNATE headline "AI that turns visitors into buyers, and every order into a bigger one." (outcome claim, "every" is an absolute).
2. **The approval sentence, stated as fact:** "You approve every change" (S03 Support, S10 Support, S07 Caption; UNPROVEN as product behaviour for every CR Scan AI fix and every AOV AI offer). Also S07 "A proposal, then your decision." / "The AI proposes. You decide." (nearest wording to an approval flow; no detail of how it works is given). It was removed from both meta descriptions in Step 15; confirm that decision.
3. **S04, the only problem-led section (A):** "Shoppers can leave without explanation." / "A store can have shoppers and still lose them for reasons that are hard to see. That is what the scan is for." No source; the echo of "without explanations" comes from complaints about platforms, not shoppers. Cut it or confirm it.
4. **"One product" versus "one store platform", and the existing merchant:** A S09 "ShopBase 2.0 is one product."; B S10 headline "one store platform". Two names for the same decision-backed fact, "store platform" is Claude's word, and the page tells an existing merchant nothing about migration (E1 to E8 unanswered).
5. **S08 "AOV AI recommends offers aimed at order value." / "AOV stands for average order value."** No pain behind it, no description of what an offer is; the softening of "raise order value" (fenced ALTERNATE "AOV AI recommends offers that raise order value.") and the expansion of AOV both await a decision. Also the word choice "builds the fix" (hero headlines, the screenshot's words) versus "a proposed fix" (hero sub-lines since Step 15, S06, S12, both meta descriptions): the hero sub-lines no longer repeat the screenshot sentence word for word.

Open placeholders the user must resolve, grouped by what they block:
- **Blocks Step 18 / the demo (images do not exist):** NEEDS ILLUSTRATION 1 scan card (S03 small crop, S05); 2 proposed fix card (S06); 3 approval step (S07); 4 AOV AI offer card, no number, no specific offer type (S08); 5 B hero, store with scan card (S10); 6 B scan-and-fix image(s) (S12); 7 optional parts labels or visual (S11 / S10).
- **Blocks wording sign-off (UNPROVEN, Gate 5):** confirm "You approve every change" for every fix and offer, and whether undo exists (item 8; also the S08 A conditional link line); proof of what CR Scan AI and AOV AI do (item 9); accept "aimed at order value" or sign off "raise", and the AOV expansion (item 10); outcome headline or descriptive headlines (item 11); keep or cut S04 (item 12).
- **Blocks B's S11 and S09 B:** NEEDS DATA which parts ship (store, catalog, payments, fulfillment, support), whether "built in" is true, box descriptions, parts visual alt text (item 13; S11 stays unbuilt until then); Free Launch plan facts (item 14; S09 B line stays empty).
- **Blocks S09 A:** confirm "ShopBase 2.0 is one product." (item 15, default yes).
- **Blocks Step 21 (header, footer, head):** NEEDS DATA K1 Pricing link and nav; footer column set and links K3 to K6 including the new App Store / Google Play labels (item 16); DMCA footer link decision with the legal owner (item 17); legal entity name and year; NEEDS LEGAL TEXT cookie and consent wording; how the variants go live, title and meta per variant (item 19); target keywords or "none" (item 20).
- **Blocks any merchant-facing line (type C):** E1 to E8 answers and a reason for the change (item 18); until then the page stays silent.

## Assumptions

1. Title and meta are DRAFT and built only from the hero promise in `11` (flagged, not approved until Gate 5); "store platform" is Claude's category word (Step 09). Title A says "finds", not "fixes": "fixes" would read as the AI applying changes itself.
2. "CR" and "AOV": no input explains "CR"; copy therefore never expands it and explains the tool by what it does ("finds what stops shoppers"). AOV is expanded as "average order value" in S08 (standard meaning, not a product claim); the user should confirm that expansion.
3. S07 body "The AI proposes. You decide." follows the Step 09 register example ("It suggests. You decide.") with the verb aligned to "proposed fix"; it says no more than the screenshot sentence, but it is the nearest wording to an approval claim and stays UNPROVEN until data item 8. Step 15 removed "You approve every change" from both meta descriptions: a search snippet is neither the caption nor the sub-line the brief allows, it would state an unconfirmed behaviour as a fact (Step 09 claim 13) to people who see no illustration, and the sentence stays on the page itself (hero sub-line and S07 caption). The body now says "The AI proposes. You decide." (was "suggests"), to match "proposed fix" and "proposal".
4. A's S08 link line is fenced CONDITIONAL (default not shown): it would say that AOV AI offers wait for approval, which no input confirms (data item 8).
5. S09 headline "Start with ShopBase 2.0." and the A line "ShopBase 2.0 is one product." rest on the Decisions log (one independent product).
6. S06, S12, both hero sub-lines and both meta descriptions say "proposed fix" because the brief requires "proposed" in S06; it is Claude's reading of the screenshot and is UNPROVEN. The two hero headlines keep the screenshot form "builds the fix" (brief reference phrase), so "the fix" and "a proposed fix" both occur; the Content reviewer may choose.
7. Footer labels, column titles and nav items are SUSPECTED defaults from the audit.
8. VoC language use is minimal (one echo, S04) because the interim VoC is unverified and the hero describes capability.
9. Variant-shared wording (S07, S08, S09, S01, S02) is identical in both variants except the labelled lines.

## Check before handing back

- [x] Every S## has copy (S11 conditional, default not built); word counts within the brief (measured, 0 over).
- [x] No invented numbers, testimonials, logos or customer names; placeholders visible (digit scan of copy lines: none).
- [x] Title and meta lengths within limits (measured in Step 15: A 47/123, B 48/132).
- [ ] B/C must-keep keywords and URLs present: PARTIAL. The user named none; K12 referral parameters and K1 are kept as SUSPECTED; old keywords deliberately dropped (K15), user decides.
- [ ] Content reviewer sign-off (Gate 5), proof of AI claims, rendered fit: NOT MET / NOT RUN (Step 15).
