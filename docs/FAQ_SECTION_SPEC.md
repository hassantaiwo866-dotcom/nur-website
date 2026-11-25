# Nūr Website — FAQ Section Specification

**Status:** Six-question homepage FAQ implemented; full FAQ page and verification pending
**Date:** 25 November 2026
**Website branch:** `feature/website-design-system`
**App implementation baseline:** `integration/alpha-readiness` at `055d9cc5d3e8fa0f7bd87fa0fe8defdb819ef9fc`
**Supporting app documentation:** `docs/NUR_BUILD_ROADMAP.md`, `docs/PHASE_0_DATA_STORAGE_INVENTORY.md`, `docs/privacy-user-autonomy-build.md`, and `docs/PROTECTION_SECURITY_AUDIT.md`

---

## 1. Purpose

The FAQ should answer the questions a careful visitor is likely to ask before joining an alpha or installing Nūr. It must reduce uncertainty without turning the page into a sales pitch.

This is a content specification, not evidence that every described feature is released. Answers must be updated against the actual public build, live services, privacy notice and release terms before publication.

## 2. Section introduction

**Eyebrow:** GOOD QUESTIONS. CLEAR ANSWERS.

**Headline:** Before you begin.

**Supporting copy:** A few practical answers about what Nūr does, how it handles information, and what it is still learning to do.

Do not use fake urgency, countdowns, fabricated user numbers or unsupported testimonials.

## 3. Recommended FAQ groups and proposed copy

### A. Understanding Nūr

**What is Nūr?**

Nūr is being built as a self-control, protection, recovery and personal-growth app. It brings together tools intended to help you protect your attention, make more intentional choices, recover without shame and build habits that matter to you. It is more than a website blocker.

**Is Nūr only for people who want to block explicit content?**

No. Protection is one part of Nūr. The wider direction includes Focus, recovery activities, reflection, habits and intentional living. You can use the parts that are available and relevant to you.

**Who is Nūr for?**

Nūr is intended for adults who want more control over their digital habits and attention. It is being designed with mobile-first use, including mid-range Android devices and slower connections, in mind. Do not imply support for every platform until a release has been tested and announced.

**Does Nūr judge people when they struggle?**

No. Nūr's product philosophy is no shame and no guilt. A difficult moment is information, not a verdict on your character. The experience should help you choose a next step rather than punish you.

### B. Protection and limits

**Can Nūr block every explicit website or app?**

No. Nūr's current Android protection foundation is DNS-focused, with configured exact-IP rules. It is not a full-device content firewall, and it cannot guarantee that every explicit website, app, browser or network route will be blocked. Some encrypted-DNS and other bypass paths are not comprehensively covered. Protection reliability and device behaviour still require validation.

**Does protection work when the VPN is not active?**

Do not assume it does. The app must report its actual protection state accurately. If the VPN or filtering service is stopped, interrupted or unable to operate, the website must not suggest that protection continues regardless. Explain the exact state indicators and recovery behaviour only after the public build has been tested.

**Will Nūr slow down my phone or drain my battery?**

Performance and battery impact depend on the device, Android version, network and enabled features. We should not promise zero impact. The team will test on representative Android devices and publish measured information only when reliable results are available.

**Does Nūr monitor everything I do on my phone?**

Nūr should not be described as comprehensive phone surveillance. Current reporting is based on activity that the app records; it does not establish complete monitoring of every app, unlock, website or digital action. Explain the exact data collected by each released feature in the Privacy & Trust section.

### C. Privacy and information

**Where is my Nūr data stored?**

Some personal preferences and activity records are stored locally on your device. Features that use online services may process or store specific information remotely. The exact storage location depends on the feature. Read the Privacy & Trust section and the current privacy notice for the data flows in the version you use.

**Does Nūr send my browsing history to an accountability partner?**

