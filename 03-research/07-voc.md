# 07 · Voice of customer

Project: ShopBase website redesign · type **C · Rebrand** · page **P01 Home** · files in English · Gate 0 and Gate 1 `APPROVED` (`_progress.md`). Research date: **2026-10-24**.
Inputs read: `CLAUDE.md`, `_prompts/README.md`, `_prompts/07-voc.md`, `_progress.md`, `01-strategy/01-strategy-pack.md`, `01-strategy/personas-draft.md`, `01-strategy/source-persona-sheets.md`, `03-research/06-positioning.md`, `03-research/04-audit.md`.

> **STATUS: INTERIM VoC, NOT a full VoC.** (1) **No Reddit material at all**: Reddit could not be reached, so the communities the personas actually use are missing. (2) **Only 2 of 71 quoted strings are byte-verified** (S23, S25). The other 69 Trustpilot and Shopify Community quotes are `summariser-read, not byte-verified`: at review (2026-10-24) both sites answered a plain `curl` with HTTP 403 and a bot-check page ("Verifying your connection" / "Checking your browser"), so the live text could not be compared. (3) The sample is complaint-heavy and is not shown to be Vietnam-based sellers. **Use it for direction only. Do not put any quote into copy or show it externally until it is checked by hand on the live page.**

## READ THIS FIRST: what this file is and is not

- **Reddit was not reachable at all.** `WebSearch` rejected `reddit.com` as a domain ("not accessible to our user agent"). `WebFetch` refused `old.reddit.com` and the `.json` form. A `curl` attempt was blocked by the permission system and was **not** retried. No Reddit text was read, so **nothing from Reddit is quoted** and nothing is invented. The prompt's preferred communities (r/dropshipping, r/printondemand, r/shopify, r/ecommerce) are **missing** from this file.
- **What was read instead:** Trustpilot review pages of the platforms and services the personas use (page 1 of each filtered view), four Shopify Community threads (search-result excerpt only, no full page), one Hacker News comment fragment, and one vendor blog that relays forum quotes. See "Sources read".
- **Trustpilot reviews are reviews of a vendor.** Reviewers are not identified as "experienced", as dropshipper or POD seller, or as Vietnam-based. Many are small shop owners, some are buyers. Persona assignment below is **by topic** (`ASSUMPTION`), not by who the reviewer is.
- **Quote reliability:** `WebFetch` returns text through a small summarising model; Step 06 found such quotes unreliable until byte-checked. These quotes were **not** byte-verified. Treat each as "as returned by the fetch tool". Re-check against the live page before any line is reused in copy or shown to anyone.
- **Byte-check result (review, 2026-10-24):** each cited page was downloaded with `curl` and searched for the exact quoted string (whitespace and quote marks normalised). **Exact match: 2** (S25 Hacker News, "I was tired of the hidden app fees on Shopify (upsells, reviews, sourcing tools, etc. all cost extra)."; S23 SureBright relay of the S22 post, "After 5 months of struggling with Shopify's AI tools (Sidekick and Shopify Magic), I have decided to migrate", and S23 does link the S22 thread). **Paraphrased: 0. Not found: 0. Page not fetchable: 69** (68 Trustpilot strings, 5 of them short language phrases, plus 1 Shopify Community excerpt; HTTP 403 bot challenge, which was not worked around). So every quote below that does not cite S23 or S25 is `summariser-read, not byte-verified`. Its wording and its date or country label may be wrong. The ShopBase Trustpilot facts (rating, review count, star mix, country mix, the two copyright accusations, the AI request) could **not** be checked against the live page either.
- **Not enough for a full VoC.** There is real material (below), but it is a thin, complaint-heavy, non-Reddit sample. **Recommendation: ask the user to paste material** (their own customer interviews, support tickets, Facebook/Zalo group posts, or exported Reddit threads) to cover what is missing: the AI-trust question, conversion/AOV pain, ad-spend pain, and Vietnam-specific pain.

### What I could not reach
| Target | Result |
|---|---|
| Reddit (any subreddit, any form) | blocked by search tool and fetch tool |
| G2 ShopBase reviews, Capterra ShopBase reviews | HTTP 403 |
| Shopify Community full threads (unfreeze funds, FB ads banned, store terminated, AI warning) | HTTP 403; only search-result excerpts seen |
| BlackHatWorld thread (FB ads, ecom dropshipping) | HTTP 403 |
| YouTube comments | not attempted: no usable route in this toolset |
| Trustpilot ReConvert (upsell app) | HTTP 404 |
| Hacker News: recent threads on Shopify bans and on AI editing a store | search returned zero hits |
| Trustpilot pages 2+ of any filter | only page 1 was read |
| Old PrintBase / PlusBase sources | only what appears inside the ShopBase Trustpilot page; no dedicated PrintBase/PlusBase pages checked |

