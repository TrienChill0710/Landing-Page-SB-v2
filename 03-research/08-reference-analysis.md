# 08 · Reference analysis

Project: ShopBase website redesign · type **C · Rebrand** · page **P01 Home** · files in English · Gate 0 and Gate 1 `APPROVED` (`_progress.md`, 2026-10-24). Research date: **2026-10-24**.
Inputs read: `CLAUDE.md`, `_prompts/README.md`, `_prompts/08-reference.md`, `_progress.md`, `01-strategy/01-strategy-pack.md`, `01-strategy/brief.md`, `03-research/06-positioning.md`, `03-research/07-voc.md` (interim: no Reddit, quotes not byte-verified), `03-research/04-audit.md`, and the hero screenshot `02-assets/images/hero-2.0-reference.png` (viewed).

> **Status and limits (read first).**
> - **The user supplied no reference sites.** The set below was chosen by Claude to learn one specific thing each for our USP: an AI feature that scans a store, finds what stops shoppers, proposes fixes, and the seller approves every change (results `UNPROVEN`, no numbers). See open question 1.
> - **Method.** Each page was fetched on 2026-10-24 with `curl` (browser User-Agent, 1 s pauses, HTTP 200) into a new folder under the scratchpad and read with a script run as `python3 -I` from another folder. All 8 pages returned server-rendered HTML, so headings, buttons and body text are **byte-read from the HTML** (not summariser-read). `WebFetch` was not needed for any reference. `lovable.dev` answered HTTP 403 and was dropped (no bypass tried). `shopify.com/magic` redirects to `shopify.com/sidekick`; `hotjar.com` redirects to `contentsquare.com/hotjar/`; neither is used as a reference.
> - **Not viewed in a browser.** Anything about visuals, colour, motion, imagery, layout or whether a demo is animated is `NOT VERIFIED (not viewed in a browser)`. Section order below is the **order of headings in the HTML source**, which is usually but not always the visual order.
> - **Evidence rule (N10).** No reference below has conversion evidence in what was fetched. For every reference: **no conversion evidence**. Some pages print their own numbers; those are the vendor's claims, unchecked, and are not a reason to choose a pattern.
> - **VoC ids** cited below point to `03-research/07-voc.md` (interim; "A-n" = Persona A pain rank n, "B-n" = Persona B pain rank n, "AI section" = "AI that changes the store: what real sellers said"). The sample is complaint-heavy and not byte-verified; the ids give direction only.
> - **Review re-check (2026-10-24, about 07:50 UTC).** All 8 URLs were downloaded again with `curl` (browser User-Agent, 1 s pauses; all HTTP 200, no block) into a new folder and every quote, heading, CTA label and section order below was searched as an exact string in the parsed text (`python3 -I`, run from another folder). Corrected at review: Cursor's control sentence is a customer quote (Andrej Karpathy), and "Ready for Review" is a status group in a task list; Copilot's "Direct agents from issue to merge" / "Enforce quality at merge" are site-menu text and its "open issue" line is the meta description; Intelligems' rollback line is a full-code feature, its closing CTA is "Book A Demo", and its mock card also shows "+6.2%"; Notion's control line is a card inside "Designed for teams."; Squarespace's "No credit card required" sits under the hero, in step 1 and in the closing CTA (not the FAQ), and a scale strip sits right under the hero; Clarity's "Free heatmaps" line is the page title; a Shoplift heading was misquoted. Hex counts reproduced exactly.
> - **Search note.** Two standard `WebSearch` queries returned mostly vendor blogs and directories, not homepages, so candidates were chosen by name and then fetched. The set is a judgement, not a survey (`ASSUMPTION`).

## References

All fetched **2026-10-24** (HTTP 200, server-rendered).

