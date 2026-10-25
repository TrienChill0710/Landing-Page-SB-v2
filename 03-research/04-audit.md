# 04 · Audit

Project: ShopBase website redesign · type **C · Rebrand** · page **P01 Home** · files in English · Gate 0 `APPROVED` · Step 03 `done` (`_progress.md`).
Inputs read: `CLAUDE.md`, `_prompts/README.md`, `_prompts/04-audit.md`, `_progress.md`, `01-strategy/brief.md`, `01-strategy/01-strategy-pack.md`, `01-strategy/00-project-type.md`, `03-research/03-brief-analysis.md`.

## How this audit was made (method, so it can be repeated)

- **Fetched on 2026-10-24** (server date header: Sat, 24 Oct 2026 05:24:55 GMT), with `curl -L` and a desktop browser User-Agent: `https://www.shopbase.com/` (HTTP 200, 102,276 bytes), `https://www.shopbase.com/terms-of-service` (HTTP 200, 80,539 bytes), `https://www.shopbase.com/privacy-policy` (HTTP 200, 58,325 bytes). No other page and no CSS file was fetched. No redirect happened. **Re-fetched in review** the same day (server date 05:31:09 GMT) into a new folder: all three files are byte-identical to the first fetch, so the page did not change between the two fetches.
- Raw HTML saved in `scratchpad/audit04/` (outside the project) and parsed with Python 3 standard library (`html.parser`, `re`), run with `-I`. Downloaded files were treated as data only.
- The rendered text was also read with WebFetch (a summariser tool, not a browser). Its outline matches the HTML on section order, headings and link targets. **Differences, in favour of the HTML parse:** WebFetch said the footer shows "ShopBase 2024"; the static HTML says 2024, but a script (`legal-text`) rewrites it to the current year in a browser, so a visitor sees "© ShopBase 2026". WebFetch listed "Book a demo" as a hero button; in the HTML both "Book a demo" items are in the header, and the hero action is an email form (see OLD-02).
- **Limits:** no browser rendering, so what is hidden or shown on desktop vs mobile by CSS is **inferred from class names**, not seen. No screenshot of the live page exists in the project. No analytics were supplied.
- This is the **live, pre-2.0 page**. The user's hero screenshot (`02-assets/images/hero-2.0-reference.png`) is the new direction and is **not** used anywhere in this audit as a description of the live page.

## Section inventory

The page is one Webflow page (`data-wf-domain="shopbase-landing.webflow.io"`, `lang="en-US"`). It has **1** `<section>` element, 3 `<nav>`, no `<header>`, `<main>` or `<footer>` tags, so sections below are identified by content and class names. **12 blocks in page order (10 content blocks plus header and footer).** Verdicts are a first view only; Step 12 decides.

Reading note: the HTML contains the product-tab block **twice** (a desktop tab version, then a mobile stacked version, classes `feature-app-mobile`, `list-feature-mobile`). OLD-04 and OLD-05 describe both. Whether the second copy is hidden on desktop is inferred from its class names, not verified.