## Sources read

Counted for frequencies below: **M = 22 customer-voice sources (S1 to S22)**. S23 (a vendor blog relaying the S22 post), S24 (context) and S25 (a vendor pitch) are listed but **not counted**. The earlier "of 25" counts mixed them in and were corrected at review. "TP" = Trustpilot company page, filtered or searched view. All fetched 2026-10-24. Type: `fetch-read` = page returned by WebFetch (first page of the view); `snippet-read` = only the search-result excerpt seen, quoted only where the excerpt text itself was quoted.

| ID | Link | What / who | Read as |
|---|---|---|---|
| S1 | https://www.trustpilot.com/review/shopbase.com | TP ShopBase overview: 4.0 of 5, 253 reviews (81% 5-star, 13% 1-star) | fetch-read |
| S2 | https://www.trustpilot.com/review/shopbase.com?stars=1 | TP ShopBase, 1-star, 20 reviews, Jul 2022 to May 2026 | fetch-read |
| S3 | https://www.trustpilot.com/review/shopbase.com?stars=5 | TP ShopBase, 5-star | fetch-read |
| S4 | https://www.trustpilot.com/review/shopbase.com?search=payment | TP ShopBase, search "payment" (includes PlusBase, PrintBase mentions) | fetch-read |
| S5 | https://www.trustpilot.com/review/shopify.com?stars=1&search=apps | TP Shopify, 1-star, search "apps" (cost, fees) | fetch-read |
| S6 | https://www.trustpilot.com/review/shopify.com?stars=1&search=banned | TP Shopify, 1-star, search "banned" | fetch-read |
| S7 | https://www.trustpilot.com/review/shopify.com?search=AI+sidekick | TP Shopify, search "AI sidekick" | fetch-read |
| S8 | https://www.trustpilot.com/review/shopify.com?search=conversion+checkout | TP Shopify, search "conversion checkout" | fetch-read |
| S9 | https://www.trustpilot.com/review/shopify.com?search=stolen+copied+competitor+ads | TP Shopify, search "stolen copied competitor ads" | fetch-read |
| S10 | https://www.trustpilot.com/review/shopify.com?search=expensive+monthly+fees+transaction | TP Shopify, search "expensive monthly fees transaction" | fetch-read |
| S11 | https://www.trustpilot.com/review/stripe.com?stars=1&search=dropshipping | TP Stripe, 1-star, search "dropshipping" | fetch-read |
| S12 | https://www.trustpilot.com/review/paypal.com?stars=1&search=dropshipping | TP PayPal, 1-star, search "dropshipping" | fetch-read |
| S13 | https://www.trustpilot.com/review/facebook.com?search=ad+account+disabled+shopify | TP Facebook, search "ad account disabled shopify" (reviewers are businesses, not shown to be dropshippers) | fetch-read |
| S14 | https://www.trustpilot.com/review/printify.com?stars=1 | TP Printify, 1-star; 4.4 of 5, 7,696 reviews; 8 recent reviews Sep 28 to Oct 23 2026 | fetch-read |
| S15 | https://www.trustpilot.com/review/printify.com?search=margin+price+cost | TP Printify, search "margin price cost" | fetch-read |
| S16 | https://www.trustpilot.com/review/printful.com?stars=1 | TP Printful, 1-star; 4.2 of 5, 7,950 reviews | fetch-read |
| S17 | https://www.trustpilot.com/review/gelato.com?stars=1 | TP Gelato, 1-star, 8 recent (Sep 29 to Oct 19 2026) | fetch-read |
| S18 | https://www.trustpilot.com/review/cjdropshipping.com?stars=1 | TP CJdropshipping, 1-star (page notes rating unavailable and fake reviews removed) | fetch-read |
| S19 | https://www.trustpilot.com/review/zendrop.com?stars=1 | TP Zendrop, 1-star (Zendrop replies dispute some) | fetch-read |
| S20 | https://community.shopify.com/c/ecommerce-marketing/facebook-ads-keep-on-getting-banned-account-permanently/td-p/1240887 (also .../facebook-banned-ad-account-on-my-first-day-need-help-to-appeal/m-p/1308964) | Shopify Community, FB ad accounts banned (threads from about 2021; date not confirmed) | snippet-read |
| S21 | https://community.shopify.com/t/store-has-been-terminated/421777 | Shopify Community, store terminated after 2 sales, FB campaigns | snippet-read |
| S22 | https://community.shopify.com/t/warning-shopify-ai-sidekick-magic-hallucinates-technical-data-and-sabotages-strategic-seo/589483 | Shopify Community, merchant warning about Sidekick/Magic (date not seen) | snippet-read |
| S23 | https://www.surebright.com/blog/why-shopify-users-are-losing-patience-with-its-ai-support-sidekick | Vendor blog (SureBright, warranty company); relays merchant quotes from Reddit and Shopify Community, no dates | fetch-read, secondary |
| S24 | https://terms.law/FAQ/payment-processors/stripe-holds-faq.html and https://www.easypaydirect.com/blog/stripe-holding-funds-and-how-to-fix-it/ | Law-firm FAQ and payment-vendor blog on Stripe holds; context only, **no quotes used** | snippet-read |
| S25 | https://news.ycombinator.com/item?id=48164405 | Hacker News comment by "nivroo", 2026-05-16; author is building a Shopify alternative (a pitch, not a neutral user) | snippet-read (125-char fragment) |