| # | Reference | Link | Family | Why chosen (one line) |
|---|---|---|---|---|
| R1 | Cursor | https://cursor.com/ | AI product with real UI and a human review step | Hero pairs the claim with a mock of the product's task list, grouped under "In Progress" and "Ready for Review"; a customer quote on the page (Andrej Karpathy) says "you control how much independence to give the AI". Learn: how to show a task-then-review loop. |
| R2 | GitHub Copilot | https://github.com/features/copilot | AI product, approval and control | Describes the chain "from an open issue to reviewing and merging a pull request" (meta description, not visible copy; the visible body says "review changes, and merge completed work"); FAQ has Privacy and Responsible AI. Learn: approval as a named step before anything ships. |
| R3 | Intelligems | https://www.intelligems.io/ | AI CRO / AOV tool for Shopify | Closest topic to CR Scan AI and AOV AI: AI surfaces test ideas, builds them, store recommendations; has rollback copy. Learn: how a CRO/AOV AI is shown without a store-wide promise. |
| R4 | Shoplift | https://www.shoplift.ai/ | AI CRO tool for Shopify | "Lift Assist" analyses sessions, recommends and generates changes; one-click "Apply Variant". Learn: recommend-then-apply wording, and the proof layout to avoid. |
| R5 | Microsoft Clarity | https://clarity.microsoft.com/ | AI analytics that finds where shoppers get stuck | "Where people get stuck and why", AI summaries, free; a scan-and-find story without a fix step. Learn: how "finds what stops shoppers" is worded and shown. |
| R6 | Notion AI | https://www.notion.com/product/ai | Control and trust for AI | A "Custom permissions" card reading "You're in control of what Notion AI can see and do." inside a four-card "Designed for teams." block, plus governance and data copy. Learn: how a trust/control section is built for an AI that acts on your work. |
| R7 | Squarespace | https://www.squarespace.com/ | All-in-one platform | "Everything you need on one platform" with a named list of built-in parts. Learn: how "no apps to stitch together" is shown as a list, not a slogan. |
| R8 | Shopify Sidekick page | https://www.shopify.com/sidekick | Same-category AI assistant (Step 06 competitor Shopify, a different page) | Used mainly as a contrast and for its FAQ on permissions. Mentioned briefly; not a main reference. |

## Analysis by aspect

Format: what the HTML shows, then "Learn" for us. Layout and Motion are added only where they matter, and are `NOT VERIFIED` unless stated.

### R1 · Cursor (https://cursor.com/)

| Aspect | What the HTML shows | What we can learn |
|---|---|---|
| Positioning | H1 "Cursor is your coding agent for building ambitious software." Page title "AI Coding Agent for Building Ambitious Software". The product is shown by mock-UI text inside the page (a task list grouped "In Progress" / "Ready for Review" with tasks such as "Plan Mission Control"; buttons "Build", "View PR"). Whether it is an image, HTML or an animation: `NOT VERIFIED`. | The claim is backed in the first screen by the product doing one named task. We can do the same with one store task (scan result → proposed fix). Must use our real UI or an honest mock; not a fake result. |
| Information order | Headings in order: H1 → "Trusted every day by teams that build world-class software" → "Agents turn ideas into code" → "Works autonomously, runs in parallel" → "In every tool, at every step" → "Hand work to AI teammates" → "The new way to build software." → "Use the best model for every task" → "Build with autonomous agents" → "Develop enduring software" → Changelog → "Try Cursor now." The first CTAs ("Download for macOS", "Get started", "Request a demo") come **before** the proof line; the proof (logo/trust heading) sits right after the hero. | Proof right under the hero CTA; one repeated closing CTA with a short imperative. |
| Trust | Trust heading "Trusted every day by teams..." and, lower, "Trusted by over half of the Fortune 500 ... securely and at scale." (a vendor claim). Control line, **in a customer quote by Andrej Karpathy, not Cursor's own copy**: "The best LLM applications have an autonomy slider: you control how much independence to give the AI." (it continues "or let it rip with the full autonomy agentic version", so it is not a review-gate claim). Named-customer quotes sit in the same block. Footer links Privacy Policy, Data Use, Security. | One sentence that states control in plain words is enough; we need it to be true of our product (open question 3). We cannot borrow a scale claim. |
| Colour | Inline CSS contains warm neutrals (by code: `#edecec` ×8, `#26251e` ×4, `#14120b` ×4, `#f7f7f4` ×2 in 6,791 characters of inline CSS). What is actually rendered: `NOT VERIFIED (not viewed in a browser)`. | Not a conclusion; see Colour direction. |
| Difference | A developer tool: jargon (agents, PR, models, Slack). A store seller would not read it. A one-model-picker or "agents in parallel" frame would make us sound like a dev tool. | Copy the *structure* (claim + task shown + review step), not the vocabulary. |
| Layout / motion | `NOT VERIFIED`. | n/a |

Conversion evidence: **none**. Cursor prints "over half of the Fortune 500" as its own claim.

### R2 · GitHub Copilot (https://github.com/features/copilot)

