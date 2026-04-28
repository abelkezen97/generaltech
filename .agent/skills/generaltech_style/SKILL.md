---
name: generaltech_style
description: Design system and interaction patterns for the GeneralTech.ae "Silent Luxury" and "Precision Engineering" aesthetic.
---

# GeneralTech Style Guide & Precision Design System

This document codifies the "Silent Luxury" and "Precision Engineering" aesthetic developed for the GeneralTech.ae project. Use these instructions to maintain visual and interactive consistency across all sub-pages (Services, Products, Rental, etc.).

## 1. Visual Identity & Aesthetic
- **Brand Core:** "Precision Monolith" — High contrast, sharp geometry, and a sense of architectural weight.
- **Palette:** 
  - **Primary:** White (`#FFFFFF`) and Deep Gray/Black (`#0A0A0A`).
  - **Accent:** Signature Brand Red (`#FF0000`) used sparingly for emphasis and "technical heat."
  - **Neutrals:** Subtle grays (`#FAFAFA` for backgrounds, `#F3F4F6` for borders) to maintain an airy, premium feel.
- **Micro-Styling:** Use HSL-curated shadows and subtle gradients (vignettes) on interactive cards.

## 2. Typography Standards
- **Headlines:** Use `font-black`, `tracking-tight`, and a tight `leading-[0.95]`.
- **The "Highlight" Pattern:** Almost every major headline should feature one italicized word in the signature red.
  - *Example:* `The <span className="text-[#FF0000] italic font-medium">precision</span> standard.`
- **Body Text:** Use `font-light` or `font-normal` with increased `leading-relaxed` for an editorial, spacious feel.
- **Taglines:** Small uppercase text with wide tracking (`tracking-[0.2em]`) preceded by a `w-8 h-[2px] bg-[#FF0000]` horizontal line.

## 3. Layout & Section Architecture
- **Space is Luxury:** Never crowd the layout. Use generous vertical padding:
  - **Section Padding:** Default `py-24 lg:py-32`. 
  - **Header Padding:** Section headers should start at `pt-30` (`120px`) to clear navigation bars comfortably.
- **Content Alignment:** Always align content to the `max-w-7xl mx-auto px-12` vertical grid line. Horizontal elements (like galleries) should start at this line but are permitted to scroll out to the viewport edges.

## 4. Interactive Patterns
- **Cinematic Pacing:** Interactions should feel deliberate, not frantic.
- **The "Sticky Gallery" Pattern:** 
  - Section height should be approximately `350vh`.
  - Use `framer-motion` to convert vertical scroll into horizontal translation.
  - Translate to exactly `-62%` or a value that locks the final card to the right viewport edge.
- **Glassmorphism:** Use `backdrop-blur-md` and `bg-white/5` for overlays on dark backgrounds to imply technical precision and depth.
- **Hover Effects:** Interactive elements (cards/buttons) should "light up" using red ambient glows or white-to-red transitions.

## 5. Coding Principles
- **React + Framer Motion:** Use these for all non-static storytelling sections.
- **Tailwind v4:** Adhere to the `@theme` and `@apply` patterns established in `global.css`.
- **Component Reusability:** Ensure typography classes are abstracted or mirrored exactly (e.g., `text-5xl lg:text-[72px]`) to prevent visual drift.

## 6. Iconography
- **Technical Set:** Use `lucide-react` with thin weights (`strokeWidth={1.25}` or `1.5`) for a precise, "blueprint" aesthetic.
- **Icon Framing:** House icons in rounded-square containers with subtle borders or frosted glass effects.