S24 and S25 are context, not customer evidence. Customer-voice sources proper: S1 to S22 (22). Each Trustpilot "page" is page 1 of a filtered view (about 20 reviews), so one source can hold several reviewers. S2 shows 20 reviews because that is the page size, not because it is the total 1-star count (13% of 253 is about 33).

Verification at review: S1 to S22 → **not fetchable by curl** (HTTP 403 bot challenge), so their quotes are summariser-read, not byte-verified. S23 → fetched, quote exact; no publish date on the page. S25 → fetched, quote exact; timestamp 2026-05-16T22:41:57.

## Persona: A · Experienced dropshipper (primary)

Persona assignment is by topic (`ASSUMPTION`). Frequencies are "in N of 22 customer-voice sources read" (a count of pages read, not of the market); where one page held many reviewers, that is stated. Quotes are summariser-read and not byte-verified unless marked otherwise. ⏳ = older than 2 years (before 2024-10-24).

### Pain points

| Rank | Pain | Real quote (as returned by the fetch tool; summariser-read, not byte-verified unless marked) | Frequency (of 22 customer-voice sources) | Links |
|---|---|---|---|---|
| 1 | **Costs that stack up on the platform: paid apps, add-ons, fees, transaction charges** | "You have to buy apps for almost anything you would do normally on any site." (TP Shopify, US, Feb 23, 2026) · "I no longer want to pay monthly Shopify fees" (ES, Jun 4, 2025) · "an extra 3.5% international fee paired with a compulsory 2% currency conversion fee" (AU, Aug 20, 2026) · vendor context, not counted: "I was tired of the hidden app fees on Shopify (upsells, reviews, sourcing tools, etc. all cost extra)." (Hacker News, 2026-05-16; **byte-verified exact**; the author sells an alternative) | 3 of 22 (S5, S10, S19); S5 alone lists 14 reviewers on app cost (unverified). The S19 (Zendrop) item is not shown and may be supplier markup, not platform fees. S25 is vendor context and is not counted | S5, S10, S19, S25 |
| 2 | **Payments held, frozen or processor closes the account** | "They put all of my money on hold for 4 MONTHS!?!?" (TP Stripe, EE, Mar 31, 2020 ⏳) · "they refuse to return $2,000 USD." (TP Stripe, AR, Jun 9, 2026) · "Be aware. I have a dropshipping store and PayPal blocked my account with 4k on it without proper explanation!" (TP PayPal, HR, Jun 9, 2024 ⏳) · "they've banned my store for no reason, held the money for 6+ months" (TP Shopify, SE, Jul 29, 2025) | 3 of 22 (S6, S11, S12); S11 shows 15 reviewers on holds/closures (unverified) | S6, S11, S12 |
| 3 | **Store banned by the platform with little explanation** | "I received my first three orders, but the next day I was banned by Shopify." (TP Shopify, GB, Nov 4, 2024) · "Shopify immediately banned my account without any fair investigation." (US, May 20, 2025) · "they will close your shop for any dumb reason." (TP Shopify, US, Jun 2, 2026) | 3 of 22 (S5, S6, S21; S21 is a search excerpt with no quote) | S5, S6, S21 |
| 4 | **Ad account disabled or restricted** | "I am locked out of my business page" (TP Facebook, US, Oct 1, 2026; the full sentence returned was "Because of this deceptive, broken system, I am locked out of my business page") · Shopify Community (search-result excerpt only; page 403): an ad account "disabled no less than 60 seconds after trying to use my Ad Account for the first time" (thread probably about 2021 ⏳, date not confirmed) | 2 of 22 (S13, S20). Weak: S13 reviewers are not shown to be dropshippers; S20 is old and only an excerpt | S13, S20 |
| 5 | **Slow, unreliable supplier fulfilment and stock** | "They often display 2 to 4 days of processing, but in reality this is very rarely respected." (TP CJ, FR, Jul 7, 2026) · "Dispatching item came take as long as 3-4 weeks" (CJ, GB, Sep 7, 2026) · "it has been more than one month since I submitted an order for fulfillment" (TP Zendrop, DE, Feb 7, 2026) · "I purchased stock with their PlusHub service, and never arrived" (TP ShopBase, MA, Mar 19, 2023 ⏳) | 3 of 22 (S18, S19, S2) | S18, S19, S2 |
| 6 | **Traffic or ad spend without sales** | "my store received visitors but zero sales" (TP Shopify, SA, Mar 7, 2026; the same reviewer also cites payment limits) · "I spent hundreds on ads in their apps and didn't get ONE SINGLE SALE." (TP Shopify, CA, Aug 10, 2026) | 2 of 22 (S8, S9). Thin, and neither reviewer describes conversion work | S8, S9 |
| 7 | **Store or content copied by others** | "Shopify allow thieves to copy legitimate websites." (TP Shopify, US, Jul 3, 2026) | 1 of 22 (S9). The "rival runs ads over my campaign" version was **not found** | S9 |

