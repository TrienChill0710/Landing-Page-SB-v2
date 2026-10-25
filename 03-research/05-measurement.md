# 05 · Measurement

Project: ShopBase website redesign · type **C · Rebrand** · page **P01 Home** · files in English · Gate 0 `APPROVED` · Steps 03 and 04 `done` (`_progress.md`).
Inputs read: `CLAUDE.md`, `_prompts/README.md`, `_prompts/05-measurement.md`, `_progress.md` (Decisions log), `01-strategy/01-strategy-pack.md` (§Goal & North Star), `01-strategy/brief.md`, `03-research/03-brief-analysis.md`, `03-research/04-audit.md`.
Source tags: `[brief]` = `01-strategy/brief.md` · `[pack]` = strategy pack · `[b-an]` = `03-research/03-brief-analysis.md` · `[audit]` = `03-research/04-audit.md` · `[log]` = Decisions log. Anything not in a source is `ASSUMPTION`. No analytics data exists in the project, so this file contains **no measured performance number**; the only numbers are counts quoted from the audit or computed by the check in "Checks run".

## North Star & formula

**Metric (one):** Home visitor to sign-up rate. Proposed by Claude in the brief, so `ASSUMPTION` [brief §1]. The pack's older wording ("sign-up-or-demo-request") is narrowed because the user answered that the primary CTA is sign-up only ("Get started for free") [log 2026-10-24] [b-an R6].

**Formula (explicit):**

```
Home visitor to sign-up rate  =  N_signup / N_visitors      over a reading window W

N_visitors  (denominator) = distinct visitors (browser or device id) with at least one
                            view of P01 Home (www.shopbase.com/) inside W.
N_signup    (numerator)   = those same visitors who reach the sign-up event (below)
                            in the same session as a Home view, inside W.
W           (time window) = see "Reading window" (proposed 14 full days, ASSUMPTION).
```

Every part is a default until the owner answers the question below:

| Part | Default (all `ASSUMPTION`) | Why it is open |
|---|---|---|
| "Sign-up" event | `signup_complete` = an account is created on `accounts.shopbase.com`. Store creation is a second, later event (`store_create_complete`), tracked but not the North Star. | The brief says "sign-up" but not whether that means create account or create store [brief §1] [b-an Q6]. |
| Visitor unit | distinct visitor, not session, so a returning visitor is counted once per W | The brief names the metric per "visitor" [brief §1]; the pack's older wording divided by Home sessions [pack §Goal & North Star]. No analytics tool is chosen; the unit depends on what the tool can count. Whichever unit is used, the baseline must use the same one. |
| Attribution | same session as a Home view | A visitor who returns days later and signs up directly would not count; the audit gives no data on how long visitors take. |
| Exclusions | internal staff traffic and known bots | Not specified by any input. |
| Segments (reported next to the total, not instead of it) | new vs returning visitors; device (desktop, mobile); source (paid, organic, referral/affiliate) | Current merchants also read Home [brief §2], and they log in rather than sign up, so they dilute the denominator. The split is needed to read the rate fairly. |

**Question (🔴 below, Q2):** what counts as a "sign-up": account created, or first store created? Default: account created.

## Baseline

**NOT AVAILABLE.** The user supplied no analytics, traffic or sign-up numbers [audit §Feedback: "No analytics, heat maps, sign-up rate or conversion numbers exist in the project"] [b-an Q15]. No value is estimated.

