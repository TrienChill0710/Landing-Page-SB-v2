# 06 · Positioning & competitors

Project: ShopBase website redesign · type **C · Rebrand** · page **P01 Home** · files in English · Gate 0 and Gate 1 `APPROVED` (`_progress.md`, 2026-10-24).
Inputs read: `CLAUDE.md`, `_prompts/README.md`, `_prompts/06-positioning.md`, `_progress.md`, `01-strategy/01-strategy-pack.md`, `01-strategy/brief.md`, `01-strategy/personas-draft.md`, `03-research/03-brief-analysis.md`, `03-research/04-audit.md`, `02-assets/images/hero-2.0-reference.png`.

## How this was researched (method and limits)

- **Web access: yes.** One WebSearch (standard) to pick candidates, then WebFetch on each competitor's homepage. **All fetches on 2026-10-24.**
- **Limit that matters:** WebFetch converts the page to text and a small model answers the question, so its "verbatim" quotes were not reliable on their own.
- **Review re-check (byte-verified, 2026-10-24, server dates 05:52:26–05:52:29 GMT):** all five homepages were downloaded with `curl -L` and a desktop browser User-Agent (all HTTP 200, no block; every page carries its text in the static HTML, none is client-side only) and parsed with Python `html.parser` (visible text, title, meta, H1/H2, links). Every quote in this file was matched against that text; quotes that did not match were corrected (Shopify and Wix figures, a BigCommerce line, Printify's pricing link and AI nav item). What the static HTML cannot show (images, layout, what animates) is still `NOT VERIFIED`; no rendered browser view was made. Re-check before any line is reused or compared in public.
- Competitor homepages change often (Shopify and BigCommerce are campaign-driven). These are a snapshot of 2026-10-24, not a standing fact.
- The search results were mostly affiliate or vendor blogs (the search tool itself warned of this). They were used **only to pick names**, never as a source of a competitor claim. Every claim below comes from the competitor's own homepage.
- Competitors were picked by the type of seller the page targets (experienced dropshipping and POD sellers), not from memory alone: Shopify is named by the user's sources; the rest come from the search (store builders and dropshipping/POD platforms) and are justified in the table.

## Competitors

All rows: fetched 2026-10-24. Quotes are the competitor's own words.

| Competitor | Type | Why picked (one line) | Their headline and promise (verbatim) | USP they claim | Where they look like everyone else | Link |
|---|---|---|---|---|---|---|
| **Shopify** | direct | The default store builder for dropshipping and POD; named in the user's sources; the persona's "platform they currently use" is most likely this (`ASSUMPTION`). | H1 "Be the next" + a rotating phrase; the static HTML lists "AI all-star", "household name", "solo-preneur", "category creator", "global empire", "store they line up for", "big thing" (which one shows first in a browser: `NOT VERIFIED`). Sub: "Dream big and build fast on Shopify. The world's best commerce platform." Page title: "Shopify: The All-in-One Commerce Platform for Businesses". | "The world's best commerce platform"; scale and ecosystem: stats strip "High-intent shoppers 250M+", "The Shopify App Store has 21,000+ commerce apps". AI: "Your very own commerce AI", "Spot opportunities for growth and automate tedious tasks with Sidekick.", "Hyperdriven by AI. Commerce to the core." | Primary CTA "Start for free"; "Pricing" in the nav; named-merchant stories (e.g. "Jackie Prince launched Guests on Earth out of her home. Now it's a $4M+ business.") and a stats strip; "world's best" superlative. | https://www.shopify.com/ |
| **Wix eCommerce** | direct (general store builder) | Mass-market store builder that sells to the same first-store and small-seller searches; appears in the search as the beginner alternative. | "BUILD AN ECOMMERCE WEBSITE". Sub: "Start selling immediately. Grow without limits." "Get everything you need to build, run and scale your business—on one AI-powered eCommerce platform." | "one AI-powered eCommerce platform" + no-code design. AI, as two named features: "AI product descriptions" ("Uplift conversions and SEO performance with unique AI product descriptions.") and "AI product recommendations" ("Increase your average order value with related products sections at checkout."). | CTA "Create Your Store"; static desktop-and-mobile mockup of a sample store; review count "based on 10,760+ reviews" and "over 1M sites"; "Start for free. Upgrade anytime." | https://www.wix.com/ecommerce/website |
| **BigCommerce** | direct (store builder, mid-market) | Established store builder that now leads with AI; shows how a competitor frames AI. Less aimed at first-time dropshippers (`ASSUMPTION`). | "Get your brand ready for agentic commerce." (page title: "Commerce built for momentum.") Sub: "AI agents are changing how customers discover, evaluate, and buy." | "our open platform", "new agentic-ready features built to grow with the shift"; "Over 1,200 apps", "600+ integrations". AI: "AI is the new shopper. Be its first pick." and "Meet Companion: an AI assistant that answers questions, surfaces insights, and handles operations for you." | Customer and partner logo wall; analyst/ROI stats ("211% ROI within 8 months", cited to a 2023 Forrester report); "Get a demo" and "Try for free" in the header; "Pricing" link. | https://www.bigcommerce.com/ |
| **Printify** | direct for persona B (POD) | The largest POD-specific platform in the search results; the POD seller's other main tool. It is a fulfilment layer, not a store builder, so it is a partial competitor. | "Create and sell custom products". Hero checklist: "100% Free to use", "2000+ products", "Global delivery." | No upfront cost: "On-demand orders mean no upfront cost" (meta), "Start with $0 investment". **No AI claim in the hero or body copy**; the only AI mention is a nav link "AI Image Generator". | CTA "Get started for free" ("No credit card required"); "Trusted by 10M+ sellers"; press logos (image alts: Forbes, CNBC, The Wall Street Journal, Business Insider and others); a Shopify logo next to a "4.8" star rating (it sits on top of Shopify rather than replacing it); "Pricing" link in nav and footer (`/pricing/`) despite "100% Free to use". | https://printify.com/ |
| **Zendrop** | direct for persona A (dropshipping) | All-in-one dropshipping platform that also gives a store; its AI claim targets the same seller. | "The Fastest Way to Start a Profitable Dropshipping Business". Sub: "The all-in-one dropshipping platform. Get a free AI-built store. Discover winning products." | "all-in-one" (FAQ: it "controls the entire process from the factory to the customer"). AI: "Get a free AI-built store." and "Create high-converting UGC video or image ads for any Zendrop product in minutes." | CTA "Try for free"; "Trusted by over 5,000,000+ sellers"; media logos; Trustpilot and Shopify App Store badges; "/pricing/" link; a trending-products showcase. | https://www.zendrop.com/ |

**Not picked, on purpose:** WooCommerce, Sellfy, OnPrintShop, Ecwid (appeared in the search but are open-source, creator-led or web-to-print; weaker fit). CJdropshipping, Gelato, GemPages and others were not researched: `NOT RESEARCHED`. Ask the user (Q1).

### Is "AI-first" already a common claim in this category?

An AI claim in the hero or body copy on 4 of the 5 homepages (byte-verified); Printify has none in its copy, only a nav link "AI Image Generator" (so the word "AI" appears on 5 of 5). In their own words:

| Competitor | Exact AI claim | What the AI is for |
|---|---|---|
| Shopify | "Your very own commerce AI" · "Spot opportunities for growth and automate tedious tasks with Sidekick." · "Hyperdriven by AI. Commerce to the core." · "Get discovered across AI channels. Shoppers check out right in the chat. You don't lift a finger." | assistant for the merchant; being sold through AI chat |
| Wix | "one AI-powered eCommerce platform" · "Leverage built-in AI features and exceptional no-code creation to turn your vision into reality even faster." · "AI product descriptions": "Uplift conversions and SEO performance with unique AI product descriptions." · "AI product recommendations": "Increase your average order value with related products sections at checkout." | building faster; product text; related-product recommendations for order value |
| BigCommerce | "Get your brand ready for agentic commerce." · "Meet Companion: an AI assistant that answers questions, surfaces insights, and handles operations for you." | selling to AI shoppers; ops assistant |
| Zendrop | "Get a free AI-built store." · "Create high-converting UGC video or image ads for any Zendrop product in minutes." | store creation; ad creative |

Finding: **"AI" as a word is not unique to ShopBase; 4 of 5 pages make an AI claim in their copy (5 of 5 if Printify's nav link counts), and two put it in the product description line (Wix "one AI-powered eCommerce platform", Zendrop "AI-built store").** Wix even pairs the same two outcomes with two named AI features (conversions via "AI product descriptions", order value via "AI product recommendations"). What none of the five says, in the static text of these homepages on 2026-10-24, is that AI scans the store for what stops shoppers and that the seller approves each change (the words "approve"/"approval" in a seller-control sense appear on none; BigCommerce's "Approvals without the slowdown" is about B2B buyer roles). That is an observation about 5 homepages on one day, not proof that nobody says it (`NOT VERIFIED` beyond these pages).

## Category patterns

Counted over the 5 pages fetched (n = 5, a small sample; a pattern here means "most of these five", not "the whole market").

| Pattern | Count | Detail |
|---|---|---|
| Social proof block (merchant count, stars, logos, testimonials or stats) | **5 / 5** | Shopify stats + named-merchant stories + merchant domain list; Wix "1M sites" + reviews; BigCommerce logos + ROI; Printify "10M+ sellers" + press; Zendrop "5,000,000+ sellers" + media |
| Giant scale number ("1M", "5M", "10M", "250M") | **4 / 5** | Shopify, Wix, Printify, Zendrop (BigCommerce uses ROI and app counts) |
| Free-entry CTA somewhere in header/hero ("Start for free", "Try for free", "Get started for free", "Start for free. Upgrade anytime.") | **5 / 5** | Shopify "Start for free"; Wix "Create Your Store" + "Start for free. Upgrade anytime."; BigCommerce "Try for free" (header); Printify "Get started for free"; Zendrop "Try for free" |
| Hero primary button wording | 3 / 5 say free | Shopify "Start for free", Printify "Get started for free", Zendrop "Try for free"; Wix "Create Your Store"; BigCommerce "Explore Agentic Commerce" |
| Demo or sales route in the nav | 1 / 5 | BigCommerce "Get a demo" (this is the only one; ShopBase's live page also has "Book a demo") |
| Pricing link | **5 / 5** | Shopify `/pricing`, Wix `/plans`, BigCommerce `/pricing/`, Printify `/pricing/` (nav and footer), Zendrop `/pricing/` |
| AI claim in the Home copy | **4 / 5** (5 / 5 counting nav links) | see the table above; Printify only has a nav link "AI Image Generator" |
| Hero visual | **4 / 5 confirmed** | background photo (Shopify), static store mockup (Wix), diagram (BigCommerce), product showcase (Zendrop); Printify's hero image `NOT VERIFIED`. **None was reported as a live product screen showing AI recommending a change** (`NOT VERIFIED`: static HTML only, images not viewed) |
| Superlative or "all-in-one" framing | **4 / 5** | "world's best commerce platform"; "one AI-powered eCommerce platform"; "all-in-one dropshipping platform" (Zendrop; title "The #1 high margin dropshipping platform"); Printify "Everything you need to start your own online business"; BigCommerce ("open platform", "agentic-ready") is the exception |
| Headline names a category outcome in generic terms ("build / start / create a store or business") | 4 / 5 | Shopify (rotating), Wix, Printify, Zendrop; BigCommerce leads with a trend (agentic commerce) |

What a visitor therefore expects: a big headline, one free CTA, a number proving scale, a logo or testimonial row, a pricing link, a sample-store visual. Skipping any of these is not harmful by itself, but copying all of them makes the page look like the other five.

## "Me too" test

**Our promise, in the user's words only:** the hero screenshot headline "AI that turns visitors into buyers, and every order into a bigger one." Sub-line from the same screenshot: "CR Scan AI finds what stops shoppers and builds the fix. AOV AI recommends offers that raise order value. You approve every change. Store, catalog, payments, fulfillment and support are built in." Check-marks: "You approve every change", "Free Launch plan", "No apps to stitch together". USP (strategy pack): AI "CR Scan" and "AOV" help raise conversion rate and order value; the seller stays in control.

**Closest competitor lines:**

| Competitor line (verbatim) | Overlap with ours |
|---|---|
| Wix: "Uplift conversions and SEO performance with unique AI product descriptions." and "Increase your average order value with related products sections at checkout." | Closest on **the two outcomes** (conversions, average order value), each under a named AI feature ("AI product descriptions", "AI product recommendations"). Wix ties conversions to a text generator and order value to related-product recommendations at checkout; it does not say the AI scans the store or that the seller approves changes |
| Wix: "one AI-powered eCommerce platform" / Zendrop: "The all-in-one dropshipping platform. Get a free AI-built store." | Overlap on **"AI + all in one"**; ours says "No apps to stitch together" |
| Shopify: "Spot opportunities for growth and automate tedious tasks with Sidekick." | Closest on **"AI finds opportunities"**. Sidekick is framed as an assistant, with no stated conversion or order-value outcome in the homepage text |
| BigCommerce: "Meet Companion: an AI assistant that answers questions, surfaces insights, and handles operations for you." | Overlap on "AI that handles things for the merchant" |

**Would a reader confuse ours with theirs?** Partly. The sentence "AI helps your store sell more" would be confused with Wix and Shopify; a reader who skims only the first line of ours ("AI that turns visitors into buyers") sees a claim of the same kind as "Uplift conversions ... with AI". What is different, **by the wording alone**:
1. A *scan of the store* for what stops shoppers, which then builds the fix (CR Scan AI), paired with an order-value recommender (AOV AI), in the hero. Naming both outcomes with two AI features is **not** new on its own: Wix does it lower on its page ("AI product descriptions" for conversions, "AI product recommendations" for order value). The difference is the scan-and-fix mechanism and its place in the hero, a difference of description only.
2. "You approve every change." The static text of the five competitor homepages contains no seller-approval statement (byte-checked: no "approve" on any page; BigCommerce's "Approvals without the slowdown" is about B2B buyer roles). Shopify's "You don't lift a finger" is the opposite tone (about AI channels, not about store changes).
3. The same promise on a store that includes "payments, fulfillment and support" (ShopBase's platform scope; compare Zendrop "all-in-one").

**Is the difference provable?** **No, not today.** Every part of the USP is `UNPROVEN` (strategy pack): there is no result, no test, no customer number for CR Scan AI, AOV AI or the approval flow. Difference 1 and 3 are differences of *description* (what the product is called and includes), which can be shown on the page by showing the feature. Difference 2 (the seller approves) is a product behaviour that the page can state only if the product really works that way (user's screenshot says so; not tested here). **The claim "raises conversion rate and order value" cannot be differentiated from Wix's "Uplift conversions" without proof**; with no proof, it is a claim of the same strength as theirs. Proof that would change this: a measured before/after, a named merchant case, or a visible product screen. Competitors do print numbers as their own claims (Wix "24% increase in monthly revenue for stores using Wix SEO tools"; Shopify's stats strip "Higher conversions 15%" under "The world's best-converting checkout"; neither checked, both are the competitors' claims, not facts), so a number-free AI promise is weaker against them.

## Our position

For experienced dropshipping and print-on-demand sellers, ShopBase 2.0 is one store platform with built-in AI that finds what stops shoppers (CR Scan AI) and recommends offers that raise order value (AOV AI), where the seller approves every change.

(This restates the USP and the hero-screenshot text; it adds no result and no claim. Whether "for experienced dropshipping and POD sellers" is said on the page is a Step 09/11 decision; the audience is from the personas.)

## Old vs new positioning (type C)

| | **Old (live page, audit 2026-10-24)** | **New (USP, Gate 0)** |
|---|---|---|
| Promise | "Build a profitable E-commerce business in a few clicks with ShopBase" (H1; "E-commerce" cycles through "Dropshipping" and "Print-On-Demand") | "AI that turns visitors into buyers, and every order into a bigger one." |
| Role of AI | none: 0 mentions on the page | the core: CR Scan AI and AOV AI |
| Product | per-model tabs: E-commerce brands / Dropshipping / Print-On-Demand (+ Digital products in the mobile block); old brands PrintBase and PlusBase still named | one independent product, ShopBase 2.0 |
| Seller's role | "Team ShopBase will handle everything for you" (testimonial); "app mazes" removed by being all-in-one | the seller approves every change |
| Entry offer | "Start 14-Day Free Trial" | "Free Launch plan" (screenshot) |
| Type of benefit | speed and ease of building | outcome of the store: conversion and order value |

**What the reader must now believe:**
1. ShopBase is a place to *raise a store's sales*, not only to *set one up in a few clicks*.
2. An AI tool can find what stops shoppers and build the fix, and another can recommend offers that raise order value (`UNPROVEN`).
3. They stay in control: nothing changes without their approval.
4. One product covers store, catalog, payments, fulfilment and support, with no separate apps.

**What the reader must stop believing (current merchants and returning visitors read this page too):**
1. That ShopBase is a quick store builder with three separate products for three business models.
2. That PrintBase and PlusBase are separate brands.
3. That the free entry is a 14-day trial (if the Free Launch plan replaces it; open in the brief).
4. That AI on a store builder means a text writer or a chat assistant (the category's common use of the word, see the table).

## Implications

Each line points to a finding above.

1. **Because 4 of 5 competitor homepages already make an AI claim in their copy (Shopify, Wix, BigCommerce, Zendrop; Printify links an "AI Image Generator") and Wix says "one AI-powered eCommerce platform", the page must not rest on the word "AI" alone;** the hero must name the two specific tools (CR Scan AI, AOV AI) and what each does, as in the screenshot. [AI claims table; me-too test]
2. **Because Wix already says "Uplift conversions" and "Increase your average order value" under named AI features, the page must show the difference by showing the feature (a real product view of what CR Scan AI finds and the fix it builds),** not by repeating the outcome words. [me-too test]
3. **Because no seller-approval statement appears on any of the five homepages (static text, 2026-10-24) and Shopify's tone is "You don't lift a finger", the page must keep the approval statement in the hero and show one approval step in the product view.** It is the only line that separates our AI from the rest on wording alone; it is true only if the product behaves this way, so the user confirms (Q3). [me-too test]
4. **Because the difference is not provable and every USP part is `UNPROVEN`, the page must not state a number or an uplift for conversion rate or order value until proof arrives,** and Step 09 stays blocked on proof. Competitors print figures as their own claims (Wix "24% increase in monthly revenue for stores using Wix SEO tools", Shopify "Higher conversions 15%"), so the page must replace them with something checkable (a feature screen, a named merchant, a dated result) or say less, not invent a number. [me-too test; strategy pack proof table]
5. **Because 5 of 5 competitors show a scale number or logo block and the old page has unsourced numbers ("$700 Millions+", "365,500+ merchants"),** any proof strip on the new page must carry a source and a date, or be left out. Copying the category's scale-number habit with unverified figures would weaken the "seller in control, no hype" tone. [category patterns; audit "What does not work" 4]
6. **Because 5 of 5 competitors show a free-entry CTA and the old page has 5 spellings of the sign-up action,** the page must use one primary CTA with one label ("Get started for free", from the screenshot) everywhere, and a secondary CTA ("Explore CR Scan AI") that goes to the feature, not a second sign-up. [category patterns; audit finding 6]
7. **Because the category hero visual is a store mockup, a photo or a diagram, and none was reported to show AI changing a store,** the hero visual should be the product doing the AI work (one focal point, N5), which is also the evidence the claim needs. Whether such a screen exists is open (Q4). [category patterns]
8. **Because the old page sells three products by audience and names dead brands, and the new position is one product,** the Home must drop the per-model tabs, the typing animation and PrintBase/PlusBase, and answer both personas (dropshipper, POD seller) inside one story, not in separate tabs. [old vs new; audit "What does not work" 2 and 3]

Persona note (no Vietnam content on the English Home): the personas' pains are payment holds, ad-account problems, copied products, conversion and disputes (`personas-draft.md`, all `ASSUMPTION` until Step 07). None of the five homepages speaks to payment holds or disputes as a seller pain (static text searched; the only hit is a Wix FAQ line that fraud checks "help reduce chargebacks"). Step 07 should check whether that is an open lane before Step 11.

## Assumptions

| # | Assumption | Status |
|---|---|---|
| A1 | The five competitors are the right set for this audience. Picked by Claude from search, not named by the user (except Shopify, from the user's sources). | `ASSUMPTION`, ask Q1 |
| A2 | The persona's current platform is most likely Shopify. | `ASSUMPTION — not verified online` |
| A3 | BigCommerce is less aimed at first-time dropshippers than the others. | `ASSUMPTION` |
| A4 | Quotes were byte-checked against the static HTML (curl, 2026-10-24); images, layout, and which rotating phrase a browser shows first could not be seen. | text verified; rendered view `NOT VERIFIED` |
| A5 | "No competitor says 'you approve every change'" is true only for the static text of 5 homepages on one day; deeper pages, product pages and Shopify Sidekick pages were not read. | `NOT VERIFIED` beyond these pages |
| A6 | Competitor figures (Shopify "Higher conversions 15%", Wix "24% increase in monthly revenue for stores using Wix SEO tools", BigCommerce "211% ROI within 8 months") are quoted as their claims, not checked. | competitor claims, unverified |
| A7 | The screenshot headline and sub-line describe the intended hero; it is not proof of results and not confirmed as final copy (progress log: "describes the features; not proof"). | user decision |
| A8 | Counts in "Category patterns" are over n = 5 and one day; they describe the sample, not the market. | stated limit |
| A9 | Zendrop's stats block is "0 M+" placeholders in the static HTML (filled by script); the "5,000,000+" claim is from the hero line only. | stats values `NOT VERIFIED` |

## Open questions

| | Question | Default used without an answer |
|---|---|---|
| 🟡 Q1 | Which competitors does the business actually lose deals to or compare itself with (for example Shopify plus which others: CJdropshipping, Gelato, GemPages, Wix)? | Use the five above; Shopify first. |
| 🟡 Q2 | Does ShopBase want to be compared with Shopify head-on (a "Compare ShopBase" item exists on the live nav), or position next to it without naming it? | No competitor named on the Home. |
| 🟡 Q3 | Is "You approve every change" true of the product as shipped (every CR Scan AI fix and every AOV AI offer waits for approval)? | Keep it, as the user's screenshot says it; flag in Step 09. |
| 🟡 Q4 | Is there a real product screen (CR Scan AI result, an AOV AI offer, an approval step) that can be the hero visual? | Assume none; Step 18 uses a placeholder labelled as such. |
| 🔴 Q5 | Any proof of results for CR Scan AI or AOV AI (a test, a beta merchant, a dated number)? (Already blocking Step 09.) | Page claims no result; the difference stays description-only. |
| ⚪ Q6 | Do you want a second research pass on Shopify's Sidekick and Wix's AI product pages to test the "no one says approval" finding? | Not done; finding stays marked `NOT VERIFIED`. |
| ⚪ Q7 | Does the Free Launch plan replace the 14-day trial? (Affects the "stop believing" line.) | Home says "Free Launch plan" only if the user confirms; otherwise only "Get started for free". |

## Check-list

- [x] At least 3 real competitors, each with a source link (5, links in the table; fetched 2026-10-24).
- [x] The me-too test quotes a real competitor line (Wix, Shopify, BigCommerce, Zendrop; byte-checked against the static HTML).
- [x] Our position matches the USP in the strategy pack and does not add claims.
- [x] Every implication points back to a finding (bracketed after each).
- [x] Quotes and pattern counts verified against the raw HTML (curl + Python, 2026-10-24); corrections made in review.
- [ ] Quotes seen in a rendered browser page: `NOT RUN` (no browser; images and animation unseen; see A4).
- [ ] Deeper pages (pricing, product, AI feature pages) read: `NOT RUN` (homepages only, as scoped).
