# Nūr Website — Information Architecture & Navigation Specification

**Status:** Architecture specification; homepage core sections, closed-alpha status callout and responsive footer implemented in source control; verification pending
**Date:** 25 November 2026
**Repository:** `hassantaiwo866-dotcom/nur-website`
**Working branch:** `feature/website-design-system`
**Website branch baseline:** `f3fa560571e9e276ef58d6144173e30b5b3d4bb9`
**App evidence baseline:** `N-r` / `integration/alpha-readiness` at `055d9cc5d3e8fa0f7bd87fa0fe8defdb819ef9fc`

---

## 1. Purpose

This document defines the public website's page structure, navigation, URL conventions, user journeys and implementation order. It consolidates the existing design, feature, privacy, FAQ, About and closed-alpha specifications into one navigable site.

This remains the information-architecture reference. Selected homepage components are now implemented; secondary routes, legal pages, support services and backend services remain pending.

## 2. Site goals and priority

The website has five jobs, in this order:

1. Explain Nūr clearly within the first few seconds.
2. Earn trust through transparent product and privacy information.
3. Give visitors a useful understanding of how Nūr works.
4. Provide a truthful path to closed-alpha information and, when operational, an access request.
5. Establish a credible home for support, legal information and future updates.

Primary audience: adults exploring better control of attention, digital habits, recovery and intentional living. The site should be usable on mid-range Android devices, narrow screens and slower connections.

Islamic Mode is optional. The website is for a broad audience and must not assume that every visitor is Muslim.

## 3. Recommended navigation

### Desktop header

- **Nūr wordmark** → Home
- How it works
- Features
- Privacy
- About
- **Alpha status / Request access** → Closed Alpha page

Keep the header compact. The alpha action is visually distinct but must reflect the real application state. If applications are closed, label it **Alpha status**, not **Join now**.

### Mobile navigation

- Wordmark
- Menu button with accessible expanded state
- Navigation links in the same order as desktop
- Alpha status/action visible without requiring a long scroll where practical

The menu must work by keyboard and screen reader, close predictably, and respect reduced-motion settings. Do not rely on hover.

### Footer navigation

Group links into three clear columns or stacked groups:

**Explore**
- How Nūr works
- Features
- About Nūr

**Trust**
- Privacy & Trust
- What Nūr Cannot Do
- FAQ

**Help & legal**
- Help & contact (only when a real support destination exists)
- Privacy notice
- Terms of use
- Data requests (only when an operational process exists)

Include the Nūr wordmark, concise brand line and current copyright year generated at build time. Do not display empty social icons or invented contact details. Add social links only for official, active accounts.

## 4. Page map and routes

Use lowercase, short, readable paths. Keep the brand spelling Nūr in visible copy; use `nur` in URLs.

| Page | Proposed path | Launch priority | Purpose |
|---|---|---|---|
| Home | `/` | Phase 1 | Explain Nūr and direct visitors |
| How it works | `/how-it-works/` | Phase 1 | Explain the product cycle |
| Features | `/features/` | Phase 1 | Present verified feature foundations and boundaries |
| Privacy & Trust | `/privacy/` | Phase 1 | Explain data principles and verified behaviour |
| What Nūr Cannot Do | `/limitations/` | Phase 1 | Set honest capability boundaries |
| FAQ | `/faq/` | Phase 1 | Answer common questions |
| About Nūr | `/about/` | Phase 1 | Explain mission, vision and principles |
| Closed Alpha | `/alpha/` | Phase 1 | Show accurate access status and future request process |
| Privacy notice | `/legal/privacy/` | Before data collection | Formal legal privacy information |
| Terms of use | `/legal/terms/` | Before public use/distribution | Terms governing use |
| Help & contact | `/help/` | Before alpha invitations | Real support and issue-reporting routes |
| Data requests | `/data-requests/` | Before personal data collection | Access, correction, withdrawal and deletion request process |

A route can be omitted from navigation while still being accessible from relevant pages. Do not create a page that contains only a title and placeholder links and present it as complete.

### Future routes — not part of initial launch

- `/journal/` and individual article paths — educational articles, only when editorial ownership and review are established.
- `/partners/` — accountability partner guidance and approved partnership information.
- `/updates/` — release notes and product announcements.
- `/pricing/` — only after pricing and entitlements are decided.
- `/ask/` — only if a product-bounded assistant is built, privacy-reviewed and clearly limited.
- Localised paths such as `/ha/` or `/yo/` — only after translations receive fluent human review.

Do not add these routes to the live navigation before their content and operational requirements are met.

## 5. Homepage section order

The homepage should be a concise guided introduction, not a copy of every full page.