Not found in any source read: Epacket specifically, packaging with Chinese writing (closest: "The packing on my sample order was a plastic sheet wrapped with clear tape", TP Zendrop, TH, Apr 2, 2026), tracking the buyer journey, template cost, bulk-editing workload, staying up at night for ads, Vietnamese-language support.

### Their language (as seen in these sources)
- **The problem:** "banned", "held the money", "blocked my account", "closed", "without proper explanation", "for no reason", "hidden app fees" (S25, vendor, verified), "forced to purchase addon apps", "never arrived", "stuck in sorting centers". These are summariser-read; no source ID was recorded for "forced to purchase addon apps" or "stuck in sorting centers".
- **The goal:** very little goal language appeared (reviews are complaints). Seen: "highest conversion rates" (source not recorded), "so simple and effective" (TP ShopBase, BD, Dec 6, 2024).
- **Alternatives named:** WooCommerce / WordPress ("If you already have an independent site (like WordPress/WooCommerce)", TP Shopify, GB, Oct 20, 2026); "build from scratch using AI and publish elsewhere" (TP Shopify, GB, Aug 16, 2026); Shopify Payments, Stripe, PayPal as the gateways that hold money; CJ and Zendrop as suppliers.
- Terms like "CR", "AOV", "upsell" appeared only once, from a vendor (S25). No reviewer used "AOV".

### Beliefs & objections
- Platforms and processors are **arbitrary and unaccountable**: bans and holds come "without explanations" and appeals do not work (S6, S11, S12, S20). Reading this as a wider distrust of any system that acts on the store without clear reasons is `ASSUMPTION`: the sources are about bans and holds, not about tools.
- **Automation done to them without consent is a fear:** "Printify's system automatically published duplicate listings to my Etsy store without my consent" (S14, TR, Oct 23, 2026; this is a POD seller but the fear transfers to the AI claim: `ASSUMPTION`).
- **AI:** see the AI section below. Evidence is about AI support bots and Shopify's Sidekick/Magic, not about AI that edits a store for conversion.
- Fees are read as "profit-enhancing fees that have nothing to do with sellers" (TP Shopify, US, Sep 4, 2026).
- Trust in ShopBase specifically: see Type C extras.