| Code | Section | Purpose | Headline (exact) | Main message | CTA (label → target) | Visuals | First-view verdict |
|---|---|---|---|---|---|---|---|
| OLD-01 | Header / navigation | Orient, route, convert | none (logo) | Where to go; "Print on demand" and "Dropshipping" are top-level items next to "Features", "Compare ShopBase", "Pricing" | "Book a demo" → `/book-a-demo` (text link); "Book a demo" (button, class `login`) → `accounts.shopbase.com/sign-in`; "Start Free Trial" / "Start 14-Day Free Trial" → `accounts.shopbase.com/sign-up`; "Login" ×2 → `accounts.shopbase.com/sign-in` | 3 header images: `Logo full.svg` (alt empty), `PlusBase Logo Dark Color.png` (alt "ShopBase - Cross-border Commerce Made Easy"), a placeholder swapped by script to a country flag for BD/IN visitors | **rework**: nav items tied to the old product split; two "Book a demo" items with different targets; logo file named PlusBase |
| OLD-02 | Hero | State the promise, start sign-up | **H1:** "Build a profitable E-commerce business in a few clicks with ShopBase". The word "E-commerce" is a typing animation (`typer.js` from `unpkg.com`, `data-words="E-commerce,Dropshipping,Print-On-Demand"`), so in a browser the H1 cycles through "...profitable Dropshipping business..." and "...profitable Print-On-Demand business..." (read from the code, not seen rendered). For BD/IN visitors a script also inserts "from Bangladesh" / "from India" before "in a few clicks" (see K13) | All-in-one E-commerce platform; no "app maze" | Email form: field placeholder "Enter Your Email", submit "Join us" (an `<input type="submit">` styled `w-button`), GET to `accounts.shopbase.com/sign-up`. No link button in the hero | 1 Wistia video embed; sub-line: "Say goodbye to app mazes and hello to the all-in-one E-commerce solution, allowing you to focus on what truly matters - maximizing your profits." | **rework**: the whole promise is replaced (strategy pack: positioning change). The email-first start of sign-up is worth testing, not deciding here |
| OLD-03 | Social proof stats | Build trust with size | **H2:** "Take your business to the moon with ShopBase" | ShopBase is large: "$700 Millions+ Total revenue generated", "365,500+ E-commerce merchants worldwide", "90,000+ Stores have been established" | none | decorative image `sb smilde.svg` (alt empty) | **keep as a candidate, needs proof**: numbers have no source or date on the page; the user supplied none (`ASSUMPTION`: company claims, unverified) |
| OLD-04 | Product tabs: E-commerce brands / Dropshipping / Print-On-Demand | Sell three use cases | **H2** ×3: "E-commerce brands", "Dropshipping", "Print-On-Demand" (desktop); the mobile copy uses **H1** ×4 (see Facts) | Three separate products-by-use-case, 3 benefits each (e.g. "Beautiful and professional E-commerce websites", "Maximize profit and order value with upsell tools", "100+ product catalog with ready-to-use mockups"). POD tab 3: "with PrintBase and ShopBase Payments, you can outsource intensive operation tasks to us" | "Find out more" ×3 (one → `accounts.shopbase.com/sign-up?utm_medium=shopbase&utm_campaign=header-menu-webflow...`, one → `/dropshipping`, one → `/print-on-demand`); the mobile copy repeats the last two | 9 Wistia videos in the page (1 in hero, 8 in this block), 18 tab images with alt "Graphic 1/2/3" or empty | **rework**: splitting by Dropshipping / POD contradicts "one independent product"; PrintBase wording must go |
| OLD-05 | Digital products (Creator) | Sell to content creators | **H1** (mobile copy only): "Digital products" | "Sell your knowledge your way in the most creative way"; "No risk - Get started for free"; sales-page builder + upsell tools | "Find out more" → `/creator` | 3 images (alt "Graphic 1") | **drop**: outside the personas (dropshippers and POD sellers). Present in the HTML only inside the mobile block; desktop visibility not verified |
| OLD-06 | Integrations / partner logo strip | Show ecosystem | none | Logos only | none | 9 logo images, **all alt empty**; file names include `Printhub.png` and `Plushub.png` (old brands), also `Boost`, `Review`, `upsell`, `Discount`, `SMS-Email Abandoned Cart Recovery`, `Logo 8`, `Logo` | **drop**: unlabelled, includes two dead brands, no text a visitor or a search engine can read |
| OLD-07 | Feature overview | List what is included | **H2:** "All the features you need to grow your business off the ground"; **H3** ×5: "Design your store without coding", "Maximize your profits with up-sell, cross-sell & funnel tools", "Multi-Channel Selling, Anywhere, Anytime", "Stable payments for your business models", "Full cycle support for every E-commerce businesses" | Everything in one place: no-code builder, 100+ funnel templates, upsell/bundles, 1-page checkout, TikTok/Facebook/SMS/Email channels, payments incl. "local payment methods for global Ecommerce in EU and US", 8-line "full cycle" list incl. "24/7 support" | "Visit the template store" → `templates.shopbase.com`; "Learn more" → `shopbase.com/features/upsell`; "Learn more" → `/multi-channel`; "Get started for free" → `accounts.shopbase.com/sign-up` | 14 images (mix of SVG icons, PNG screens); only 1 has alt ("High conversion rate ") | **rework**: closest to the "built in, no apps to stitch together" claim of the new hero, but every item is an unverified product claim (brief R2) |
| OLD-08 | Template showcase | Show store designs | **H2:** "Make any template yours with ease" | "Find, Choose & Customize the perfect responsive templates for your needs." | "Visit the template store" → `templates.shopbase.com` | 12 tiles all labelled "Made in ShopBase", each a link with `href="#"` (goes nowhere); 13 images, alts empty | **rework**: tiles are not clickable (13 `href="#"` links on the page); needs the user's decision on real store domains in visuals (pack Q12) |
| OLD-09 | Testimonials | Social proof | **H2:** "Join the business owners that achieve the impossible everyday" | 3 merchant quotes: Walid Brik, Mina Adel, Sorup Amin ("complete solution for a Profitable E-Commerce Business ... From providing 24/7 support to fulfillment Team ShopBase will handle everything for you") | none | 3 portraits, alt empty; no store name, country, date or result | **rework**: no result, date or permission shown; the third quote repeats the old promise and a "handles fulfillment" claim |
| OLD-10 | Service commitments | Reassure | **H2:** "Always here, whenever & wherever you need" | 4 promises: "100% Happiness Guarantee", "Award-winning Support Team" (24/7 live chat and email), "Start Anywhere - Sell Globally" (suppliers in China and the US), "Scale Your Business Easily" | "Start 14 Day Free Trial" → `accounts.shopbase.com/sign-up` | 1 illustration (alt "Always here, whenever & wherever you need") + 4 vector icons | **rework**: guarantee, award and 24/7 claims have no source on the page; need confirmation they remain true in 2.0 |
| OLD-11 | Closing call to action | Last push to sign up | **H2:** "Kickstart your path to success today and grow your business at scale with ShopBase" | Start now | "Get Started For Free" → `accounts.shopbase.com/sign-up` | none | **keep (pattern)**: closing CTA to sign-up matches the chosen primary action; copy changes |
| OLD-12 | Footer | Navigate, legal, community | none (column titles "Features", "Shopbase", "Learn & Get Help") | 13 feature links, company links incl. **PrintBase** and **PlusBase**, apps, DMCA, Terms, Privacy, ShopBase Payments terms, ShopBase Marketplace terms, help, blog, wiki, updates, status; 4 Facebook community links | none (links only) | logo (alt "Shopbase - Cross-border Commerce Made Easy"), 4 social icons (alt empty) | **rework**: remove PrintBase and PlusBase; **keep** legal links |

