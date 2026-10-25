# 00 · Project type

## Type
**C · Rebrand.** A live site exists (https://www.shopbase.com/) and the product exists. The positioning and promise change: ShopBase 2.0 is "ShopBase for the AI era" (user decision, 2026-10-24). The ShopBase name, logo and colours stay.

**Reason for C (not B):** type B means "the brand stays". Here the name, logo and colours stay, but the positioning and promise change (toward AI-first), and ShopBase 2.0 becomes one independent product (PrintBase and PlusBase no longer exist as brands). Per `CLAUDE.md`, C covers "the name, positioning or identity changes"; positioning changes.

**History:** changed from B on 2026-10-24 (user decision). No later step had been run yet (`_progress.md`: Steps 01–26 `not started`), so nothing is stale. Steps 09 and 10 and Gate 3 now apply (Brand module on).

## Answers
1. **Landing page today?** Yes. https://www.shopbase.com/ (page title: "ShopBase | Build a profitable eCommerce business"; headline: "Build a profitable E-commerce business in a few clicks with ShopBase").
2. **Brand today?** Yes: logo and colour palette. Name, logo and colours stay unchanged. What changes is the positioning and promise (ShopBase 2.0, "ShopBase for the AI era"). Identity work is limited to the existing logo and colours.
3. **Numbers, feedback, must-keep items?** Not provided. Default used: no numbers, no feedback, no must-keep list. `ASSUMPTION`
4. **Scope?** The whole website is the long-term scope. The workflow runs on the **Home page only** for now, to settle concept and style. Page inventory below. Confirmed by the user (2026-10-24): only Home.
5. **Do current customers read this page?** Yes (confirmed by the user). Current merchants read the Home page. `ASSUMPTION`: they resemble personas A and B. What they need to hear that a new visitor does not: not stated yet; Step 01 and Step 07 ask or research it.
6. **Audience (decided 2026-10-24):** follows the personas: experienced dropshipping and POD sellers, Vietnam-based, selling to US/EU buyers. Vietnam-specific pains from the sheet are kept.
7. **Product structure (decided 2026-10-24):** ShopBase 2.0 is one independent product. PrintBase and PlusBase no longer exist as brands.

## Pages in scope
- **P01 · Home** · `https://www.shopbase.com/` · job: present ShopBase 2.0 ("ShopBase for the AI era") to experienced sellers and send the visitor to sign up. Updated 2026-10-24: the user chose sign-up as the primary call to action (earlier "sign up or book a demo" from the live nav is superseded); the North Star wording is still `ASSUMPTION` (see Step 03). (Headline on the live page today: "Build a profitable E-commerce business in a few clicks with ShopBase".)

Other pages are **not in scope for now** and have no `P##` code. They can be added later; they take the next free code.

## Page inventory (for scope decision)
Source: header and footer navigation of the homepage, plus `sitemap.xml`, which lists **321 URLs** (collected at the first Step 00 run; not re-checked in this rewrite; for scope only, not a source for Home claims).

**Main-site pages from the navigation (candidates for later):**
- Header: Features, Print on demand, Dropshipping, Compare ShopBase, About, Learning hub, ShopBase Hero, Apps, Pricing, Book a demo
- Features sub-pages (13): storefront, upsell, marketing-seo, products, store-management, cart, hosting, analytics, mobile-ecommerce, fulfillment, ecosystem, global-selling, support
- Company: About us, Partners, Affiliate
- Learn: E-commerce wiki (`/wiki/`, probably on another host, to check), Apps
- Legal (5): DMCA, Terms of service, Privacy policy, ShopBase Payments terms, ShopBase Marketplace terms
- Other linked pages: Creator, Multi-channel (plus 6 channel sub-pages: Pinterest, TikTok ads, SEO, email marketing, Google Ads, Facebook advertising)

**Sitemap groups (321 URLs in total):**
- `dkb` 51: ebooks, webinars, store demos, product lists (campaign / content pages)
- `zh` 35: Chinese-language version
- `features-vn` 13 and `viet-nam-page` 8: Vietnamese version
- `features` 14 (same as the navigation)
- `multi-channel` 7, `learning-hub` 2, `contest` 3, `confirmation` 2, `a-b-test-hero-image` 2, `vn` 3, `webinars` 1
- Root-level slugs 179: many are old campaigns, duplicates, test pages (for example `home-test`, `home-backup`, `old-home-3`, `pricing-copy`) and other-country pages

Most of the 321 URLs are probably old campaigns or language variants. The user decided: only Home for now. Note: the header nav on the live page still shows "Print on demand" and "Dropshipping" as items; whether they stay under the one-product ShopBase 2.0 is not stated (`01-strategy-pack.md` 🟡 Q8).

## Modules
- **Brand module: ON.** Type C. Steps 09 (Messaging) and 10 (Identity) will run later, and Gate 3 applies. Identity is limited to the existing logo and colours (name, logo, colours stay); the work is the new messaging and how the existing assets express "ShopBase for the AI era".
- Figma / handoff: off (default).

## Roles
- Strategy owner: the user
- Publisher: the user
- Content reviewer: the user (confirmed 2026-10-24). Gate 5 approver, and sign-off before any wording on trademarked, DMCA or restricted products.
- Builder: not assigned (`ASSUMPTION`: Claude runs the workflow, the user exports the build)

Language: English only (confirmed by the user 2026-10-24: no Vietnam-specific content and no Vietnamese-support promise on Home; pack 🔴 Q2 closed).

## Steps skipped for this type
None. Type C applies to every step 00–26; the Brand module is on, so Steps 09 and 10 and Gate 3 run.

## Brand references received (for later steps)
- Colour scale (Neutral, Blue as Primary, Green, Red, Yellow, Indigo; shades 50–950). Primary blue at 500 is `#0096ed`. Used at Step 16 Palette, not decided here.
- Typography scale: h1 28px/36, h2 23px/32, h3 20px/28, h4 16px/24, h5 12px/16, body 14px/20, large 16px/24, small 12px/16. Used at Step 19 Tokens.
- Logo (full colour, white version, icon). Stored later in `02-assets/logo/`.
- These stay for ShopBase 2.0 (user decision, 2026-10-24).

## Open questions
Carried into `01-strategy/01-strategy-pack.md` (Open questions), which holds the current numbering and priority:
- 1. What current merchants need to hear on Home that a new visitor does not → pack 🟡 Q3. *Default: nothing different.*
- 2. ~~Vietnam-specific items on an English page → pack 🔴 Q2.~~ Closed 2026-10-24: English only, no Vietnam-specific content, no Vietnamese-support promise.
- 3. Are the "Print on demand" and "Dropshipping" nav items kept in ShopBase 2.0? → pack 🟡 Q8. *Default: not assumed; Home does not depend on them.*

## Assumptions
- No numbers, feedback or must-keep items were supplied (Q3).
- Builder not named (see Roles).
- Existing merchants resemble personas A and B (Q5).
- ~~The Home conversion goal (sign up / book a demo) is inferred from the live nav only.~~ Closed 2026-10-24: the user chose sign-up.
