# Nūr Website — Component Architecture Specification

**Status:** Architecture specification; initial homepage foundation partially implemented
**Date:** 25 November 2026
**Repository:** `hassantaiwo866-dotcom/nur-website`
**Working branch:** `feature/website-design-system`
**Website baseline:** `13c6062d0cb3de530b760f7841d81589030fe6af`
**Framework decision:** Preserve the existing local Astro project; no framework replacement authorised.

---

## 1. Purpose

Define reusable Astro components, layouts, page composition, styling boundaries and interaction ownership before implementation.

This document began as a component architecture specification. Initial Astro page, layout, header, hero and global stylesheet files have since been added on this branch. The existing local Astro scaffold still must be inspected and reconciled before these files are merged into the local working copy or deployed.

## 2. Architecture principles

1. **Astro-first, static by default.** Render content and layout on the server/build; add client JavaScript only to interactions that need it.
2. **One source of truth for tokens.** Colours, spacing, typography, radii and motion come from the approved design system.
3. **Semantic HTML.** Components should expose meaningful headings, landmarks, buttons, links and disclosure controls.
4. **Progressive enhancement.** Core copy and navigation remain usable if JavaScript is unavailable.
5. **Small client surface.** Avoid a frontend framework or animation library for simple interactions.
6. **No invented product state.** Availability labels, alpha state and app screenshots must come from approved, verified content.
7. **Low-end device awareness.** Keep CSS effects restrained, images optimised and interaction code small.
8. **Privacy-first.** Components do not add analytics, tracking, fingerprinting or hidden data collection.

## 3. Proposed project structure

This is a target structure to adapt to the actual Astro scaffold—not permission to overwrite existing files.

```text
nur-website/
├── public/
│   ├── favicon.svg
│   ├── robots.txt
│   └── images/
│       ├── app/
│       └── brand/
├── src/
│   ├── components/
│   │   ├── layout/
│   │   │   ├── SiteHeader.astro
│   │   │   ├── MobileNavigation.astro
│   │   │   ├── SiteFooter.astro
│   │   │   └── SkipLink.astro
│   │   ├── ui/
│   │   │   ├── Button.astro
│   │   │   ├── TextLink.astro
│   │   │   ├── GlassPanel.astro
│   │   │   ├── SectionHeading.astro
│   │   │   ├── StatusLabel.astro
│   │   │   └── Container.astro
│   │   ├── home/
│   │   │   ├── HeroSection.astro
│   │   │   ├── HoldDemo.astro
│   │   │   ├── ProductLoop.astro
│   │   │   ├── FeatureGrid.astro
│   │   │   ├── ProductPreview.astro
│   │   │   ├── TrustPreview.astro
│   │   │   ├── LimitsPreview.astro
│   │   │   ├── AboutPreview.astro
│   │   │   ├── FAQPreview.astro
│   │   │   └── AlphaCallout.astro
│   │   ├── features/
│   │   │   ├── FeatureCard.astro
│   │   │   └── FeatureAvailability.astro
│   │   └── content/
│   │       ├── FAQAccordion.astro
│   │       └── ProseContent.astro
│   ├── layouts/
│   │   ├── BaseLayout.astro
│   │   └── ContentLayout.astro
│   ├── pages/
│   │   ├── index.astro
│   │   ├── how-it-works.astro
│   │   ├── features.astro
│   │   ├── privacy.astro
│   │   ├── limitations.astro
│   │   ├── faq.astro
│   │   ├── about.astro
│   │   ├── alpha.astro
│   │   ├── 404.astro
│   │   └── legal/
│   │       ├── privacy.astro
│   │       └── terms.astro
│   ├── data/
│   │   ├── navigation.ts
│   │   ├── features.ts
│   │   └── faq.ts
│   └── styles/
│       ├── global.css
│       ├── tokens.css
│       └── utilities.css
├── docs/
└── [existing Astro config, package files and tests]
```

Do not create empty placeholder pages for routes that are not approved or ready. Do not duplicate global styles inside individual components.

## 4. Layout components

### BaseLayout.astro

Responsibilities:
- HTML document shell and language.
- Metadata slots: title, description, canonical URL and social image.
- Global CSS and theme preference.
- Skip link, site header, main content slot and footer.
- Favicon and lightweight font strategy.
- Optional page-specific structured metadata only when valid.

Must not:
- Inject analytics or third-party scripts.
- contain app-user data or authentication assumptions.
- hardcode a launch date, alpha state or unsupported claim.