## What works / what does not

**Basis.** The user supplied **no analytics, no feedback and no test results**. Everything below is judged against the strategy pack and the brief and is therefore `ASSUMPTION — no analytics`. No performance metric is stated. The only numbers are counts measured from the fetched HTML.

### Measured facts (computed with Python from the fetched HTML, 2026-10-24)

| Fact | Value |
|---|---|
| Page weight, HTML only | **102,276 bytes** (server sent it uncompressed; `gzip -c` locally gives 19,839 bytes). Images, CSS, fonts and video are separate and not measured |
| Lines of HTML / words of visible text | 499 lines / 1,464 words (includes the duplicated desktop and mobile blocks and the header and footer links) |
| Blocks (see inventory) | 12 (10 content blocks + header + footer); `<section>` tags: 1 |
| Anchors (`<a>`) | 102 in total: 31 relative paths, 16 fragment links (of which **13 are `href="#"`**, dead: 12 "Made in ShopBase" template tiles and the nav item "Why ShopBase"; 3 are the tab switches `#Ecommerce`, `#Drop-Shipping`, `#Print-On-Demand`), 9 without `href` (dropdown toggles), 18 on `www.shopbase.com`, 9 on `accounts.shopbase.com`, 3 on `templates.shopbase.com`, 16 on other hosts |
| CTAs styled as buttons (`w-button`) | **21**: 6 sign-up buttons (incl. 1 "Find out more") + 2 "Login" + 1 "Book a demo" button + 3 tab-switch buttons + 5 other "Find out more" (`/dropshipping` ×2, `/print-on-demand` ×2, `/creator` ×1) + 2 "Visit the template store" + 2 "Learn more". Not counted in the 21: the hero **email form** ("Join us") and the `/book-a-demo` text link in the nav |
| Routes to sign-up (`accounts.shopbase.com/sign-up`) | **7**: hero email form ("Join us"), "Start Free Trial", "Start 14-Day Free Trial", "Find out more" (tab 1, with utm), "Get started for free", "Start 14 Day Free Trial", "Get Started For Free" |
| Sign-up labels | **5 different spellings** for one action: "Join us", "Start Free Trial", "Start 14-Day Free Trial" / "Start 14 Day Free Trial" (hyphen differs), "Get started for free" / "Get Started For Free" (capitals differ), "Find out more" |
| Routes to sign-in | 3 ("Login" ×2 and the "Book a demo" **button**, whose `href` is `accounts.shopbase.com/sign-in`, a likely mislabel: `ASSUMPTION`, not confirmed) |
| Demo route | 1 (`/book-a-demo` text link in the header) |
| Heading structure | **H1 ×5** (hero + 4 in the mobile copy: "E-commerce brands", "Dropshipping", "Print-On-Demand", "Digital products"), H2 ×9, H3 ×8 (3 of them are the stat numbers "$700 Millions+", "365,500+", "90,000+"), no H4-H6. A page should normally have one H1 |
| Images (`<img>`) | **75** in total: 1 Facebook tracking pixel (`noscript`, no alt), 1 placeholder (a country flag swapped in by script), **73 content images**. Alt text: **13 non-empty**, **61 empty**, **1 missing**. Of the 13, 9 are placeholders ("Graphic 1" ×6, "Graphic 2", "graphic 3" ×2), 2 are the logo sentence, 2 are descriptive ("High conversion rate ", "Always here, whenever & wherever you need"). So 4 of 75 images carry a meaningful alt. 68 are `loading="lazy"`; 38 have `srcset` |
| Video | 9 Wistia iframes (`fast.wistia.net`, `seo=true`), 0 `<video>` |
| Mentions of AI | **0**. Searched visible text, attributes, meta tags and raw HTML for `\bAI\b`, "artificial intelligence", "machine learning", "CR Scan", "AOV": 0 hits each, on the homepage and on both legal pages |
| Mentions of PrintBase / PlusBase | PrintBase 3 in visible text (POD tab copy in the desktop tab and in the mobile copy, footer link); PlusBase 1 (footer link). Details in the Old-brand inventory |
| Mentions of Print on demand / Dropshipping | "Print on demand" (any spelling) 7 and "dropship*" 6 in static visible text; plus 3 meta tags that list "Dropshipping, Print-on-Demand"; plus the H1 typing animation, which shows both words to every visitor (`data-words` attribute, 1 each) |
| Mentions of Apps | the word "app(s)" 6 times in visible text: nav "Apps" ×2, "third-party apps" ×2 (desktop and mobile copy), "Apps & global partners ecosystem 24/7 support", footer "Apps"; plus "Mobile app (Android/iOS)" ×2 and "app mazes" ×1 in the hero sub-line |
| `<script>` tags | 24 (11 with `src`, 13 inline; inline total 19,136 bytes, of which one block is 15,610 bytes) |
| Third-party script hosts (by `<script src>`) | **7**: `cdn.prod.website-files.com` (Webflow), `ajax.googleapis.com` (webfont loader), `www.googletagmanager.com`, `www.googleoptimize.com`, `d3e54v103j8qbb.cloudfront.net` (Webflow jQuery), `statuspal.io`, `unpkg.com`. Plus 1 same-site relative script (`/haqt6iy0...`, Google tag first-party path) |
| Third-party hosts that run or load something (scripts, injected scripts, pixel, iframes, API calls) | **12**: the 7 above + `connect.facebook.net` (script injected), `www.facebook.com/tr` (pixel), `cdn.sender.net` (injected), `fast.wistia.net` (iframes), `loc.beeketing.com` (location lookup call). Plus Google Fonts (`fonts.googleapis.com`, `fonts.gstatic.com`) = 14 if fonts are counted. Same-company hosts called by script: `xt.shopbase.com`, `api.shopbase.com` |