1. **Hero** — “Build the person you want to become.” Supporting line: “Protect your attention. Strengthen self-control. Recover, rebuild and grow.” Main CTA follows the real alpha state; secondary CTA: “Discover Nūr”.
2. **Hold demonstration** — a small, optional interactive preview with clear explanation that it is a website demonstration, not the app's protection system.
3. **How Nūr works** — introduce PROTECT → RESIST → RECOVER → REBUILD → LIVE → LEARN → ADAPT as a guiding, non-linear framework.
4. **Feature overview** — concise cards linking to the Features page; label availability accurately.
5. **Product preview** — genuine screenshots only, from an identified app build. Never fabricate UI and present it as shipped.
6. **Privacy & Trust** — short principles and link to the full page.
7. **Honest limits** — a short statement and link to What Nūr Cannot Do.
8. **About Nūr** — concise mission and link to About.
9. **FAQ preview** — no more than six priority questions, linking to the full FAQ.
10. **Final alpha status** — repeat the real status and next step.

Do not add testimonials, user counts, ratings, partner logos, pricing or impact statistics without genuine evidence and permission.

## 6. Page responsibilities and boundaries

### How it works
Explains the philosophy and product cycle. It must say the cycle is a guiding framework, not a mandatory sequence or proof that every stage is implemented.

### Features
Introduces Shield/Protection, Focus, Reset & Recovery, Insights & Growth, Accountability and optional Islamic Mode. Each feature must have an availability label grounded in the current release evidence. Re-audit the app before publication.

### Privacy & Trust
Explains local versus remote processing, collection minimisation, sharing, controls, retention and current limitations. Link to the formal privacy notice. Never use absolute claims such as “100% private”.

### What Nūr Cannot Do
Explains technical, personal, medical and religious boundaries. It is a trust page, not a disclaimer hidden in tiny text.

### FAQ
Answers common questions in plain language. Avoid duplicating the complete legal notice; link to it.

### About
Explains the mission and principles. Founder biography, portrait or personal story requires explicit approval.

### Closed Alpha
Shows whether applications are closed, open or paused. If open, links to the implemented, tested and privacy-reviewed request flow. The page itself must not imply that the waitlist already exists.

### Legal pages
Must be reviewed for the actual operator, services, data flows, countries and release. Do not publish generic legal templates as if they were legal advice or completed review.

## 7. Key visitor journeys

### Journey A — first-time visitor
Home → How it works → Features → Privacy & Trust → Alpha status

### Journey B — privacy-conscious visitor
Home → Privacy & Trust → FAQ → Privacy notice → Alpha status

### Journey C — protection-focused visitor
Home → Features / Protection → What Nūr Cannot Do → FAQ → Alpha status

### Journey D — Muslim visitor exploring Islamic Mode
Home → Features / Islamic Mode → FAQ → Privacy & Trust

The journey must explain that Islamic Mode is optional and Nūr does not issue religious rulings.

### Journey E — prospective alpha tester
Home → Alpha status → Read limitations and privacy information → Request access (only when open) → Verify email → Wait for review → Invitation (if selected)

Do not skip consent, email verification or the explanation of alpha risks.

### Journey F — existing tester seeking help
Footer or invitation → Help & contact → Troubleshooting / report issue / privacy request

This journey is not live until a real support process and response owner exist.

## 8. Cross-linking rules

- Every feature card links to the relevant feature detail or section.
- Every privacy summary links to Privacy & Trust and the formal privacy notice.
- Protection claims link to What Nūr Cannot Do.
- FAQ answers link to deeper pages when the answer needs detail.
- Alpha request pages link to limitations, privacy notice and terms before submission.
- Data requests are linked from Privacy & Trust and the privacy notice once operational.
- No dead-end CTA, `#` placeholder, empty social link or non-functional button.
- External links must identify their destination and use secure official URLs.

## 9. Content status and release labels

Use a small, consistent set of labels:

- **Available** — verified in the actual public release.
- **Limited** — implemented but subject to documented scope or platform limits.
- **In testing** — available only to a controlled test group.
- **In development** — not available for general use.
- **Planned** — intended future work, not implemented.

Do not use a label as a substitute for explaining material limitations. Avoid vague terms such as “coming soon” unless a release window is approved.

## 10. SEO, metadata and technical structure

- Each page has a unique title, description, canonical URL and social preview metadata.
- One clear H1 per page; headings follow a logical hierarchy.
- Generate sitemap and robots directives from the actual published routes.
- Provide a useful 404 page with links to Home, Features and FAQ.
- Use semantic landmarks: header, navigation, main, sections and footer.
- Use descriptive link text and meaningful image alternative text.
- Avoid indexing unfinished, private preview or staging pages.
- Keep page content readable if JavaScript fails.
- Do not add analytics, cookies, trackers or third-party embeds by default. Any later addition requires privacy and legal review and accurate disclosure.
- Keep website hosting and any alpha-request service separate from app user data systems.