| Aspect | What the HTML shows | What we can learn |
|---|---|---|
| Positioning | H1 "Command your craft". Meta: "GitHub Copilot works every step of the way, from an open issue to reviewing and merging a pull request." ("Direct agents from issue to merge" and "Enforce quality at merge" are GitHub site-navigation menu text, not headings of this page; corrected at review.) Visible body: "track progress across multiple agents, review changes, and merge completed work". | The *whole chain including the human step* is the story, not just the AI action. "From scan to approved change" is the same shape for us. |
| Information order | H1 → "Companies powered by GitHub" → "Go beyond one-size-fits-all" → "Use your agents, your way" → "Stay in your flow" → "Code, command, and collaborate" → "Manage agent-driven work from one place" (text: "track progress across multiple agents, review changes, and merge completed work") → editor and cloud-agent blocks → one customer-story heading ("...increases developer productivity by 94% with Copilot", the customer's/vendor's claim) → "Tailor-made for your organization" → plan cards "Free / Pro / Pro+ / Max / Business / Enterprise" → blog → "Visit the GitHub Copilot Trust Center" → FAQ with tabs General, Plans & Pricing, Privacy, Responsible AI. Logos sit right after the hero. | Plan cards **on the product page** and an FAQ tab for Privacy and Responsible AI. For us: a Privacy/AI question in the FAQ. |
| Trust | Admin-control text: access, models and policies "managed by your GitHub Administrator"; Copilot code review for users without a licence is "off by default" (an admin billing/cost setting). FAQ tabs "Privacy", "Responsible AI"; a link block "Visit the GitHub Copilot Trust Center". | "Off by default, you switch it on" is a control pattern in words. Do not copy the policy detail; it is enterprise-specific. |
| Colour | `NOT VERIFIED` (only 120 characters of inline CSS; no values to compute). | none |
| Difference | Enterprise and developer framing; six plan tiers. Copying the plan table would be wrong for a Home with a single "Free Launch plan" tick (plan details unknown, brief Q3). | Structure of the approval chain only. |

Conversion evidence: **none**. The "94%" is a customer-story claim on their page; not used.

### R3 · Intelligems (https://www.intelligems.io/)

| Aspect | What the HTML shows | What we can learn |
|---|---|---|
| Positioning | H1 "Decide Confidently. Grow Profitably." Sub: "Test pricing, offers, content, and more, powered by AI that brings your data into every decision." Top banner: "Meet Atlas: AI that helps you ideate, build, and analyze." Block "Discover what to build next: Our AI surfaces high-impact experiment ideas based on your data, so you can prioritize the changes most likely to move the business." and "Describe the experience you want to create, and Intelligems helps build it in the Visual Builder". | Closest in topic to us: AI finds what to change, then builds it. Two sub-points, "Discover" and "Launch", map to scan and fix. Note their H1 is generic; ours names the two tools. |
| Information order | H1 → CTAs "Try For Free" and "Book a Demo" → "4.8 (150+ Shopify reviews) Trusted by thousands" (text, not a heading) → "Improve 100% of the on-site journey" (top / middle / bottom of funnel; list includes "Drive higher AOV with discounts, progress bars, and gifts") → "Turn a lean team into a powerhouse" (Discover / Launch / Understand) → "Power every decision with one platform" (intro "AI powers your analytics, builds tests, and surfaces store recommendations automatically."; cards: "AI RECOMMENDATIONS" with mock rows "3 ready", "Test free shipping at $75 +6.2% 94% confident", "Bundle pricing test +4.1%"; "AUDIENCE TARGETING"; "VISUAL BUILDER") → "No-code for speed. Full-code for control." (three columns; "Version control and rollback for every change" is in the third, "Build anything with full code control", for in-house engineering) → "Describe the change and AI builds it" ("Every AI-generated mod is on-brand, inspectable, editable, and re-promptable in the Visual Builder.") → "Launch fast. Learn even faster" (a Week 1 to Week 4 timeline; "Start optimizing in minutes" is its Week 1 step) → closing "Did it happen if you don't see the bars?" with a "Book A Demo" button. Proof (rating and review count) is right after the hero CTAs. | A product-card block "AI RECOMMENDATIONS" shows a proposed change as a UI card. We can show a "proposed fix" card with an approve control. **Do not show a confidence percentage or an uplift figure** ("94% confident", "+6.2%" in their mock): a fake number in a mock invites a result claim (no numbers rule). |
| Trust | "Trusted by thousands", "(150+ Shopify reviews)"; control through "Full-code for control"; "Version control and rollback for every change" (listed only under the full-code, in-house engineering option, not as a general promise); "Every AI-generated mod is on-brand, inspectable, editable, and re-promptable". No security or privacy section above the footer ("Privacy Policies" link only). The words "approve"/"approval" do not appear. | "Rollback for every change" and "inspectable, editable" are trust lines that fit "you approve every change" (needs product confirmation). In their page rollback is a developer feature; for us it would have to be a seller-facing undo. |
| Colour | By code over 255,528 characters of inline CSS: `#191919` ×10, `#2962ff` ×7, `#1e1e1e` ×7. Rendered result `NOT VERIFIED`. | Evidence only that a saturated blue accent appears in the CSS; not a conclusion. |
| Difference | A testing/analytics tool aimed at CRO operators (pricing tests, audiences, Snowflake). We are a platform; copying its test-and-statistics frame would turn us into a CRO app. | Take the "idea → built → apply" rhythm; skip experiment and confidence vocabulary. |

