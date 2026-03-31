# Design System: High-End Editorial Specification

## 1. Overview & Creative North Star: "The Heritage Curator"

This design system rejects the "standard e-commerce template" in favor of a **High-End Editorial** experience. Our Creative North Star is **"The Heritage Curator."** Imagine a premium gallery exhibition where ancient medicinal wisdom meets avant-garde minimalism.

We move beyond the grid by embracing **intentional asymmetry**. Product imagery should often bleed off the edge of the container, or overlap across two different surface tiers. We use high-contrast typography scales—pairing oversized, elegant serifs with microscopic, wide-tracked labels—to create a sense of rhythmic authority. This is not just a shop; it is a digital sanctuary for Korean Red Ginseng.

---

## 2. Color & Tonal Depth

Our palette is rooted in the earth (Ginseng) and the sun (Gold), but its execution must feel airy and atmospheric.

* **The "No-Line" Rule:** We do not use 1px solid borders to define sections. Traditional boxes feel restrictive. Instead, define space through background shifts. A section using `surface-container-low` (#f6f3ee) sitting atop a `background` (#fcf9f4) creates a sophisticated, "invisible" boundary.
* **Surface Hierarchy & Nesting:** Treat the UI as stacked sheets of fine handmade paper.
* **Level 0 (Base):** `surface` (#fcf9f4)
* **Level 1 (Sections):** `surface-container-low` (#f6f3ee)
* **Level 2 (Feature Cards):** `surface-container-lowest` (#ffffff)
* **The "Glass & Gradient" Rule:** For floating navigation or product callouts, use `surface-bright` at 80% opacity with a `24px` backdrop-blur.
* **Signature Textures:** For high-impact CTAs, use a subtle linear gradient from `primary` (#60000c) to `primary_container` (#8a0015). This prevents the "flat red" look and adds a velvet-like depth to the brand's signature color.

---

## 3. Typography: The Editorial Voice

The tension between the serif and sans-serif is the heartbeat of this system.

* **The Heroic Serif (Noto Serif):** Used for `display` and `headline` tiers. It conveys the "Traditional" aspect of the fusion. It should feel expensive. Use `headline-lg` for storytelling and `display-lg` for high-impact hero statements.
* **The Functional Modernist (Manrope):** Used for `title`, `body`, and `label` tiers. It provides the "Modern" counterpoint. Manrope’s geometric clarity ensures technical data about ginseng density remains legible.
* **Hierarchy Tip:** Pair a `display-md` headline with a `label-md` (uppercase with 0.1rem letter spacing) immediately above it to act as a "eyebrow" category marker.

---

## 4. Elevation & Depth: Tonal Layering

We do not "drop shadows"; we "lift surfaces" using light and color.

* **The Layering Principle:** Use the Spacing Scale `3` (1rem) or `4` (1.4rem) to inset `surface-container-lowest` elements inside `surface-container-high` areas. This "recessed" look mimics luxury packaging.
* **Ambient Shadows:** If a product bottle must float, use a shadow with `blur: 60px`, `y-offset: 20px`, and an opacity of 4% using the `on-surface` (#1c1c19) color. It should feel like an ambient glow, not a hard shadow.
* **The "Ghost Border" Fallback:** If a container requires a boundary (e.g., an input field), use `outline-variant` (#e3beb8) at **15% opacity**. It should be barely perceptible—felt rather than seen.

---

## 5. Components & Primitive Styling

### Buttons

* **Primary:** `primary` background, `on-primary` text. No border. Roundedness: `sm` (0.125rem) for a sharp, architectural feel.
* **Secondary:** `surface` background with a `secondary` (#735c00) text. Use the "Ghost Border" rule here.
* **Tertiary:** No background. `primary` text with an underline that only appears on hover.

### Cards & Product Grids

* **Constraint:** Absolutely no divider lines.
* **Roundedness:** Use `rounded-[2rem]` to `rounded-[3rem]` radius system for all containers and images. No sharp corners anywhere. This applies globally — cards, image containers, feature blocks, and product grids all follow this cinematic roundedness.
* **Execution:** Use `spacing-8` (2.75rem) between cards. Product photography should have the background removed and be placed on `surface-container-low`. The shadow should be cast *onto* the card, not the card onto the page.

### Chips (Herbal Properties)

* **Style:** `surface-container-highest` background with `on-surface-variant` text. Roundedness: `full` (9999px). Use these to label "6-Year Grown" or "Immunity."

### Input Fields

* **Style:** Minimalist. No background. A single `outline-variant` (20% opacity) bottom-border only. On focus, the border transitions to `secondary` (Gold).

### Signature Component: "The Heritage Scroll"

An asymmetric horizontal carousel where images use different aspect ratios (e.g., 4:5 and 1:1) and overlap slightly, utilizing `spacing-negative` to create a collage-like, curated feel.

---

## 6. Do’s and Don’ts

### Do:

* **Do** use extreme whitespace. If you think there is enough space, add 20% more from the Spacing Scale.
* **Do** use `secondary` (Gold) sparingly as an accent—for icons, small labels, or focus states—never for large backgrounds.
* **Do** allow product imagery to overlap from a `surface` section into a `surface-container` section to break the horizontal "stripe" layout.

### Don’t:

* **Don't** use 100% black. Use `on-surface` (#1c1c19) for all text to maintain the "warm" natural feel.
* **Don't** use sharp corners on containers or images. Use `rounded-[2rem]` to `rounded-[3rem]` consistently for a cinematic, premium feel.
* **Don't** use "Standard" icons. Use ultra-thin (1pt or 1.5pt) custom iconography that matches the stroke weight of the Manrope typeface.
