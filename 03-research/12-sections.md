# 12 · Sitemap & sections

Project: ShopBase website redesign · type **C · Rebrand** · page **P01 Home** in **two variants (P01·A and P01·B)** · files in English · Gates 0 to 4 `APPROVED` (`_progress.md`; Gate 4, 2026-10-24: the user chose both options, "Làm cả 2 đi").
Inputs read: `CLAUDE.md`, `_prompts/README.md`, `_prompts/12-sections.md`, `_progress.md` (whole file, with the Decisions log), `03-research/11-narrative-options.md`, `01-strategy/01-strategy-pack.md`, `01-strategy/brief.md`, `03-research/03-brief-analysis.md`, `03-research/04-audit.md`, `03-research/05-measurement.md`, `03-research/06-positioning.md` (via the pack, 08 and 11, not re-read in full), `03-research/07-voc.md` (interim), `03-research/08-reference-analysis.md`, `04-brand/09-messaging.md`, `04-brand/10-identity.md`.

> **Read this first.**
> - This file is the sitemap and the section list. It writes **no page copy** (Step 14). Section names are working labels, not headlines.
> - **Both options are built.** P01·A follows Option A "Find, fix, approve"; P01·B follows Option B "One store, with AI on top". Each variant keeps its own option's message order and hero promise from `11-narrative-options.md`. A variant uses something from the other option **only** through a section marked SHARED.
> - This replaces the base prompt's check-list line "follows the chosen option, not the other one" (user decision at Gate 4). One file, two variant parts; no `-v2` or `-final` file.
> - **Nothing here is proven.** Every AI description is `UNPROVEN`; no result number; outcome wording stays qualitative and for the Content reviewer to check at Gate 5. VoC pain ids (A1 to A7, B1 to B7, AI-1) are **INTERIM** (`07-voc.md`).
> - **Not in any section, by earlier decisions:** a control or approval block (the sentence "You approve every change" is only a caption under the approval illustration, UNPROVEN as product behaviour), "built in" / "No apps to stitch together" / "Free Launch plan" as facts, DMCA or restricted products, comparisons, PrintBase / PlusBase / "Print on demand" tabs, result numbers, a Vietnam-specific block.

## Code scheme (read this before the tables)

Codes are assigned once and are permanent (`_prompts/README.md`). A code is an **identifier, not a position**: page order is given per variant in the section lists.

| Code | Meaning | Rule |
|---|---|---|
| `P01` | The page Home | The only page in scope. `P01·A` and `P01·B` are two **variants** of this one page, not two pages |
| `S##` | A section | **One S## per section.** A section used identically in both variants keeps the same S## and is marked **SHARED**. A section that exists in only one variant has its own S## and is marked **A only** or **B only**. If a SHARED section ever has to differ between variants, the variant that changes takes a **new** S## (the old code is never reused or renumbered) |
| `FL##` | A flow (arrive, read, click) | One per persona per variant, plus entry-source and secondary-CTA flows |
| `OLD-##` | A section of today's live page (from `04-audit.md`) | Not a new code; used in the keep / rework / drop table |
| `CONDITIONAL` | A section that exists only if the user confirms the claim it rests on | Listed with and without it (see "Section list per variant") |

### Code registry (checked by code, see Cap check)

`Pos` = position on the page, top to bottom, inside that variant (`-` = not in that variant). The B column counts S11 (the CONDITIONAL section); without it, S12, S08, S07, S09 and S02 move up one place.

**What "used identically" means for a SHARED code** (review addition, so the rule can be checked): same focal point, same purpose, same structure and same illustration in both variants. Position may differ. One optional line slot whose wording differs by variant (S08's link line in A, S09's optional line) is copy for Step 14, not structure; it is stated in the rows. If a SHARED section needs a different focal point, illustration or structure in one variant, that variant takes the next free code (S13 onward).

| S## | Name | Pos in P01·A | Pos in P01·B | Status |
|---|---|---|---|---|
| S01 | Header | 1 | 1 | SHARED |
| S02 | Footer | 9 | 8 | SHARED |
| S03 | Hero A: AI that finds and fixes | 2 | - | A only |
| S04 | The unseen problem | 3 | - | A only |
| S05 | Scan | 4 | - | A only |
| S06 | Fix | 5 | - | A only |
| S07 | Approve | 6 | 6 | SHARED |
| S08 | AOV AI | 7 | 5 | SHARED |
| S09 | Closing call to action | 8 | 7 | SHARED |
| S10 | Hero B: one store, with AI | - | 2 | B only |
| S11 | One product: the parts list | - | 3 | B only, CONDITIONAL |
| S12 | Scan and fix | - | 4 | B only |

### Message order to section map (proves each variant follows its own option)

| Option A beat (from 11) | Section | Option B beat (from 11) | Section |
|---|---|---|---|
| 1 Promise | S03 | 1 Promise | S10 |
| 2 The unseen problem | S04 | 2 One product | S11 (CONDITIONAL) |
| 3 Scan | S05 | 3 AI layer: scan and fix | S12 |
| 4 Fix | S06 | 4 AI layer: order value | S08 |
| 5 Approve | S07 | 5 You approve | S07 |
| 6 Order value | S08 | 6 Start | S09 |
| 7 Start | S09 | | |

S01 Header and S02 Footer are page chrome, not beats; both variants have them (SHARED). Where a SHARED section sits differs by variant: S08 comes after S07 in A and before S07 in B, because that is each option's own order.