Conversion evidence: **none**. "Reduce iteration cycles by 60%" (under the freelance/agency column), the "4.8" rating, the mock "+6.2%" / "+4.1%" and "SITEWIDE PROFIT +24%" are the vendor's own figures, unchecked and not used.

### R4 · Shoplift (https://www.shoplift.ai/)

| Aspect | What the HTML shows | What we can learn |
|---|---|---|
| Positioning | H1 "A/B Testing Doesn't Have to be a Pain in the SaaS". Sub: "Unleash your store's profit potential with the first CRO platform purpose-built for Shopify". "Lift Assist" text: "analyzes millions of shopper sessions to recommend what converts and automatically generates features like countdown timers, sticky carts, inventory indicators, and more." Also: "Instantly implement winning tests with one-click 'Apply Variant.'" | "Recommend what converts" then "generate" then "Apply" is the same loop as ours; the click that applies a change is the approval moment. Wording to avoid: "automatically generates" without a human step. |
| Information order | H1 → CTAs "Start 14-day Free Trial" and "Request a Demo" → "Trusted by 2,000+ Shopify Plus Brands" (logos) → testimonials → stat strip ("GMV of merchants", "Sessions analyzed", "Median CVR lift") → feature blocks → "Build your test directly in Shopify" (body: "within the Shopify Theme Customizer") / "or Lift Assist™ will build it for you" → "Personalize" / "Analyze" / "Iterate" → "All The Power None of the BullS#!T" → "Shoplift Success Stories" (case studies with numbers, e.g. "72% Add-to-Cart Growth") → "READY TO UNLOCK NEW REVENUE GROWTH?" | Shows proof **after** the CTA (logos, quotes, numbers). It is a clear example of the proof layout we **cannot** reproduce: our results are unproven. We can reuse the *placement* (a proof strip right under the CTA) with a non-numeric proof such as the product screen. |
| Trust | Logos, testimonials, stat strip, case studies. No security or control section. Words "approve"/"approval": `NOT FOUND` in the copy read. | Nothing on control; learn from the gap. |
| Colour | By code over 4,798 characters of inline CSS: `#4d65ff` ×1, `#c40076` ×1 (too few to say anything). Rendered result `NOT VERIFIED`. | none |
| Difference | Profanity in a heading ("BullS#!T"), stat strips and case-study numbers = a CRO-vendor voice. Copying the numbers would break the no-numbers rule; copying the voice would make us sound like a testing app. | Placement only. |

Conversion evidence: **none**. The "Median CVR lift" stat and case-study percentages are Shoplift's own claims, not read as evidence, and no figure is repeated here.

### R5 · Microsoft Clarity (https://clarity.microsoft.com/)

| Aspect | What the HTML shows | What we can learn |
|---|---|---|
| Positioning | H1 "From clicks to clarity— with AI". Page title: "Microsoft Clarity - Free Heatmaps & Session Recordings". Blocks: "Watch real users on your site" ("uncover where people get stuck and why"), "Visualize what grabs attention", "Summarize key takeaways with AI" ("Get clear and actionable takeaways with one click"; "Reveal where users struggle"), "Chat with your data". | Closest wording to "finds what stops shoppers": "where people get stuck and why". The page stops at insight; the fix step is ours to add. |
| Information order | H1 → six product tabs (Session recordings, Heatmaps, AI summaries, AI chat, AI visibility, Brand agents) with "See live demo" → one H2 per product → "Trusted by millions of customers" → "Customers love Clarity!" → Integrations → mobile apps → "Clarity connected" (MCP server, browser extension) → "Stop guessing. Get Clarity." | A "See live demo" link next to the hero; closing line "Stop guessing. Get Clarity." is short and ours could echo the shape (a problem-then-action pair). |
| Trust | Hero line of three: "Free forever", "2M+ sites and apps globally" (vendor scale claim), "GDPR & CCPA ready"; under the closing CTA: "Free forever. Built to grow with your business. No limits on traffic."; privacy links in the footer. | Free-entry claim in one line; a privacy line is short. We cannot make the legal claim for our product without confirmation. |
| Colour | By code over 97,276 characters of inline CSS: `#ffffff` ×24, `#605e5c` ×21, `#201f1e` ×12, `#6a5ae0` ×12, `#0078d4` ×11. A violet-leaning value and a blue both appear; rendered result `NOT VERIFIED`. | Evidence that blue-violet accents occur in the CSS of an AI analytics page; relevant only as a note for the Step 16 tension. |
| Difference | Analytics-first (recordings, heatmaps); no fix, no approval. Copying the six-tab product gallery would turn Home into a feature menu. | Take the "stuck and why" phrasing idea only; the wording must be ours. |

Conversion evidence: **none**. "Trusted by millions" and "2M+ sites and apps" are vendor claims.

### R6 · Notion AI (https://www.notion.com/product/ai)

