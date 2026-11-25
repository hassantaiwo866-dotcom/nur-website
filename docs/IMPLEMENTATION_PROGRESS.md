# Nūr Website — Implementation Progress

**Updated:** 25 November 2026  
**Branch:** `feature/website-design-system`

## Current milestone: homepage foundation and feature storytelling

Initial homepage sections are committed to the website branch. This is implementation progress, not a verified release. The Astro build, browser behaviour, accessibility and physical-device rendering have not been tested in this environment.

### Implemented in source control

- Global CSS tokens for the approved forest-green identity and system-preference themes.
- Shared Astro document layout, metadata defaults, skip link, header and footer.
- Responsive navigation and homepage hero with CSS-generated concentric light, emerald illumination and horizon arc.
- Privacy-first interactive Hold demonstration with ready, running, complete and early-ended states.
- Seven-stage product philosophy section: PROTECT, RESIST, RECOVER, REBUILD, LIVE, LEARN and ADAPT.
- Six-card feature grid: Nūr Shield, Focus, Reset & Recovery, Insights & Growth, Accountability and optional Islamic Mode.
- Qualified product copy based on the inspected app implementation evidence.
- Responsive card layouts, reduced-motion handling and visible focus styling.

### Website source files

- `src/styles/global.css`
- `src/layouts/BaseLayout.astro`
- `src/components/layout/SiteHeader.astro`
- `src/components/home/HeroSection.astro`
- `src/components/home/HoldDemo.astro`
- `src/components/home/ProductLoop.astro`
- `src/components/home/FeatureGrid.astro`
- `src/pages/index.astro`

### Documentation updated

- `docs/COMPONENT_ARCHITECTURE.md`
- `docs/HOW_NUR_WORKS_SPEC.md`
- `docs/FEATURES_SECTION_SPEC.md`
- `docs/IMPLEMENTATION_PROGRESS.md`

### Deliberately not implemented

- Closed-alpha registration or waitlist submission.
- Analytics, cookies, trackers or third-party scripts.
- Fabricated app screenshots, testimonials or metrics.
- Live app-user integrations or app data access.
- Public deployment, domain configuration or hosting.
- Claims that protection is unbreakable, accountability is fully verified, or insights are comprehensive.

## Verification status

| Check | Status |
|---|---|
| Homepage and feature source committed | Complete |
| Source readback from GitHub | Pending final verification |
| App evidence reviewed for feature claims | Complete (static source/docs review) |
| App tests run in this task | No |
| Astro production build | Not run |
| Type checking | Not run |
| Accessibility/contrast audit | Not run |
| Real-device visual review | Not run |
| Deployment | Not configured |

## Integration note

The user's existing local Astro scaffold remains on their PC and has not been reconciled with this branch. Before merging or deploying, inspect local Git status, package files, Astro configuration, source files and tests. Preserve local work; do not reset or overwrite it.

A successful production build and browser review are required before describing the website as working.
