# Nūr Website — Implementation Progress

**Updated:** 25 November 2026  
**Branch:** `feature/website-design-system`

## Current milestone: homepage foundation, trust storytelling, product-boundary education and About storytelling

Initial homepage sections are committed to the website branch. This is implementation progress, not a verified release. The Astro build, browser behaviour, accessibility and physical-device rendering have not been tested in this environment.

### Implemented in source control

- Global CSS tokens for the approved forest-green identity and system-preference themes.
- Shared Astro document layout, metadata defaults, skip link, header and footer.
- Responsive navigation and homepage hero with CSS-generated concentric light, emerald illumination and horizon arc.
- Privacy-first interactive Hold demonstration with ready, running, complete and early-ended states.
- Seven-stage product philosophy section: PROTECT, RESIST, RECOVER, REBUILD, LIVE, LEARN and ADAPT.
- Six-card feature grid: Nūr Shield, Focus, Reset & Recovery, Insights & Growth, Accountability and optional Islamic Mode.
- Privacy & Trust section: three principles, local-versus-online explanation, accountability boundary and export/deletion limitations.
- What Nūr Cannot Do preview: six concise boundary cards covering protection, user agency, recovery, Islamic Mode, privacy/accountability and AI/real-world support.\n- About Nūr preview: purpose, six-stage guiding framework, non-shaming product principles and an honest development-status note.
- Product claims qualified against inspected app source and privacy inventory.
- Responsive layouts, reduced-motion handling and visible focus styling.

### Website source files

- `src/styles/global.css`
- `src/layouts/BaseLayout.astro`
- `src/components/layout/SiteHeader.astro`
- `src/components/home/HeroSection.astro`
- `src/components/home/HoldDemo.astro`
- `src/components/home/ProductLoop.astro`
- `src/components/home/FeatureGrid.astro`
- `src/components/home/PrivacyTrust.astro`
- `src/components/home/LimitsPreview.astro`\n- `src/components/home/AboutPreview.astro`
- `src/pages/index.astro`

### Documentation updated

- `docs/COMPONENT_ARCHITECTURE.md`
- `docs/HOW_NUR_WORKS_SPEC.md`
- `docs/FEATURES_SECTION_SPEC.md`
- `docs/PRIVACY_TRUST_SECTION_SPEC.md`
- `docs/WHAT_NUR_CANNOT_DO_SPEC.md`\n- `docs/ABOUT_NUR_SECTION_SPEC.md`
- `docs/IMPLEMENTATION_PROGRESS.md`

### Deliberately not implemented

- Closed-alpha registration or waitlist submission.
- Analytics, cookies, trackers or third-party scripts.
- Fabricated app screenshots, testimonials or metrics.
- Live app-user integrations or app data access.
- Public deployment, domain configuration or hosting.
- Claims that protection is unbreakable, accountability is fully verified, export/deletion is complete or insights are comprehensive.

## Verification status

| Check | Status |
|---|---|
| Homepage source committed | Complete |
| Privacy section source committed | Complete |
| Limitations preview source committed | Complete |\n| About preview source committed | Complete |
| Documentation updated | Complete |
| GitHub readback | Complete for current changes |
| App privacy source/docs reviewed | Complete (static source review) |
| App tests run in this task | No |
| Astro production build | Not run |
| Type checking | Not run |
| Accessibility/contrast audit | Not run |
| Real-device visual review | Not run |
| Deployment | Not configured |

## Integration note

The user's existing local Astro scaffold remains on their PC and has not been reconciled with this branch. Before merging or deploying, inspect local Git status, package files, Astro configuration, source files and tests. Preserve local work; do not reset or overwrite it.

A successful production build and browser review are required before describing the website as working.