## Caps

Set with the user at this step. The user has given no view, so the prompt's defaults are proposed. All are `ASSUMPTION` until the user says otherwise; the lead records them in `_progress.md` (this step may not edit it).

| Cap | Proposed | Basis | Status |
|---|---|---|---|
| Sections per page (per variant) | **10**, counting Header and Footer | Prompt default. Counting the chrome is the stricter reading (the audit counts 12 blocks including header and footer) | `ASSUMPTION` |
| Page length, desktop (1440) | **9,000 px** | Prompt default | `ASSUMPTION` |
| Page length, mobile (375) | **16,000 px** | My own rule: desktop cap x 1.8, rounded. Reason: two-column blocks become one column and headlines wrap to more lines, so a responsive page is longer on a phone. The factor 1.8 is a guess, not a measurement; nothing is rendered yet. The frame lock (responsive 1440 + 375) comes from `03-brief-analysis.md`, still "to confirm" | `ASSUMPTION` |
| Boxes (cards or panels) per section | **4** | Prompt default. Navigation items and footer link columns are not counted as boxes (`ASSUMPTION`) | `ASSUMPTION` |
| CTAs per section | **1 primary** | Prompt default; N5. **One proposed exception:** the hero may also carry the brief's one secondary button "Explore CR Scan AI" (`brief.md` §1, §3, both buttons are the user's). Counted separately below as `[S]`. A plain "Login" text link in the header is navigation, not a CTA | `ASSUMPTION` |

## Pages

| P## | Page | Variants | Job | Who links to it | Links to | Primary CTA | Dead ends |
|---|---|---|---|---|---|---|---|
| P01 | Home · `https://www.shopbase.com/` | P01·A, P01·B | Present ShopBase 2.0 to experienced sellers and move them to sign up (`brief.md` §1) | Inbound sources **unknown, no analytics** (`05-measurement.md` Baseline). Not verified: other shopbase.com pages through the logo and header | `accounts.shopbase.com/sign-up` (primary), `accounts.shopbase.com/sign-in`, `/pricing` (if kept, K1), on-page anchor (secondary CTA target: S05 in A, S12 in B), footer links (K5, K6 as the user confirms) | "Get started for free" | None on the page itself (every exit is sign-up, sign-in or a footer link). **One risk:** between the hero and the closing section no section carries a primary button; see FL11 and open decision 9 |

Other pages (`/pricing`, `/features/*`, `/about`, legal pages, ...) are outside scope and have no `P##`. They may be linked only as the user confirms (K1 to K6 below).

## Section list per variant

Columns follow the prompt. `CTA` uses `[P]` for the primary button and `[S]` for the secondary button; `none` means no button. Persona codes: **A** dropshipper, **B** POD seller, **M** existing merchant. Pain ids are interim; "none" is stated where no pain matches. All claims stay `UNPROVEN`.

### Section list P01·A (Find, fix, approve)