### Fit with the USP (the user's AI-first words; results `UNPROVEN`; no numbers)
| Pain | Fit | Why (no stretching) |
|---|---|---|
| App/fee stacking (1) | **partial, only by ASSUMPTION** | The USP says AI "helps increase CR and AOV". If it replaces paid upsell/popup apps the pain is touched, but the USP does not say what is included or what it costs (pricing and AI packaging unknown, strategy pack open question). Nothing here lets Home claim "fewer apps". |
| Payment holds (2) | **none** | The USP is not about payments. |
| Store banned (3) | **none** | |
| Ad account blocked (4) | **none** | |
| Fulfilment speed and supplier quality (5) | **none** | |
| Traffic but no sales (6) | **partial** | "Helps increase CR" addresses the goal behind the complaint; sources show the pain only twice and give no sign this reader wants AI for it. Outcome stays `UNPROVEN`. |
| Copying (7) | **none** | |

## Persona: B · Experienced POD seller (primary)

### Pain points

| Rank | Pain | Real quote | Frequency | Links |
|---|---|---|---|---|
| 1 | **Thin margin: base cost and shipping cost rise, little left per item** | "It is very difficult to make more than $2-$3 per item if you cover shipping and offer any discounts." (TP Printify, US, Jul 9, 2026) · "before a shipment used to cost me around $6 now is is costing me $18" (AE, Jul 17, 2026) · "After charges, fees, and marketing sometimes I feel Printify is the only one making real money." (US, Jul 16, 2026) | 2 of 22 (S15, where the fetch tool reported 8 reviewers, unverified; plus a dropship-supplier echo in S19: "Their prices are heavily marked up, which kills profit margins", AU, Mar 19, 2026) | S15, S19 |
| 2 | **Slow production and unreliable fulfilment** | "Processing times have taken up to TWO WEEKS, which is simply unacceptable" (TP Printify, US, Sep 28, 2026) · "Completely unreliable order fulfillment." (TP Printful, US, Oct 17, 2026) | 3 of 22 (S14, S16, S17) | S14, S16, S17 |
| 3 | **Misprints, defects, wrong or missing items** | "They misprint orders then gaslight you into thinking it's your fault." (TP Printify, US, Oct 9, 2026) · "Every one of these five Printful orders contained defective items." (TP Printful, GB, Jul 16, 2026) · "Printify sent me the order receipt and only shipped 1 of the products." (AU, Oct 6, 2026) | 2 of 22 (S14, S16) | S14, S16 |
| 4 | **Unhelpful support, bots instead of people** | "Customer service is NONEXISTENT." (TP Gelato, DE, Oct 12, 2026) · "Long production times, sloppy production, and chat is useless." (TP Printify, US, Oct 6, 2026) · "The AI chatbot is about as useful as the instructions on a bar of soap." (TP Gelato, DK, Oct 16, 2026) | 3 of 22 (S14, S17, S7 for the AI-bot theme) | S14, S17, S7 |
| 5 | **Marketplace/integration problems and changes made without consent** | "Printify's system automatically published duplicate listings to my Etsy store without my consent" (TP Printify, TR, Oct 23, 2026) · "Gelato seriously needs to improve its Etsy integration and automatically handle marketplace-collected sales tax." (TP Gelato, VN, Oct 8, 2026) | 2 of 22 (S14, S17) | S14, S17 |
| 6 | **Restricted or copyright-flagged products, designs taken** | "I bought a bunch of samples, but all of my products are restricted - I can't sell them" (TP Printify, US, Oct 19, 2026) · "This company have stolen my mockup photograph (listed on a popular selling platform) on acrylic plaques." (TP ShopBase, GB, Jun 27, 2024 ⏳) | 2 of 22 (S14, S2) | S14, S2 |
| 7 | **Platform bans and held payouts (shared with A)** | see A rank 2 and 3 | 3 of 22 (S6, S11, S12) | S6, S11, S12 |

Not found: "clean products get no orders versus trademark products get orders", "cannot find a factory fast enough for thousands of products", rivals copying designs and running ads over the campaign (closest is rank 6, which is a mockup photo taken, not a design copied for ads).

### Their language
- **Problem:** "misprint", "defective", "sloppy production", "processing times", "thin profit margin", "I have to absorb the cost", "restricted", "useless".
- **Goal:** not stated in complaints; "an Etsy seller" selling at a price buyers accept ("find some products too pricy, making it a tuff sale for an Etsy seller", TP Printify, US, Jul 28, 2026).
- **Alternatives named:** Printify, Printful, Gelato (providers compared against each other); Etsy as the sales channel. ShopBase's POD name PrintBase appears only in one 2022 praise line ⏳ ("all the amazing products from POD ( Printbase )").