### What works (first view, against the strategy pack and the brief; `ASSUMPTION — no analytics`)

1. **One action repeated.** 7 of the sign-up routes lead to the same place, which matches the chosen primary CTA (sign up). (Kept in spirit; labels need unifying.)
2. **A clear trial hook.** "Start 14-Day Free Trial" and meta "free for 14 days" are explicit. Whether 2.0's "Free Launch plan" replaces this is open (brief Q3). Not an observation about performance.
3. **Short, scannable structure:** 10 content blocks, one H2 per block, benefit-style tab titles. Candidates to reuse as a pattern.
4. **Stats and testimonials exist**: the page already has a trust layer to rebuild with proof (but see below).
5. **Affiliate and campaign tracking is wired** (see Must-keep K12). The page passes referral parameters into some sign-up paths (header sign-up buttons, hero form, one tab link); losing it would be silent.

### What does not work (first view, against the strategy pack and the brief; `ASSUMPTION — no analytics`)

1. **The page says nothing about AI** (0 mentions) and its promise is "build a business in a few clicks / all-in-one". It does not carry the new AI-first USP at all.
2. **It sells three products by audience** (E-commerce brands, Dropshipping, POD, plus Digital products on mobile) and links out to `/dropshipping`, `/print-on-demand`, `/creator`; even the hero H1 cycles through "E-commerce / Dropshipping / Print-On-Demand". This contradicts "ShopBase 2.0 is one independent product".
3. **It names dead brands** (PrintBase, PlusBase, PrintHub, PlusHub) in copy, footer and logo files (see inventory).
4. **Unsupported claims**, which the brief says need proof: "$700 Millions+", "365,500+ merchants", "90,000+ stores", "100% Happiness Guarantee", "Award-winning Support Team", "24/7", "best eCommerce platform" (meta description), "higher conversion rate". No source or date is shown on the page for any of them.
5. **Five H1s** and, for images, 4 of 75 with a meaningful alt. For SEO and accessibility this is weak (measured, see table).
6. **Inconsistent CTA labels** (5 spellings of one action) and a "Book a demo" **button** that points to sign-in, while the nav text link "Book a demo" points to `/book-a-demo`.
7. **Dead interaction:** 13 `href="#"` links (12 template tiles and the nav item "Why ShopBase").
8. **Persona fit:** the page does not mention what the personas care about (payment holds, ads, conversion, Vietnamese support: pack). `ASSUMPTION`: this is a gap against the pack, not a measured loss.
9. **Weight and tag clutter:** 24 scripts, 12 third-party hosts that run code or load content, a Google Optimize tag and a Universal Analytics ID (see Must-keep K7, K9). Both products are retired, verified on 2026-10-24 from Google's own help pages: standard Universal Analytics properties "stopped processing hits" from July 1, 2023 (https://support.google.com/analytics/answer/11583528), and "Google Optimize and Optimize 360 are no longer available as of September 30, 2023" (https://support.google.com/optimize/answer/12979939). The Optimize script URL still answers HTTP 200 with 329,504 bytes (checked by status only, not opened), so it may still cost load time while doing no testing.
10. **No canonical, no hreflang, no structured data in the homepage HTML** (see SEO snapshot), while both legal pages have a canonical and hreflang.

## Feedback received

**None supplied.** The user gave no stakeholder, customer or test feedback (`00-project-type.md` answer 3; `brief.md` §5; `03-brief-analysis.md` Q15). No analytics, heat maps, sign-up rate or conversion numbers exist in the project. `ASSUMPTION`: none.

## Must-keep list

**The user named nothing** (brief §5: "Must-keep list ... none supplied. `ASSUMPTION`: none."). Default: **none confirmed**.

Everything below is **SUSPECTED** (found by Claude in the live HTML) and **needs the user to confirm** (table in the Questions section). Do not treat any row as mandatory until confirmed.

