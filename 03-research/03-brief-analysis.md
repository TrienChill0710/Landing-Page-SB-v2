# 03 · Brief analysis

Project: ShopBase website redesign · type **C · Rebrand** · page **P01 Home** · files in English · Gate 0 `APPROVED` · Step 02 `done` (`_progress.md`). Inputs: `01-strategy/brief.md` (confirmed 2026-10-24), `01-strategy/01-strategy-pack.md`, `01-strategy/00-project-type.md`, `01-strategy/personas-draft.md`, `03-research/02-intake.md`, hero screenshot `02-assets/images/hero-2.0-reference.png` (1890 x 866 px, read). Anything not in an input is `ASSUMPTION`. Numbers below were computed by code (Python 3 + PIL, RGB sampling and the WCAG formula).

## What the brief says

| Topic | Quote from `01-strategy/brief.md` |
|---|---|
| Goal | "Present ShopBase 2.0 ("ShopBase for the AI era") to experienced sellers and move them to **sign up**. Primary call to action: "Get started for free"; secondary: "Explore CR Scan AI"." |
| North Star | "Home visitor to sign-up rate. `ASSUMPTION`, proposed by Claude ... event definition open; no baseline or target." |
| Scope | "Home (P01) only; English only." |
| Audience | "Experienced dropshipping and POD sellers, Vietnam-based, selling to US/EU buyers. Primary A (dropshipper) and B (POD seller) have equal weight." · "Current merchants also read Home; what they need to hear is not stated." |
| Language | "The page itself is English only: no Vietnam-specific content and no promise of Vietnamese support." |
| Message | "CR Scan AI finds what stops shoppers and builds the fix; AOV AI recommends offers that raise order value; the seller approves every change." |
| Proof | "This describes what the features do. It is **not proof** that they raise CR or AOV. Results stay `UNPROVEN`: no numbers, no outcome promise until proof arrives." |
| Business model | "Business-model claim from the screenshot (unverified): the tick "Free Launch plan". Not confirmed separately by the user; plan details, limits and price unknown (open Q3)." |
| Changes | "promise moves to AI-first; ShopBase 2.0 is one independent product; PrintBase and PlusBase no longer exist as brands." |
| Stays | "ShopBase name, logo, colours." |
| Must-nots | "any mention, promotion or implied support of trademark, DMCA or restricted-product selling" · "numbers, outcome promises or comparative claims without proof" · ""Vít đè" in copy" |
| Must-keep | "none supplied. `ASSUMPTION`: none." |
| Tone / deadline | "Not supplied." |

Screenshot text, transcribed verbatim (user-supplied; its status is unknown): headline "AI that turns visitors into buyers, and every order into a bigger one." · sub-headline "CR Scan AI finds what stops shoppers and builds the fix. AOV AI recommends offers that raise order value. You approve every change. Store, catalog, payments, fulfillment and support are built in." · buttons "Get started for free" (arrow), "Explore CR Scan AI" · ticks "You approve every change", "Free Launch plan", "No apps to stitch together".

## Gaps

