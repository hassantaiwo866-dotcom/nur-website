# Nūr Website — Design System

**Status:** Approved design direction; implementation specification  
**Version:** 1.0  
**Date:** 25 November 2026  
**Repository:** `hassantaiwo866-dotcom/nur-website`  
**Branch:** `feature/website-design-system`

---

## 1. Purpose

This document defines the visual and interaction standards for the Nūr public website. It translates the approved website vision into practical rules for implementation.

The website must communicate that Nūr is a system for self-control, attention, recovery and personal growth—not merely a website blocker.

The design must preserve Nūr's product principles: privacy-first, no shame, no guilt, honest claims and user-controlled growth.

## 2. Approved creative direction

The approved direction combines:

- Elegant serif display headings with a clean sans-serif body typeface.
- A dark forest-green visual foundation with a light theme that follows the visitor's system preference.
- Concentric light as Nūr's signature visual motif.
- Soft emerald illumination as ambient atmosphere.
- A subtle horizon / new-beginning motif for recovery and forward movement.
- Restrained liquid-glass treatment in the hero, interactive demonstrations and feature cards.
- Clean, solid surfaces for long-form content, privacy, legal and support pages.

The design should feel calm, premium, human, focused and technologically capable. It must not resemble a gaming interface, nightclub aesthetic, clinical dashboard or generic SaaS template.

## 3. Brand and content

### Primary tagline

**Build the person you want to become.**

### Supporting message

Protect your attention. Strengthen self-control. Recover, rebuild and grow.

### Voice

- Warm, direct and non-judgmental.
- Clear rather than grandiose.
- Encouraging without pressure.
- Honest about limitations and current product maturity.

Avoid shame, fear, labels such as “addict”, guilt-based streak messaging, guaranteed outcomes, cure claims and unsupported medical claims.

## 4. Colour tokens

### Dark theme

| Token | Value | Intended use |
|---|---|---|
| `--color-bg` | `#03140F` | Main page background |
| `--color-surface` | `#0D3023` | Cards and panels |
| `--color-surface-elevated` | `#123B2B` | Elevated surfaces |
| `--color-accent` | `#65D9A0` | Primary actions and highlights |
| `--color-accent-hover` | `#80E5B2` | Hover / active accent |
| `--color-text` | `#F1F7F3` | Primary text |
| `--color-text-muted` | `#9AAFA6` | Secondary text |
| `--color-border` | `#244638` | Borders and dividers |
| `--color-error` | `#E28B8B` | Error states only |

### Light theme

The light theme must be designed as a deliberate counterpart, not a mechanical inversion. Use warm off-white or pale neutral backgrounds, white or near-white surfaces, deep forest-green text, muted green-grey secondary text and accessible green actions.

Exact light-theme values must be validated for contrast before implementation is considered complete.

### Colour rules

- Accent green is for actions, focus indicators and meaningful highlights—not every decorative element.
- Do not use glow as a substitute for contrast.
- Error and warning colours must remain semantically meaningful.
- Text contrast must meet WCAG 2.2 AA where applicable.

## 5. Typography

### Typeface roles

- Display and section headings: an elegant serif. DM Serif Display is a candidate, subject to licensing, performance and rendering review.
- Body, navigation, labels and controls: a clean sans-serif. Inter is a candidate, subject to licensing and performance review.

Use locally hosted, optimised font files where licensing permits. Provide robust system fallbacks. Avoid blocking first render on remote font services.

### Type scale

Initial responsive targets:

| Role | Desktop target | Mobile target |
|---|---:|---:|
| Hero heading | 42–64 px | 36–44 px |
| Section heading | 32–44 px | 28–36 px |
| Card heading | 20–26 px | 20–24 px |
| Body | 16–19 px | 16–18 px |
| Small label | 12–14 px | 12–14 px |

These are starting values. Actual sizes, line lengths and line heights must be checked on real devices.

## 6. Signature visual language

### Concentric light

Concentric rings represent focus, clarity and direction. Use thin, translucent strokes and restrained opacity. They should not look like a radar screen, target reticle or neon interface.

### Soft illumination

Use subtle radial gradients to create a sense of depth. Keep the light source behind content, never behind text in a way that harms readability.

### New beginnings / horizon

A quiet horizon or emerging light may support storytelling about recovery and forward movement. It is a supporting motif, not a literal sunrise illustration on every page.

### Curved arc

A curved luminous arc may sit above or around the Nūr wordmark or focal light. It should be original to Nūr and must not imitate another brand's logo or proprietary artwork.

### Asset strategy

Prefer lightweight CSS gradients and SVG for simple abstract effects. Use optimised raster artwork only when it materially improves the experience. Avoid autoplay video and large hero media.

## 7. Liquid-glass usage

Glass treatment is approved for:

1. The homepage hero where it improves depth and hierarchy.
2. Interactive demonstrations such as Hold and Reset.
3. Feature cards and selected interactive panels.