### Beliefs & objections
- Margin is eaten by the provider and fees: "Printify is the only one making real money" (S15).
- Distrust of **automatic actions** on the store or listings (S14 rank 5).
- Distrust of AI as a front for human support (S7, S17).
- Provider quality is a lottery by order (S14, S16).

### Fit with the USP
| Pain | Fit |
|---|---|
| Margin, base cost (1) | **none**. The USP does not mention cost, and the PrintBase offers (cost, cashback) are superseded. |
| Production speed, defects, support (2, 3, 4) | **none** |
| Changes made without consent (5) | **partial, as a trust condition, not a benefit.** "Seller stays in control and makes the final decision" speaks to this fear. How it works in the product is unknown (`UNPROVEN`). |
| Restricted/copyright (6) | **none, and a content risk.** Home must not touch it (strategy pack, user decision 5). |
| Bans and holds (7) | **none** |

## Secondary crossover groups (short note only)
Dropshipping oldies + POD newbie and POD oldies + dropshipping newbie: in the sources read, their pains are the same two sets above (platform and fee pain, fulfilment pain). No source addressed "need for design" or "need winning products and audiences". `ASSUMPTION` unchanged.

## AI that changes the store: what real sellers said (applies to A and B)

Evidence is **indirect**. No source found a seller reacting to an AI that scans a store and proposes conversion or AOV changes for approval. What exists is reaction to Shopify's Sidekick and Magic and to AI support bots.

| Theme | Quote | Where | Count |
|---|---|---|---|
| AI output is wrong or ignores instructions | "the ai give misinformation and then apologizes" (US, Jun 25, 2026) · "the ai recommended are so bad for the aps" (AU, Sep 20, 2026) · "After 5 months of struggling with Shopify's AI tools (Sidekick and Shopify Magic), I have decided to migrate" (Shopify Community post S22, quoted via SureBright S23; **byte-verified exact on S23**, and S23 links the S22 thread; S22 itself returned 403; date not seen) | S7, S22 (via S23) | 2 of 22 (S7 has 2 reviewers) |
| AI instead of humans in support | "SHOP USE AI AND WILL NEVER ALLOW YOU TO SPEAK WITH A HUMAN AGENT" (AU, Aug 21, 2026) · "I'm not sure why Shopify thinks that humans will be ok with talking to AI endlessly every day for everything" (GB, Oct 16, 2026) | S7 | in S7, 8+ of the 20 reviews shown; also S17 |
| Mixed or mild | "The ai isn't bad but can't do certain things and it explaining it doesn't really help me." (US, Jun 27, 2026) · "Their AI, Sidekick, is user friendly." (CA, Jul 28, 2026) | S7 | 2 reviewers |
| Rights/ownership | "editing images with AI does not give me the right to use the originals." (MA, Oct 14, 2026) | S7 | 1 |
| Wanting AI in a builder | "i want to add landing page with ai please" (TP ShopBase, DZ, Sep 1, 2026; one review shown in two views) | S1, S3 | 1 |

What this supports, carefully: in this sample the fear is **bad or invented output and no human to fix it**, plus **changes made without asking**. The fear "AI costs too much" was not seen. "Losing control" as a phrase was not seen, but the Etsy "without my consent" review is the nearest case. Nothing here shows that sellers want or reject a CR/AOV scan. Do not write "sellers trust" or "sellers distrust" from this: the AI evidence is a handful of Trustpilot lines about a different company's AI.

## Internal sheet pains versus outside sources