## 11. Visual and responsive rules

Follow `docs/DESIGN_SYSTEM.md`:
- Deep forest-green foundation with soft emerald illumination.
- Refined serif headings and readable sans-serif body text.
- Concentric light, subtle arcs and new-beginnings motifs.
- Restrained liquid glass on hero, demonstrations and feature cards; solid backgrounds for long-form text.
- System colour preference support.
- Respect reduced motion and data-saving needs.
- Avoid large video backgrounds, heavy animation libraries and oversized assets.
- Ensure readable contrast, visible focus states and comfortable touch targets.
- Mobile layout is a first-class design, not a squeezed desktop page.

## 12. Recommended implementation sequence

Build in controlled increments, keeping the existing local Astro project as the intended implementation base. The GitHub branch currently contains documentation only; it does not yet contain the Astro scaffold.

**Stage 0 — reconcile project source**
1. When the user's PC is available, inspect the local Astro project and Git status.
2. Compare local files and dependencies with the latest GitHub branch.
3. Preserve the Astro scaffold; do not create a competing framework or overwrite local work.
4. Integrate the Astro project into the agreed working branch with a reviewed commit.
5. Confirm the actual Astro version, scripts, lockfile and build command from the checked-in files.

**Stage 1 — foundation**
1. Global layout, design tokens, typography and responsive container.
2. Header, mobile navigation and footer.
3. SEO defaults, metadata, sitemap, 404 and accessibility baseline.

**Stage 2 — launch pages**
1. Home page.
2. How it works.
3. Features.
4. Privacy & Trust.
5. What Nūr Cannot Do.
6. FAQ.
7. About.
8. Alpha status page (closed-state copy only until backend exists).

**Stage 3 — legal and support readiness**
1. Privacy notice and terms reviewed against real data flows.
2. Support route and data-rights contact operational.
3. Links, contact details and release status verified.

**Stage 4 — interactive and conversion features**
1. Hold demo with no collection and accessible fallback.
2. Optional personal-path quiz only after privacy behaviour is specified and tested.
3. Alpha request backend only after the separate security and privacy gates in `docs/CLOSED_ALPHA_ACCESS_SPEC.md`.
4. App download links only after signed release artifacts and distribution process are ready.

**Stage 5 — launch validation**
1. Build and automated checks.
2. Accessibility and responsive testing on representative devices.
3. Performance checks on slower networks and mid-range Android.
4. Link, SEO, privacy and security review.
5. Preview deployment and owner approval before production.

## 13. Current repository reality

At the baseline commit recorded above, `feature/website-design-system` contains `README.md` and the website specification documents under `docs/`. It does not contain `package.json`, Astro configuration, `src/`, page routes, components, tests or CI workflows.

The Astro scaffold was previously created locally on the user's PC and has not yet been reconciled into this GitHub branch. Do not report the website as implemented or build-verified until those source files are present in the repository and checks have been run.

The app implementation baseline is a separate repository and branch. The app is not modified by this website architecture document.

## 14. Acceptance checklist

- [ ] Navigation labels and page routes match this specification.
- [ ] All Phase 1 pages have approved content and no placeholder claims.
- [ ] Header, mobile navigation and footer work accessibly.
- [ ] Every CTA has a real destination and accurate state.
- [ ] No planned feature is presented as released.
- [ ] Legal, support and data-request links are operational before they are shown.
- [ ] Alpha status matches the actual recruitment system.
- [ ] Sitemap, metadata, canonical URLs and 404 are tested.
- [ ] Responsive, keyboard, screen-reader and reduced-motion checks pass.
- [ ] Performance is checked on a representative mid-range Android and slow connection.
- [ ] Astro scaffold has been reconciled and committed without replacing the chosen framework.
- [ ] Production deployment is approved only after build, security and privacy checks pass.

---

**Implementation boundary:** This document defines site architecture and implementation order. It does not create website routes or components, connect a waitlist, publish legal pages, deploy hosting or change the Nūr app.


## 15. Homepage closing CTA and footer — implementation record

The homepage now ends with a static closed-alpha status callout:
- It states that Nūr is in development and closed-alpha applications are not open.
- It offers a working in-page link to How Nūr Works.
- It does not display an active application form, collect email addresses or promise a release date.

The shared layout footer now groups links into:
- Explore: How Nūr Works, Features and About.
- Trust: Privacy & Trust, What Nūr Cannot Do and FAQ.
- Availability: current development status and closed-alpha status anchor.

Every footer destination currently points to an existing homepage section. Legal, contact, data-request and social links are intentionally omitted because no verified destination or operational process has been established.

The Astro build, browser rendering, accessibility and device checks remain pending.