What the live page does show (from the audit's fetch of 2026-10-24, read from the HTML, not from a dashboard) [audit K7 to K11, "What does not work" 9]:

| Tag found on the live Home | Fact stated by the audit |
|---|---|
| Universal Analytics `UA-138241145-1` | The audit cites Google's help page: standard Universal Analytics properties "stopped processing hits" from July 1, 2023 (https://support.google.com/analytics/answer/11583528). |
| Google Ads `AW-944639611` | Present; its page_view event carries the placeholder text "replace with value". Whether the account is active is not verifiable. |
| Google Optimize `OPT-WTCPP3K` | Retired by Google on September 30, 2023 (https://support.google.com/optimize/answer/12979939), per the audit. |
| Facebook Pixels `1078285869667214` and `501990101818261` | Present. Whether the ad accounts are active is not verifiable. |
| Sender (email) | Present; hero email form posts to the sign-up route. Use unknown. |
| GA4 (`G-` id) and Google Tag Manager | **Not seen** in the HTML: no `G-` id and no `GTM-` container. The host `www.googletagmanager.com` does appear, but only as the gtag.js loader for the Google Ads id (`gtag/js?id=AW-944639611`; re-checked in review on 2026-10-24), not as a GTM container. The audit says whether GA4 or GTM exists elsewhere is unknown [audit K7, Q3]. |

So the page's own tags do not tell us which system, if any, holds trustworthy Home visit and sign-up counts. **No tool is named here as the source of truth.** The baseline must come from whatever the owner confirms records both numbers.

**How to get the baseline (🔴 Q1):**

| Number needed | Where it could come from (candidates, none confirmed) | Proposed date range (`ASSUMPTION`) |
|---|---|---|
| N_visitors: Home visitors | A web analytics tool that actually receives Home hits (GA4 or GTM if it exists elsewhere), or hosting / CDN logs if they exist. Unknown which exists. | Last 90 full days, as a weekly series, plus the same 90 days one year earlier if available (seasonality) |
| N_signup: accounts created | The ShopBase account database (counts accounts created regardless of any web tag); or the analytics tool above if it tracks `accounts.shopbase.com` | Same range, same weekly buckets |
| Split | Source (paid, organic, referral/affiliate), device, new vs returning | Same range |

Also ask: dates of campaigns, launches or outages inside the range, so spikes are marked rather than averaged in. Until this arrives, Step 26 has nothing to compare with; Steps 06 to 25 can run.

## Events to track

**Ground rules (all `ASSUMPTION` until the tooling question Q3 is answered):**

- Event names are `snake_case`. Parameters are listed so the same names work in any tool.
- The 2.0 Home direction the user gave: primary CTA "Get started for free", secondary CTA "Explore CR Scan AI" [log] [brief §1, §3]. The section list is decided at Step 12, so events are stated **per section type** and `section_id` is **TBD at Step 12** (Step 12 fills the ids; Step 21 implements them).
- Section types used below are generic (`header`, `hero`, `feature`, `proof`, `closing`, `footer`). Which of them exist in 2.0 is not known. Nothing here proposes a section.
- No analytics vendor is recommended. Whether the tool is GA4, GTM or another one is a question (Q3).

### A. Events for the 2.0 Home (to build)

| # | Page / section | Trigger | Event name | Parameters | Why |
|---|---|---|---|---|---|
| E01 | P01 · whole page | Home loads | `home_view` | `device`, `source`, `has_referral_params` | Denominator of the North Star. |
| E02 | P01 · each section type that holds the primary CTA `header`, `hero`, `feature`, `proof`, `closing` (ids TBD at Step 12) | Click on the primary CTA "Get started for free" | `cta_primary_click` | `section_type`, `section_id` (TBD at Step 12), `cta_label`, `destination` | Shows which placement starts sign-up. One event, one row per section type that carries it. |
| E03 | P01 · each section type that holds the secondary CTA (hero in the user's screenshot; others TBD at Step 12) | Click on the secondary CTA "Explore CR Scan AI" | `cta_secondary_click` | `section_type`, `section_id` (TBD), `cta_label`, `destination` | Measures interest in the AI USP. Its target is not decided (default: an on-page anchor, `ASSUMPTION` [b-an Q5]). |
| E04 | P01 · the section the secondary CTA scrolls to (TBD at Step 12) | That section becomes visible after an E03 click | `cta_secondary_target_view` | `section_id` (TBD) | Only needed if the target is an on-page anchor; skip if it is another page. |
| E05 | P01 · any section | Click on any link or button whose destination is `accounts.shopbase.com/sign-up` | `signup_outbound_click` | `section_type`, `section_id` (TBD), `cta_label`, `has_referral_params` (true or false), `destination` | Catch-all, independent of label. Lets the old and new page be compared even if labels change. |
| E06 | P01 · any section that holds a form (the live hero has an email form; 2.0 form presence unknown) | Form submitted | `signup_form_submit` | `section_type`, `section_id` (TBD), `form_id`, `field_count` | Required by the prompt. Conditional: only if the 2.0 Home keeps an email-first form (the audit calls it "worth testing, not deciding here" [audit OLD-02]). Never send the email address itself. |
| E07 | P01 · whole page | Scroll reaches 25 / 50 / 75 / 100 % of page height | `scroll_depth` | `percent` (25, 50, 75, 100), `device` | Required by the prompt. Shows where visitors stop. The 25/50/75/100 milestones are `ASSUMPTION` (a convention, not an input). Page height is unknown until Step 12 / 21. |
| E08 | P01 · every section (ids TBD at Step 12) | Section is at least half in view | `section_view` | `section_id` (TBD), `section_type`, `position` | Pairs with E07 to find the drop-off section. Thresholds (half in view) are `ASSUMPTION`. |
| E09 | P01 · header (and any other place a "Login" exists) | Click on a sign-in link | `signin_click` | `section_type`, `destination` | Separates current merchants (who log in) from prospects; they read Home too [brief §2]. |
| E10 | P01 · header, if kept | Click on a "Book a demo" link | `demo_link_click` | `section_type`, `destination` | Only if the link survives; the audit asks whether to keep it (audit Q5). It is not a Home CTA any more. |
| E11 | `accounts.shopbase.com` (outside P01) | Sign-up page loads | `signup_start` | `entry_page`, `has_referral_params` | Closes the gap between a Home click and a finished sign-up; shows form-level drop-off. |
| E12 | `accounts.shopbase.com` (outside P01) | Account created | `signup_complete` | `entry_page`, `source` | **Numerator of the North Star** (default definition, Q2). |
| E13 | `accounts.shopbase.com` or the app (outside P01) | First store created | `store_create_complete` | `entry_page` | Second-level outcome if the owner defines "sign-up" as a store (Q2). |

E11 to E13 live on `accounts.shopbase.com`, which the audit lists as a working first-party host. **Whether it can carry the same tracking, and who owns it, is unknown** (Q3). Without them the North Star cannot be computed from Home events alone.

Every primary CTA appears in the table: "Get started for free" (E02 by label; E05 also catches it by destination, not by label) and "Explore CR Scan AI" (E03). The numbers of sections per CTA are not stated because the section list is not decided.

### B. Current-state events (the live Home on 2026-10-24, to compare with)

The live page has **7 routes to `accounts.shopbase.com/sign-up`** and **5 spellings of one action** [audit "Routes to sign-up", "Sign-up labels"]. To compare old and new, E05 (`signup_outbound_click`) should be measured the same way on both pages, using the label as a parameter:

| Current-state sign-up route (audit) | Section | Label as spelled on the live page | Maps to |
|---|---|---|---|
| Hero email form, GET to `/sign-up` | OLD-02 Hero | "Join us" (placeholder "Enter Your Email") | E06 and E05 |
| Header button | OLD-01 Header | "Start Free Trial" | E05 |
| Header button (second spelling) | OLD-01 Header | "Start 14-Day Free Trial" | E05 |
| Tab 1 link (carries a utm) | OLD-04 Product tabs | "Find out more" | E05 |
| Feature-overview button | OLD-07 Feature overview | "Get started for free" | E05 |
| Service commitments button | OLD-10 Service commitments | "Start 14 Day Free Trial" (no hyphen, unlike the header) | E05 |
| Closing button | OLD-11 Closing CTA | "Get Started For Free" (capital letters differ) | E05 |

The live page also has "Book a demo" twice in the header: a text link to `/book-a-demo` and a button whose `href` is `accounts.shopbase.com/sign-in` (the audit calls it a likely mislabel, `ASSUMPTION`) [audit OLD-01, K2]. When compared, the text link is tracked as E10 (`demo_link_click`) and the button, by its destination, as E09 (`signin_click`) with `cta_label` "Book a demo", so the mislabel stays visible. The two "Login" links are E09.

**No live page click data exists**, so this table gives the structure to compare, not numbers.

### C. Tracking constraint to preserve: the referral / affiliate script

From the audit [audit K12]: an inline script reads the URL parameters `fpr`, `fpt`, `clickId` and `invite_trial`, stores them in cookies and every 3 seconds appends them to (a) sign-up or sign-in links that already contain `sign-in?` or `sign-up?` (only the tab-1 "Find out more" link on this page), (b) the two header sign-up buttons, (c) forms posting to `accounts.shopbase.com` (the hero form). If `fpr` is present it also posts the click to `api.shopbase.com/admin/affiliate/link-log`. The plain body buttons ("Get started for free", "Start 14 Day Free Trial", "Get Started For Free") and the sign-in links are **not** rewritten. This was read from the code, not tested in a browser, and the audit notes it looks buggy.

Constraints for measurement (and for Step 21 / 24):

1. The new instrumentation must not strip, rename or block these parameters, and must not break the cookies the script writes. A silent loss would cost referral credit [audit K12].
2. Because the script rewrites some links after load, the click events (E02, E05) must read the destination at click time, not at page load.
3. `has_referral_params` is recorded as true or false only. Parameter values are not logged by default (`ASSUMPTION`).
4. Whether the new primary CTA "Get started for free" must carry the parameters is not decided. Today the body buttons do not. Default: it must, so affiliate sign-ups from the new hero are not lost (Q6, 🟡).
5. Which tags stay on the new Home (Ads, Facebook Pixels, Sender, the retired Universal Analytics and Optimize tags) is the audit's open question [audit Q2]; this file does not decide it.

## Target

**No target set.** The user gave none [audit §Feedback] [b-an Q15] [brief §1: "no baseline or target"]. No target is invented, and none can be sensibly proposed before the baseline exists. 🟡 Q4 asks the owner for one (a number, a direction, or "just do not drop below the baseline").

## Reading window

Proposed by Claude, all `ASSUMPTION`:

| Item | Proposal | Reason |
|---|---|---|
| Minimum days | **14 full days** after launch, covering two full weekly cycles (weekday and weekend behaviour repeats) | A weekly rhythm is a common property of web traffic; nothing in the inputs confirms ShopBase's own pattern. |
| Read early? | Do not judge before day 14. Days 1 to 7 are for checking that every event in table A fires, not for comparing rates | New tracking can be wrong at first. |
| Compare against | The baseline's weekly series for the same weekdays (Q1), with campaign dates marked | Avoids comparing a campaign week with an ordinary week. |
| Launch confound (writer's addition, not asked by the prompt) | The new page changes the promise, the audience message and the CTA at once; a before/after comparison cannot separate those causes. Google Optimize, the A/B tool the page had, is retired (audit), and no replacement is known. | Say it plainly so Step 26 does not over-claim. |
| Visitor count | **BLOCKED until the baseline exists.** | See formula below. |

**Visitor count (formula only, no number).** The count of visitors needed per period depends on the baseline rate p1 and the smallest change worth detecting (p2 minus p1). Neither is known (no baseline, no target). A standard two-proportion formula, per group:

```
n = ( z(1 - alpha/2) * sqrt(2 * pbar * (1 - pbar))  +  z(1 - beta) * sqrt(p1(1 - p1) + p2(1 - p2)) )^2  /  (p2 - p1)^2
pbar = (p1 + p2) / 2      alpha = tolerated false-alarm rate      1 - beta = power
```

The value is not computed because choosing a baseline range here would be false precision, and the user told us nothing about it. Once the baseline (Q1) and a target or a minimum change (Q4) exist, Step 26 computes n by code, and the reading date becomes the later of 14 days and the day n is reached. Alpha and power are also `ASSUMPTION` until chosen (a common convention is 0.05 and 0.80; not an input of this project).

## Open questions (grouped, each with the default used)

### 🔴 Must answer
1. **Baseline numbers [needed before Step 26; Steps 06 to 25 can run].** Can you share Home visitors and accounts created for the last 90 full days, weekly, with source and device split, from whichever system actually records them? Which system is it (GA4 or GTM elsewhere, the account database, Google Ads, Facebook Ads Manager, other)? *Default: baseline stays `NOT AVAILABLE`; Step 26 can only report the new page's own numbers, not a change.*
2. **What is a "sign-up"?** Account created, or first store created? *Default: account created (`signup_complete`); store creation tracked as a second event.*

### 🟡 Should answer
3. **Tooling.** Is GA4 or Google Tag Manager set up somewhere the HTML does not show? Who owns `accounts.shopbase.com` tracking, and can events E11 to E13 be added there? Which tool should record the events? *Default: unknown; no tool chosen; event names and parameters are tool-neutral; the build keeps existing tags unchanged and adds nothing.*
4. **Target.** Is there a goal for the sign-up rate (a number, a minimum uplift, or "no drop")? *Default: no target set.*
5. **Reading date rules.** Is 14 days the right minimum, and who decides when the result is read? *Default: 14 full days, the Strategy owner reads.*
6. **Referral parameters on the new CTA.** Must the new primary CTA carry `fpr`, `fpt`, `clickId`, `invite_trial` (today only the header buttons, hero form and tab link do)? *Default: yes, all sign-up CTAs carry them.*

### ⚪ Nice to have
7. Which events beyond the minimum set matter (video plays, nav clicks, section views)? *Default: the E01 to E13 set only.*
8. Should internal and bot traffic be filtered, and is there a list of internal IPs? *Default: filter if the tool allows; no list assumed.*

## Assumptions

1. North Star "Home visitor to sign-up rate" is Claude's proposal, not the user's. `ASSUMPTION`
2. "Sign-up" = account created; store creation is secondary. `ASSUMPTION`
3. Denominator counts distinct visitors with at least one Home view; numerator requires sign-up in the same session; internal and bot traffic excluded. `ASSUMPTION`
4. Baseline range (last 90 full days, weekly, same period a year earlier) is a proposal. `ASSUMPTION`
5. Minimum reading window of 14 full days, and the "half in view" threshold for `section_view`. `ASSUMPTION`
6. Sections for events are generic section types; ids are TBD at Step 12. The 2.0 secondary CTA goes to an on-page anchor (from `[b-an]` assumption 2). `ASSUMPTION`
7. `accounts.shopbase.com` can be instrumented by the team. Unknown. `ASSUMPTION`
8. The referral script behaves as the audit read it; it was not tested in a browser. `ASSUMPTION`
9. No tracking tool is the source of truth; the tags seen on the page (audit) show what is installed, not what works. `ASSUMPTION`
10. Parameter values of the referral script are not logged. `ASSUMPTION`

## Checks run

Run with `python3 -I` on this file; results re-run in review on 2026-10-24:

- Event names in table A: **13 rows, 13 unique names, 13 of 13 match `snake_case`** (E01 to E13).
- Both 2.0 CTA labels appear in the event rows: "Get started for free" in 1 row (E02), "Explore CR Scan AI" in 1 row (E03); E05 covers sign-up links by destination.
- The words "NOT AVAILABLE" and "no target set" are present; the only "%" in the file is the 100 % scroll milestone; no sign-up rate or visitor count was written.
- Sample-size formula checked by code (Python `statistics.NormalDist`): with illustrative test values p1 = 0.05, p2 = 0.10, alpha 0.05, power 0.80 it gives 434.4 per group, the textbook value for this formula, and a simulation at n = 435 gave power 0.821. These test values are **not** project values and are not used anywhere else.
- Live Home re-fetched in review on 2026-10-24 (HTTP 200, 102,276 bytes, same size as the audit's fetch): the 7 sign-up routes and the label spellings in table B, the two "Book a demo" targets, and the tag ids above match the HTML.

## Check before handing back

- [x] North Star has an explicit formula (numerator, denominator, window).
- [x] No baseline or target was invented (baseline `NOT AVAILABLE`; target "no target set"; visitor count blocked, formula only).
- [x] Every primary CTA appears in the events table (E02 for "Get started for free", also caught by destination in E05; E03 for "Explore CR Scan AI").
- [ ] Section ids in events: **NOT DONE**, TBD at Step 12.
- [ ] Baseline value: **NOT AVAILABLE**, waiting for Q1.
- [ ] Gate 1 approval: **NOT GIVEN**. The Strategy owner approves the frame lock (Step 03) and the audit (Step 04) and says `approved`; `_progress.md` is updated by the lead, not here.