| # | Item | Where found | Why it may need to stay | Status |
|---|---|---|---|---|
| K1 | `/pricing` | nav link | existing URL, linked from the header | SUSPECTED, confirm |
| K2 | `/book-a-demo` | nav link | existing URL; the brief says Home CTA is sign-up only, so the page may stay while the link goes | SUSPECTED, confirm |
| K3 | `/features` and the 13 `/features/*` pages (storefront, upsell, marketing-seo, products, store-management, cart, hosting, analytics, mobile-ecommerce, fulfillment, ecosystem, global-selling, support) | nav and footer | inbound links and SEO of other pages (outside P01 scope) | SUSPECTED, confirm |
| K4 | `/about`, `/partners`, `/affiliate`, `/compare`, `/learning-hub`, `/shopbasehero`, `/shopbase-apps`, `/multi-channel`, `/creator`, `/dropshipping`, `/print-on-demand` | nav, footer, body CTAs | existing URLs; the last two and `/creator` belong to the old product split and their fate is a user decision (pack Q8) | SUSPECTED, confirm |
| K5 | Legal links: `/dmcareport`, `/terms-of-service`, `/privacy-policy`, `/shopbase-payments-terms`, `/shopbase-marketplace-payments-terms` | footer | legal text must stay reachable from Home | SUSPECTED, confirm |
| K6 | External app and community links: `accounts.shopbase.com/sign-in` and `/sign-up`, `templates.shopbase.com`, `blog.shopbase.com`, `help.shopbase.com`, `developers.shopbase.com`, `updates.shopbase.com`, `network.shopbase.com`, `www.shopbasestatus.com`, Google Play and App Store app links, 4 Facebook community links | header, body, footer | working destinations; sign-up and sign-in are the conversion path | SUSPECTED, confirm |
| K7 | Google tags: Universal Analytics `UA-138241145-1` (called both via a first-party path `/haqt6iy0.../...` and a normal gtag config) and Google Ads `AW-944639611` (+ a page_view event whose values are still the placeholder text "replace with value") | head | analytics and ads measurement; no GA4 (`G-`) id and no GTM container appear in the HTML | SUSPECTED, confirm; also confirm whether GA4 is set elsewhere |
| K8 | Facebook Pixel `1078285869667214` (script) and `501990101818261` (noscript image + a second init) | head, body | ad measurement | SUSPECTED, confirm |
| K9 | Google Optimize container `OPT-WTCPP3K` | head | A/B test tag; page `/a-b-test-hero-image` exists in the sitemap (Step 00). Google Optimize was retired on September 30, 2023 (source in "What does not work" 9), so the tag runs no tests; UA `UA-138241145-1` (K7) likewise no longer processes hits | probably **drop**, not keep; confirm |
| K10 | Domain verification metas: `google-site-verification` ×2 (`Tq8pr3zH...`, `C_fi6GTTN...`) and `facebook-domain-verification` (`4517kwjo...`) | head | removing them can break Search Console or Facebook domain verification | SUSPECTED, confirm |
| K11 | Sender (email) universal script, id `2c42e340654674`; hero email form posts to sign-up | head, hero | email capture and marketing; whether it is still used is unknown | SUSPECTED, confirm |
| K12 | Affiliate / referral logic in an inline script (15,610-byte block): reads `fpr`, `fpt`, `clickId`, `invite_trial` from the URL, stores them in cookies, and every 3 s appends them to (a) links whose `href` already contains `sign-in?` or `sign-up?` (on this page: only the tab-1 "Find out more" sign-up link; no sign-in link has a `?`), (b) the two header sign-up buttons (`.navigation-right .button-navigation`), (c) forms posting to `accounts.shopbase.com` (the hero form, as URL parameters and hidden inputs). The plain body sign-up buttons ("Get started for free", "Start 14 Day Free Trial", "Get Started For Free") and the sign-in links are **not** rewritten. If `fpr` is in the URL it also POSTs `ref_code`, `shop_type` (second label of the hostname, i.e. "shopbase") and the URL to `api.shopbase.com/admin/affiliate/link-log`. Read from the code, not tested in a browser; it also looks buggy (the `clickId` cookie is written with the `fpt` value; the cookie-only branch passes URL values to the header button and forms) | inline script | the Affiliate programme and invite trials probably depend on it; if the new Home drops it, referral credit is lost | SUSPECTED, strong; confirm |
| K13 | Country cookie `sbLdingCtryCode` (lookup on `loc.beeketing.com`), which, for BD/IN visitors, shows a country flag in the header and inserts "from Bangladesh" / "from India" into the hero H1; and hides footer Facebook links by country (everyone sees "ShopBase"; VN also "ShopBase VN"; CN also "ShopBase CN"; all others also "Dropshipping Zone") | inline script | localisation behaviour; note it depends on a `beeketing.com` host (old company domain) | SUSPECTED, confirm |
| K14 | `xt.shopbase.com/uts/app.js` (first-party tracker), Statuspal status widget (`.sp-status`), the "sitekit smart bar" handler | inline scripts | internal tooling | SUSPECTED, confirm |
| K15 | Page title and meta description wording (with keywords "eCommerce", "dropshipping", "print-on-demand") | head | existing ranking, if any (no data) | SUSPECTED; positioning change means these probably change; the user decides (Step 12/13) |
| K16 | Structured data, canonical, hreflang | **not present** on the homepage HTML | n/a | nothing to keep; to add later (see SEO snapshot) |

## SEO snapshot

Page: **P01 Home**. Source: the fetched raw HTML and response headers of 2026-10-24. Keywords are read **only** from title, H1 and meta; no search volume is claimed (none available).