| Aspect | What the HTML shows | What we can learn |
|---|---|---|
| Positioning | H1 "Meet your 24/7 AI team". Meta: "One tool that does it all. Search, generate, analyze, and chat—right inside Notion." "Your Notion Agent can build, edit, and take action." | A broad assistant frame: close to Shopify Sidekick. Not our frame. |
| Information order | H1 → "Try for free" / "Request a demo" → "Trusted by teams at" (logos) → "AI that works where your team works. Try for free." with plan cards (Free, Business) **above** the feature list → "Custom Agents automate work that repeats." → "Your Notion Agent can build, edit, and take action." → search / meeting notes → "Designed for teams." (Usage & analytics dashboards, Custom permissions, Model agnostic, Governance tools & controls) → "Trusted by enterprise." (No training on your data; SOC 2 Type 2 & ISO 27001; GDPR & CCPA; Secure encryption; Zero data retention for Enterprise; HIPAA compliant for Enterprise) → "See what Notion AI can do." (use cases) → "Questions & answers". | **Best trust/control pattern found:** inside the four-card "Designed for teams." block, the "Custom permissions" card reads "You're in control of what Notion AI can see and do."; two cards later (after "Model agnostic"), "Governance tools & controls" reads "Get a bird's eye view of AI actions across your workspace, with controls for who can do what."; the next block, "Trusted by enterprise.", carries the data statement. Together: a control statement, a view of what AI did, and a data statement ("Notion AI will not use your data to train our models unless you opt in"). |
| Trust | As above. Certifications are Notion's claims. | Structure: control → visibility of AI actions → data use. We can only fill it with what ShopBase confirms (open question 3). **No certification copy without proof.** |
| Colour | Only 25 characters of inline CSS: no values to compute. `NOT VERIFIED`. | none |
| Difference | Enterprise-compliance heavy (SOC 2, HIPAA, ISO) and team-permission language; our persona is a solo or small-team seller who "keeps the business quiet" (strategy pack, SB-R14). Copying the badge wall would imply compliance we do not have. | Take the control-then-visibility structure; skip the badges. |

Conversion evidence: **none**.

### R7 · Squarespace (https://www.squarespace.com/)

| Aspect | What the HTML shows | What we can learn |
|---|---|---|
| Positioning | H1 "A website makes it real". Meta mentions "AI website builder tools". H2 "Everything you need on one platform"; "Getting started has never been easier with AI". | The "everything on one platform" claim is made by a **named list**, not only a slogan. |
| Information order | H1 → "Get Started" with "Start for free. No credit card required." under it → a scale strip ("14M+ Entrepreneurs Served", "$36B+ Earned by Entrepreneurs", "200+ Countries & Territories"; counter digits in the HTML, so likely animated: `NOT VERIFIED`) → "Grow your business" (offer services, sell products, invoice, ...) → **"Everything you need on one platform"**: Extensions, Squarespace Payments, Squarespace Capital, Analytics, Website Editing, Design Intelligence, Business Email, Domains, Search & AI Optimization → "Getting started has never been easier with AI" (Blueprint AI Builder) → templates → domains → "Trusted by 14 million entrepreneurs worldwide" → "Websites made with Squarespace" → "How to build a website" (six steps) → FAQ → "24/7 Support" → closing "Start your free website trial today" ("No credit card required. Cancel anytime."). Proof: a scale strip right under the hero CTA, and "Trusted by 14 million" again after the built-in list. (Corrected at review: the earlier draft said the scale proof sat only far below the CTA.) | A named list of built-in parts maps to "Store, catalog, payments, fulfillment and support are built in." Each name should be a real ShopBase part (to confirm). Note: their list opens with "Extensions" ("powerful third-party extensions"), so their "one platform" still relies on add-ons; ours must list only parts that are truly built in, or it contradicts "No apps to stitch together". |
| Trust | "Trusted by 14 million entrepreneurs worldwide" and the 14M+ / $36B+ / 200+ strip (vendor claims). "No credit card required" appears 3 times (checked at review): under the hero button ("Start for free. No credit card required."), in step 1 of "How to build a website", and in the closing CTA ("No credit card required. Cancel anytime."); it is **not** in the FAQ, as the draft said. No AI-control block; one FAQ answer on hosting and security (SSL, firewall, DDoS protection). | A "no credit card" line next to every sign-up button is a pattern of free entry; not for ours unless the user confirms it is true (Free Launch plan and its terms unconfirmed). |
| Colour | 0 characters of inline CSS: no values to compute. `NOT VERIFIED`. | none |
| Difference | A general website builder; template-first, "How to build a website" steps. Copying the template gallery would make us look like a general site builder. | Only the built-in list. |

Conversion evidence: **none**. "14 million", "$36B+" and "200+" are vendor claims.