| Internal-sheet pain | Outside sources | Notes |
|---|---|---|
| PayPal/Stripe hold payments up to 180 days [SB-R5] | **supports (holds); "180 days" only in a 2019 review** | "So then they stuck the 200 I had in the account on hold for 180 days" (TP PayPal, US, Feb 12, 2019 ⏳); "held the money for 6+ months" (Shopify, 2025); "4 MONTHS" (Stripe, 2020 ⏳). Not Vietnam-specific; reviewer countries vary (HR, SE, AR, EE, US). |
| Stripe does not open accounts in Vietnam [SB-R5] | **does not mention** | |
| Payment gateway "dies" / account closed [LEAD-2] | **supports** | S6, S11, S12 |
| High transaction fee lowers margin [LEAD-2] | **supports** | S10; S5 |
| Shopify blocks the seller [SB-R9 need] | **supports** | S6, S5, S21 |
| No budget for upsell/popup apps and templates [SB-R4] | **supports for app cost** (S5, S10); **templates: does not mention** | Reviewers complain that apps cost extra; "no budget" is not stated. S25 says the same but is a vendor pitch, not counted |
| Cannot track buyer journey step by step [SB-R4] | **does not mention** | |
| Little time to customise a high-conversion store [SB-R4] | **does not mention** | only "zero sales" twice (S8, S9) |
| Bulk edits, copy store structure [SB-R4] | **does not mention** | |
| Facebook / Google Shopping ads blocked [SB-R5] | **partly supports (Facebook only, weak)** | S13, S20; Google Shopping not mentioned |
| Ad spend over $3000, two months without profit [SB-R5] | **does not mention** | only one "hundreds on ads ... ONE SINGLE SALE" (S9) |
| Staying up at night for ads [SB-R5] | **does not mention** | |
| Epacket 11 days + processing [SB-R6] | **partly supports** | no Epacket; slow fulfilment seen in S18, S19, S14, S16 |
| Poor packaging, broken goods [SB-R6] | **weakly supports** | S19 packing line; S16 "the package was empty" |
| Rivals copy the product and run ads over the campaign [SB-R6, SB-R7] | **mostly does not mention** | only "copy legitimate websites" (S9) and a stolen mockup photo (S2); "ads over my campaign" not found |
| Clean POD hard to get orders versus trademark risk [SB-R7, SB-R15] | **does not mention** | restricted-products review (S14) is the nearest |
| Cannot find a factory fast enough [SB-R7] | **does not mention** | |
| Low margin, little variety at competitive base cost [LEAD-1] | **supports (margin)**; variety not mentioned | S15 |
| Heavy workload: suppliers, fulfilment, support [LEAD-2] | **weak** | only complaints about the provider's own support (S14, S17); the seller's workload is not stated |
| No Vietnamese support [SB-R4] | **does not mention** | all sources are English or international |
| Fear of being spied on, keeps business quiet [SB-R14, SB-R15] | **does not mention** | |

## Pain points the USP does not answer
- Payment holds, freezes and processor closure (A 2, B 7).
- Store or account bans by the platform (A 3, B 7).
- Ad account blocks (A 4).
- Slow and unreliable supplier or POD fulfilment, defects, wrong items (A 5, B 2, B 3).
- Base cost and margin (B 1).
- Support quality (B 4).
- Restricted/copyright products (B 6; also a content risk, never on Home).
- Copying and rival ads (A 7).
- Costs from stacked apps and fees: touched only if the AI replaces paid apps and the pricing supports it; **unknown**, so treat as **not answered**.

If Home speaks only to AI for CR and AOV, these stay unanswered. That is a scope fact for Steps 09 and 11, not a copy problem to hide.

## Type C extras: what people say about ShopBase and the old brands

Sources: S1 to S4. This is what is **visible on Trustpilot only**; G2, Capterra and Reddit were unreachable. **None of the facts or quotes in this section could be checked against the live page at review** (Trustpilot answered `curl` with a 403 bot challenge). Treat every figure and quote as summariser-read, not byte-verified. ⏳ = older than 2 years.

- **Overall:** 4.0 of 5, 253 reviews, 81% 5-star, 13% 1-star (about 33 one-star reviews; only the 20 on page 1 were read). Trustpilot notes the company "hasn't recently invited customers to review and hasn't replied to negative reviews".
- **Who writes:** the visible country codes are heavily BD, MA, IN, with a few US, GB, DK, IT. Most 5-star lines are short and generic ("This is an amazing platform." BD, Aug 2, 2026). That does not look like the English-market, experienced A/B reader; do not treat the score as their view.
- **Praise:** one interface ("Shopbase allows us to do things in a single interface that most sites can't do on their own." TR, Dec 23, 2024); simple store building; built-in payments ("they have their own payment processor (Shopbase payments)" FR, Nov 6, 2023 ⏳); support ("my favorite part is the customer service", May 27, 2023 ⏳). No dated praise of payments or support after 2023 was seen. Several 5-star lines name **PlusBase**, not ShopBase ("plusbase is my life changer ...", BD, May 2, 2025), and one names PrintBase (2022). So a part of what people love is a brand that no longer exists.
- **Complaints (1-star, the 20 reviews on page 1, Jul 2022 to May 2026):** non-delivery and sourcing tied to the old fulfilment hub ("I purchased stock with their PlusHub service, and never arrived", Mar 19, 2023 ⏳; "we havn't received any products and you do not answer", DK, Sep 17, 2024 ⏳; "I paid hundreds, nothing arrived, Ecom listed it as delivered.", US, Jan 5, 2026); unwanted charge during trial ("I was charged £19 while I'm still in the trial period!!.", Sep 22, 2022 ⏳); a broken AliExpress connector ("they're Ali dropship connector doesn't work anymore.", MA, Sep 4, 2023 ⏳); payout accusations ("Basically they will keep all the profit and give you nothing", IN, May 10, 2024 ⏳). Most of these complaints are older than 2 years and concern old hub services. Several of these accuse the platform of a scam; many look like **buyers** of merchants' stores, not sellers, so the platform is blamed for what merchants sell.
- **Reputation risk for Home (important):** "This company is knowingly allowing people to sell products illegally using copyrighted material." (US, Mar 7, 2026) and "COPYRIGHT - Stolen Photograph." (GB, Jun 27, 2024 ⏳). Both are unverified against the live page. This matches the internal "DMCA / restricted products" offer in the lead sheet [LEAD-2]; outside readers read that as a negative. It confirms the user decision that Home never touches it.
- **AI:** one request for AI ("i want to add landing page with ai please", Sep 1, 2026); no other AI mention for ShopBase.
- **Old brands:** the old names PrintBase / PlusBase / PlusHub carry both love (PlusBase "life changer") and the worst complaints (PlusHub "never arrived"). A merchant who knew them may arrive with either memory. What current merchants need to hear about the change is not answered by these sources.