It is not a universal surface treatment.

### Glass rules

- Use translucent surfaces with subtle borders.
- Keep blur restrained and avoid expensive full-screen backdrop effects.
- Provide a solid fallback background for browsers and devices without backdrop-filter support.
- Preserve readable contrast in both themes.
- Do not place long-form text on busy or highly transparent surfaces.
- Avoid stacking multiple blurred layers.
- Do not make glass effects necessary for understanding or using the page.

## 8. Layout and spacing

- Mobile-first, responsive layouts.
- Clear content hierarchy and generous whitespace.
- Constrain long-form text to comfortable reading widths.
- Use a consistent spacing scale based on 4 px increments.
- Avoid horizontal overflow at narrow widths.
- Navigation must collapse into an accessible mobile menu.
- Hero content must remain readable when the decorative background is unavailable.

## 9. Homepage opening screen

### Purpose

Explain Nūr quickly, establish trust and provide a clear next action.

### Composition

- Minimal navigation with Nūr wordmark.
- Small descriptor: “SELF-CONTROL · RECOVERY · GROWTH”.
- Main heading: “Build the person you want to become.”
- Supporting sentence: “Protect your attention. Strengthen self-control. Recover, rebuild and grow.”
- Primary action: “Join the closed alpha”, only when the registration destination is operational.
- Secondary action: “Discover how Nūr works”, linking to the explanation below.
- Ambient concentric light and soft illumination behind the content.
- Subtle horizon / new-beginning motif where it supports the composition.

### Desktop

Use a balanced centred composition with a generous maximum text width. The ambient artwork occupies the hero background rather than competing with the headline.

### Mobile

Use a centred, vertically stacked composition. Keep the headline, supporting sentence and primary action visible without requiring the visitor to understand a decorative animation. Avoid excessive hero height.

### Website-specific rule

The website hero is persistent landing-page content. It is not a timed splash screen and must never force visitors to wait before browsing.

## 10. Interaction and motion

- Motion is slow, purposeful and optional.
- Respect `prefers-reduced-motion`.
- Do not use flashing, rapid pulsing or distracting particles.
- Core content and navigation must work without animation.
- Avoid forced scroll effects and scroll-jacking.
- Interactive controls require visible focus states and keyboard operation.
- Loading indicators appear only for real operations; never simulate a wait for decoration.

## 11. Components

### Header

- Nūr wordmark.
- Links to the most important pages.
- Clear alpha action only when functional.
- Accessible mobile navigation with keyboard and screen-reader support.

### Buttons

- Clear primary / secondary hierarchy.
- Adequate target size.
- Visible hover, focus, active and disabled states.
- Text labels must describe the action.

### Cards

- Consistent radius, spacing and border treatment.
- Glass only where it adds value.
- Avoid excessive nested cards.

### Forms

- Explicit labels and useful validation.
- Accessible error messages.
- Never rely on placeholder text as the only label.
- Do not collect information that is not needed.

### FAQ

- Keyboard-accessible disclosure controls.
- Correct expanded/collapsed semantics.
- No content hidden from assistive technology.

## 12. Accessibility and performance

- Target WCAG 2.2 AA.
- Semantic HTML and logical heading hierarchy.
- Keyboard accessibility and visible focus.
- Text contrast checked in both themes.
- Reduced-motion support.
- Responsive behaviour tested at narrow mobile widths.
- Avoid layout shifts and unnecessary client-side JavaScript.
- Prefer static rendering for public content.
- Optimise fonts, images and SVG.
- Avoid heavy animation libraries for simple effects.
- Test on mid-range Android hardware and slower network conditions.

The initial critical first-load budget of less than 150 KB remains a project target to measure and refine, not a verified result.

## 13. Theme behaviour

The default theme follows `prefers-color-scheme`.

If a manual theme selector is later introduced:
- It must be accessible.
- The visitor's explicit choice may override the system preference.
- Any persistence must be transparent and limited to the theme preference.
- Avoid a flash of the wrong theme on initial load.

## 14. Product truth and trust

The website must not claim that protection is unbreakable, that Nūr cures a condition, or that all privacy controls are complete.

Do not publish unsupported claims about:
- Complete data export or deletion.
- Fully verified accountability access controls.
- Mature adaptive intelligence.
- Guaranteed protection or outcomes.
- Testimonials, metrics or customer counts that have not been verified and permissioned.

Refer to `WEBSITE_PRODUCT_STATUS.md` and re-check the application repository before publishing product capability claims.

## 15. Implementation status

This document records approved design direction and implementation requirements. It does not mean the design system, components, pages, animations or accessibility checks have already been implemented.

The next implementation tasks are:
1. Reconcile this document with the existing local website documentation.
2. Inspect the current Astro project and package scripts.
3. Implement CSS tokens and light/dark themes.
4. Implement global typography and layout.
5. Build the shared header and footer.
6. Build the homepage hero.
7. Verify responsive behaviour, accessibility and production build.