### R8 · Shopify Sidekick page (https://www.shopify.com/sidekick) — brief, contrast only

| Aspect | What the HTML shows | What we can learn |
|---|---|---|
| Positioning | H1 "Starting a business? You've got backup." "Meet Sidekick. Your launch team in one tool." Title: "AI-enabled commerce assistant, Sidekick, ...". Prompt gallery as headings: "/product-description", "/pricing-strategy", "/weekly-summary", "/discount-code", "/shipping-audit" and others, with lines like "Analyze my pricing and find ways to boost sales". | Shows what the category does: a chat assistant that you ask. Ours is a scan that finds issues itself (per the screenshot). This is the main me-too risk. |
| Information order | H1 → "Get Started" → "Meet Sidekick..." (five task cards) → brand testimonials block (heading "Hear from brands who made Sidekick part of their team"; one entry reads "Your story here") → "Popular prompts to get you started" → changelog ("Sidekick keeps getting smarter") → "Sidekick's on standby. Let's go!" → FAQ ("Does using Sidekick cost money?", "How do user permissions work in Sidekick?", "What makes Sidekick different from other AI tools?"). | The FAQ places "how do permissions work" on the page: a seller-control question is answered, but in terms of staff access ("It respects access controls, so team members only interact with data and features they're authorized to use."), not in terms of approving AI changes. |
| Trust | Permissions FAQ above; `approve`/`approval` in a seller-approves sense: `NOT FOUND` in the text read (matches Step 06). | The gap is the opening for "You approve every change". |
| Difference | Copying the slash-prompt gallery or the "assistant on standby" tone would make us read like Shopify. | Avoid. |

Conversion evidence: **none**.

### Colour values found in CSS (computed by code; counts of occurrences in inline `<style>` blocks only)

External stylesheets and rendered colours were **not** read, so this is a weak signal, not what a visitor sees. Computed with a script run as `python3 -I`. **Re-computed at review (fresh download, 2026-10-24):** every hex count below reproduced exactly; the character totals came out 4 to 8 lower per page (6,784 / 255,520 / 4,794 / 97,271; R2, R6, R7, R8 identical), which is parser or markup noise, so read them as approximate.

| Reference | Inline CSS size (characters) | Most frequent hex values (count) |
|---|---|---|
| R3 Intelligems | 255,528 | `#191919` (10), `#2962ff` (7), `#1e1e1e` (7), `#e5e5e8` (4), `#f7f7f9` (3) |
| R5 Clarity | 97,276 | `#ffffff` (24), `#605e5c` (21), `#201f1e` (12), `#6a5ae0` (12), `#0078d4` (11) |
| R1 Cursor | 6,791 | `#edecec` (8), `#26251e` (4), `#14120b` (4), `#f7f7f4` (2) |
| R4 Shoplift | 4,798 | `#4d65ff` (1), `#c40076` (1) |
| R2, R6, R7 | 120 / 25 / 0 | none (nothing to compute) |
| R8 Sidekick | 463 | none |

## Pattern table

**This table is INPUT for Step 12, not a decision.** The section list, order and count are decided at Step 12 (section cap included). The rows are the section types the 2.0 Home will probably need; "best pattern seen" means best among these 8 pages for our USP, with no conversion evidence for any.

