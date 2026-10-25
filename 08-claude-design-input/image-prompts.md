# 20 · Image prompts — ShopBase 2.0 Home (P01·A and P01·B)

Six image slots, one prompt each. Paste a prompt into an image generator, **or** give the same text to your own designer as a brief. Slot codes `IMG##` are permanent; the table that fixes sizes and places is section 8 of `master-spec.md`.

Hex colours are allowed in this file (the palette and the style line); they are the locked palette values from `master-spec.md` section 2.

## Read this first (plain words)

- **An image generator will not produce an accurate ShopBase interface.** It does not know your product. It can only draw a *generic, simple picture in the right style*. That is why the page labels every one of these pictures **"Illustration"** and never presents it as real product screens. If you want pictures that match the real product, ask your designer to **draw them by hand in the same style** (this file is then their brief: same hex colours, same ratio, no text, no numbers).
- **What the page already draws for you.** The soft blue field behind the picture, the white card, its rounded corners and shadow, and the small "Illustration" label are drawn by the page from the locked palette. **Do not draw them.** Each image is only what sits *inside* the white card, on a pure white background that blends into the card.
- **No text in any image.** The page puts all words next to the picture. No letters, no numbers, no percentages, no prices, no store names, no fake product data, no faces, no logos, no watermark. No Calendly or any competitor's artwork, layout or style.
- **If the generator adds text, a border, a shadow, a background colour or a device frame: reject it** and ask again.

## Shared for every slot

- Format: **PNG, 1200 × 400 px, ratio 3:1**, sRGB, opaque pure white background (hex `#FFFFFF`), no transparency, no border, no rounded outer corners, no shadow around the picture.
- Compose inside the picture with **a margin of at least 4% on every side** (the page crops nothing except the hero, see IMG01).
- Locked palette (light only): bars `#DDE3EE` · light panel `#F4F7FC` · highlight panel `#E7F3FD` · thin outline `#7F8A9E` · title-dark for the smallest markers `#1E222B` · the one blue accent `#4371CD` (only where a prompt says so).
- Shared style line (repeated verbatim in every prompt below, so the six pictures look like one set):

