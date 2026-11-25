# Nūr Website — Implementation Progress

**Updated:** 25 November 2026  
**Branch:** `feature/website-design-system`

## Current milestone: homepage foundation

The first source files have been added to the website branch. This is an initial implementation, not a verified release.

### Implemented in source control

- Global CSS tokens for the approved forest-green identity.
- System-preference dark and light theme values.
- Display and body font stacks with local system fallbacks; no third-party font request.
- Shared Astro document layout and metadata defaults.
- Skip link and shared site footer.
- Responsive site header with desktop links and a native disclosure-based mobile menu.
- Homepage hero with CSS-generated concentric light, emerald illumination and a subtle horizon arc.
- Initial homepage sections introducing Nūr, its support areas and its user-controlled philosophy.\n- Interactive Hold demonstration with ready, running, complete and early-ended states; 10-second timer; restart and return actions; privacy boundary note.
- Reduced-motion handling, focus-visible styles and responsive layouts.

### Files added or updated

- `src/styles/global.css`
- `src/layouts/BaseLayout.astro`
- `src/components/layout/SiteHeader.astro`
- `src/components/home/HeroSection.astro`
- `src/pages/index.astro`\n- `src/components/home/HoldDemo.astro`
- `docs/COMPONENT_ARCHITECTURE.md`

### Deliberately not implemented yet

- Closed-alpha registration or waitlist submission.
- Analytics, cookies, trackers or third-party scripts.
- App screenshots or fabricated product UI.
- Live protection, account or app-user integrations.
- Additional Hold interaction verification, accessibility review and browser testing.
- Full feature, privacy, FAQ, about, legal or support pages.
- Hosting, domain configuration or public deployment.

The hero currently directs visitors to the explanatory content rather than a non-functional alpha signup.

## Verification status

| Check | Status |
|---|---|
| GitHub source files created | Complete |\n| Hold demo source committed | Complete |
| Source files re-fetched from GitHub | Pending final verification |
| Astro production build | Not run |
| Type checking | Not run |
| Accessibility audit | Not run |
| Real-device visual review | Not run |
| Deployment | Not configured |

## Integration note

The pre-existing local Astro scaffold is still on the user's PC and has not yet been reconciled with this branch. Before merging or deploying, inspect its Git status, package files, Astro configuration, existing source files and tests. Preserve local work; do not reset or overwrite it.

The source files on this branch are the initial implementation work to reconcile with that local scaffold. A successful build and browser review are required before describing the website as working.