Do not assume that it does. Accountability is intended to be deliberate and limited to information you authorise. The complete two-device workflow and remote access controls have not yet been verified as production-ready. Do not invite users to rely on this feature until that verification is complete.

**Can I export or delete my data?**

The app has a local privacy-control foundation for exporting and deleting inventoried local records. Its documented scope is limited to the keys and stores included in the current inventory. Local deletion does not automatically delete records held by remote services, and the complete account-level and remote deletion lifecycle is not yet established. The release privacy notice must explain the exact available controls.

**Does Nūr use analytics or tracking?**

The inspected integration build documents analytics as disabled by default and states that no analytics service is connected in that build. A preference setting is not proof that tracking is active. The website also intends to avoid analytics and tracking at launch. These statements must be checked again against the actual deployed app and website before publication.

**Does Nūr use AI?**

Some AI-assisted capabilities are part of the wider development plan, and an AI consent implementation exists on a separate development branch. It is not evidence that AI is enabled or integrated in the current public build. Any released AI feature must explain what information it sends, why it needs it, how to opt in or out, and which service processes it. AI must remain optional and must not be presented as a replacement for human judgement.

### D. Focus, recovery and growth

**What happens if I miss a goal or have a setback?**

You can choose what to do next. Nūr is designed around reflection and recovery, not punishment. It should not use a missed goal as a reason to shame you, erase your progress or force you to explain yourself.

**Does Nūr guarantee that I will change my habits?**

No. Nūr can provide tools and structure, but it cannot make choices on your behalf or guarantee a particular result. Your circumstances, decisions and support systems matter.

**Is Nūr a mental-health or addiction-treatment app?**

No. Nūr is not a medical service, therapist, diagnostic tool or emergency service. It does not replace qualified professional support. If you need urgent help or feel unsafe, contact appropriate local emergency or professional support.

### E. Islamic Mode

**Is Nūr only for Muslims?**

No. Nūr is intended for a broad audience. Islamic Mode is optional and should never be required to use the core app.

**What does Islamic Mode do?**

The current implementation baseline includes an optional mode setting and intention foundation. Specific religious content and flows must be checked against the actual release before being listed here. The website should describe only what is present and verified.

**Does Nūr issue fatwas or provide religious rulings?**

No. Nūr is not a mufti or religious authority. It should not claim to issue fatwas or provide authoritative interpretations of the Qur'an. Where Islamic material is presented, its sources and limitations should be clear.

### F. Availability, pricing and support

**Is Nūr available to download now?**

The website must show the current release status clearly. During a closed-alpha period, say that access is limited and explain the real invitation process. Do not display a working-looking Join Alpha button until the registration flow is operational. Do not promise an app-store release date that has not been confirmed.

**How much will Nūr cost?**

Pricing has not been finalised. We will publish pricing when the plans and included features are confirmed. Do not invent a free tier, subscription price, lifetime plan or feature entitlement.

**Which devices does Nūr support?**

The current development focus includes Android. Publish a specific minimum Android version and supported-device statement only after release testing. Do not imply iOS, desktop or web-app parity without an actual supported release.

**How can I contact the Nūr team?**

Publish a support or privacy contact only after an address and response process are established. Do not use a placeholder address that appears operational. Privacy and data-rights requests should have a clearly identified channel before the app collects data from public users.

**Can I suggest a feature or report a problem?**

Yes, once a real feedback channel is available. The page should link to the approved support channel and explain what information to include. Do not ask users to send sensitive browsing or recovery details through an unsecured public form.

## 4. Homepage FAQ selection

Keep the homepage FAQ concise. Recommended first six questions:

1. What is Nūr?
2. Can Nūr block every explicit website or app?
3. Where is my Nūr data stored?
4. Does Nūr send my browsing history to an accountability partner?
5. Is Nūr only for Muslims?
6. Is Nūr available to download now?

Link to a full FAQ page for the remaining questions. Do not duplicate long privacy disclosures; link to Privacy & Trust and the legal privacy notice.