> **STYLE LINE:** Flat, simple, clean UI-style illustration on a pure white background (#FFFFFF), light and soft with generous empty space: rounded white panels with neutral abstract bars (#DDE3EE), cool grey blocks (#F4F7FC), one pale-blue rounded panel (#E7F3FD), thin cool-grey outlines only where needed (#7F8A9E), soft rounded corners, no shadows, no gradients, no glow, no sparkle, no text, no letters, no numbers, no faces, no logos, no watermark.

- Shared exclusions (add to every prompt as "avoid"): any readable or fake text, digits, percentages, prices, scores, charts with values, real store names or domains, people or faces, logos, watermarks, window chrome (traffic-light dots), device frames, photographs, 3D, gradients, drop shadows, neon, magic wands, sparkles, robots, brain or chat-bubble icons, and anything that copies Calendly's or another company's artwork or style.
- After saving, the build crops with `object-fit` only where stated and never stretches or redraws.

---

### IMG01 · scan-card

- **File:** `02-assets/images/IMG01-scan-card.png`
- **Used in:** S05 (shown in full) and S03 (hero: the **top ~73% only**, a smaller crop). So the most important rows must sit in the upper part.
- **Ratio · size:** 3:1 · 1200 × 400 px.
- **What it is (generic illustration):** a scan result card: what a scan *found* on a store, as a short list.

**Prompt to paste:**

> Flat UI-style illustration of a scan result list, wide 3:1 landscape, 1200 × 400 px. Four short rows stacked top to bottom with even spacing. Each row: a small round outline marker on the left, one longer abstract bar (the finding) and, under it, one shorter lighter bar (the reason). The second row sits on a soft pale-blue rounded panel (#E7F3FD) to show it is highlighted. The four rows fill the upper two thirds; leave calm empty white space below and on the right. No text, no numbers, no scores, no percentages, no store name. STYLE LINE: Flat, simple, clean UI-style illustration on a pure white background (#FFFFFF), light and soft with generous empty space: rounded white panels with neutral abstract bars (#DDE3EE), cool grey blocks (#F4F7FC), one pale-blue rounded panel (#E7F3FD), thin cool-grey outlines only where needed (#7F8A9E), soft rounded corners, no shadows, no gradients, no glow, no sparkle, no text, no letters, no numbers, no faces, no logos, no watermark. Avoid: readable or fake text, digits, percentages, prices, charts with values, real store names, people or faces, logos, watermarks, window chrome, device frames, photographs, 3D, gradients, drop shadows, neon, wands, sparkles, robots, and any copy of another company's artwork or style.

---

### IMG02 · proposed-fix-card

- **File:** `02-assets/images/IMG02-proposed-fix-card.png`
- **Used in:** S06 (A).
- **Ratio · size:** 3:1 · 1200 × 400 px.
- **What it is:** one proposed fix on one card (not applied, not approved). Do not show what changes inside a store.

**Prompt to paste:**

> Flat UI-style illustration of one proposed fix, wide 3:1 landscape, 1200 × 400 px. One large soft pale-blue rounded panel (#E7F3FD) centred and filling most of the width, containing: a small round outline marker at the left, a long abstract title bar, a shorter lighter reason bar beneath it, and one "change" row made of two small stacked bars side by side. Under the panel, two neutral abstract bars (one long, one medium) on white. No buttons. No text, no numbers, no percentages, no before-and-after values, no store content. STYLE LINE: Flat, simple, clean UI-style illustration on a pure white background (#FFFFFF), light and soft with generous empty space: rounded white panels with neutral abstract bars (#DDE3EE), cool grey blocks (#F4F7FC), one pale-blue rounded panel (#E7F3FD), thin cool-grey outlines only where needed (#7F8A9E), soft rounded corners, no shadows, no gradients, no glow, no sparkle, no text, no letters, no numbers, no faces, no logos, no watermark. Avoid: readable or fake text, digits, percentages, prices, charts with values, real store names, people or faces, logos, watermarks, window chrome, device frames, photographs, 3D, gradients, drop shadows, neon, wands, sparkles, robots, and any copy of another company's artwork or style.

---

### IMG03 · approval-card

- **File:** `02-assets/images/IMG03-approval-card.png`
- **Used in:** S07 (both variants).
- **Ratio · size:** 3:1 · 1200 × 400 px.
- **What it is:** a proposed change and **one** approve control. The approve control is the **only blue element** on the page's middle sections.

**Prompt to paste:**

> Flat UI-style illustration of a proposal waiting for a decision, wide 3:1 landscape, 1200 × 400 px. Upper part: one soft pale-blue rounded panel (#E7F3FD) with two abstract bars (one long, one medium). Lower part: exactly one wide rounded button shape filled with solid blue (#4371CD) holding a single simple white check-mark icon and nothing else, no label. It is the only saturated element; everything else is neutral. Calm empty white space around. No text, no numbers, no second button, no undo, no toggle. STYLE LINE: Flat, simple, clean UI-style illustration on a pure white background (#FFFFFF), light and soft with generous empty space: rounded white panels with neutral abstract bars (#DDE3EE), cool grey blocks (#F4F7FC), one pale-blue rounded panel (#E7F3FD), thin cool-grey outlines only where needed (#7F8A9E), soft rounded corners, no shadows, no gradients, no glow, no sparkle, no text, no letters, no numbers, no faces, no logos, no watermark. Avoid: readable or fake text, digits, percentages, prices, charts with values, real store names, people or faces, logos, watermarks, window chrome, device frames, photographs, 3D, gradients, drop shadows, neon, wands, sparkles, robots, and any copy of another company's artwork or style.

---

### IMG04 · offer-card

- **File:** `02-assets/images/IMG04-offer-card.png`
- **Used in:** S08 (both variants).
- **Ratio · size:** 3:1 · 1200 × 400 px.
- **What it is:** one generic offer on one card. **No specific offer type:** no discount badge, no percentage, no price, no bundle or upsell symbol. Nobody has said yet what AOV AI recommends.

**Prompt to paste:**

> Flat UI-style illustration of one generic offer card, wide 3:1 landscape, 1200 × 400 px. One soft pale-blue rounded panel (#E7F3FD) holding a small plain rounded-square tile on the left (a neutral placeholder, no product picture, no icon inside) and, to its right, two abstract bars (one long, one short). Below the panel, one empty pill-shaped outline chip (#7F8A9E thin line) and one short neutral bar. No price tag, no percent sign, no badge, no discount, no bundle, no text, no numbers. STYLE LINE: Flat, simple, clean UI-style illustration on a pure white background (#FFFFFF), light and soft with generous empty space: rounded white panels with neutral abstract bars (#DDE3EE), cool grey blocks (#F4F7FC), one pale-blue rounded panel (#E7F3FD), thin cool-grey outlines only where needed (#7F8A9E), soft rounded corners, no shadows, no gradients, no glow, no sparkle, no text, no letters, no numbers, no faces, no logos, no watermark. Avoid: readable or fake text, digits, percentages, prices, charts with values, real store names, people or faces, logos, watermarks, window chrome, device frames, photographs, 3D, gradients, drop shadows, neon, wands, sparkles, robots, and any copy of another company's artwork or style.

---

### IMG05 · store-with-scan-card

- **File:** `02-assets/images/IMG05-store-with-scan-card.png`
- **Used in:** S10 (hero, B).
- **Ratio · size:** 3:1 · 1200 × 400 px.
- **What it is:** one store page with a scan card on top of it.

**Prompt to paste:**

> Flat UI-style illustration of a simplified online store page with a small scan card laid over it, wide 3:1 landscape, 1200 × 400 px. The store, drawn straight on: a thin top bar, a wide neutral banner block (#F4F7FC), and a row of three plain rounded-square product tiles (no pictures, no icons). On the lower right, a smaller white rounded card overlapping the store, containing one soft pale-blue panel (#E7F3FD) with two abstract bars. Thin cool-grey outlines (#7F8A9E) only on the store's outer shape. No text, no numbers, no store name, no logos, no prices. STYLE LINE: Flat, simple, clean UI-style illustration on a pure white background (#FFFFFF), light and soft with generous empty space: rounded white panels with neutral abstract bars (#DDE3EE), cool grey blocks (#F4F7FC), one pale-blue rounded panel (#E7F3FD), thin cool-grey outlines only where needed (#7F8A9E), soft rounded corners, no shadows, no gradients, no glow, no sparkle, no text, no letters, no numbers, no faces, no logos, no watermark. Avoid: readable or fake text, digits, percentages, prices, charts with values, real store names, people or faces, logos, watermarks, window chrome, device frames, photographs, 3D, gradients, drop shadows, neon, wands, sparkles, robots, and any copy of another company's artwork or style.

---

### IMG06 · finding-and-fix-on-store

- **File:** `02-assets/images/IMG06-finding-and-fix-on-store.png`
- **Used in:** S12 (B).
- **Ratio · size:** 3:1 · 1200 × 400 px.
- **What it is:** a finding and its proposed fix shown on a store, in one picture.

**Prompt to paste:**

> Flat UI-style illustration of a finding and its proposed fix on a store, wide 3:1 landscape, 1200 × 400 px. Left half: a simplified store block (a neutral banner block #F4F7FC above two plain rounded-square tiles) with one element marked by a thin cool-grey outline (#7F8A9E) to show what was found. Right half: a smaller soft pale-blue rounded panel (#E7F3FD) holding three abstract bars of decreasing length, to show the proposed fix, placed beside the marked element. No arrows, no buttons, no text, no numbers, no store name, no logos. STYLE LINE: Flat, simple, clean UI-style illustration on a pure white background (#FFFFFF), light and soft with generous empty space: rounded white panels with neutral abstract bars (#DDE3EE), cool grey blocks (#F4F7FC), one pale-blue rounded panel (#E7F3FD), thin cool-grey outlines only where needed (#7F8A9E), soft rounded corners, no shadows, no gradients, no glow, no sparkle, no text, no letters, no numbers, no faces, no logos, no watermark. Avoid: readable or fake text, digits, percentages, prices, charts with values, real store names, people or faces, logos, watermarks, window chrome, device frames, photographs, 3D, gradients, drop shadows, neon, wands, sparkles, robots, and any copy of another company's artwork or style.

---

## What you do now, then I stop

1. **Generate** each picture from its prompt (or ask your designer to draw it in this style).
2. **Save** each file with exactly the name above in `02-assets/images/` (for example `02-assets/images/IMG01-scan-card.png`).
3. Tell me **"images done"** (I will check the files exist and have the right size), or **"skip images"** (the six slots stay the labelled "Illustration" placeholders from the approved proof, and the page still builds).

This step stops here. After your answer I close Step 20 and **Gate 7** follows (you approve the tokens and the master spec and say `approved`).