### ContentLayout.astro

Used by long-form pages such as About, FAQ, Privacy and Limitations.

Responsibilities:
- Consistent content width and readable measure.
- Breadcrumb or page intro where appropriate.
- Optional table of contents for long pages.
- Main heading and prose layout.
- Clear links to related pages.

Avoid glass backgrounds behind long text.

### SiteHeader.astro

- Wordmark links to home.
- Desktop navigation follows `INFORMATION_ARCHITECTURE.md`.
- Alpha action label derives from approved site configuration.
- Sticky behaviour only if it does not obscure content or focus.
- Visible keyboard focus and active-page indication.

### MobileNavigation.astro

- Native button toggles menu state.
- Exposes `aria-expanded` and `aria-controls`.
- Supports Escape and closes after navigation.
- Focus remains predictable.
- No hover-only interaction.
- Works without a large client-side dependency.

### SiteFooter.astro

- Explore, Trust, Help & Legal groups.
- Only real, live destinations.
- No placeholder social icons or invented email address.
- Copyright year can be generated at build time.

## 5. Reusable UI components

| Component | Responsibility | Important constraints |
|---|---|---|
| Container | Standard responsive width | No nested arbitrary max-width overrides |
| Button | Primary/secondary actions | Use links for navigation, buttons for actions |
| TextLink | Inline and contextual links | Descriptive accessible text |
| GlassPanel | Restrained glass surface | Solid fallback, readable contrast |
| SectionHeading | Eyebrow, title, intro | Semantic heading level passed by parent |
| StatusLabel | Available/limited/testing/planned | Never infer status |
| FeatureCard | Feature summary and destination | Copy from approved feature spec |
| ProseContent | Long-form content | Comfortable line length, no glass |
| FAQAccordion | Expandable answers | Keyboard accessible, semantic disclosure |

Avoid building a generic component abstraction where a small semantic Astro component is clearer.

## 6. Homepage composition

`src/pages/index.astro` should compose sections in this order:

1. HeroSection
2. HoldDemo
3. ProductLoop
4. FeatureGrid
5. ProductPreview
6. TrustPreview
7. LimitsPreview
8. AboutPreview
9. FAQPreview
10. AlphaCallout

Each section is authored as a standalone Astro component with explicit props where reusable. The page controls the order; components do not secretly inject themselves into the page.

### HeroSection.astro

- Deep forest background `#03140F`.
- Ambient radial emerald illumination behind the headline.
- Subtle concentric rings and curved horizon arc.
- Serif headline and readable supporting copy.
- Primary CTA reflects real alpha status.
- Secondary link to How it works.
- Glass treatment limited to selected hero surface elements.
- No forced illustration, video background or distracting particles.

### HoldDemo.astro

- Implements the approved Hold demo specification.
- Clear Ready, Pause and Complete states.
- Accessible controls and non-JavaScript fallback.
- No data persistence, analytics or submission.
- Clear label that this is a website demonstration, not live device protection.
- Avoid requiring a press-and-hold gesture as the only way to operate it; provide an accessible equivalent.

### ProductLoop.astro

- Presents the seven-stage product framework.
- Supports narrow-screen vertical layout.
- No implication that the user must progress linearly or that every stage is released.

### FeatureGrid.astro / FeatureCard.astro

- Data-driven from a typed feature content source.
- Availability label is explicit and reviewed.
- Cards link to real page anchors or feature sections.
- No invented metrics or testimonials.

### ProductPreview.astro

- Uses only genuine screenshots from a named app build.
- Responsive images with dimensions and appropriate loading.
- If no approved screenshots exist, render a restrained explanatory layout rather than fabricated app UI.

### FAQAccordion.astro

- Uses native `details` and `summary` where suitable.
- Multiple answers may remain open.
- Answers exist in page HTML and remain readable without JavaScript.
- Does not trap focus.

## 7. Content data and type safety

Keep repeatable content in `src/data/` where this makes maintenance safer.

Suggested feature record shape:

```ts
export type Availability =
  | "available"
  | "limited"
  | "testing"
  | "development"
  | "planned";

export interface FeatureItem {
  slug: string;
  title: string;
  summary: string;
  availability: Availability;
  href: string;
}
```

The values are content, not runtime discovery. The site owner must review and update availability against the actual app release before deployment.

FAQ content should have stable IDs, question, answer and optional related-page link. Do not store HTML strings and inject them unsafely.