| Section type | Best pattern seen | Reference | Why it suits the USP and personas (pain ids: VoC, interim) |
|---|---|---|---|
| Hero | One H1 + one sub that says what the product does + free-entry primary button + a product view straight under it; trust ticks as short lines. Our screenshot already has the H1, sub, two buttons and three ticks; the open part is the product view beside or under it. | R1 Cursor (task shown in the hero), R3 Intelligems (H1 + sub in the hero; its product cards come lower on the page) | Our USP is easier to believe when the AI is shown doing the task (06 positioning implication 2: show the feature, not the outcome words). Addresses the AI-trust theme: sellers' fear is bad output and no human to fix it (AI section); the hero tick "You approve every change" answers it in words. |
| Proof of the product doing the AI task | A mock/real product card that lists a **proposed change** with its reason, next to an approve control; no confidence or uplift figure. | R3 Intelligems "AI RECOMMENDATIONS" card (without its "+6.2%" and "94% confident"); R1 Cursor task list grouped "In Progress" / "Ready for Review"; R4 Shoplift's recommend-then-generate loop (shape only: its "automatically generates" wording is on the do-not-copy list) | Results are `UNPROVEN` and numbers are not allowed (Decisions log 2026-10-24), so the product screen is the only proof available. Tied to A-6 (traffic or ad spend without sales): the card shows what was found; no outcome is claimed. |
| How it works / approval step | Three named steps with a human gate between them, in the shape scan → proposed fix → you approve → live (with undo). | R2 GitHub Copilot ("from an open issue to reviewing and merging", meta description; visible: "review changes, and merge completed work"); R1 Cursor ("Ready for Review" status group); R4 Shoplift ("Apply Variant" as the apply click); R3 Intelligems ("rollback for every change", a full-code feature there; "inspectable, editable") | "You approve every change" is the one line that none of the five Step 06 homepages says (06, me-too test point 2). Showing the step makes it checkable. Answers the AI-section fear "changes made without asking" (nearest case B-5: "published duplicate listings ... without my consent"). Whether undo/rollback exists in ShopBase: unknown (open question 3). |
| Trust and control | A short block: control statement → visibility of what the AI did → data use, in plain words. | R6 Notion AI ("You're in control of what Notion AI can see and do", "Governance tools & controls", "No training on your data"); R1 Cursor autonomy-slider sentence (a customer quote on their page, not Cursor's own claim) | Persona behaviour: keeps the business quiet, fears exposure and spying (strategy pack, SB-R14, SB-R15). Also A-2 and A-3 (holds and bans "without proper explanation", "for no reason"): sellers dislike unaccountable systems, so a "what the AI changed and why" log fits (`ASSUMPTION`; sources are about bans, not AI tools). No certification copy until proof. |
| Integrations / built-in ("no apps to stitch together") | A named list of built-in parts under one heading, each with a one-line description. | R7 Squarespace "Everything you need on one platform" (the form only: their list starts with third-party "Extensions") | Brief tick "No apps to stitch together" and sub "Store, catalog, payments, fulfillment and support are built in." The list makes it concrete, and must contain only parts that are truly built in. Ties to A-1 (costs that stack up: paid apps, add-ons): only partial, because what is included and its cost are unknown (VoC Fit table). Do not claim "fewer apps" or "no extra cost". |
| Pricing entry | Either plan cards on the product page, or just the free-entry line near the CTA. | R2 Copilot and R6 Notion (cards on the page); R5 Clarity ("Free forever" line); R7 Squarespace ("Start for free. No credit card required." under the hero button) | Brief default: no pricing on Home; the plan name only if the user confirms (brief Q3). So the safe pattern is the tick line plus a link to Pricing. Plan cards are an option only after the user supplies plan facts. |
| FAQ | An FAQ with a permissions or "what can the AI change" question and a privacy/AI question. | R8 Sidekick FAQ ("How do user permissions work", "What makes Sidekick different from other AI tools?"), R2 Copilot FAQ tabs (Privacy, Responsible AI) | Lets us state approval and data handling once, in answer form. Addresses the AI-section themes (wrong output, no human, consent). Answers must come from the user; nothing invented. |
| Closing CTA | A short imperative that repeats the **same primary button** as the hero. | R1 Cursor ("Try Cursor now."), R5 Clarity ("Stop guessing. Get Clarity.") | Brief: one primary action, sign up ("Get started for free"). A repeated single action keeps one focal point (N5). Avoid a second route (demo) because the brief closed that. |

Patterns seen but not recommended as a section for us: a six-tab product gallery (R5), a prompt gallery (R8), plan tables with six tiers (R2), stat strips and case studies with numbers (R4, R7), a compliance badge wall (R6).

## Do-not-copy list

Tied to the Step 06 "me too" test (06 positioning, implications 1 to 4). Each item would make us look like a competitor or break a rule.

1. **"AI" alone as the headline idea.** 4 of 5 Step 06 homepages already make an AI claim; R6 Notion ("24/7 AI team"), R8 Sidekick ("commerce-obsessed AI assistant", Shopify's site-menu text on that page) and R7 do too. Keep the two named tools and what each does (06 implication 1).
2. **The chat-assistant frame** (slash-prompt gallery, "your AI team", "on standby", R8 and R6). It is Shopify's frame and is not our scan-then-approve mechanism (06 me-too: Sidekick overlap).
3. **Outcome words without a product view** ("uplift conversions", "raise order value" as a stand-alone line). Wix already says this (06 implication 2). Show the feature.
4. **Any number: uplift, "Median CVR lift", case-study percentages, "94% confident" or "+6.2%" in a mock card, scale numbers ("14 million", "$36B+", "2M+ sites", "Fortune 500", "2,000+ brands").** Step 06 implication 4 and the Decisions log forbid numbers until proof exists; R1, R3, R4, R5 and R7 print some of these as their own claims.
5. **"You don't lift a finger" / fully automatic tone** ("automatically generates", "autopilot"). It is the opposite of "You approve every change" (06 me-too point 2).
6. **Compliance and enterprise badges** (SOC 2, ISO, HIPAA, R6). Not ours to claim; the persona is a solo seller, not an enterprise buyer.
7. **A second CTA route like "Request a demo"** next to the sign-up button (R1, R4, R6; R3 "Book a Demo", also its closing button). The brief closed this: sign up only.
8. **Superlatives and "all-in-one" as a slogan** ("world's best", "one AI-powered platform"; 06 category patterns). Use a named list of built-in parts instead (R7 pattern).
9. **Vendor-voice jargon** (agents, PRs, experiments, statistical significance; R1, R3, R4) and the profanity in a heading (R4).
10. **Giant scale numbers as the first proof** (06 category patterns: 4 of 5 pages do it). Use the product screen first.

## Colour direction

Aim for a calm, mostly light and neutral page with one saturated blue family used only for actions and for the approval moment, so the "approve" control is the one thing that stands out (the AI references in this set that show a human review step keep the rest of the interface neutral; `NOT VERIFIED` visually, only CSS counts and headings were read). Keep the feel plain and checkable rather than flashy, because the audience distrusts systems that act without explanation (VoC A-2 and A-3, interim). Avoid a gradient or glow treatment that signals "magic AI", since the Step 06 finding is that the page must be trusted on description, not on spectacle.

**Open question for Step 16 (not a decision):** the logo blue, the colour-scale "Primary 500" blue (both measured in `03-research/02-intake.md`; no values repeated here, per the no-hex rule of this step) and the violet-leaning blues in the hero screenshot (`02-assets/images/hero-2.0-reference.png`, a blue-to-violet gradient on the second headline line and a saturated blue button) do not form one family. Which one is the brand accent for 2.0, and does the screenshot's violet stay? Reference CSS shows both blue and violet values on AI pages (R3 and R5), so they do not settle it. Step 16 measures contrast and decides.

## Open questions

### 🔴 Must answer
None blocking Gate 2.

### 🟡 Should answer
1. **Which reference sites do you like (or dislike), from any industry?** *Default: the 8 above are used; if you name others they are fetched and added, and re-running this step marks Step 09 onward `stale` only if the pattern table changes.*
2. **Does the Home view of CR Scan AI have a real UI screenshot of a proposed fix and its approve control?** *Default: the proof section uses a labelled mock with no numbers, built at Step 18 from the user's screenshot; no real store domains (strategy pack Q12).*
3. **Is the approval flow as described, and does undo/rollback exist? What does ShopBase say about how AI uses store data?** *Default: only "You approve every change" (from the screenshot) is stated; no undo, no rollback, no data or privacy claim until the user confirms. This also blocks the trust and FAQ answers.*
4. **Which parts are actually built in (store, catalog, payments, fulfillment, support, others)?** *Default: only the five named in the screenshot sub-line.*
5. **Is "Free Launch plan" a confirmed public claim, and may Home show pricing?** *Default: the tick line only if confirmed; no pricing on Home.* (brief Q3)

### ⚪ Nice to have
6. Is a blue-to-violet gradient on the headline an intended part of the 2.0 look, or just the draft's styling? *Default: treated as a draft; decided at Step 16.*
7. Paste Reddit or Facebook-group material to replace the interim VoC. *Default: the interim VoC stays; ids are directional only.*

## Assumptions

1. The 8 references are a judgement set chosen by Claude after two weak searches; no claim that they are the best pages in their families. `ASSUMPTION`
2. Order of headings in the HTML source equals the visual order of sections. `ASSUMPTION` (not viewed in a browser)
3. A product view, a review step and a control block (patterns from R1, R2, R3, R6) help a seller trust an AI that edits a store. `ASSUMPTION`; the VoC shows what AI users complain about (wrong output, no human, no consent), not what they respond to on a landing page.
4. The VoC pain ids are interim: complaint-heavy, not byte-verified, not shown to be Vietnam-based sellers.
5. The hero screenshot text and ticks are the user's wording (Decisions log) and not proof of results.
6. Hex values in the colour table are counts in inline CSS only, not rendered colours.
7. No reference has conversion evidence; vendor-printed numbers are not used.

## Check-list

- [x] Every reference has a link and a stated reason (table above).
- [x] No reference is called "high converting"; each says "no conversion evidence".
- [x] The do-not-copy list exists and ties back to Step 06 (06 implications 1 to 4, me-too test).
- [x] Every pattern ties to the USP or a persona pain point (VoC ids, interim).
- [x] Colour values were computed by code (counts in inline CSS; stated as such). Re-computed at review: hex counts identical.
- [x] Quotes, headings, CTA labels and section order re-checked as exact strings against a fresh download at review (8 of 8 HTTP 200); mismatches corrected (see Status).
- [x] Colour direction has no hex values (the brand blues are referred to `02-intake.md`).
- [ ] Anything about visuals, colour, motion or imagery verified in a browser: **NOT DONE (not viewed in a browser)**.
- [ ] The user supplied or confirmed reference sites: **NOT DONE (open question 1)**.
