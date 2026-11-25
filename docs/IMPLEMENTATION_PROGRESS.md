# Nūr Website — Implementation Progress

**Updated:** 25 November 2026  
**Branch:** `feature/website-design-system`

## Current milestone: homepage sections

The homepage foundation, Hold preview and seven-stage product-cycle section now exist in source control. This is implementation progress, not a verified release: the Astro build and browser behaviour have not yet been tested.

### Implemented in source control

- Global CSS tokens for the approved forest-green identity.
- System-preference dark and light theme values.
- Display and body font stacks with local system fallbacks; no third-party font request.
- Shared Astro document layout and metadata defaults.
- Skip link and shared site footer.
- Responsive site header with desktop links and a native disclosure-based mobile menu.
- Homepage hero with CSS-generated concentric light, emerald illumination and a subtle horizon arc.
- Privacy-first interactive Hold demonstration with ready, running, complete and early-ended states; 10-second timer; restart and return actions; privacy boundary note.
- Seven-stage Nūr approach section: PROTECT, RESIST, RECOVER, REBUILD, LIVE, LEARN and ADAPT.
- Non-linear cycle framing, responsive cards, reduced-motion-compatible static presentation and explicit product-availability boundary.
- Initial feature overview and user-controlled growth statement.
- Reduced-motion handling, focus-visible styles and responsive layouts.

### Files added or updated

- `src/styles/global.css`
- `src/layouts/BaseLayout.astro`
- `src/components/layout/SiteHeader.astro`
- `src/components/home/HeroSection.astro`
- `src/components/home/HoldDemo.astro`
- `src/components/home/ProductLoop.astro`
- `src/pages/index.astro`
- `docs/COMPONENT_ARCHITECTURE.md`
- `docs/HOW_NUR_WORKS_SPEC.md`
- `docs/IMPLEMENTATION_PROGRESS.md`

### Deliberately not implemented yet

- Closed-alpha registration or waitlist submission.
- Analytics, cookies, trackers or third-party scripts.
- App screenshots or fabricated product UI.
- Live protection, account or app-user integrations.
- Full feature, privacy, FAQ, about, legal or support pages.
- Hosting, domain configuration or public deployment.

The homepage uses explanatory navigation rather than a non-functional alpha signup. The product-cycle section explains the intended framework; it does not claim all seven stages are implemented app features.

## Verification status

| Check | Status |
|---|---|
| Homepage source committed to GitHub | Complete |
| Product-cycle component committed | Complete |
| Source files re-fetched from GitHub | Pending final verification |
| Astro production build | Not run |
| Type checking | Not run |
| Accessibility audit | Not run |
| Real-device visual review | Not run |
| Deployment | Not configured |

## Integration note

The pre-existing local Astro scaffold is still on the user's PC and has not yet been reconciled with this branch. Before merging or deploying, inspect its Git status, package files, Astro configuration, existing source files and tests. Preserve local work; do not reset or overwrite it.

A successful build and browser review are required before describing the website as working.