## 8. Styling architecture

- `tokens.css`: colour, typography, spacing, radii, shadows and motion tokens from `DESIGN_SYSTEM.md`.
- `global.css`: reset, base typography, document defaults, focus and selection styles.
- `utilities.css`: a small set of layout and accessibility utilities only.
- Component styles: scoped to the component unless a pattern is genuinely shared.
- No inline style duplication for design tokens.
- Support `prefers-color-scheme` as approved; system preference is the default theme behaviour.
- Support `prefers-reduced-motion: reduce`.
- Glass uses backdrop-filter only as progressive enhancement, with an opaque or sufficiently solid fallback.
- Do not add a heavy animation, icon or UI framework for decorative effects.

## 9. Interaction ownership

| Interaction | Implementation approach | Data behaviour |
|---|---|---|
| Main navigation | Native links | No collection |
| Mobile menu | Small local script | No persistence |
| FAQ | Native disclosure | No collection |
| Hold demo | Small local script | In-memory only |
| Theme | CSS system preference | No saved preference by default |
| Personal-path quiz (future) | Separate specification first | Local-only unless separately consented |
| Alpha request (future) | Dedicated backend service | Separate waitlist data store |

No component may send user interaction data to a server unless a separate reviewed feature explicitly requires it and documents the purpose, consent and retention.

## 10. Accessibility and performance requirements

- Semantic HTML and logical heading hierarchy.
- Skip link and keyboard-operable navigation.
- Focus indicators visible against all surfaces.
- Colour contrast checked for normal and large text.
- Interactive controls have accessible names and comfortable touch targets.
- Reduced motion respected.
- Images have appropriate alt text; decorative motifs are hidden from assistive technology.
- No layout shift from missing image dimensions or late font loading.
- Use modern image formats where practical and lazy-load below-the-fold images.
- Avoid loading large images or scripts before they are needed.
- Test on a representative mid-range Android device and slow connection.
- Keep JavaScript limited to the menu and small demos until justified otherwise.

## 11. Testing expectations

When the Astro project is reconciled, add or adapt tests for:

- Build and type checking.
- Header desktop/mobile links and active state.
- Keyboard menu operation and Escape behaviour.
- FAQ keyboard and screen-reader semantics.
- Hold demo state transitions, early exit and no-data behaviour.
- All links and route targets.
- Metadata and sitemap output.
- Reduced-motion styling.
- Responsive overflow and contrast.
- No analytics, cookies or third-party requests unless explicitly approved.

Do not invent test scripts before inspecting the actual package scripts and installed test tooling.

## 12. Implementation sequence

1. Inspect the local Astro project and current Git status.
2. Reconcile it with the current GitHub branch without overwriting either side.
3. Confirm actual Astro version, dependencies, scripts, lockfile and build.
4. Create or adapt tokens and BaseLayout.
5. Build header, mobile navigation and footer.
6. Build shared UI components.
7. Compose homepage in approved order.
8. Build secondary pages using ContentLayout.
9. Add Hold demo and FAQ disclosure behaviour.
10. Run tests/build, accessibility and responsive checks.
11. Update docs and commit verified changes.

## 13. Repository boundary and current status

At website branch commit `13c6062d0cb3de530b760f7841d81589030fe6af`, GitHub contains `README.md` and documentation files only. There is no checked-in `package.json`, Astro config, `src/`, test suite or CI workflow.

The user previously created an Astro scaffold locally. Its current state cannot be inferred from the GitHub branch and must be inspected on the user's PC before any implementation or merge.

The Nūr app repository is separate. This document does not change app source, app architecture, database or release status.

## 14. Acceptance checklist

- [ ] Local Astro scaffold inspected and preserved.
- [ ] Actual Astro config and package scripts confirmed.
- [ ] Shared tokens have one source of truth.
- [ ] Layout components are semantic and responsive.
- [ ] Interactive components use minimal JavaScript and collect no data.
- [ ] Feature status is sourced from approved, current evidence.
- [ ] No fabricated screenshots or placeholder CTAs.
- [ ] All routes and navigation destinations exist.
- [ ] Keyboard, screen reader, reduced motion and contrast checks pass.
- [ ] Build and tests pass on the reconciled repository.
- [ ] Documentation reflects the implemented architecture.

---

**Implementation boundary:** This document defines a proposed component architecture. It does not create components, modify the local Astro project, implement interactions or claim a successful build.