| # | Gap | Becomes |
|---|---|---|
| G1 | Status of the screenshot: live page, draft, or approved reference. Unknown. | Q1 |
| G2 | No proof that CR Scan AI / AOV AI raise CR or AOV (description only). | Q2 [BLOCKER for Step 09] |
| G3 | "Free Launch plan": no details (limits, duration, price, card needed) and no source for the claim beyond the user's word. | Q3 |
| G4 | "Store, catalog, payments, fulfillment and support are built in" / "No apps to stitch together": no product evidence. | Q4 |
| G5 | Where "Explore CR Scan AI" leads (a CR Scan page does not exist in scope; only Home is in scope). | Q5 |
| G6 | Sign-up event definition and whether a sign-up flow exists; no baseline, no target. | Q6 |
| G7 | Brand tone words. | Q7 |
| G8 | Deadline, legal review, tech stack, builder. | Q8 |
| G9 | What else is new in 2.0 and why now. | Q9 |
| G10 | What current merchants need to hear. | Q10 |
| G11 | Header nav on the new Home ("Print on demand", "Dropshipping", "Book a demo" no longer a CTA). | Q11 |
| G12 | Dark headers or dark mode planned? (`Logo (1).svg` is the white-wordmark file.) | Frame lock, Q12 |
| G13 | Brand primary blue (`#497BDF` logo vs `#0096ED` scale vs the screenshot's button blue, see Risks R4). | Q13 |
| G14 | Font family and icon set (needed before Step 16); intake notes are older than the screenshot. | Q14 |
| G15 | Numbers, feedback, must-keep list, real store domains in visuals. | Q15 |

## Questions for the client

### 🔴 Must answer
1. **Status of the hero screenshot.** Is it the live homepage, a draft, or a reference the team approved? *Default: reference only; its wording is quoted as input, not treated as approved copy.* `ASSUMPTION`
2. **[BLOCKER for Step 09] Proof of results.** Is there any evidence (data, case study, demo, merchant quote, internal test) that CR Scan AI / AOV AI raise CR or AOV? Is "CR Scan" a public name? *Default: results `UNPROVEN`; no numbers; outcome claims are flagged, not published as fact. Steps 04–08 can run.*

### 🟡 Should answer
3. **Free Launch plan.** What does it include, for how long, any limit or card required? Who may state it on Home? *Default: no plan details on Home; the words "Free Launch plan" appear only if you confirm the claim.*
4. **"Built in" and "No apps to stitch together".** Which of store, catalog, payments, fulfillment and support really ship inside ShopBase 2.0, in the markets the audience sells to? *Default: not stated as fact; flagged for confirmation.*
5. **"Explore CR Scan AI" target.** Where does it go (section on Home, other page, demo)? *Default: an on-page anchor to a Home section; no other page assumed.* `ASSUMPTION`
6. **Sign-up goal.** Confirm North Star "Home visitor to sign-up rate", the event (account created? first store?), and any baseline. *Default: as proposed; no baseline (Step 05 records "no baseline").*
7. **Brand tone words** (3 to 5, and words to avoid). *Default: none; Step 09 proposes options.*
8. **Deadline and constraints** (launch date, legal review, stack, builder). *Default: none; Claude produces, the user exports; no dates invented.*
9. **What else is new in 2.0, and why now?** *Default: Home presents only the AI USP.*
10. **Existing merchants:** a special message? *Default: no; they resemble A and B.*
11. **Header nav** on the new Home: which items stay? *Default: Home does not depend on them; the nav is not specified until Step 12.*
12. **Dark headers or dark mode?** *Default: no; light only.*
13. **Brand primary blue** (logo `#497BDF` or another). *Default: logo blue stays the brand colour; decided at Step 16.*

### ⚪ Nice to have
14. Font family (name, licence) and icon set. *Default: none chosen, nothing guessed; required before Step 16.*
15. Numbers, feedback, must-keep items, real store domains in visuals. *Default: none, none, none, no.*

## Frame lock

Status: **to confirm** (becomes LOCKED when the user confirms; approved at Gate 1).

| Item | Proposed default | Status |
|---|---|---|
| Devices | Responsive: desktop 1440 + mobile 375 | to confirm |
| Width / orientation | 1440 px, one long scrolling page | to confirm |
| Colour mode | Light only (the screenshot is on a white background). Dark headers and `Logo (1).svg` unused; need unknown (Q12) | to confirm |
| Language | English, no language switch | to confirm (user: "English only for now") |
| **Project language (for files)** | English | to confirm (already accepted in `_progress.md`) |
| Pages | P01 Home only | to confirm (user decision 2026-10-24) |

## Risks & unverifiable claims

Flagged only; no claim is rewritten.

**R1 · Outcome claims with no proof (headline and sub-headline of the screenshot).**
- "AI that turns visitors into buyers" promises conversion.
- "and every order into a bigger one" promises a larger order value for every order.
- "AOV AI recommends offers that raise order value" promises a result.
- "CR Scan AI finds what stops shoppers and builds the fix" claims a capability whose accuracy is unproven.
All are outcome claims. The brief says the screenshot "is not proof" and forbids "outcome promises ... without proof"; the screenshot's headline is itself an outcome promise, so the brief and the screenshot pull against each other. Needs Q1/Q2 before Step 09. "Every order" is an absolute and the strongest of these.

**R2 · "Built in" and "No apps to stitch together" (unverified).** "Store, catalog, payments, fulfillment and support are built in" and the tick "No apps to stitch together" are product-coverage claims with no source. They also touch pack open points: payments (the sheets say Stripe is unavailable in Vietnam and gateways get held; the pack records the payment business model as unknown), fulfillment (old PlusHub/PrintHub services are `SUPERSEDED/UNKNOWN`, pack Q7) and support (Vietnamese support unknown). The live nav showing "Apps" suggests an app ecosystem exists, which "No apps to stitch together" sits next to (observation, not a verdict).

**R3 · "Free Launch plan" is a pricing claim needing a source.** Known only from the screenshot (the user has not confirmed it separately). The pack says "no pricing or fee on Home" (pack Q6 default); a free-plan claim touches that rule. Needs Q3.

**R4 · Screenshot colours versus the logo.** Computed with Python PIL (available; run on the screenshot, sampled pixels, most frequent colour per region). Logo blue `#497BDF` = RGB (73, 123, 223), hue 220 degrees. Maximum RGB distance is 441.7.

| Sample | Hex | Hue | RGB distance to `#497BDF` (% of max) | Contrast vs white |
|---|---|---|---|---|
| CTA button fill ("Get started for free") | `#3B59F6` | 230 degrees | 43.4 (9.8%) | 5.32:1 |
| Headline gradient, left ("and every") | `#4454D0` | 233 degrees | 42.1 (9.5%) | 6.13:1 |
| Headline gradient, middle | `#565CD7` | 237 degrees | 34.6 (7.8%) | 5.37:1 |
| Headline gradient, right ("one.") | `#6862DD` | 243 degrees | 39.9 (9.0%) | 4.79:1 |
| Logo blue (reference) | `#497BDF` | 220 degrees | 0 | 4.05:1 |

The screenshot's accents are a more violet, more saturated blue than the logo (hue 230 to 243 vs 220 degrees); the gradient runs toward indigo/violet. Distance from the button to the intake's scale Primary 500 `#0096ED` is 85.3 (gradient samples: 99.1 left, 106.0 middle, 117.4 right), so the screenshot is closer to the logo than to that scale, but it matches neither. The brief says "ShopBase name, logo, colours" stay; whether this screenshot's blue counts as "the colours" is a conflict to resolve at Step 16 (Q13). The sampling is of anti-aliased gradient text; values are the most frequent saturated pixel per region, not an exact design token.

**R5 · Contrast of the screenshot's button.** White text (`#FFFFFF`) on the button fill `#3B59F6`: **5.32:1** by the WCAG 2.x formula, which passes AA for normal text (4.5:1). For comparison the logo blue under white text gives 4.05:1 (fails 4.5:1 for normal text; passes 3:1 for large text/UI). Re-check by the reviewer (same method): secondary button text `#121212` on white about 18.7:1; sub-headline grey `#676767` on white about 5.7:1 (both pass AA; approximate, anti-aliased text). Result applies to the screenshot only, not to a token decision.

**R6 · Conflicts between the strategy pack and the brief.**
- **CTA:** pack goal, North Star and Q5 say "sign up or book a demo"; the brief now says sign-up only. The pack is approved and not edited here; the brief/Step 05 North Star must read "sign-up rate". The pack's reason (live nav item "Book a demo") no longer drives the Home CTA.
- **Vietnamese pains vs English-only page:** the pack keeps the Vietnam-specific pains (180-day holds, Stripe not supported in Vietnam, no Vietnamese support, staying up at night for US/EU ads) and its default is "shape the message only". The brief now says "no Vietnam-specific content". Compatible only if those pains stay out of Home copy; the audience stays "Vietnam-based" while the page is English only (`ASSUMPTION`: they read English).
- **USP table:** the pack marks "what the feature does is unknown" for CR Scan and AOV; that is now partly answered by the screenshot (description only; results still `UNPROVEN`).
- **Pack Q2 and Q1:** Q2 is answered by the user (English only, no promise); Q1 is half answered (description yes, proof no).
- **Screenshot vs pack:** the pack's USP says AI "helps increase" CR and AOV and its Q1 default allows "no outcome promise beyond the user's wording"; the screenshot headline is stronger ("turns visitors into buyers", "every order", R1). The screenshot also touches pack unknowns: payments and fulfillment "built in" vs pack Q6/Q7 (R2), "Free Launch plan" vs "no pricing or fee on Home" (R3), and its blue vs "colours stay" (R4).
- **Project-type file and `03-research/02-intake.md`** had status wording that predated the answers (Home job "sign up or book a demo"; open Vietnamese-support point; "waiting for the brief [BLOCKER]"). Fixed in review on 2026-10-24 (status wording only).

**R7 · Other unverifiable items carried from the pack.** The USP is entirely `UNPROVEN`; persona content is internal opinion; "ShopBase for the AI era" is a positioning claim; "You approve every change" is a product-behaviour claim (how approval works is unknown); the Content risk on trademark/DMCA/restricted products stays off Home.

## Assumptions

1. The screenshot is a reference, not approved copy, until the user says otherwise. `ASSUMPTION`
2. "Explore CR Scan AI" goes to an on-page section. `ASSUMPTION`
3. The North Star is "Home visitor to sign-up rate"; the event is undefined. `ASSUMPTION`
4. Frame lock defaults: responsive 1440 + 375, 1440 px one long page, light only, English with no switch, files in English, P01 only. `ASSUMPTION` until confirmed.
5. English-only readers among Vietnam-based sellers. `ASSUMPTION`
6. No tone, deadline, legal step, tech stack, must-keep list, numbers or real domains were supplied; none invented. `ASSUMPTION`
7. Colour values in R4 are sampled from a screenshot and may differ from the source CSS (compression, gradient, anti-aliasing). `ASSUMPTION`
8. The `#0096ED` scale value comes from the user's earlier chat screenshot, which is not stored in the project (intake W9); distance figures to it are unverifiable here.

## Next

Next: Step 04 (Audit of the existing page, types B and C). Please confirm the frame lock above; it is approved at Gate 1. Step 09 stays blocked until Q2 (proof) is answered.