| Item | Value |
|---|---|
| URL | `https://www.shopbase.com/` (HTTP 200, no redirect) |
| Title (48 characters) | `ShopBase | Build a profitable eCommerce business` |
| Meta description (179 characters) | `ShopBase is the best eCommerce platform specialized for modern businesses with easy setup, no risk, free for 14 days. Dropshipping, Print-on-Demand, Online Brand, Content Creator.` |
| H1 | `Build a profitable E-commerce business in a few clicks with ShopBase` (hero; static HTML. In a browser "E-commerce" cycles to "Dropshipping" and "Print-On-Demand" by script, see OLD-02). **4 more H1s** in the mobile copy: "E-commerce brands", "Dropshipping", "Print-On-Demand", "Digital products" (5 in total) |
| Canonical | **not present** in the HTML (no `<link rel="canonical">`; no `Link` header). The two legal pages do have one |
| Robots | **not present**: no `meta name="robots"`; no `X-Robots-Tag` header. `robots.txt` was **not fetched** (outside scope): `NOT AVAILABLE` |
| Open Graph | 4 tags: `og:title` = same as title, `og:description` = same as meta description, `og:image` = `https://cdn.prod.website-files.com/5e941e9c459693aeff757d94/645e055176ae297d29827628_ShopBase.jpg`, `og:type` = `website`. **Missing:** `og:url`, `og:site_name`, `og:image:alt` |
| Twitter card | `summary_large_image`; title, description, image same as Open Graph |
| hreflang | **not present** on the homepage. (Privacy policy page has `en` and `zh-cn` → `www.shopbase.net.cn/privacy-policy`; Terms has `en` only.) The Chinese and Vietnamese variants named in Step 00 are not linked from the homepage HTML |
| Structured data (JSON-LD / microdata) | **none** in the static HTML (0 `application/ld+json`, 0 `itemtype`). The 9 Wistia embeds use `seo=true`; whether Wistia injects video markup at runtime was not checked: `NOT AVAILABLE` |
| `<html lang>` | `en-US` |
| Main keywords (from title, H1, meta only) | "ShopBase" (brand), "eCommerce business", "profitable", "eCommerce platform", "dropshipping", "print-on-demand", "online brand", "content creator", "free for 14 days", "in a few clicks". Note: the meta description lists the old product split (dropshipping, POD, online brand, content creator) and the superlative "the best eCommerce platform" |
| Favicon / touch icon | `logo32.png`, `logo 256.png` (present) |
| Hosting / stack | Webflow (CloudFront in front); `Cache-Control: public, max-age=120` |
| Not available | search rankings, queries, backlinks, Search Console data, sitemap check (321 URLs per Step 00; not re-fetched), `robots.txt`: `NOT AVAILABLE` |

## Old-brand inventory

**Type C: the ShopBase name and logo stay; positioning changes; PrintBase and PlusBase no longer exist as brands.** This list drives Step 24 (pre-launch).

### How it was searched

1. Downloaded the raw HTML of the homepage, `/terms-of-service` and `/privacy-policy`.
2. Parsed with Python `html.parser`. Built three views of each page: **(a) visible text** (script and style removed), **(b) attributes** (`alt`, `title`, `href`, `src`, `content`, `placeholder`, `value`, `aria-label`), **(c) raw HTML** (everything, including scripts and `srcset`).
3. Case-insensitive regular expressions: `printbase`, `plusbase`, `plushub`, `printhub`, `print[\s-]*on[\s-]*demand`, `\bPOD\b`, `drop[\s-]?ship`, `profitable\s+e-?commerce\s+business`, `in a few clicks`, `all[\s-]in[\s-]one`, `app mazes`, `beeketing`, e-mail pattern, legal-entity words (`Inc|LLC|Ltd|Limited|Pte|Corp|Corporation|JSC|Company|GmbH`), plus host extraction from every `href`/`src`/URL in the HTML.
4. Every hit was printed with its surrounding words and read by hand to remove false positives (for example "limited" in legal text; `typer-dot-js@0.1.0` matching the e-mail pattern; "profitable eCommerce" matched in the `<title>`).
5. **Counting rule:** the homepage nav text appears twice (top-level and dropdown, plus a mobile menu) and the product-tab block appears twice (desktop tabs and the mobile copy), so visible counts include these repeats. The "where" column says which.
6. **Not searched:** images as pixels (logos are checked by **file name** only; what the logo files show was not viewed), CSS, the other 319 URLs, PDF/ebook assets, ad accounts, the app stores, `help.`, `blog.`, `templates.`, `accounts.` pages.

### Homepage

