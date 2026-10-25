# Hand-off: ShopBase 2.0 Home redesign (landing-page kit project)

Hand-off date: 2026-10-26. For an AI assistant with no prior context. Paths are relative to the project root `SB v2 LD/`. `_progress.md` is the authority on status: if this file and `_progress.md` disagree, `_progress.md` wins.

## 1. TL;DR

1. Project: new Home page (P01, https://www.shopbase.com/) for ShopBase 2.0 ("ShopBase for the AI era"), English only, run with the Landing Page Kit (Steps 00–26, Gates 0–9). Type **C · Rebrand** (changed from B on 2026-10-24).
2. Two variants are in the work, because the user chose both narrative options at Gate 4: P01·A "Find, fix, approve" and P01·B "One store, with AI on top".
3. Steps 00–19 are done; Gates 0–6 are APPROVED. Step 20 (master spec) is written and reviewed, status `waiting for user`. Gate 7 is open. Nothing has been built.
4. Next: the user says "images done" (six `IMG01`–`IMG06` files saved in `02-assets/images/`; none exist today) or "skip images"; then Gate 7 (the user, as Strategy owner, approves tokens and master spec in words). Step 21 (build) may not start before both are recorded in `_progress.md`.
5. The AI USP is UNPROVEN: no result numbers anywhere; "You approve every change" is unconfirmed product behaviour.
6. Chat with the user in Vietnamese; all project files stay in English.

---

## 2. How to resume (read this first)

### 2.1 Reading order

1. `CLAUDE.md` (kit rules; never edit it). Its top section "⚠ FRESH KIT — READ THIS FIRST" ("This kit contains NO completed work. A project starts at Step 00.") is stale stock kit text for this project: Steps 00–19 are done. Follow its "Read Folder" rule 0 instead (resume from `_progress.md`).
2. `_progress.md` (status, gates, roles, caps, the whole Decisions log).
3. This file (`handoff.md`).
4. The base prompt for the next step: now `_prompts/20-master-spec.md` (Part 1b: ask for the images, then Gate 7); after Gate 7, `_prompts/21-build.md` (Reads: `08-claude-design-input/` and `02-assets/images/`).
5. Shared rules: `_prompts/README.md` (gate rule, the "measure, don't eyeball" rule, stale table, chat summary format, end-of-turn block).
6. For the build itself: `08-claude-design-input/build-prompt.md`, `08-claude-design-input/master-spec.md`, `08-claude-design-input/image-prompts.md`, and the approved look `06-proof-ui/proof.html`.

### 2.2 Kit rules that bind the AI

| Rule | What it means here |
|---|---|
| One step at a time | Stop after every step (the user says `continue`) and at every gate (the named approver says `approved`). Never run two steps in one turn. |
| Gates count only in words | A gate is approved only when the approver named in `_progress.md` says so in words (the user is the approver for Gates 0-4, 6-9 as Strategy owner and Gate 5 as Content reviewer), and `_progress.md` records `APPROVED` with the date and their words. A chat message from an earlier session or the existence of a file does not count. |
| Stop-if first | Every `_prompts/NN-*.md` begins with "Stop if". If one is true, say which and stop. |
| No invention | Anything not in an input or a source is written `ASSUMPTION`. Never invent a USP, persona, number, quote or product behaviour. |
| Labels | `UNPROVEN` (a claim without proof), `ASSUMPTION`, `SUSPECTED` (must-keep item not yet confirmed), `NEEDS DATA`, `NEEDS ILLUSTRATION`, `NOT RUN - why`, `[BLOCKER]`. |
| Measure by code | Any check with a number (contrast, section count, page height, hex outside `:root`, inline `style=` count, old-brand count) is computed by running code and the number goes in the report. A check not run is `NOT RUN - why`, never ticked. Reference sites are never proof of conversion rate (N10). |
| Assets as given | Logo, icons and font are used exactly as provided: never redraw the logo, never mix icon styles. Only commercially usable fonts and icons (Inter, SIL OFL 1.1; Lucide, ISC). |
| Never edit approved files or base prompts | `_prompts/` and `CLAUDE.md` are never edited for a project. Approved copy (`05-content/14-copy.md`), the locked palette (`03-research/16-palette.md`) and the approved proof (`06-proof-ui/proof.html`) change only on a user decision, and a change makes later steps `stale` (see the table in `_prompts/README.md`). |
| Permanent codes | `P##`, `S##`, `FL##`, `IMG##` are permanent. New items take the next free number; dropped items stay listed as `removed`. Never renumber. |
| No copies | Never create `-v2` or `-final` copies; re-running a step overwrites its file. A backup before a code-level fix sits next to the original as `<name>.backup-step##.<ext>`. Never create folders outside the kit's folder map. |
| Content before UI | N3: Steps 16+ need Gate 5 APPROVED (it is). N5: one focal point per section. N6: the user chooses the direction. N9: self-review before submitting. |
| Do not follow other playbooks | Only `00-workflow-map.md` and `_prompts/`. |
| Chat summary every step | Structured, plain language, ends with "what this means for the design", questions grouped as must / should / nice with defaults; end-of-turn block from `_prompts/README.md`. |

### 2.3 The "Read Folder" trigger

When the user says **"Read Folder"**: read `_progress.md` first. Because steps are already done, this project is resuming: report the project type (C · Rebrand), the last step done (19; Step 20 is `waiting for user`), the open gate (Gate 7) and any `stale` steps (none recorded), then ask what to run. Do **not** redo Step 00. (`CLAUDE.md`)

### 2.4 Talking to the user

- Chat in Vietnamese (the user writes Vietnamese, e.g. Gate 4 "Làm cả 2 đi"); files stay English. Follow the chat-summary format and end-of-turn block in `_prompts/README.md`.
- The user writes short messages ("continue", "approved", "Approved", "approve"). "continue" only moves on one step. A short approval word counts as a gate approval only when that gate is waiting for that approver in `_progress.md` (now: Gate 7, after the images answer); record the exact words and date there. "images done" / "skip images" are the Step 20 answer, not a gate approval (`_prompts/20-master-spec.md`).
- If a message is ambiguous, ask in Vietnamese; never treat it as approval of something else.

---

## 3. Project at a glance

### 3.1 Product and page

| Item | Value (source) |
|---|---|
| Product | ShopBase 2.0, "ShopBase for the AI era". One independent product; PrintBase and PlusBase no longer exist as brands (`_progress.md` Decisions log) |
| USP (user's words, translated) | "AI-first: AI ("CR Scan" and "AOV") helps increase the store's conversion rate (CR) and average order value (AOV), while the seller stays in control and makes the final decision." (`01-strategy/01-strategy-pack.md`; from the user's chat message, not a file) |
| What the AI does (only source: user's hero screenshot `02-assets/images/hero-2.0-reference.png`) | CR Scan AI finds what stops shoppers and builds the fix. AOV AI recommends offers that raise order value. "You approve every change." This describes features; it is not proof of results |
| Page in scope | **P01 Home only**, English only. Other pages (321 URLs in the sitemap) are out of scope and get no `P##` code until the user adds them |
| Primary CTA | "Get started for free" -> `https://accounts.shopbase.com/sign-up` (sign up). Secondary CTA in the hero only: "Explore CR Scan AI" (on-page anchor, ASSUMPTION) |
| Proof decision | No result numbers. The page shows what the AI does (scan finds problems, proposes improvements, seller approves) as user-supplied illustrations labelled "Illustration", never as real product UI |

### 3.2 The two variants (both chosen at Gate 4: user said "Làm cả 2 đi")

| | **P01·A "Find, fix, approve"** (Option A) | **P01·B "One store, with AI on top"** (Option B) |
|---|---|---|
| Idea | The whole page walks through the AI loop: scan, proposed fix, seller approves; AOV AI as the second tool | ShopBase 2.0 is one store platform; AI is the layer on it; seller approves |
| Hero promise (descriptive, flagged; approved at Gate 5) | "AI that finds what stops shoppers on your store and builds the fix." | "ShopBase 2.0: one store platform, with AI that finds what stops shoppers and builds the fix." |
| Sections (page order) | 9: S01, S03, S04, S05, S06, S07, S08, S09, S02 | 7 by default: S01, S10, S12, S08, S07, S09, S02 (8 with the CONDITIONAL S11, which is not built) |
| Estimated length | desktop 4,864 px / mobile 4,943 px (derived from proof frames plus estimates) | desktop 3,903 px / mobile 3,944 px (S11 not built) |

Shared sections (same S## code, same markup and text except the variant differences listed in master-spec section 10, e.g. S09's optional line shows only in A): S01 Header, S02 Footer, S07 Approve, S08 AOV AI, S09 Closing CTA. A-only: S03 Hero A, S04 The unseen problem, S05 Scan, S06 Fix. B-only: S10 Hero B, S11 One product (CONDITIONAL, not built), S12 Scan and fix. Claude recommended Option A (N6: the user decides; the user chose both).

### 3.3 Audience

- Primary A: experienced dropshipper. Primary B: experienced POD seller. Equal weight. Both Vietnam-based, selling to US/EU buyers (user decision). Secondary (not ranked by the source, ASSUMPTION): dropshipping old hands who are POD newbies, and POD old hands who are dropshipping newbies. Newbie groups are out of primary scope.
- Existing merchants also read Home (user confirmed). They are ASSUMED to resemble A and B. What they need to hear is not stated; questions E1-E8 in `04-brand/09-messaging.md` are unanswered, so the page stays silent about migration.
- All persona content is internal opinion from the user's sheets (`01-strategy/source-persona-sheets.md`, `01-strategy/personas-draft.md`), unverified. English-only page: no Vietnam-specific content and no promise of Vietnamese support (user decision).

### 3.4 USP status

Everything about the AI is `UNPROVEN` (what it does, that it raises CR/AOV, that the seller approves every change). Outcome wording ("raise order value", "turns visitors into buyers") is fenced as ALTERNATE. Positioning "AI" is not unique: 4 of 5 competitor homepages make an AI claim (Step 06). The only wording that no competitor homepage carried is the seller-approval statement.

### 3.5 Locked decisions

| Item | Locked value |
|---|---|
| Frame lock (Step 03 defaults, accepted at Gate 1) | Responsive, locked frames 1440 and 375; one long scrolling page; light mode only; English, no language switch; files in English; P01 only |
| Palette | **Option 1 · Logo-true Blue, LOCKED 2026-10-25** (`03-research/16-palette.md`). Primary `#4371CD` (logo blue `#497BDF` at 92% brightness, white on it 4.69:1); primary hover and link `#3A62B2`; accent / logo sky `#8BCDF6`; accent tint `#E7F3FD`; page `#FFFFFF`; panel `#F4F7FC`; title `#1E222B`; body `#373B43`; muted `#596070`; UI border `#7F8A9E`; field border `#66718A`; divider `#DDE3EE`; focus ring `#1E4A9E`. Status colours: success `#1B7A47`, warning `#8A5300`, danger `#B3261E` (with tints) |
| Soft colour fields (Amendment, ASSUMPTION until the user saw the proof; the proof was approved at Gate 6) | F1 Mist `#F3FAFE`->`#EDF2FC`; F2 Sky `#D1EBFB`->`#D9E4F9`; F3 Azure `#C5E6FA`->`#A4BDEF`. No gradient on text, no glow/sparkle, no dark panel by default |
| Visual direction | Follow Calendly's structure (rounded containers, white cards with soft shadow on soft colour fields, alternating rows, one clear button); reproduce the approach, never Calendly's assets, wording or artwork. Colours do not carry over (Calendly's warm off-white, multi-hue fields and navy are not reproducible with Option 1) |
| Font | Inter (SIL OFL 1.1), `02-assets/fonts/InterVariable.woff2` |
| Icons | Lucide outline (ISC). Only `02-assets/icons/arrow-right.svg` exists so far |
| Logo | `02-assets/logo/Logo (6).svg` (dark wordmark, light surfaces), `Logo (1).svg` (white wordmark, dark surfaces only; unused by default), `Logo (3).svg` (icon only). Never edited, never recoloured, never on a colour field |
Not locked: the caps (ASSUMPTION, awaiting the user's OK; 10 sections per page counting header and footer, 9,000 px desktop, 16,000 px mobile, 4 boxes, 1 primary CTA per section; header line in section 4).

### 3.6 Roles

The user is Strategy owner (Gates 0–4 and 6–9), Content reviewer (Gate 5; also signs off any wording on trademark, DMCA or restricted products) and Publisher. Builder is not answered (`_?`, default "Claude runs, user exports"): confirm before Step 21.

---

## 4. Status board (copied verbatim from `_progress.md`, 2026-10-26)

Header lines (verbatim):

**Project:** ShopBase website redesign (https://www.shopbase.com/)
**Project type:** C · Rebrand (ShopBase 2.0: positioning changes to AI-first; logo, colours and name stay) — changed from B on 2026-10-24
**Pages in scope:** P01 · Home · https://www.shopbase.com/ (only Home for now; other pages listed in `01-strategy/00-project-type.md`, added later with next free code)
**Project language (files):** English (user accepted default; confirmed at Step 03)
**Modules:** Brand = on (type C; identity limited to the existing logo and colours) · Figma/handoff = off
**Roles:** Strategy owner = user · Content reviewer = user · Builder = _? (default: Claude runs, user exports)_ · Publisher = user
**Section cap / page-length cap:** ASSUMPTION defaults, awaiting the user's OK: 10 sections per page · 9,000 px desktop · 16,000 px mobile (writer's ×1.8 guess; 13,500 px is the stricter option) · 4 boxes per section · 1 primary CTA per section (hero has one extra secondary button)
**Chosen narrative option:** BOTH A and B, built as two variants of P01 (P01·A "Find, fix, approve" and P01·B "One store, with AI on top"). User, 2026-10-24: "Làm cả 2 đi". The user picks which to publish later (or tests both).
**Current position:** Gate 0 APPROVED (2026-10-24). Gate 1 APPROVED (2026-10-24). Gate 2 APPROVED (2026-10-24). Gate 3 and Gate 4 APPROVED (2026-10-24; Gate 4: both options). Gate 5 APPROVED (2026-10-25). Palette Option 1 LOCKED, with soft colour fields F1–F3. Gate 6 APPROVED (2026-10-25). Steps 19 and 20 written and reviewed. Waiting for the user: "images done" or "skip images", then GATE 7 (approve tokens and master spec). Then Step 21 (the user builds in Claude Design). The user's style reference is saved at `02-assets/moodboard/style-ref-01-calendly-fullpage.png`; use it at Steps 16, 17 and 18. The AI USP will be shown as a product demonstration (AI scan finds issues, proposes improvements, seller approves), with no result numbers. This unblocks Step 09 on the proof question; copy must stay descriptive.

| Step | Applies to | Status | Date | Note |
|---|---|---|---|---|
| 00 Project type | A B C | done (updated) | 2026-10-24 | Type changed B → C; Home = P01 only; EN only; current merchants read the page |
| 01 Strategy pack | A B C | done | 2026-10-24 | Sonnet wrote, Opus reviewed. AI USP is UNPROVEN (blocks Step 09). Gate 0 waiting |
| 02 Intake | A B C | done | 2026-10-24 | Brief drafted, then answered by the user (Q1 CR Scan/AOV via hero screenshot, Q2 English only, Q3 sign-up CTA); the lead read this as confirmation. Logo OK (3 vector SVGs). Fonts, icons, moodboard missing (needed before Step 16) |
| 03 Brief analysis & frame lock | A B C | done | 2026-10-24 | Sonnet wrote, Opus reviewed. Frame lock is proposed ("to confirm"); the user approves it at Gate 1. Top open: hero screenshot status; proof of results [BLOCKER at Step 09] |
| 04 Audit of the existing page | B C | done | 2026-10-24 | Sonnet wrote, Opus re-fetched and re-measured. No analytics supplied; must-keep list is all SUSPECTED. Tracking/script decisions block Step 21 |
| 05 Measurement | A B C | done | 2026-10-24 | Sonnet wrote, Opus reviewed. Baseline NOT AVAILABLE, no target set. Gate 1 waiting |
| 06 Positioning & competitors | A B C | done | 2026-10-24 | Sonnet wrote, Opus re-checked quotes against the real pages and fixed 15 items. AI is not unique in this category; difference is unproven |
| 07 Voice of customer | A B C | done | 2026-10-24 | INTERIM only: no Reddit (blocked), 22 customer-voice sources (mostly Trustpilot), 2 of 71 quotes byte-verified. No quote may go into copy until checked. User may paste Reddit/FB-group material; re-running makes 09–26 stale |
| 08 Reference analysis | A B C | done | 2026-10-24 | Sonnet wrote, Opus re-fetched all 8 pages and fixed ~20 items. References chosen by Claude (user has not supplied any). Visuals NOT VERIFIED (no browser). Gate 2 waiting |
| 09 Messaging (Brand module) | A C | done | 2026-10-24 | Sonnet wrote, Opus reviewed (12 fixes). All three supporting messages UNPROVEN (product demo does not exist yet). "aimed at order value" softening awaits user's accept/reject. AOV AI message has no matching VoC pain |
| 10 Identity (Brand module) | A C | done | 2026-10-24 | Sonnet wrote, Opus re-measured and fixed 19 items. Logo and colours kept; no logo drawn. Primary blue, font, icons and old-brand decisions open. Gate 3 waiting |
| 11 Narrative options | A B C | done | 2026-10-24 | Sonnet wrote two options, Opus reviewed (10 fixes). User chose both (Gate 4) |
| 12 Sitemap & section list | A B C | done | 2026-10-24 | Sonnet wrote, Opus recounted by code and fixed 18 items. P01·A 9 sections, P01·B 8 (7 without conditional S11); lengths are estimates, nothing rendered. Approved with the copy at Gate 5. Open: must-keep list and how both variants go live (block Step 21) |
| 13 Content brief | A B C | done | 2026-10-24 | Sonnet wrote, Opus checked by code and fixed 8 items. 12 section briefs; 20-item "data the user must supply" list. Only S04 (A) is problem-led. Approved with the copy at Gate 5 |
| 14 Copy | A B C | done | 2026-10-24 | Sonnet wrote, Opus audited claims and counts and fixed 14 items. Outcome headline and "raise order value" are fenced ALTERNATE (Gate 5 sign-off). Word counts and SEO lengths measured. 14 placeholders open |
| 15 Content self-review | A B C | done | 2026-10-25 | Two rounds (11 then 5 failures, all fixed) plus Opus final check by code. Both heroes would fit a competitor's site (stated honestly); existing-merchant gap (E1–E8) not answered by design. Gate 5 waiting |
| 16 Palette | A B C | done (updated) | 2026-10-25 | Three options written, Opus recomputed all 99 contrast rows and fixed 9 items. User chose Option 1 (logo-true blue, primary `#4371CD`); being marked LOCKED in the file, together with soft colour-field tints for the Calendly-style visual direction |
| 17 Moodboard | A B C | done | 2026-10-25 | Parts 1 and 2 done. Calendly capture is the main reference plus cues from Notion AI, Cursor, Intelligems (14 crops saved under `02-assets/moodboard/screens/`). Opus re-viewed all crops and re-measured; 21 fixes. Clarity, Shoplift, Sidekick not viewed; Copilot and Squarespace set aside (dark). K5 read from Calendly only |
| 18 Proof sections | A B C | done | 2026-10-25 | `06-proof-ui/proof.html`, 7 frames. Opus re-measured in headless Chrome and fixed 3 items: 0 hex outside :root, 0 inline style, 12/12 contrast pairs pass, copy exact, caps respected. All illustrations are labelled placeholders. Gate 6 waiting |
| 19 Tokens | A B C | done | 2026-10-25 | 80 primitive + 87 semantic tokens, 0 broken aliases; all 83 proof variables accounted for; 62/62 allowed contrast pairs pass. Opus re-measured and fixed 3 items (a role-named primitive, two forbidden contrast pairs listed, "body" renamed "paragraph"). Mobile field radius (1rem vs probably 1.5rem) flagged for Step 20/21. Approved with the spec at Gate 7 |
| 20 Master spec | A B C | waiting for user | 2026-10-26 | `08-claude-design-input/` has master-spec.md, image-prompts.md (6 slots IMG01–IMG06, 3:1, 1200×400) and build-prompt.md. Opus re-ran all checks and fixed 15 items (copy verbatim, 83/83 `:root` variables, fences intact). Waiting for the user to say "images done" or "skip images", then Gate 7. Default build: two HTML files, final-ui-A.html first |
| 21 Build | A B C | not started | | |
| 22 UI self-review | A B C | not started | | |
| 23 Spec check | A B C | not started | | |
| 24 Pre-launch checklist | A B C | not started | | |
| 25 Publish / handoff | A B C | not started | | |
| 26 Results after launch | A B C | not started | | |

Reading notes (this hand-off's, not `_progress.md`'s): "Gate N waiting" in a step note is the state when that step ended; all of Gates 0–6 were approved later (table below). Step 19's "Approved with the spec at Gate 7" is the plan, not a fact: Gate 7 is open. Step 10's "primary blue, font, icons" were settled later (palette at Step 16; Inter and Lucide by default, `02-assets/fonts/font-name.txt`, `02-assets/icons/icon-library.txt`).

### Gates

| Gate | After step | Who approves | Status | Date | What was decided or changed |
|---|---|---|---|---|---|
| 0 · Type & strategy | 01 | Strategy owner | APPROVED | 2026-10-24 | User: "Approved". AI USP still has no proof (blocks Step 09) |
| 1 · Frame & audit | 05 | Strategy owner | APPROVED | 2026-10-24 | User: "Approve". Frame lock (Step 03 defaults) and audit (Step 04) accepted. Baseline and sign-up definition still open |
| 2 · Research | 08 | Strategy owner | APPROVED | 2026-10-24 | User: "Approved". Positioning (06), interim VoC (07, no Reddit) and references (08) accepted |
| 3 · Brand | 10 | Strategy owner | APPROVED | 2026-10-24 | User: "approve". Messaging (09) and identity (10) accepted; primary blue, legal entity/support email decisions still open |
| 4 · Direction (choose option) | 11 | Strategy owner | APPROVED | 2026-10-24 | User: "Làm cả 2 đi" — both options A and B proceed as two variants. B's conditional beats stay conditional until the user confirms the product-coverage claims |
| 5 · Content | 15 | Content reviewer | APPROVED | 2026-10-25 | User: "Approved". Section list (12) and copy (14) accepted as written. The five flagged items were not changed, so their defaults stand: outcome headline and "raise order value" stay fenced; S04 stays in A (recommended cut not requested); "You approve every change" stays UNPROVEN; S11 and Free Launch stay unbuilt |
| 6 · Visual direction | 18 | Strategy owner | APPROVED | 2026-10-25 | User: "APPROVED". Visual direction accepted from `06-proof-ui/proof.html`: palette Option 1, Calendly-structure style, soft fields. The three visual judgement calls (hero field width, card shadow exception, amount of blue) were not changed, so the proof's current values stand and are to be fixed as tokens at Step 19 |
| 7 · Tokens & spec | 20 | Strategy owner | open | | |
| 8 · UI review | 23 | Strategy owner | open | | |
| 9 · Launch | 25 | Strategy owner | open | | |

(Gate 3's "primary blue ... still open" was settled later: Option 1, LOCKED 2026-10-25.)

---

## 5. What happened, in order

The date the repo was cloned is not recorded in any file. The earliest dated work is 2026-10-24. Most `_progress.md` step notes say "Sonnet wrote, Opus reviewed" (a Sonnet subagent wrote, an Opus subagent reviewed and fixed the files); the model versions and the method come from the working session (section 7.1).

### 2026-10-24

| Step | Output file | Key result (and what review fixed where it mattered) |
|---|---|---|
| 00 Project type | `01-strategy/00-project-type.md` | First classified B (page exists, brand stays; user's answers to Step 00 Q1–Q2). The same day the user said it is a rebrand ("vì là rebrand"): type **C**, because the positioning and promise change to AI-first ("ShopBase for the AI era") while the name, logo and colours stay. No later step had run, so nothing became stale. Brand module turned on (Steps 09–10, Gate 3). Home only; the 321-URL sitemap was listed for scope only |
| 01 Strategy pack | `01-strategy/01-strategy-pack.md` (inputs: `00-project-type.md`, `personas-draft.md`, `source-persona-sheets.md`) | Sources: the project-type file; `personas-draft.md`, derived only from `source-persona-sheets.md` (a verbatim transcription of the user's screenshots of two internal sheets, Vietnamese kept; the PrintBase and PlusBase tabs were not supplied); the user's decisions of 2026-10-24; and live-homepage facts supplied. The USP traces to the user's chat message, not to a file. USP entirely UNPROVEN. Gate 0 APPROVED ("Approved") |
| 02 Intake | `03-research/02-intake.md`, `01-strategy/brief.md` | No brief existed, so Step 02 stopped; a brief was drafted and the user answered it (Q1 CR Scan/AOV are described by the hero screenshot, Q2 English only, Q3 primary CTA is sign-up). `brief.md` says "Confirmed by the user's answers on 2026-10-24; remaining questions use their defaults". Logo: 3 real vector SVGs, measured (logo blue `#497BDF`, RGB distance 79.1 from the "Blue (Primary) 500" `#0096ED` of a colour-scale screenshot the user showed in chat). Fonts, icons, moodboard were missing (added later) |
| 03 Brief analysis and frame lock | `03-research/03-brief-analysis.md` | Gaps G1-G15; risks: the screenshot headline is an outcome promise that conflicts with the brief's "no outcome promise without proof"; "built in" / "No apps to stitch together" / "Free Launch plan" are unverified. Screenshot colours sampled by code (button `#3B59F6`, 5.32:1 with white). Frame lock proposed (accepted at Gate 1) |
| 04 Audit | `03-research/04-audit.md` | Live page fetched and parsed (102,276 bytes HTML; 12 blocks). Measured: 102 anchors, 13 dead `href="#"`; 7 routes to sign-up with 5 different spellings of the sign-up label; H1 x5; 75 images, 4 with meaningful alt; 0 mentions of AI; PrintBase/PlusBase named in body and footer; 1 Wistia video in the hero and 8 more in the product-tab block; hero H1 has a typing animation cycling "E-commerce / Dropshipping / Print-On-Demand"; 7 third-party script hosts. Must-keep list K1-K16, all SUSPECTED (referral/affiliate script K12; retired Universal Analytics and Google Optimize tags K7, K9). Old-brand inventory written for Step 24. Opus re-fetched; files were byte-identical |
| 05 Measurement | `03-research/05-measurement.md` | North Star: Home visitor to sign-up rate (ASSUMPTION; event default `signup_complete`). **Baseline NOT AVAILABLE**, no target set; 14-day reading window proposed; visitor count blocked until baseline and target exist. Gate 1 APPROVED ("Approve") |
| 06 Positioning | `03-research/06-positioning.md` | 5 competitor homepages (Shopify, Wix, BigCommerce, Printify, Zendrop) re-checked by `curl` byte-match (Opus fixed 15 items). **AI is not unique**: 4 of 5 make an AI claim in copy. Wix already pairs the same two outcomes (conversions, average order value) with named AI features; no competitor homepage carried a seller-approval statement (static text, 2026-10-24). Difference is unproven |
| 07 VoC | `03-research/07-voc.md` | **INTERIM**. Reddit unreachable (WebSearch and WebFetch refused it; one `curl` try was blocked by the permission system and not retried); G2, Capterra, BlackHatWorld and full Shopify Community threads returned 403; Trustpilot and Shopify Community answered `curl` with a 403 bot check at review, so 69 quotes stay summariser-read. 22 customer-voice sources (mostly Trustpilot); **only 2 of 71 quotes byte-verified**. No source showed sellers reacting to a CR/AOV scan. Pains the USP does not answer are listed (payment holds, bans, ad blocks, fulfilment, margin) |
| 08 Reference analysis | `03-research/08-reference-analysis.md` | 8 references chosen by Claude (Cursor, GitHub Copilot, Intelligems, Shoplift, Clarity, Notion AI, Squarespace, Shopify Sidekick). Pattern table, do-not-copy list (no numbers, no chat-assistant frame, no "you don't lift a finger" tone). Visuals NOT VERIFIED then. Gate 2 APPROVED ("Approved") |
| 09 Messaging | `04-brand/09-messaging.md` | Positioning statement (safe default without an "unlike" clause), message hierarchy, voice (plain, calm, seller in charge, friendly/direct = ASSUMPTION), change message for existing merchants (mostly unknown), claims to avoid. Support message 2 (AOV AI) has no matching VoC pain. Opus fixed 12 items |
| 10 Identity | `04-brand/10-identity.md` | Logo kept and measured, not redrawn; clear-space and minimum-size proposals; Inter and Lucide proposed (live site already loads Inter); 19-row migration list for old brand items (legal entity "OpenCommerce Group, Inc", `support@shopbase.com` and 2021 dates are the user's decision only). Inter and Lucide were chosen by default at Step 10 (so say `02-assets/fonts/font-name.txt` and `02-assets/icons/icon-library.txt`; the files in `fonts/` and `icons/` were written on 2026-10-25). Gate 3 APPROVED ("approve") |
| 11 Narrative options | `03-research/11-narrative-options.md` | Option A (7 beats) and Option B (6 beats), with a recommendation for A. **Gate 4: the user chose both ("Làm cả 2 đi")**. Opus fixed 10 items |
| 12 Sections | `03-research/12-sections.md` | 12 permanent section codes S01-S12, FL01-FL12, caps proposed, keep/rework/drop table, cap check by script (A 9 sections; B 8, 7 without S11; estimates only, nothing rendered). Opus recounted and fixed 18 items |
| 13 Content brief | `05-content/13-content-brief.md` | 12 section briefs, 20-item list of data the user must supply. Opus fixed 8 items |
| 14 Copy | `05-content/14-copy.md` | Copy for both variants from the screenshot's own words plus "proposed" and "scan"; word counts and SEO lengths measured. Opus audited and fixed 14 items. 14 placeholders open |

### 2026-10-25

| Step | Output | Key result |
|---|---|---|
| 15 Content self-review | review log in `05-content/14-copy.md` | Round 1: 11 failures (e.g. meta descriptions stated "You approve every change" as fact; "visitors/shoppers" and four verbs for one act); 8 fixed, 3 (existing-merchant gap, me-too, hero "for whom") not fixable by wording. Round 2: 5 stale-statement failures fixed. Final independent check by code reproduced the counts. **Gate 5 APPROVED ("Approved")** |
| 16 Palette | `03-research/16-palette.md`, `03-research/16-palette-options.html` | Three options (Logo-true Blue, Blue-Violet, Ink and Soft Fields), 99 contrast rows recomputed by Opus (9 fixes). **User chose Option 1 ("Phương án 1")**. Then, with the Calendly-style direction, soft fields F1-F3 were added as an Amendment (23/23 allowed field pairs pass) |
| 17 Moodboard | `03-research/17-moodboard.md`, `02-assets/moodboard/` | The user's Calendly full-page capture (`style-ref-01-calendly-fullpage.png`, 1920 x 14305) is the main reference ("Calendly là đủ… light hướng đến sự clean"); selective cues from Notion AI, Cursor, Intelligems. 14 crops saved; measurements by script; "clean, light" rules proposed. Opus re-viewed all crops, 21 fixes |
| 18 Proof sections | `06-proof-ui/proof.html` | 7 frames: S03, S10, S05, S06, S12, S07, S09 (header and footer out of scope). All pictures are labelled placeholders. Opus fixed 3 items. **Gate 6 APPROVED ("APPROVED")** |
| 19 Tokens | `07-tokens/1-primitive.json`, `07-tokens/2-semantic.json`, `07-tokens/token-mapping.md` | W3C-style tokens, one light mode, no component tier. 83 proof `:root` variables all mapped or classified. Finding: on mobile the proof's field and card radius are both 1rem (the "inner smaller than parent" rule does not hold at 375); open for Step 20/21 |

### 2026-10-26

| Step | Output | Key result |
|---|---|---|
| 20 Master spec | `08-claude-design-input/master-spec.md`, `image-prompts.md`, `build-prompt.md` | Single source for the build: every section with verbatim copy, states, components, coverage, measurement hooks, image slots IMG01-IMG06 (3:1, 1200 x 400), type C brand rules, `:root` block (Appendix A, 83 variables). Opus re-ran all checks and fixed 15 items. Status `waiting for user` |

Honest limits carried from this history: baseline and target do not exist; VoC is interim; competitor colours were not measured; page lengths are estimates; header, footer, S04, S08, the mobile menu and hover/pressed states are not in the proof and were never rendered; nothing was rendered on a real phone.

---

## 6. Decisions made by the user (condensed from the `_progress.md` Decisions log)

`_progress.md` Decisions log has **16 entries** (13 dated 2026-10-24, 3 dated 2026-10-25; not in date order: the Step 09 Q1, Q2 and proof entries are dated 2026-10-24 but sit at the end). Rows below are condensed in wording; dates, "By" and "Affects" match the log. Text in *[brackets, italic]* is this hand-off's note, not part of the log. Gate approvals and the user's exact words are in the Gates table in section 4.

| Date | Decision | By | Affects |
|---|---|---|---|
| 2026-10-24 | Project type B (Redesign); brand (logo, colours) kept; Brand module off. *[Hand-off note: replaced by the B → C entry below.]* | User (answers to Step 00 Q1–Q2) | All steps |
| 2026-10-24 | Home (P01) is the first page through the workflow; other pages wait for user decision | User | 12 onward |
| 2026-10-24 | Type changed B -> C: ShopBase 2.0 is "ShopBase for the AI era"; positioning changes, logo and colours stay; Brand module on | User ("vì là rebrand") | All steps (nothing built yet) |
| 2026-10-24 | USP direction AI-first: AI CR Scan and AOV raise conversion rate and average order value; the seller keeps final control. No proof supplied | User | 01, 06, 09, 11 |
| 2026-10-24 | Audience follows the personas: experienced dropshipping and POD sellers, Vietnam-based, selling to US/EU | User | 01, 07, 14 |
| 2026-10-24 | ShopBase 2.0 is one independent product; PrintBase and PlusBase no longer exist as brands | User | 01, 09, 12, 14 |
| 2026-10-24 | CR Scan AI and AOV AI are described by the hero screenshot `02-assets/images/hero-2.0-reference.png`; it describes features, it is not proof of results | User | 03, 09, 14 |
| 2026-10-24 | Primary Home CTA is sign up ("Get started for free"); Home is English only, no Vietnam-specific content | User | 03, 12, 14 |
| 2026-10-24 | The user supplied a style reference, a full-page Calendly homepage screenshot, saved in `02-assets/moodboard/`; a style direction to learn from, not to copy | User | 16, 17, 18, 20, 21 |
| 2026-10-24 | Gate 4: the user chose BOTH narrative options ("Làm cả 2 đi"); they run as two variants of P01 (P01·A and P01·B) through Steps 12–23; shared sections keep one S## code; cost roughly doubles from Step 13; measurement needs a variant id on every event if both are tested live | User | 12–26 |
| 2026-10-25 | Palette: Option 1 (logo-true blue, primary `#4371CD`) chosen and LOCKED | User ("Phương án 1") | 17-23 |
| 2026-10-25 | Visual style: follow Calendly's visual approach closely (layout rhythm, card system, spacing, type hierarchy, colour fields behind product cards); page content differs; reproduce the approach, never Calendly's assets, illustrations, wording or artwork. Changes the Step 16 default "no gradient": soft colour fields behind illustrations allowed, from Option 1's blue family; no gradient text. Tints to be tested (ASSUMPTION until the user saw the proof) | User | 17-21 |
| 2026-10-25 | Step 17: the Calendly capture is enough as the main reference; selective cues from the Step 08 references (Cursor, Copilot, Intelligems, Shoplift, Clarity, Notion AI, Squarespace), overall direction light and clean; the user judges at the Step 18 proof | User ("Calendly là đủ… light hướng đến sự clean") | 17-20 |
| 2026-10-24 | Step 09 Q1: "You approve every change" stays only as the screenshot sentence, UNPROVEN; no dedicated control/approval block until the product behaviour (including undo) is confirmed | User (accepted default) | 11, 12, 14, 18 |
| 2026-10-24 | Step 09 Q2: the product demo (scan -> proposal -> approval step) is shown as illustrations supplied by the user; Step 18 must label them as illustrations, not real product UI | User | 17, 18, 20, 21 |
| 2026-10-24 | Proof for the AI USP: no result numbers (no "+30%"); the page shows what the AI does (scan detects problems, proposes improvements); outcome wording stays qualitative and is for the Content reviewer to check | User | 09, 11, 14, 15, 18 |

Other user inputs recorded outside the log: Step 02 answers (Q1 screenshot describes CR Scan/AOV; Q2 English only; Q3 sign-up CTA), content reviewer = the user (`01-strategy/00-project-type.md`), "Vít đè" must stay out of copy, no trademark / DMCA / restricted-product mention on Home (pack, "Closed by the user").

---

## 7. How the work was run

Everything in this section is a **lesson from the working session** (the lead session and its subagents), not a kit rule and not a project decision. Where a project file corroborates it, the file is named.

### 7.1 Working method (lesson from the working session)

- Source: the lead's Claude Code memory note `subagent-build-then-review.md` (on the user's machine, outside the project; dated 2026-10-24). It records the user's request, in Vietnamese: "Từ giờ hãy vận hành theo hướng subagent… sonnet 5.5 medium làm task trước, opus 5.5 medium review lại… chạy automation để báo lại kết quả cuối cùng". Corroborated in the project only by the `_progress.md` notes "Sonnet wrote, Opus reviewed".
- Method used: a Sonnet 5.5 (medium) subagent does the step; an Opus 5.5 (medium) subagent reviews it against the sources (briefed with the files, not Sonnet's conclusions) and fixes errors in the output files; only the reviewed result goes to the user. The kit's stop points (`continue`, gates) still apply between steps.
- The lead (main session) alone updates `_progress.md` and records gates (step files say so, e.g. `03-research/12-sections.md`: "this step may not edit it").
- Python ran as `python3 -I` from a folder outside the project; scripts and scratch output lived in that session's scratchpad under `/private/tmp/`, which several step files cite. A new session has a different scratchpad, so those scripts may be gone: re-run checks from scratch, never put scratch files in the project.

### 7.2 Tool and environment lessons (lessons from the working session)

| Lesson | Corroboration in project files |
|---|---|
| WebFetch passes pages through a small summarising model, so its "verbatim" quotes are unreliable. Byte-verify with `curl` | Yes: `03-research/06-positioning.md` (WebFetch quotes "not reliable on their own"; all five homepages re-checked by `curl`, mismatching quotes corrected) and `03-research/07-voc.md` ("returns text through a small summarising model"). `08-reference-analysis.md` used `curl` only |
| Reddit, G2, Capterra, Trustpilot and Shopify Community block automated fetching. Do not bypass | Yes: `03-research/07-voc.md` ("What I could not reach": Reddit refused by WebSearch and WebFetch, a `curl` try blocked by the permission system and not retried; G2, Capterra, BlackHatWorld HTTP 403; Trustpilot and Shopify Community answered `curl` with a 403 bot check). `08-reference-analysis.md`: `lovable.dev` dropped on HTTP 403, no bypass |
| Headless Chrome will not open a window narrower than 500 px: render 375 px mobile by putting the page in a 375-wide iframe | Partly: `07-tokens/token-mapping.md` and `08-claude-design-input/master-spec.md` Appendix B use the 375 iframe; no file mentions the 500 px limit |
| `sips --cropOffset 0` ignores offset 0, and a crop whose offset + height reaches the image edge can fail. Use a pure-Python PNG slicer/reader | Partly: `03-research/17-moodboard.md` records slices starting at offset 1 (row 0 in no slice), `sips` silently ignoring a 1704-row crop at the end, and a review with a pure-Python PNG reader |
| A sleeping laptop interrupts running agents: write output files early | No: not in the project files |
| Keep the project free of scratch files | No file states it; `.gitignore` lists only `.DS_Store` (two `.DS_Store` files exist and are ignored) |

---

## 8. Open items and decisions waiting

### (a) Immediate (blocks Step 21)

1. The user says **`images done`** (after saving the six `IMG##-name.png` into `02-assets/images/`) or **`skip images`**. Today `02-assets/images/` holds only `hero-2.0-reference.png`. With `skip images`, the six slots stay labelled placeholders.
2. The user approves **GATE 7 (tokens and master spec)** in words. Record `APPROVED`, date and the user's words in `_progress.md`.

### (b) Decisions that block Step 21 (build) or its wiring (all have defaults in `08-claude-design-input/master-spec.md` section 11 and `03-research/12-sections.md` "Open decisions")

The files differ on how hard these block: `_progress.md` says tracking/script decisions (Step 04 note), the must-keep list and how both variants go live (Step 12 note) block Step 21; the master spec builds with the defaults below, treats variant go-live as blocking publishing, not building, and wires tags at Step 24. Ask the user before Step 21 which reading applies; do not decide for them.

| # | Decision | Default used if unanswered |
|---|---|---|
| 1 | Must-keep list K1-K16 (`03-research/04-audit.md`), above all the referral/affiliate script (K12: reads `fpr`, `fpt`, `clickId`, `invite_trial`, must not break), Google Ads tag, Facebook Pixels, Sender, domain-verification metas, retired Universal Analytics (K7) and Google Optimize (K9) tags | All kept as a technical requirement; the audit proposes removing only the retired UA config (K7) and Optimize (K9), and only with the user's yes; the spec drops the K13 country logic by default. Not part of the design build; wired at Step 24; the referral script must be updated to target `data-signup-link` (spec section 7) |
| 2 | DMCA link `/dmcareport` in the footer (user rule: no DMCA mention on Home; dropping a DMCA contact link may have a legal consequence, ask the legal owner) | Not drawn; flagged for Step 24 |
| 3 | Pricing link `https://www.shopbase.com/pricing` (K1) in the header | Not built; confirm to add |
| 4 | Footer link set (K3-K6 incl. Help, Blog, Developers, Updates, Templates, Status, legal links) | The twelve approved labels as links to the live destinations (App Store and Google Play only once URLs exist, row 5); K3 (`/features/*`) and K4 not built |
| 5 | App Store and Google Play exact URLs | Labels left off until the user gives the URLs |
| 6 | Legal entity name and year ("OpenCommerce Group, Inc", `support@shopbase.com`, 2021 dates are on the legal pages) and cookie/consent text | No copyright line, no cookie text; nothing invented (user's decision only) |
| 7 | Mobile header menu icons: Lucide `menu` and `x` are not yet in `02-assets/icons/` | Add the two files unchanged |
| 8 | Mobile field radius (proof renders field and card both at 1rem; probably meant field 1.5rem) | Keep 1rem; one-line change in the mobile `:root` block |
| 9 | How the two variants go live (one URL with a traffic split, two URLs, or one in reserve), which tool splits traffic (none known; Google Optimize is retired), whether the live page stays as a control, how the variant id reaches sign-up without breaking the referral parameters; canonical, title/meta per variant | Not decided; the build keeps one file per variant and adds nothing (blocks publishing, not building) |
| 10 | Sticky header (S05-S08 carry no button; header is the only primary button mid-page) and mobile menu holding the primary button | Sticky; button inside the mobile menu |
| 11 | Two output files, A first | `09-final-ui/final-ui-A.html` first, then `final-ui-B.html` |
| 12 | Accept the caps (10 sections, 9,000 px, 16,000 px mobile or stricter 13,500 px, 4 boxes, 1 primary CTA per section) | Used as ASSUMPTION |

### (c) Only the user can supply

- The six "Illustration" images IMG01-IMG06 (3:1, 1200 x 400 px, `02-assets/images/IMG##-name.png`) or `skip images`. Slots: IMG01 scan-card (S05, and top crop in S03), IMG02 proposed-fix-card (S06), IMG03 approval-card (S07), IMG04 offer-card (S08), IMG05 store-with-scan-card (S10), IMG06 finding-and-fix-on-store (S12). Prompts: `08-claude-design-input/image-prompts.md` (no text, numbers, faces, logos in any image; an image generator will not produce an accurate ShopBase interface, so every picture stays labelled "Illustration").
- Proof for AI claims: none exists; the page shows what the AI does without result numbers.
- Answers about existing merchants (E1-E8 in `04-brand/09-messaging.md`: migration, plan, AI included or extra, what became of PrintBase/PlusBase, apps, support, removed items) and a reason for the change. Until then Home stays silent.
- Analytics baseline and a target (none supplied); confirmation that GA4 or GTM exists elsewhere (only Universal Analytics `UA-138241145-1` and Google Ads `AW-944639611` are in the HTML).
- The rest of the 20-item list in `05-content/13-content-brief.md` ("Data the user must supply").

### (d) Unconfirmed claims fenced out of the build (do not publish or build)

S11 (B's parts list, CONDITIONAL); the "Free Launch plan" line; S08's link line; the screenshot's outcome headline "AI that turns visitors into buyers, and every order into a bigger one." (ALTERNATE); "raise order value" (the default says "aimed at order value"); "built in"; "No apps to stitch together". The approval behaviour "You approve every change" is UNPROVEN (kept only as the hero sub-line sentence and the S07 caption, with no control block, no undo claim).

### (e) Known weak spots stated honestly in the files

- Both hero headlines would fit a competitor's site (`05-content/14-copy.md` Review log, me-too test). The difference is wording only; the one line no competitor homepage carried is "You approve every change".
- Existing merchants cannot tell what happens to their store (E1-E8 unanswered).
- The VoC is interim (no Reddit; 2 of 71 quotes byte-verified; complaint-heavy sample).
- Competitor colours were not measured.
- Page lengths are estimates; nothing was rendered; nothing was rendered on a real phone.
- Header, footer, S04, S08, mobile menu, hover/pressed states are not in the proof.
- S04 (A only) has no source; the Content reviewer may cut it (kept by default at Gate 5).
- Not yet confirmed in `_progress.md`: the caps (ASSUMPTION, "awaiting the user's OK"); the Builder role (`_?`, default only).
- Must-keep items K1–K16 are all SUSPECTED; footer link labels are SUSPECTED; the referral script will not rewrite the new buttons as built (spec section 7).

---

## 9. What comes next

Output files named below for Steps 21–26 are **not yet created**.

| Step | Base prompt | What it needs | Stop on |
|---|---|---|---|
| 20 Part 1b → Gate 7 | `_prompts/20-master-spec.md` | First the user's "images done" or "skip images"; then end-of-turn block and GATE 7: the Strategy owner (the user) says `approved` in words | Do not move on without both; record Step 20 `done` and Gate 7 `APPROVED` with date and words in `_progress.md`. Stop |
| 21 Build | `_prompts/21-build.md` | The user drives Claude Design; Claude guides step by step: open the tool, load tokens/components, attach the files listed in `08-claude-design-input/build-prompt.md` (including every image), paste the build prompt, answer the tool's questions only from the spec (if the answer is not in the spec, say so and stop). Default output: two HTML files, `09-final-ui/final-ui-A.html` first, then `09-final-ui/final-ui-B.html`. The user exports and says **`build done`** | Gate 7 not APPROVED; images neither saved nor skipped. After guiding, STOP and wait. Note: the base prompts 21–25 name a single `09-final-ui/final-ui.html`; the spec's default (section 10, open decision 15) is two files, so Steps 22 and 23 run once per file (file names for the per-variant reports are not decided; ask). The user may change the default (e.g. build only A) |
| 22 UI self-review | `_prompts/22-ui-review.md` | The built file(s), `08-claude-design-input/master-spec.md`, `06-proof-ui/proof.html`, `03-research/12-sections.md`, `03-research/06-positioning.md`. Two-round loop; measure boxes, focal point, length, sections, hex outside `:root`, inline `style=`, `loading="lazy"`, contrast, copy, old-brand names; render and screenshot if possible (else `NOT RUN - no browser`). Output `09-final-ui/22-self-review.md` | A final-ui file does not exist |
| 23 Spec check | `_prompts/23-spec-check.md` | Compare build to spec row by row (sections, copy diff against `05-content/14-copy.md`, token drift, components, images, actions, hooks, caps, must-keep, old-brand count 0). Output `09-final-ui/23-spec-check.md`, then **Gate 8** (user approves) | Step 22 not `done` |
| 24 Pre-launch | `_prompts/24-prelaunch.md` | Checklist incl. type C items: old-brand scan with count 0 (exact command and output), redirects, SEO, legal pages with the correct entity, referral/tracking tags per the user's yes. Output `10-launch/24-prelaunch.md` | Gate 8 not APPROVED |
| 25 Publish | `_prompts/25-publish.md` | Route, handoff package, publish plan with rollback, smoke test. Output `10-launch/25-publish.md`, then **Gate 9** | Open 🔴 items from Step 24; no Publisher named (the Publisher is the user) |
| 26 Results | `_prompts/26-results.md` | Optional if the user does not want it. The Step 05 reading window (proposed 14 days) must have passed and the user must supply analytics data. Output `10-launch/26-results.md` | Gate 9 not APPROVED; reading window not passed; no data (never estimate) |

Feedback after Gate 8 goes back to the right step per the table in `_prompts/README.md` (visual bugs -> Step 22; wording -> Step 14; section order or length -> Step 12; USP unclear or me-too -> Step 06-07 or Gate 4). A change to an earlier step makes later steps `stale` (table in `_prompts/README.md`).

---

## 10. File map

Legend: LOCKED/APPROVED = do not change without a user decision; INTERIM = known to be incomplete; DRAFT = not cleared for publication; INPUT = user-supplied, never edit; EMPTY = expected to be empty now.

```
SB v2 LD/
  CLAUDE.md                     kit rules for Claude. DO NOT EDIT
  00-START-HERE.md              kit intro (Vietnamese). DO NOT EDIT
  00-workflow-map.md            full playbook (Vietnamese); phases, gates, on/off table. DO NOT EDIT
  _progress.md                  THE record of status, gates, roles, caps, Decisions log. Only the lead edits it
  handoff.md                    this file
  .gitignore                    lists .DS_Store only (.DS_Store and 02-assets/.DS_Store exist and are ignored)
  .git/                         clone of the kit repo (see section 12)
  _prompts/                     27 base prompts 00-26 + README.md. NEVER EDIT
  01-strategy/
    00-project-type.md          Step 00 output (type C). approved at Gate 0
    01-strategy-pack.md         Step 01. approved at Gate 0; USP UNPROVEN; persona content unverified
    brief.md                    brief confirmed by the user's answers 2026-10-24
    personas-draft.md           personas (internal opinion, unverified)
    source-persona-sheets.md    verbatim transcription of the user's Vietnamese persona sheets. INPUT
    strategy-pack-template.md   kit template
    README.md
  02-assets/                    user-supplied assets
    README.md
    logo/                       Logo (1).svg (white wordmark), Logo (3).svg (icon), Logo (6).svg (dark wordmark). INPUT, never edited
    fonts/                      InterVariable.woff2, LICENSE-Inter.txt, font-name.txt
    icons/                      arrow-right.svg, LICENSE-Lucide.txt, icon-library.txt (menu and x still to add)
    images/                     hero-2.0-reference.png (the user's hero screenshot, reference only). IMG01-IMG06 NOT YET PRESENT
    moodboard/                  style-ref-01-calendly-fullpage.png (user's Calendly capture) and screens/ (14 third-party crops in 5 folders S03-S10-hero, S05-S12-scan, S06-S12-proposed-fix, S07-approval, S09-closing-cta: internal reference only, never reproduce, never ship)
  03-research/                  README.md and
    02-intake.md  03-brief-analysis.md  04-audit.md  05-measurement.md  06-positioning.md
    07-voc.md                   INTERIM
    08-reference-analysis.md
    11-narrative-options.md  12-sections.md (approved at Gate 5; caps ASSUMPTION)
    16-palette.md               LOCKED (Option 1)
    16-palette-options.html     preview of the three options (Options 2 and 3 not chosen)
    17-moodboard.md
  04-brand/                     09-messaging.md, 10-identity.md (approved at Gate 3), README.md
  05-content/                   13-content-brief.md, 14-copy.md (both approved at Gate 5; 14-copy.md contains the Review log), README.md
  06-proof-ui/                  proof.html (APPROVED at Gate 6; the look), README.md
  07-tokens/                    1-primitive.json, 2-semantic.json, token-mapping.md (await Gate 7), README.md
  08-claude-design-input/       master-spec.md, image-prompts.md, build-prompt.md (await Gate 7), README.md
  09-final-ui/                  README.md only (EMPTY; the build goes here)
  10-launch/                    README.md only (EMPTY)
```

Not yet created (expected later): `02-assets/images/IMG01-scan-card.png` … `IMG06-finding-and-fix-on-store.png`; `02-assets/icons/` Lucide `menu` and `x`; `09-final-ui/final-ui-A.html`, `final-ui-B.html`, `22-self-review.md`, `23-spec-check.md`; `10-launch/24-prelaunch.md`, `25-publish.md`, `26-results.md`.

Never-edit files: the three logo SVGs; `02-assets/fonts/InterVariable.woff2`; the `LICENSE-*.txt` files; `02-assets/moodboard/` (third-party screenshots). `08-claude-design-input/master-spec.md` Appendix A is generated by code from `07-tokens/` (hand-off advice: regenerate it rather than hand-edit).

---

## 11. Pitfalls and traps for the next AI

1. Never treat a chat message, an earlier session or a file's existence as a gate approval. Gate 7 is `open`; only the user's words plus a `_progress.md` entry count.
2. Never decide the narrative or palette for the user. Both are settled (both options; Option 1); changing either makes later steps stale and needs a user decision.
3. Never reuse VoC quotes as copy or proof (interim, 2 of 71 byte-verified).
4. Never add numbers, percentages, scores, results or comparisons anywhere, including inside images and mock cards.
5. Never mention trademark, DMCA or restricted-product selling on Home (user rule; Content reviewer sign-off first). The `/dmcareport` footer link is an open decision, not a licence to mention it.
6. Do not carry old brand names or old promise wording: PrintBase, PlusBase, PrintHub, PlusHub, "Dropshipping Zone", "Print on demand" tabs, "in a few clicks", "all-in-one", "app mazes", the typing animation, "Book a demo", "Made in ShopBase" tiles. The Step 24 old-brand count must be 0. ("ShopBase Payments terms" and "Marketplace payments terms" are footer legal labels still marked NEEDS DECISION.)
7. The "Illustration" images are not real product UI. Keep the "Illustration" label on every one; never present them as screenshots.
8. Do not rebuild the proof or the spec from memory. Use `06-proof-ui/proof.html` and `08-claude-design-input/master-spec.md` (Appendix A is the `:root` block; copy it unchanged).
9. Build rules that Step 22/23 will measure: every design value in `:root` variables, 0 hex outside `:root`, 0 inline `style=`, no `!important`, no `loading="lazy"`, images with `width` and `height`, exactly one `<h1>` (the hero headline; the proof draws it as `<h2>`), one `<main id="main">`, a skip link, no motion, no gradient on text, no dark section.
10. Do not build fenced content: S11, the Free Launch plan line, S08's link line, the ALTERNATE headlines, "built in", "No apps to stitch together".
11. Do not invent footer links, URLs, legal entity, year or cookie text. Missing items stay `[NEEDS DECISION]` with the defaults in the spec.
12. Do not use Calendly's (or any reference's) assets, wording, illustrations or artwork. Only the structure approach is reproduced; the moodboard crops are internal references.
13. Do not rewrite the hero headlines to sound stronger: the screenshot's outcome headline is fenced; the descriptive headlines were approved. If the user wants to revisit the me-too finding, that is a Step 14/Gate 5 matter and makes Steps 18-26 stale.
14. Recorded writer/reviewer disagreements and judgement calls to know about: (a) `16-palette.md` F2 could not pass the standard border without becoming almost white, so a new field border `#66718A` was added (flagged as a judgement call); (b) the hero sub-lines no longer repeat the screenshot sentence word for word ("builds the fix" became "builds a proposed fix" in Step 15; the hero headlines keep "the fix"); (c) both meta descriptions had "You approve every change" removed at Step 15 (the brief allows it only as a caption or sub-line sentence); (d) Gate 6's three "visual judgement calls" were read by Step 19 from the proof (`07-tokens/token-mapping.md` section 2) because no earlier file defined them in detail; (e) `_progress.md` records Step 16 as `done (updated)` with the palette "being marked LOCKED"; the file itself says LOCKED.
15. Hierarchy of truth: `_progress.md` for status; `CLAUDE.md` over any prompt if they disagree (`_prompts/README.md`); for the look, the build must "match the proof exactly" (`_prompts/20-master-spec.md`, `build-prompt.md`), so if the spec and the proof disagree on the look, raise it with the user rather than pick silently.
16. Pain ids in the files (A1-A7, B1-B7, AI-1) come from the interim VoC. "AI-1" is a label for the VoC section "AI that changes the store", not a Step 07 id.

---

## 12. Repository note

- The folder is a git clone of the kit repo `https://github.com/TrienChill0710/Landingpage-workflow.git` (remote `origin`; one commit, the kit itself). When this file was written, all project work was uncommitted (new files untracked, `_progress.md` modified).
- Plan (not yet done when this file was written): commit the project, this file included, and push it to `https://github.com/TrienChill0710/Landing-Page-SB-v2.git` as a separate remote, which was not configured yet (only `origin`). The lead will confirm the push result in chat. To check: `git remote -v`, `git log`, `git status`.
- Commit and push only when the user asks.
- Before publishing the repo (especially if public), let the user decide on: `02-assets/moodboard/` (third-party screenshots of Calendly, Notion AI, Cursor, Intelligems: internal reference only, never reproduce or ship); `01-strategy/source-persona-sheets.md` and `personas-draft.md` (internal company persona sheets); local scratchpad paths that contain the macOS user name (cited in 8 step files).
- No passwords, API keys, private keys or personal e-mail addresses were found (search in "Verification"). The Google, Facebook, Sender and domain-verification ids in `03-research/04-audit.md` and `05-measurement.md` are public page-source ids, not credentials; `support@shopbase.com` is ShopBase's public support address.

---

## Verification

Fact-checked on 2026-10-26 against the project files, by script where possible (`python3 -I`, run outside the project):

- Status board: the header lines, 27 step rows and 10 gate rows are copied verbatim from `_progress.md`; statuses and dates diffed by script, 0 differences. Gate words checked one by one: "Approved", "Approve", "Approved", "approve", "Làm cả 2 đi", "Approved", "APPROVED" (Gates 0–6); Gates 7–9 `open`.
- Decisions log: 16 of 16 entries (13 dated 2026-10-24, 3 dated 2026-10-25); date, By and Affects match row by row; hand-off notes are bracketed.
- Numbers recomputed from the files: 80 primitive + 87 semantic tokens (JSON leaves with `$value`); 83 `:root` variables in `proof.html` and 83 in master-spec Appendix A; proof has 7 frames (S03, S10, S05, S06, S12, S07, S09); `_prompts/` has 27 step prompts; 14 moodboard crops. Hexes, hero promises, section orders and lengths (A 9 sections 4,864 / 4,943 px; B 7, or 8 with S11, 3,903 / 3,944 px), IMG01–IMG06 (3:1, 1200 × 400), audit counts, VoC counts and Step 15 round counts were each found in their source file.
- Every path cited was tested for existence; the only missing ones are marked "not yet created" (section 10) or are name patterns (`IMG##-name.png`).
- Confidentiality search (excluding `.git`): no hit for `@beeketing`, `password`, `token=`, `api_key`, `secret` (other than in this file's own sentence), `BEGIN PRIVATE KEY`, `ghp_`; one `sk-` hit is ordinary text in `03-research/08-reference-analysis.md`; "beeketing" appears only as the host `loc.beeketing.com` in the audit and spec.

Could not confirm:

- The date the repo was cloned (not in any file).
- Whether the destination repo `Landing-Page-SB-v2.git` exists; the push had not happened when this was written.
- The 500 px Chrome limit and the sleeping-laptop lesson (working session only; section 7.2).
- Which model wrote Steps 00 and 02 (their `_progress.md` notes do not say).