## Limits & bias
- **Sample:** 22 customer-voice sources, page 1 of each Trustpilot view only; about 150 individual review lines were seen. This is a handful for each pain, not a market measure. No sentence here means "most sellers".
- **Complaints dominate:** filters were 1-star or search terms like "banned", so negative voices are over-represented by design. The 5-star views of ShopBase are short and generic.
- **Wrong population:** Trustpilot reviewers are customers of Stripe, PayPal, Shopify, Facebook, Printify and others, not shown to be experienced dropshippers or POD sellers, and not Vietnam-based. Some may be buyers.
- **Platform skew:** most evidence concerns Shopify, Printify, Printful, Gelato, CJ and Zendrop, not ShopBase.
- **No Reddit, no YouTube, no G2, no Capterra:** the communities named in the brief were not read. The AI-trust picture, CRO pain and Vietnam-specific pain are the thinnest.
- **Dates:** most quotes are from late 2024 to 2026. Quotes older than 2 years (before 2024-10-24) are flagged ⏳: Stripe 2020, PayPal 2019 and Jun 2024, ShopBase 2022, 2023 and 2024 (most of the ShopBase complaints and both dated support/payment praise lines), the 2024 stolen-mockup review, and the Shopify Community threads from about 2021.
- **Quote integrity:** only 2 of 71 quoted strings are byte-verified (S23, S25). The other 69 are fetch-tool text whose pages blocked `curl` at review (see top). S20 to S22 are search-result excerpts only; S23 is a vendor blog relaying quotes it did not date.
- **Trustpilot:** does not fact-check reviews; some companies dispute reviewers (Zendrop) or have removed fake reviews (CJ).

## Assumptions
1. Persona assignment of each pain is by topic, not by reviewer identity.
2. The fear transfer from "Printify published listings without my consent" to "AI that edits my store" is an inference.
3. The USP touches app-cost stacking only if the AI replaces paid apps and pricing supports it; unknown.
4. The reader of the Home resembles the people reviewing Shopify/Printify; not shown.
5. Frequencies are counts of the 22 customer-voice sources read (S1 to S22), not of the market.
6. Reviewer countries in S11 and S12 suggest holds are not Vietnam-specific; it does not show Vietnamese sellers are not hit harder.
7. The country, date and star labels on Trustpilot quotes come from the fetch tool and were not checked against the live page.

## What would close the gaps (for the user)
Paste any of: real customer or lead interview notes; support tickets about holds or ads; exports of Facebook/Zalo group posts; Reddit threads from r/dropshipping, r/printondemand, r/shopify, r/ecommerce on payment holds, app costs and AI tools; any merchant feedback on AI features; and, if possible, a copy-paste of the ShopBase Trustpilot pages (page 1 and page 2+ of the 1-star view) taken from a normal browser, so the quotes and figures above can be byte-checked. Suggested format, one item per block: `Source: <where, link if any> · Date · Who (dropship / POD / both; VN or not; how long selling) · Verbatim text (original language, unedited) · Optional note`. Then Step 07 can be re-run, which also marks Steps 09 to 26 `stale`.