| Old item | Visible-text count | Where (homepage) |
|---|---|---|
| **PrintBase** | 3 | POD tab 3: "Focus on what you do best, with PrintBase and ShopBase Payments, you can outsource intensive operation tasks to us." (desktop tab ×1 and mobile copy ×1); footer link "PrintBase" → `https://www.printbase.com/?utm_source=cs&utm_medium=sb-footer` (also 1 in attributes) |
| **PlusBase** | 1 | footer link "PlusBase" → `https://www.plusbase.com/`; image file `PlusBase Logo Dark Color.png` in the header (the second header logo, alt "ShopBase - Cross-border Commerce Made Easy"; which logo it actually shows was not viewed: `NOT VERIFIED`) |
| **PrintHub** | 0 | integrations strip: image file `Printhub.png` (alt empty) |
| **PlusHub** | 0 | integrations strip: image file `Plushub.png` (alt empty) |
| **"Print on demand" / "Print-On-Demand" / "Print-on-demand"** | 7 | nav "Print on demand" ×2 (top level and dropdown); tab button "Print-On-Demand" ×1; H2 "Print-On-Demand" ×1; mobile H1 "Print-On-Demand" ×1; body "Print-on-demand products" ×2 (desktop and mobile copy). Also the **hero H1 typing animation** (`data-words`, shown to every visitor in a browser) ×1. Also in links: `/print-on-demand` ×4 (nav ×2, "Find out more" ×2), `#Print-On-Demand` ×1. Also meta description, `og:description`, `twitter:description` ("Dropshipping, Print-on-Demand, ...") ×3 |
| **"Dropshipping"** | 6 | nav ×2; tab button ×1; H2 ×1; mobile H1 ×1; footer community link "Dropshipping Zone" ×1 (hidden by script for VN and CN visitors). Also the hero H1 typing animation ×1. Also links `/dropshipping` ×4, `#Drop-Shipping` ×1; and the same 3 meta descriptions |
| **Old promise** "Build a profitable E-commerce business in a few clicks with ShopBase" | 1 exact (H1); "profitable eCommerce business" 3 in visible text (`<title>`, H1, testimonial "Profitable E-Commerce Business"); also `og:title` and `twitter:title` | head (title, og, twitter), hero H1, testimonial 3 |
| Other old-promise wording | "in a few clicks" 1 (H1); "all-in-one" 3 (hero sub-line; "all in one convenient spot" ×2); "app mazes" 1 (hero sub-line); "No more money waste for third-party apps" ×2 | hero, OLD-04 |
| **Old product names** (other) | | "ShopBase Payments" ×3 (POD tab ×2, footer ×1); "ShopBase Marketplace" ×1 (footer); "ShopBase Hero" ×1 (nav dropdown); "ShopBase Network" ×1 (nav dropdown, `network.shopbase.com`); "Templates" (nav, `templates.shopbase.com`); "Made in ShopBase" ×12 (tiles). These are not on the user's removed list; whether they stay under 2.0 is open |
| **Support e-mail** | 0 | none on the homepage |
| **Legal entity name** | 0 | none on the homepage; the footer says "© ShopBase 2024. All rights reserved." in the HTML (rewritten by script to the current year) |
| **External domains / hosts** | see right | `accounts.shopbase.com` (sign-in/up, 9 anchors + form), `templates.shopbase.com` (3), `blog.shopbase.com` (1, plus `www.shopbase.com/blog` ×2 in nav), `help.shopbase.com` (2), `developers.shopbase.com`, `updates.shopbase.com`, `network.shopbase.com`, `www.shopbasestatus.com`, `www.printbase.com`, `www.plusbase.com`, `play.google.com`, `apps.apple.com`, `www.facebook.com` (4 groups/pages). Script-only: `loc.beeketing.com`, `api.shopbase.com`, `xt.shopbase.com` |
| Old brand assets (file names) | | `Logo full.svg`, `PlusBase Logo Dark Color.png`, `ShopBase-Logo Light@1x.svg` (footer), `sb smilde.svg`. The logo files were **not opened**; whether the PlusBase-named file shows the ShopBase or PlusBase logo is `NOT VERIFIED` |
| Copyright | | "© ShopBase 2024" in HTML (script rewrites to current year) |

### Legal pages (`/terms-of-service`, `/privacy-policy`)

Body text of both pages contains **none** of PrintBase, PlusBase, PrintHub, PlusHub (0 hits in the legal text itself). Old names appear only in the shared header and **two footers** that each legal page carries (an older footer variant plus a second block).

| Old item | Terms of service | Privacy policy |
|---|---|---|
| PrintBase | 2 (footer link text ×2 → `printbase.com/?utm_source=cs&utm_medium=sb-footer`) | 2 (same) |
| PlusBase | 2 (footer link ×2 → `plusbase.com`) + image file `PlusBase Logo Dark Color.png` in the header | 2 + same header image |
| PrintHub | 1 (footer link text "PrintHub", its `href` is `/privacy-policy`, a likely wrong target: `ASSUMPTION`) | 1 (same) |
| "Print on demand" / "Dropshipping" | nav only: 2 + 3 (no body use). Body: 0 | nav only: 2 + 3. Body: 0 |
| **Legal entity** | **"OpenCommerce Group, Inc"** ×2 (opening paragraph: `offered by OpenCommerce Group, Inc ("ShopBase")`; closing line `Copyright 2021 OpenCommerce Group, Inc.`) | **"OpenCommerce Group, Inc."** ×1 (opening: "operated by OpenCommerce Group, Inc. ("ShopBase", ...)") |
| **Support e-mail** | `support@shopbase.com` ×1 | `support@shopbase.com` ×1 and `support@ShopBase.com` ×1; link to `support.shopbase.com/support/home` ×1 |
| Copyright line | "© ShopBase 2021" ×2 (two footers) and "Copyright 2021 OpenCommerce Group, Inc." ×1 | "© ShopBase 2021" ×2 |
| Governing law / jurisdiction | "laws of Singapore" and "courts located in Singapore" (observed in the text; not interpreted) | "Your California Privacy Rights" section |
| Extra hosts in footers | `apps.shopbase.com` ("App Store", `apps.shopbase.com/category/all-apps`), `www.shopbase.com/wiki/` ("Wikipedia"), `blog.`, `help.`, `updates.` | same + `www.shopbase.net.cn` (hreflang `zh-cn`) |
| Other legal-side facts | Both pages say ShopBase is a name defined for OpenCommerce Group, Inc. The company name differs from "ShopBase" everywhere else on the site | The privacy policy names Google Inc. (Analytics) as a third party |
| Last-updated date | none found in the text | none found |