| S## | Name | Purpose | The ONE message (focal point) | Persona served | Pain point it answers (Step 07, interim) | CTA |
|---|---|---|---|---|---|---|
| S01 | Header (SHARED) | Orient; give the way in (sign up) and the way back in (log in) | ShopBase, and where to start or sign in | A, B, M | none (navigation). For M it answers nothing in E1 to E8 | [P] Get started for free (plus a Login text link, not a CTA) |
| S03 | Hero A (A only) | State the promise; show the thing first | ShopBase 2.0 has AI that finds what stops shoppers and builds the fix (illustration 1 under the button, labelled "Illustration") | A, B, M | A6 partial. Hero sub-line also touches B5 and AI-1 as a trust condition | [P] Get started for free · [S] Explore CR Scan AI |
| S04 | The unseen problem (A only) | Frame why a scan is needed | A store can have visitors and still lose them for reasons the dashboard does not show (framing sentence only; `ASSUMPTION`, `11` Assumption 4; the Content reviewer may cut it) | A, B | A6 as framing only. It is not a VoC finding | none |
| S05 | Scan (A only) | Show step 1 of the loop | CR Scan AI scans the store and lists what it found (illustration; the secondary CTA lands here) | A, B | A6 partial | none |
| S06 | Fix (A only) | Show step 2 of the loop | It builds a proposed fix for what it found (illustration; whether there is one fix per finding is stated in no input) | A, B | A6 partial | none |
| S07 | Approve (SHARED) | Show the approval step: who decides | The seller approves a proposed change before it goes live: "You approve every change" is the caption under the approval illustration, not a block (UNPROVEN as product behaviour) | A, B, M | B5 consent part and AI-1 (changes without asking; the "no human to fix it" fear is not answered). For M it touches E5, only if the behaviour is confirmed | none |
| S08 | AOV AI (SHARED) | Show the second AI tool | AOV AI recommends offers aimed at order value (softened wording, awaits the user's accept or reject) | A, B | **None: no matching VoC pain** (`09-messaging.md` Support 2). Not tied to A6, B1 or any other pain | none |
| S09 | Closing call to action (SHARED) | Last push to the same action | Same primary button as the hero. One optional line slot, never a separate section (copy, Step 14): in A the "one product" line (known fact; decision 7, default yes); in B the Free Launch plan line only if the user confirms it (decision 5, default empty) | A, B, M | none | [P] Get started for free |
| S02 | Footer (SHARED) | Navigate, legal, help | Legal and help links stay reachable | A, B, M | none | none |

In A, S07 is step 3 of the loop and S08 follows it, so S08 may carry one link line back to the loop ("the same shape: proposal, then approval", `11` beat 6). That line is copy and order-dependent; S08's focal point, purpose and illustration are the same as in B.

### Section list P01·B (One store, with AI on top)

Rows tagged `CONDITIONAL` in the Name column exist only if the user confirms the claim they rest on (decision 5). The "Free Launch plan" beat is **not a separate section**: it is one optional line inside S09 (as in `11`, beat 6), marked CONDITIONAL there as a line, not as a row. If the user wants it to be its own section, it takes the next free S## and adds one section (B would still be under the cap) and plan facts are needed first (decision 5).

| S## | Name | Purpose | The ONE message (focal point) | Persona served | Pain point it answers (Step 07, interim) | CTA |
|---|---|---|---|---|---|---|
| S01 | Header (SHARED) | Orient; give the way in (sign up) and the way back in (log in) | ShopBase, and where to start or sign in | A, B, M | none (navigation). For M it answers nothing in E1 to E8 | [P] Get started for free (plus a Login text link, not a CTA) |
| S10 | Hero B (B only) | State the promise as a store platform with AI on top | ShopBase 2.0: one store platform, with AI that finds what stops shoppers and builds the fix (one illustration: a store with the scan card on it, labelled "Illustration") | A, B, M | A6 partial. "One" rests on the user's one-product decision; it is not a coverage claim. Hero sub-line also touches B5 and AI-1 as a trust condition (the screenshot sentence only, `11` option B) | [P] Get started for free · [S] Explore CR Scan AI |
| S11 | One product: the parts list (B only, CONDITIONAL) | Say what ShopBase 2.0 is now | ShopBase 2.0 is one independent product for running a store; lists only the parts the user confirms (store, catalog, payments, fulfillment, support: each UNCONFIRMED) | A, B, M | A1 partial and only by `ASSUMPTION`; workload (LEAD-2) weak. Type C need ("what is ShopBase now"), not a VoC pain. For M it partly answers E3 (old brand names gone) and may trigger E6, which the page cannot answer | none |
| S12 | Scan and fix (B only) | Show the AI layer on this store | CR Scan AI finds what stops shoppers on this store and builds the fix (illustration; the secondary CTA lands here) | A, B | A6 partial | none |
| S08 | AOV AI (SHARED) | Show the second AI tool | AOV AI recommends offers aimed at order value (softened wording, awaits the user's accept or reject) | A, B | **None: no matching VoC pain** (`09-messaging.md` Support 2). Not tied to A6, B1 or any other pain | none |
| S07 | Approve (SHARED) | Show the approval step: who decides | The seller approves a proposed change before it goes live: "You approve every change" is the caption under the approval illustration, not a block (UNPROVEN as product behaviour) | A, B, M | B5 consent part and AI-1 (changes without asking; the "no human to fix it" fear is not answered). For M it touches E5, only if the behaviour is confirmed | none |
| S09 | Closing call to action (SHARED) | Last push to the same action | Same primary button as the hero. One optional line slot, never a separate section (copy, Step 14): in A the "one product" line (known fact; decision 7, default yes); in B the Free Launch plan line only if the user confirms it (decision 5, default empty) | A, B, M | none | [P] Get started for free |
| S02 | Footer (SHARED) | Navigate, legal, help | Legal and help links stay reachable | A, B, M | none | none |

**Without the conditional sections (nothing confirmed, the default):** P01·B = S01, S10, S12, S08, S07, S09, S02 (7 sections). It is Option A with a weaker opening (`11`, Cons 1): S11 is dropped, the "one product" statement stays only in the S10 headline, and the existing-merchant "what is ShopBase now" beat is lost. **With S11** (the user confirms at least one part): S01, S10, S11, S12, S08, S07, S09, S02 (8 sections). If only some parts are confirmed, the list keeps only those; with few confirmed it is cheaper to show them as small labels on the S10 illustration (`11` option B, "first thing the reader sees") and drop S11 anyway (decision 5).
**Box cap and S11:** the screenshot names five parts, the box cap is 4. If all five are confirmed they must be merged to 4 boxes (for example store and catalog together) or shown as labels. Not decided here.

### Sections in neither variant (and why)

| Pattern seen at Step 08 | Why it is not in A or B |
|---|---|
| Trust and control block | The user decided (Step 09 Q1) there is no control block until the product behaviour, including undo, is confirmed |
| FAQ | Answers must come from the user (08 pattern table); none supplied |
| Plan cards or pricing entry | No plan facts; pricing stays off Home (brief Q3 default). A "Pricing" link is allowed in the header (K1, to confirm) |
| Stats strip, testimonials, case studies | Numbers and quotes are unconfirmed (audit Q7) and result numbers are barred |
| Integrations or template showcase | Unlabelled dead-brand logos; tiles are dead links (audit OLD-06, OLD-08); neither carries either option's message |
| Merchant "what changes" block | E1 to E8 are unanswered; default: Home says nothing (`09-messaging.md`) |

## Keep / rework / drop (type C)

Decision for the live page's 12 blocks (`04-audit.md`). "Differs" is yes only where A and B take different decisions. Every verdict is a first view on **no analytics** (`ASSUMPTION`).

| OLD | Live section | Decision in P01·A | Decision in P01·B | Differs | Reason | Becomes in A | Becomes in B |
|---|---|---|---|---|---|---|---|
| OLD-01 | Header / navigation | Rework | Rework | no | Nav is tied to the old product split ("Print on demand", "Dropshipping"); two different "Book a demo" items (one is a button that points to sign-in); a second logo file named PlusBase; sign-up labels differ across the page (5 spellings in the audit, header ones included). Proposed nav: logo, Pricing (if confirmed), Login, "Get started for free"; "Book a demo" and the two product items are not carried (decision 3) | S01 | S01 |
| OLD-02 | Hero | Rework (promise replaced) | Rework (promise replaced) | no (the new promise differs per variant) | Whole promise changes; typing headline, video and "all-in-one / app mazes" lines are not carried. The email-first form is **not** carried (the primary CTA is a button); "worth testing, not deciding here" stays open (decision 12) | S03 | S10 |
| OLD-03 | Social proof stats | Drop | Drop | no | The three numbers have no source or date; result-style numbers are barred; nothing supplied. Can return as a new code only if the user sources them (audit Q7) | dropped | dropped |
| OLD-04 | Product tabs (E-commerce brands / Dropshipping / POD) | Drop | Drop (its job of saying what ShopBase is passes to S11 if confirmed) | yes, in what replaces it | Three products by audience contradicts "one independent product"; PrintBase wording must go | dropped | dropped (role partly S11, CONDITIONAL) |
| OLD-05 | Digital products (Creator) | Drop | Drop | no | Outside the personas; present only in the mobile copy of the tab block (inferred, not verified). The URL `/creator` is a suspected must-keep (K4), outside P01 | dropped | dropped |
| OLD-06 | Integrations / partner logo strip | Drop | Drop | no | Unlabelled; includes the dead brands PrintHub and PlusHub; no readable text | dropped | dropped |
| OLD-07 | Feature overview | Drop | Rework into S11 only for the parts the user confirms; otherwise drop | yes | Closest to the unconfirmed coverage claims; A leaves coverage out entirely, B may state only confirmed parts. Links such as "Visit the template store" are not carried | dropped | S11 (CONDITIONAL) or dropped |
| OLD-08 | Template showcase | Drop | Drop | no | 13 dead `href="#"` links; real store domains in visuals not decided; not part of either message. `templates.shopbase.com` stays reachable by a link in S01 or S02 if the user confirms (K6) | dropped | dropped |
| OLD-09 | Testimonials | Drop | Drop | no | No result, date or permission shown; the third quote repeats the old promise and a "handles fulfillment" claim; no replacement supplied (customer stories are barred under the imagery rules) | dropped | dropped |
| OLD-10 | Service commitments | Drop | Drop | no | Guarantee, award and 24/7 claims have no source; the support route is unknown (E7) and Vietnamese support is not promised | dropped | dropped |
| OLD-11 | Closing call to action | Keep (pattern), copy changes | Keep (pattern), copy changes | no | One repeated sign-up action matches the chosen primary CTA | S09 | S09 |
| OLD-12 | Footer | Rework | Rework | no | Remove PrintBase and PlusBase; keep legal and help links (see must-keep table; DMCA link conflict, decision 4) | S02 | S02 |

### Suspected must-keep items: how each survives (all SUSPECTED until the user confirms; "to confirm at Step 21")

The user named no must-keep item (`brief.md` §5). Nothing below is mandatory yet. "Both" means the same handling in P01·A and P01·B. Tags and scripts live in the page `<head>` or inline, not in a section, so they are the same for both variants.

| # | Item (audit) | In P01·A | In P01·B | Status |
|---|---|---|---|---|
| K1 | `/pricing` | Header link in S01 (and optionally S02) | Same | SUSPECTED, to confirm at Step 21 |
| K2 | `/book-a-demo` | Link removed from Home (sign-up is the only CTA); the URL stays live outside P01 | Same | SUSPECTED, to confirm at Step 21 |
| K3 | `/features` and 13 `/features/*` | Footer link group in S02 (set as the user confirms) | Same | SUSPECTED, to confirm at Step 21 |
| K4 | `/about`, `/partners`, `/affiliate`, `/compare`, `/learning-hub`, `/shopbasehero`, `/shopbase-apps`, `/multi-channel` | Footer, as confirmed | Same | SUSPECTED, to confirm at Step 21 |
| K4b | `/dropshipping`, `/print-on-demand`, `/creator` (split out of audit K4 here; not a new audit item) | Not linked from Home (product split, pack Q8); URLs stay outside P01 | Same | SUSPECTED, to confirm at Step 21 |
| K5 | Legal links: terms, privacy, ShopBase Payments terms, Marketplace payments terms | S02 | S02 | SUSPECTED, to confirm at Step 21 |
| K5b | `/dmcareport` (split out of audit K5 here; not a new audit item) | **Conflict:** the user's rule says no DMCA mention on Home, yet the live footer links it. Default: not drawn on Home until the user decides (legal consequence flagged; decision 4) | Same | SUSPECTED, to confirm at Step 21 |
| K6 | `accounts.shopbase.com` sign-up and sign-in; `templates`, `blog`, `help`, `developers`, `updates`, `network`, status, app-store links, Facebook community links | Sign-up in S01, S03, S09; sign-in in S01; the rest in S02 or S01 as confirmed | Sign-up in S01, S10, S09; sign-in in S01; the rest in S02 or S01 | SUSPECTED, to confirm at Step 21 |
| K7 | Google tags: Universal Analytics, Google Ads | Kept unchanged in `<head>`; the retired Universal Analytics config is proposed for removal, only with the user's yes (it is not a Home design item) | Same | SUSPECTED, to confirm at Step 21 (also whether GA4 exists elsewhere) |
| K8 | Two Facebook Pixels | Kept unchanged | Same | SUSPECTED, to confirm at Step 21 |
| K9 | Google Optimize container | Proposed drop (retired by Google, audit); the A/B tool for this very test is an open question (decision 2) | Same | SUSPECTED, to confirm at Step 21 |
| K10 | Domain-verification metas (Google, Facebook) | Kept | Kept | SUSPECTED, to confirm at Step 21 |
| K11 | Sender script | Kept in `<head>`; use unknown. The hero email form is not carried, so what Sender receives on Home may change | Same | SUSPECTED, to confirm at Step 21 |
| K12 | Referral script (`fpr`, `fpt`, `clickId`, `invite_trial`) | Kept. All primary buttons (S01, S03, S09) must carry the parameters (default of `05-measurement.md` Q6); today only the header buttons, the hero form and one tab link do, so the new buttons are a change to build and test | Same, for S01, S10, S09 | SUSPECTED (strong), to confirm at Step 21 |
| K13 | Country cookie, flag, "from Bangladesh/India" text, Facebook groups by country | Dropped by default (English only, no country-specific content) | Same | SUSPECTED, to confirm at Step 21 |
| K14 | First-party tracker, status widget, smart-bar handler | Kept as internal tooling; the status link may sit in S02 | Same | SUSPECTED, to confirm at Step 21 |
| K15 | Title and meta description | Rewritten for the 2.0 promise (Step 13/14). With two variants the title and meta may differ per variant or be shared (decision 2) | Same | SUSPECTED, to confirm at Step 21 |
| K16 | Structured data, canonical, hreflang (absent today) | To add at Step 21/24; one canonical for the Home URL | Same | Nothing to keep; to confirm at Step 21 |

## Flows

Entry sources named in the inputs: **referral or affiliate links** (the live script reads `fpr`, `fpt`, `clickId`, `invite_trial`, audit K12), **paid ads** (Google Ads and Facebook Pixel tags are on the live page; whether campaigns are active is not verifiable, audit K7, K8), **organic search** (title and meta exist; no ranking data), **returning merchants** (they log in; `brief.md` §2). `05-measurement.md` lists "paid, organic, referral/affiliate" as segments. **Which of these carries real traffic is unknown: entry sources unknown, no analytics.** No other source is named. Flows without a named source start from an unknown source.

| FL## | Variant | Persona | Entry source | Path (section codes) | Ends at | Gap or note |
|---|---|---|---|---|---|---|
| FL01 | A | A dropshipper | unknown, no analytics | S01 → S03 → S04 → S05 → S06 → S07 → S08 → S09 | Click [P] in S03 or S09 → sign-up page (outside P01) | Pains A1 to A5 and A7 not answered (`09-messaging.md` Not claimed) |
| FL02 | A | B POD seller | unknown, no analytics | S01 → S03 → S04 → S05 → S06 → S07 → S08 → S09 | Same | Same page as FL01. B1 to B4 and B6 not answered; B5 consent part only through S07 |
| FL03 | A | M existing merchant | unknown (they read Home and log in, `brief.md` §2; how they arrive is not stated) | S01 (Login link) or S01 → S03 → S07 → S09 | Login (S01) or sign-up | New-feature story only. E1 to E4 and E6 to E8 not answered; E5 only if S07's behaviour is confirmed |
| FL04 | B | A dropshipper | unknown, no analytics | S01 → S10 → S11 (if confirmed) → S12 → S08 → S07 → S09 | Click [P] in S10 or S09 → sign-up page | Without S11: S10 → S12. A2 to A5 not answered; A1 only partly and only if S11 is confirmed |
| FL05 | B | B POD seller | unknown, no analytics | Same as FL04 | Same | Fulfillment and catalog are unconfirmed and old hub services are unknown, so S11 names no old brand and makes no cost or speed claim; B1 to B4 not answered |
| FL06 | B | M existing merchant | unknown (they read Home and log in, `brief.md` §2; how they arrive is not stated) | S01 (Login link) or S01 → S10 → S11 (if confirmed) → S12 → S08 → S07 → S09 (`11` option B merchant flow: beats 3 to 5) | Login or sign-up | Only B has a "what ShopBase is now" beat (S11), and only if confirmed. E1, E2, E4 and E6 to E8 not answered |
| FL07 | A | A and B (same path) | Referral or affiliate link with `fpr` etc. (exists in the live script; volume unknown) | S01 → S03 → S09 | Click [P] with parameters kept → sign-up | The three [P] buttons (S01, S03, S09) must all carry the parameters or referral credit is lost (K12) |
| FL08 | B | A and B (same path) | Referral or affiliate link | S01 → S10 → S09 | Same | Same, for S01, S10, S09 |
| FL09 | A | A and B | Paid ad click (tags exist; whether campaigns land on Home is unknown) | S03 (first screen) → [P] | Sign-up | The hero must hold the primary button above the first scroll, so a paid visitor needs no later section |
| FL10 | B | A and B | Paid ad click (same note) | S10 (first screen) → [P] | Sign-up | Same |
| FL11 | A | A and B | Any source, via the hero secondary button | S03 → [S] Explore CR Scan AI → S05 → S06 → S07 → ... | Primary button only in S09, or in S01 if the header stays visible while scrolling | **Dead-end risk:** S05, S06, S07 and S08 carry no button. Default: the header stays visible on scroll (`ASSUMPTION`, Step 20); otherwise add a button (decision 9) |
| FL12 | B | A and B | Any source, via the hero secondary button | S10 → [S] Explore CR Scan AI → S12 (skips S11) → S08 → S07 → ... | Same as FL11 | Same risk. With S11 present the jump skips it (acceptable per `11`; if S11 grows, drop the secondary button) |

**Organic search** (named as a segment in `05-measurement.md`; title and meta exist, no ranking data) has no flow of its own: a search visitor lands on the Home URL and follows FL01 / FL02 in A or FL04 / FL05 in B. Its only page-specific need is the title and meta (K15, decision 13).

## Cap check

**Counts are made by code, not by eye.** Script: `/private/tmp/claude-501/-Users-nguyentoan-Documents-SB-v2-LD/fb8c2ff0-4f7d-46ed-a2f8-aeb17aa0cde3/scratchpad/step12_cap_check.py`, run as `python3 -I <script> <this file>`. It parses this file's own markdown tables: the code registry, the two section lists, the estimate table below, the keep / rework / drop table and the flows table. B without the conditional sections is computed by leaving out rows whose Name contains the word `CONDITIONAL`.

### Per-section estimate assumptions (estimates; nothing is rendered)

Basis, stated once: the heights below are **my guesses by section type**, not measurements and not taken from any input. Rule used: a hero is about one screen; an illustration section is about one screen (heading, one illustration card on a colour field, a caption); a statement band is about half a screen; the header and footer are guessed. Mobile is the stacked version of the same content. "Boxes" is the planned number of cards or panels (S11 assumes the five parts are merged to four, see above).

| S## | Type | Desktop px (est.) | Mobile px (est.) | Boxes planned |
|---|---|---|---|---|
| S01 | header | 80 | 64 | 0 |
| S02 | footer | 450 | 900 | 0 |
| S03 | hero | 900 | 1500 | 1 |
| S04 | statement band | 480 | 600 | 0 |
| S05 | illustration section | 800 | 1100 | 1 |
| S06 | illustration section | 800 | 1100 | 1 |
| S07 | illustration section | 800 | 1100 | 1 |
| S08 | illustration section | 800 | 1100 | 1 |
| S09 | closing | 500 | 600 | 0 |
| S10 | hero | 900 | 1500 | 1 |
| S11 | parts list | 700 | 1500 | 4 |
| S12 | illustration section | 800 | 1100 | 1 |

### Result of the script (pasted from its output)

```
P01.A: sections=9 (cap 10) | primary CTAs total=3, max per section=1 (cap 1) | secondary total=1, max per section=1, sections with a secondary=['S03'] | max boxes=1 (cap 4)
    est. desktop=5610 px (cap 9000) x1.5 stress=8415 | est. mobile=8064 px (cap 16000) x1.5 stress=12096 | mobile/desktop=1.44
    codes in page order: S01 S03 S04 S05 S06 S07 S08 S09 S02
P01.B (with CONDITIONAL S11): sections=8 (cap 10) | primary CTAs total=3, max per section=1 (cap 1) | secondary total=1, max per section=1, sections with a secondary=['S10'] | max boxes=4 (cap 4)
    est. desktop=5030 px (cap 9000) x1.5 stress=7545 | est. mobile=7864 px (cap 16000) x1.5 stress=11796 | mobile/desktop=1.56
    codes in page order: S01 S10 S11 S12 S08 S07 S09 S02
P01.B-minus (without CONDITIONAL rows): sections=7 (cap 10) | primary CTAs total=3, max per section=1 (cap 1) | secondary total=1, max per section=1, sections with a secondary=['S10'] | max boxes=1 (cap 4)
    est. desktop=4330 px (cap 9000) x1.5 stress=6495 | est. mobile=6364 px (cap 16000) x1.5 stress=9546 | mobile/desktop=1.47
    codes in page order: S01 S10 S12 S08 S07 S09 S02
shared codes: ['S01', 'S02', 'S07', 'S08', 'S09'] | A only: ['S03', 'S04', 'S05', 'S06'] | B only: ['S10', 'S11', 'S12']
registry codes: 12 unique: 12
OLD codes present once each: True
FL ids: 12 unique: 12 sequential: True
PROBLEMS: none
```

**Independent review check** (a second script written by the reviewer, run with `python3 -I` from another folder): same counts and lengths as above (A 9 sections, 3 primary + 1 secondary, max 1 primary per section, max 1 box, 5,610 / 8,064 px; B 8 or 7 sections, same CTAs, max 4 boxes in S11 only, 5,030 / 7,864 px with S11 and 4,330 / 6,364 px without). Registry positions match both lists; S01 to S12, FL01 to FL12 and OLD-01 to OLD-12 each appear once, P01 is the only page code; all 12 OLD rows and all 18 must-keep rows have a route in both variants. It also compared the SHARED rows cell by cell: S07, S08, S09 and S01 differed in wording between the two lists and were made identical in review.

### What the cap check means

- **No variant is over a cap, so nothing was cut or merged.** P01·A has 9 sections, P01·B has 8 (7 without S11), against a cap of 10. Each variant has 3 primary buttons (S01, hero, S09) and one secondary button (the hero), never more than 1 primary per section. The only section at the box cap is S11 (4 boxes, after merging five parts to four).
- **The length figures are estimates.** They come from the guessed heights in the table above (A about 5,610 px, B about 5,030 px, B without S11 about 4,330 px on desktop; A about 8,064 px and B about 7,864 px on mobile). Even with every height 1.5 times larger (the "x1.5 stress" figures) both variants stay under 9,000 px and 16,000 px. The margin is thinnest for A on desktop: A reaches the 9,000 px cap if the real heights are about 1.60 times the estimates (B with S11: about 1.79 times). They fit `11`'s rough "5 to 6 desktop screens" for A and "6 to 7" for B only loosely: my B estimate is shorter than A's because S11 is about 700 px and B has one fewer illustration section than A.
- **The mobile cap is probably generous.** My own estimates give a mobile to desktop ratio of 1.44 to 1.56, while the cap rule assumed 1.8. That is a guess checked against another guess; real heights come from Step 21 and a rendered page (`NOT RUN` until then).
- **If a later step adds sections** (for example a mid-page button section, decision 9, or a FAQ once the user supplies answers) there is room for about 1 to 2 more sections per variant before the 10-section cap, depending on height.

## What changes for measurement

`05-measurement.md` is **not edited**; this is the note for the owner of that step. Section ids are now known: the `S##` codes in this file replace "section_id TBD at Step 12".

1. **Every event needs a `variant` property** (`A` or `B`, and `B` should also record whether S11 was present) if both variants are tested live. Without it the two variants cannot be told apart in any report, including the North Star.
2. **`section_id` = the S## code.** SHARED sections (S01, S02, S07, S08, S09) have the same id in both variants, so they can be compared by variant. Their `position` differs: S08, S09 and S02 always sit at a different place in A and B, and S07 does too when S11 is absent (only S01 is always at the same place), so `position` must be sent too.
3. **The North Star needs the variant at the sign-up.** `signup_start`, `signup_complete` and `store_create_complete` (E11 to E13) happen on `accounts.shopbase.com`, outside P01. How the variant travels there (for example a parameter on the sign-up link, next to the referral parameters the live script already appends) is **unknown**, and it must not break the referral parameters (K12). Without it, "visitor to sign-up rate" per variant cannot be computed.
4. **`scroll_depth` (E07) is not comparable across variants** (different page heights). Read it with `section_view` (E08), or record pixel depth next to the percent.
5. **No tool is known to split traffic** (Google Optimize is retired, audit K9). How visitors are assigned to A or B is open (decision 2). Two variants also split the traffic, so each needs more days; the visitor count stays **blocked** until a baseline and a target exist (`05-measurement.md`).
6. **What a test of A against B can and cannot say:** it compares the two stories against each other, not either against today's page. Whether the live page stays as a control arm is a decision (decision 2).

Which events belong to which section (variant noted where it differs):

| Event (from 05) | Name | Sections where it fires | Variant note |
|---|---|---|---|
| E01 | `home_view` | whole page | `variant` required |
| E02 | `cta_primary_click` | S01, S03 (A), S10 (B), S09 | Same section_id set per variant |
| E03 | `cta_secondary_click` | S03 (A), S10 (B) | Only in the hero of each variant |
| E04 | `cta_secondary_target_view` | S05 (A), S12 (B) | Different target per variant |
| E05 | `signup_outbound_click` | S01, S03 (A), S10 (B), S09 | Catch-all by destination |
| E06 | `signup_form_submit` | none | Only if the email-first form is kept (decision 12); then S03 and S10 |
| E07 | `scroll_depth` | whole page | Not comparable across variants (see 4) |
| E08 | `section_view` | every section of the variant: A = S01, S03, S04, S05, S06, S07, S08, S09, S02; B = S01, S10, S11 (if present), S12, S08, S07, S09, S02 | `position` differs for S08, S09, S02 (and S07 when S11 is absent) |
| E09 | `signin_click` | S01 | Same |
| E10 | `demo_link_click` | none | Only if "Book a demo" is kept (decision 3) |
| E11 to E13 | `signup_start`, `signup_complete`, `store_create_complete` | outside P01 | Need the variant carried over (see 3) |

## Open decisions

### 🔴 Must answer (each blocks a named step)
1. **[BLOCKER at Step 21] Confirm the suspected must-keep list** (K1 to K16 above), above all the tags, the referral script (K12) and the retired UA and Optimize tags (K7, K9). *Default: all kept as a technical requirement; only K7's UA config, K9 and K13 are proposed for removal, and only with your yes.*
2. **[BLOCKER at Step 21] How will the two variants go live?** One URL with a traffic split, two URLs, or one published and the other kept in reserve? Which tool splits traffic (none known), does the live page stay as a control, and how is the variant passed to sign-up without breaking the referral parameters (`fpr`, `fpt`, `clickId`, `invite_trial`, K12)? Affects the canonical URL (one canonical for Home), the title and meta per variant, and every event (see "What changes for measurement"). *Default: not decided; the build keeps one file per variant and adds nothing.*

### 🟡 Should answer (a default is used otherwise)
3. **Header contents.** Keep "Pricing"; drop "Print on demand", "Dropshipping" and "Book a demo"? *Default: logo, Pricing, Login, "Get started for free"; the other three are not carried.*
4. **DMCA footer link (K5b).** The live footer links `/dmcareport`; your rule says no DMCA mention on Home. Keep the link as a plain legal link, or leave it off Home? Dropping a DMCA contact link can have a legal consequence; please ask the person who owns that. *Default: not drawn on Home (your rule), flagged for Step 24.*
5. **B's conditional sections.** Which of store, catalog, payments, fulfillment and support really ship in 2.0; does the Free Launch plan exist, what does it include? *Default: nothing confirmed, so P01·B = 7 sections without S11 and without the plan line.*
6. **Accept the caps** (10 sections, 9,000 px desktop, 16,000 px mobile, 4 boxes, 1 primary CTA per section with the hero's one secondary as the exception)? *Default: accepted as `ASSUMPTION`.* The 16,000 px mobile cap is not a prompt default: it is desktop x 1.8, a guess. A stricter 13,500 px (x 1.5, close to the estimated 1.44 to 1.56 ratio) is the alternative if you want the mobile page held tighter; both variants' estimates pass either.
7. **Keep A's one-line "one product" in S09?** *Default: yes, one line, no old brand named (`11` ⚪ 9).*
8. **Keep S04 "The unseen problem" in A?** Its sentence is mine and has no source (`11` Assumption 4). *Default: kept, the Content reviewer may cut it; without it A has 8 sections.*
9. **A mid-page button.** S05 to S08 carry no primary button, so a reader who clicks "Explore CR Scan AI" has none until S09 (FL11, FL12). Keep the header visible on scroll, or add a button after S07? *Default: header stays visible (Step 20); no extra button.*
10. **Hero and S05 show the same illustration 1** in A (`11` says the hero shows illustration 1 and beat 3 is illustration 1). Use a smaller crop in the hero and the full card in S05, or a different view? *Default: crop in the hero, full card in S05.*
11. **Are S07, S08 and S09 identical in both variants?** They are SHARED by the rule above: same focal point, purpose and illustration; only position and one optional copy line differ (S08's link line in A; S09's optional line). If you want a different approval, AOV or closing section in one variant, that variant takes the next free code (S13 onward). *Default: identical.*

### ⚪ Nice to have
12. Keep the email-first form in the hero (the audit calls it "worth testing")? *Default: no; a button.*
13. Title and meta description per variant or one for both? *Default: decided with decision 2.*
14. Any real traffic source data (a GA4 or Ads export) so the flows FL07 to FL10 can be ranked? *Default: none; entry sources stay unknown.*

## Assumptions

1. Caps (10 sections, 9,000 px desktop, 16,000 px mobile, 4 boxes, 1 primary CTA) are proposals. The mobile cap is desktop x 1.8, a guess. `ASSUMPTION`
2. The hero's secondary button is an exception to the 1-CTA cap, because the brief names two buttons. `ASSUMPTION`
3. Header and footer count as sections for the cap. Nav items and footer link columns are not boxes. `ASSUMPTION`
4. All heights and box counts are my estimates by section type (see the estimate table); no page is rendered. `ASSUMPTION`
5. S08 and S07 are the same section in both variants even though their order and the surrounding sentences differ. This is my reading of "used identically"; decision 11. `ASSUMPTION`
6. S09 is SHARED: its focal point is the same primary button; the optional lines differ by variant (A: "one product"; B: the conditional plan line) and are copy-level, not structure. `ASSUMPTION`
7. The Free Launch plan beat is a line inside S09, not a section (as in `11`, beat 6). `ASSUMPTION`
8. The proposed header (logo, Pricing, Login, primary button) is mine; no input names it. `ASSUMPTION`
9. A visible-on-scroll header is assumed; it is a Step 20 decision. `ASSUMPTION`
10. Flows follow the persona flows of `11` and the strategy pack; persona content is internal opinion, unverified (pack Assumption 3). Entry sources are those the inputs name; their volumes are unknown.
11. Pain ids are interim and complaint-skewed (`07-voc.md` "Limits & bias"); AOV AI has no matching pain.
12. The audit verdicts (drop or rework) rest on no analytics; any block could be missed by visitors for reasons we cannot see. `ASSUMPTION`
13. Nothing in this file is cleared for publication; the Content reviewer signs off outcome wording at Gate 5.

## Check before handing back

- [x] Each variant follows its own option's message order (see the beat to section map): A = S03, S04, S05, S06, S07, S08, S09; B = S10, S11, S12, S08, S07, S09. Neither variant uses the other's sections except SHARED ones (S01, S02, S07, S08, S09). This replaces the base line "follows the chosen option, not the other one" (Gate 4 decision).
- [x] Every section has one focal point and a persona (no empty cell in either section list, checked by the script; one message per cell checked by reading in review).
- [x] Section count ≤ cap, counted by code: see the pasted script result above.
- [x] B/C: every `OLD-##` (OLD-01 to OLD-12) has a decision (checked by the script).
- [ ] Every must-keep item survives: **NOT TICKED.** Nothing is confirmed (all SUSPECTED); K5b conflicts with the no-DMCA rule; K7, K9 and K13 are proposed drops. Each item has a stated route in both variants, awaiting the user.
- [ ] Page length measured: **NOT RUN.** Nothing is rendered; the figures are estimates from stated assumptions.
- [x] `S##`, `P##`, `FL##` codes assigned once; uniqueness verified by code (script check on the registry, both lists and the flows table; see result).
- [ ] Gate 5 approval of this step: not given (approved with the copy at Gate 5).