## 5. Interaction and accessibility

- Use semantic disclosure elements or an accessible accordion pattern.
- Each question must be a keyboard-operable control with a visible focus state.
- Expose expanded/collapsed state to assistive technology.
- Keep answers in the document and readable without animation.
- Allow multiple answers to remain open; do not force visitors to lose their place.
- Respect reduced-motion preferences.
- Avoid tiny tap targets and excessive nested glass cards.
- Use a clean, solid surface for long answers.
- Ensure the FAQ works without client-side JavaScript where practical.

## 6. Content governance and publication gates

Before publishing, the owner must:

1. Re-check the current app release branch, commit, feature flags and actual installable build.
2. Verify protection claims on supported physical Android devices and align them with the latest security audit.
3. Reconcile the data inventory with every local store, native preference, database, remote table, edge function, log and third-party provider used by the release.
4. Run and record export/deletion tests; explain local versus remote scope and any retention exceptions.
5. Verify accountability access controls and two-account/two-device lifecycle before describing the workflow as available.
6. Verify whether analytics, crash reporting, AI and other third-party SDKs are connected in the shipped build.
7. Confirm Islamic Mode content and source references in the exact release.
8. Confirm alpha access method, support contact, pricing status and supported platforms.
9. Have the privacy notice and legal terms reviewed for Nigeria and any other intended launch markets.
10. Date the review and link the FAQ to the corresponding release evidence.

If an answer cannot be verified, remove it, qualify it or say that the feature is still being developed. Never fill a gap with a guess.

## 7. Content and design rules

- Keep answers short and direct; link to detailed pages for technical or legal explanations.
- Use plain language and explain technical terms such as DNS when necessary.
- Never use shame, fear, guilt, exaggerated urgency or guaranteed outcomes.
- Do not claim “100% private”, “impossible to bypass”, “fully secure”, “cures addiction” or “works on every device”.
- Avoid false precision about performance, pricing, availability, user numbers or launch dates.
- Do not publish testimonials, ratings or partner logos without genuine evidence and permission.
- Mark planned capabilities as planned, not available.
- Use the approved forest-green visual system; reserve glass surfaces for short interactive elements, not dense FAQ text.

## 8. Acceptance checklist

- [ ] Homepage FAQ contains no more than six primary questions.
- [ ] Full FAQ covers product purpose, protection, privacy, AI, accountability, recovery, Islamic Mode, availability, pricing, support and device compatibility.
- [ ] Every answer matches the current public build and privacy notice.
- [ ] No planned feature is represented as released.
- [ ] All links resolve to real pages and operational destinations.
- [ ] Keyboard, screen-reader, reduced-motion and mobile behaviour are checked.
- [ ] No analytics, waitlist or contact form is implied to exist before implementation.
- [ ] Legal and privacy review is complete before public launch.

---

**Implementation boundary:** This document defines FAQ content and behaviour only. It does not implement the website, app features, support channel, waitlist, analytics configuration or legal review.


## 8. Homepage implementation record

The homepage FAQ is implemented in `src/components/home/FAQPreview.astro` and rendered from `src/pages/index.astro`. The site header includes an FAQ anchor link.

The six homepage questions cover:
1. What Nūr is.
2. Protection limitations.
3. Local and online data storage.
4. Accountability and browsing-history boundaries.
5. Optional Islamic Mode.
6. Current download/alpha availability.

The component uses native `details` and `summary` disclosures. Multiple answers can remain open; answers are in the HTML and do not require JavaScript. Keyboard focus is visible and reduced-motion preferences are respected.

The availability answer explicitly says the product is still being developed and that no active registration form or confirmed release date is offered on this page.

**Verification pending:** Astro build, rendered browser behaviour, keyboard/screen-reader review, contrast and tap-target checks, and final claim review against the public release. The full FAQ page and remaining detailed questions are not implemented.