**What this tells Step 24:** the legal entity "OpenCommerce Group, Inc", the 2021 dates and the PrintBase/PlusBase/PrintHub footer links are in the legal pages and are **not** changed by a homepage redesign. Whether the entity name and e-mail stay is a legal question for the user (see Questions). Both footers on the legal pages would need their own cleanup if the user wants them to match the new Home.

## Assumptions

1. **No analytics, feedback or numbers were supplied; none are invented.** Every "works / does not work" statement is `ASSUMPTION — no analytics`; the only numbers are counts from the fetched HTML.
2. The live page fetched on 2026-10-24 is the current public homepage. Pages behind a login, A/B variants (the Optimize tag suggests tests existed) or geo variants (a script changes a flag, the H1 wording for BD/IN and Facebook links by country) may differ from what other visitors see. `ASSUMPTION`
3. The second copy of the product tabs (with the H1s and "Digital products") is a mobile-only block, and OLD-05 is therefore hidden on desktop. Inferred from class names only; CSS not fetched. `ASSUMPTION`
4. The header's second logo file (named `PlusBase Logo Dark Color.png`) and the "Book a demo" button pointing to sign-in are probable leftovers. `ASSUMPTION`, not confirmed.
5. All counts for "visible text" include repeated blocks (see the counting rule).
6. Universal Analytics and Google Optimize are retired products (verified from Google's help pages, sources in "What does not work" 9). Whether the Google Ads and Facebook accounts behind the other IDs are still active, and whether GA4 is set up elsewhere, is not verifiable from the HTML. `ASSUMPTION`
7. The footer PrintHub link target `/privacy-policy` is read as a mistake. `ASSUMPTION`
8. Counts of Print on demand / Dropshipping in the nav are a fact; whether those nav items stay is an open pack question (Q8).

## Questions for the user

Only things the user can answer. Defaults are used until answered.

### 🔴 Must answer
None. Nothing in this audit blocks Step 05. (The proof blocker for Step 09 stays as in `03-brief-analysis.md` Q2.)

### 🟡 Should answer
1. **Analytics access / real numbers.** Can you share (a) Home traffic, (b) the visitor-to-sign-up rate, (c) which CTAs are clicked, (d) where visitors leave (e.g. a GA4, Google Ads or Hotjar export or screenshots)? *Default: none; Step 05 records "no baseline"; every verdict stays a first view.*
2. **Which tags and scripts must stay on the new Home?** Specifically the affiliate/referral logic (`fpr`, `fpt`, `clickId`, `invite_trial`), the Google Ads tag, Facebook Pixels, Sender, and the domain-verification metas (K7-K14). *Default: all kept as a technical requirement for Step 21 / 24; none removed until you say. Exception proposed: the retired Universal Analytics config and Google Optimize tag (K7, K9) are flagged for removal, still only with your yes.*
3. **Is Google Analytics 4 (or Google Tag Manager) set up elsewhere?** The HTML only shows a Universal Analytics id and a Google Ads id. *Default: unknown; the build keeps the existing tags unchanged and adds nothing.*
4. **URLs: confirm the suspected must-keep list** (`/pricing`, `/book-a-demo`, `/features/*`, `/about`, `/compare`, `/dropshipping`, `/print-on-demand`, `/creator`, legal pages). Which stay as live pages, which are retired or redirected? *Default: all stay reachable; the Home links only to the ones you confirm.*
5. **Header "Book a demo".** Keep it as a secondary link, or remove it, given that the Home goal is now sign-up only? *Default: not specified; Step 12 proposes.*
6. **Legal entity and e-mail.** Should the legal pages and footers keep "OpenCommerce Group, Inc", `support@shopbase.com` and the 2021 copyright, or will legal text be updated with 2.0? *Default: unchanged; legal pages are not in scope (P01 only); flagged for Step 24.*
7. **Stats and testimonials.** Are "$700 Millions+", "365,500+ merchants", "90,000+ stores", "100% Happiness Guarantee", "Award-winning Support Team" and the three quotes still true, sourced and approved for reuse? *Default: not carried into new copy without your confirmation (brief: no numbers without proof).*

### ⚪ Nice to have
8. Whether the header logo file named `PlusBase Logo Dark Color.png` is a real ShopBase logo or a PlusBase logo (the audit did not open the image). *Default: treated as a mislabelled file; the logo comes from `02-assets/logo/`.*
9. Whether the Google Optimize tag and the `/a-b-test-hero-image` pages are still used. *Default: not used.*
10. Whether the country-based behaviour (flag for BD/IN, Facebook groups per country) should continue. *Default: dropped from the new Home unless you ask (English only, no Vietnam-specific content).*

## Check before handing back

- [x] Every section of the existing page is in the inventory (12 blocks: header, 10 content blocks, footer; the tab block's mobile copy is described inside OLD-04/OLD-05).
- [x] No metric appears without a source from the user. (Only counts computed from the fetched HTML; the live-page numbers "$700 Millions+", "365,500+", "90,000+" are quoted as the page's own claims and marked unverified.)
- [x] The must-keep list includes everything the user named. (The user named nothing; "none" is stated, and every listed item is labelled SUSPECTED for the user to confirm.)
- [x] Type C: the old-brand inventory has entries, with how it was searched.
- [ ] Items NOT RUN or NOT AVAILABLE: rendered view (desktop vs mobile), logo images opened, CSS, `robots.txt`, sitemap re-check, Wistia runtime structured data, all analytics. Stated above; nothing ticked for them.
