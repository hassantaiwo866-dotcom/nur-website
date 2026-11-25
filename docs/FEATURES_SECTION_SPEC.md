# Nūr Website — Features Section Specification

**Status:** Proposed content and product-claim boundaries; not implemented  
**Date:** 25 November 2026  
**Website branch:** `feature/website-design-system`  
**App evidence reviewed:** `integration/alpha-readiness` at `055d9cc5d3e8fa0f7bd87fa0fe8defdb819ef9fc`

## 1. Purpose

Introduce the main areas of Nūr without turning the homepage into a long feature catalogue.

The section should communicate that Nūr combines protection, intentional focus, recovery and personal growth. Each feature must be presented honestly according to the evidence in the app repository.

This is a website content specification. It does not implement app features or establish that the app is ready for public release.

## 2. Recommended section introduction

**Eyebrow:** ONE SYSTEM. DIFFERENT KINDS OF SUPPORT.

**Headline:** The tools to protect your attention—and build beyond it.

**Supporting copy:**  
Nūr brings together tools for protection, focus, recovery and reflection. Use the parts that help you. Your progress remains yours to shape.

Avoid describing every tool as fully available until the current app build and release scope are confirmed.

## 3. Feature cards and evidence boundaries

### 3.1 Nūr Shield — Protection

**Visitor-facing headline:** Create stronger boundaries around your attention.

**Proposed description:**  
Nūr's protection system is being developed to help limit access to selected websites and support more intentional use of your device.

**Evidence classification:** Partially implemented foundation; reliability and platform limitations remain.

**Evidence reviewed:**
- Flutter protection screens, services, history and health/recovery services exist in the inspected integration branch.
- The protection security audit describes a DNS-focused filter with configured exact-IP blocking.
- Native VPN and Flutter protection tests exist.
- The audit does not establish successful builds, complete test execution or physical-device reliability.

**Do not claim:**
- Unbreakable or impossible-to-bypass protection.
- Complete adult-content blocking or full-device content inspection.
- Universal blocking across DoH, DoT, every browser, app, network and resolver.
- Full IPv6 enforcement.
- Protection is active when the app cannot verify its actual state.

**Publication status:** May be described as an area under active development. Before presenting it as a dependable released feature, verify the release build, current tests, Android device behaviour and known bypass limitations.

### 3.2 Focus

**Visitor-facing headline:** Give your attention somewhere meaningful to go.

**Proposed description:**  
Set an intention, choose a session length and make time for the task in front of you. Nūr includes a Focus session foundation with session state and history.

**Evidence classification:** Implemented foundation; verify the complete release flow.

**Evidence reviewed:**
- Focus screen and Focus session service exist.
- Active sessions are stored locally and can be restored.
- Session intention is persisted and retained through pause/resume.
- Tests cover optional intentions, restoration, pause/resume and completed activity recording.

**Do not claim:**
- Every planned study/deep-work mode is available.
- AI automatically selects ideal session lengths.
- All notification, interruption and cross-device behaviour is complete.
- Focus guarantees productivity.

**Publication status:** Suitable for a carefully qualified description after confirming the current alpha build contains the relevant screen and flow.

### 3.3 Reset and Recovery

**Visitor-facing headline:** When a moment goes differently than planned, begin again without shame.

**Proposed description:**  
Nūr includes recovery activities and an optional way to reflect on whether an activity helped. A difficult moment does not have to become a reason to give up.

**Evidence classification:** Implemented foundation; broader recovery journey remains planned.

**Evidence reviewed:**
- Recovery screen and completion flow exist.
- Completed recovery activity can be recorded.
- Optional recovery-effectiveness feedback is stored locally.
- Tests cover saving feedback, skipping it and keeping recovery feedback separate from Focus completion.

**Do not claim:**
- Recovery is clinical treatment or therapy.
- Nūr diagnoses, cures or guarantees recovery from a condition.
- The complete planned Reset library or adaptive intervention system is available.
- A lapse automatically triggers a fully validated personalised response.

**Publication status:** Can describe the current recovery activity and optional feedback foundation once confirmed in the alpha build. Describe broader recovery capabilities as being developed.

### 3.4 Insights and Growth

**Visitor-facing headline:** Notice what is helping you move forward.

**Proposed description:**  
Nūr brings together recorded Focus, recovery, habit and protection activity to help you review patterns over time. The aim is reflection—not judgement.

**Evidence classification:** Implemented local reporting foundation; comprehensive behavioural intelligence is not established.

**Evidence reviewed:**
- Insights screen and service exist.
- The service builds reports from on-device activity, habit and protection history.
- Tests cover persistence and deduplication of Focus, recovery and Shield events.
- The inspected screen explicitly notes that phone unlocks, app opens and intervention outcomes need further reliable telemetry.
- Recovery frequency and protected time are presented neutrally; more or less is not automatically treated as better.

**Do not claim:**
- Complete monitoring of phone use or every digital behaviour.
- A mature Personal Resistance Profile or fully adaptive AI.
- That correlation proves why a person behaved in a particular way.
- Comprehensive or clinically validated behavioural analysis.

**Publication status:** Suitable for a qualified explanation of current recorded activity and local reporting, after checking the current build.

### 3.5 Accountability

**Visitor-facing headline:** Invite support without giving up your privacy.

**Proposed description:**  
Nūr is designed to let you involve a trusted person through deliberate, user-controlled sharing. Accountability is intended to support you—not monitor everything you do.

**Evidence classification:** Local and cloud implementation foundations exist; end-to-end security and two-device readiness are not established.

**Evidence reviewed:**
- Accountability models, screens, local service and history exist.
- The inspected service includes Supabase invitation, partner relationship, sharing preference and event operations.
- Supabase migrations and access-control work exist.
- The Phase 0 data inventory identifies unresolved remote deletion and RLS policy concerns, including owner event deletion and invitation state-transition issues.
- The implementation audit says the local foundation does not prove a secure, complete two-device workflow.

**Do not claim:**
- A fully verified accountability system is ready for general use.
- Partners can see browsing history, private conversations or unrestricted activity.
- Every remote access-control, invitation, revocation, export and deletion path is complete.
- Sharing is enabled by default or mandatory.

**Publication status:** Explain the privacy principle and planned user-controlled approach. Do not promote the live partner workflow as production-ready until security fixes and adversarial two-account tests are verified.

### 3.6 Optional Islamic Mode

**Visitor-facing headline:** Make room for faith, if you choose.

**Proposed description:**  
Islamic Mode is an optional part of Nūr for people who want their personal growth experience to include faith-oriented intentions and carefully sourced Islamic content.

**Evidence classification:** Optional local settings and intention foundation implemented; content and experience scope must be checked before making broader claims.

**Evidence reviewed:**
- Islamic Mode is disabled by default.
- Enabled state and selected intention are stored locally.
- Tests cover saving/reloading the profile and enabling/disabling the mode.
- Islamic content and source models/services and content tests exist.
- The product roadmap requires verified sources, no assumed madhhab, and no guilt-based religious recovery.

**Do not claim:**
- Nūr is a religious authority, mufti or source of independent fatwas.
- AI can authoritatively interpret the Qur'an or issue religious rulings.
- Every prayer, Qur'an, dhikr, du'a or learning flow in the wider vision is already available.
- Islamic Mode is required to use Nūr or defines the whole product.

**Publication status:** May be described as optional. List specific content only after reviewing the exact sources and flows included in the public alpha build.

## 4. What belongs in the first homepage feature section

Use six concise cards, in this order:

1. Shield — Protection
2. Focus
3. Reset — Recovery
4. Insights — Growth
5. Accountability
6. Islamic Mode — Optional

Each card should contain:
- A short title.
- One clear benefit-oriented sentence.
- A restrained abstract visual or verified app screenshot.
- A link to a detailed feature page only when that page exists.

Do not add status badges to every card in the visual design. Instead, use careful copy and a separate, readable availability note where needed.

## 5. Availability language

Use a small, plain-language note below the cards:

"Some Nūr features are still being developed and tested. Availability may vary during the closed alpha. We'll be clear about what is ready, what is limited and what is still on the way."

Do not publish a feature-by-feature release status until the alpha scope and supported app build are fixed.

## 6. Visual direction

Follow `docs/DESIGN_SYSTEM.md`.

- Use a balanced grid on desktop and a readable stacked or two-column layout on mobile.
- Glass treatment may be used on feature cards, but keep it restrained.
- Use original abstract motifs or verified screenshots only.
- Do not fabricate app screens or imply a planned interface is currently available.
- Give each card a distinct but consistent icon or simple visual motif.
- Avoid dashboard-like metrics, scores, streaks and gamified badges.
- Keep copy concise and readable on mid-range Android devices.
- Provide solid surface fallbacks and accessible contrast in both themes.

## 7. Privacy and trust

- Never imply that accountability partners can see browsing history or private conversations.
- Distinguish local activity history from cloud-synced data.
- Do not claim complete export/deletion until the app's local and remote data paths are reconciled and tested.
- Do not imply the website collects app activity.
- Do not use feature cards to imply consent to share sensitive recovery or religious-practice data.
- Keep Islamic Mode optional and faith-sensitive.

## 8. Acceptance criteria

The section is ready for design review when:

1. All six cards explain a clear user benefit without exaggerated claims.
2. Feature maturity is accurately represented in the underlying copy and availability note.
3. Protection limitations are not hidden behind broad claims.
4. Accountability is not described as production-ready before security and two-device verification.
5. Insights are described as local recorded activity, not comprehensive monitoring or mature AI.
6. Islamic Mode is explicitly optional and content claims are source-checked.
7. No fake screenshots, testimonials, metrics or availability claims are used.
8. Desktop and mobile layouts are readable and accessible.
9. The section remains useful without animation or JavaScript.

## 9. Evidence sources reviewed

App repository: `hassantaiwo866-dotcom/N-r`, branch `integration/alpha-readiness`, commit `055d9cc5d3e8fa0f7bd87fa0fe8defdb819ef9fc`.

Documentation:
- `docs/NUR_BUILD_ROADMAP.md`
- `docs/NUR_GITHUB_IMPLEMENTATION_AUDIT.md`
- `docs/PROTECTION_SECURITY_AUDIT.md`
- `docs/PHASE_0_DATA_STORAGE_INVENTORY.md`
- `docs/NUR_COMPLETE_PRODUCT_VISION_AND_BUILD_ROADMAP.md`

Relevant inspected source and tests:
- Focus: `lib/screens/focus_screen.dart`, `lib/services/focus_session_service.dart`, `test/focus_intention_test.dart`
- Recovery: `lib/screens/recovery_screen.dart`, `lib/services/recovery_feedback_service.dart`, `test/recovery_acceptance_test.dart`, `test/recovery_feedback_test.dart`
- Insights: `lib/screens/insights_screen.dart`, `lib/services/insights_service.dart`, `test/insights_data_persistence_test.dart`
- Accountability: `lib/screens/accountability_partner_screen.dart`, `lib/services/accountability_service.dart`, Supabase migrations and Phase 0 inventory
- Islamic Mode: `lib/services/islamic_mode_service.dart`, `test/islamic_mode_test.dart`, Islamic content models/services and tests
- Protection: `lib/screens/protection_screen.dart`, `lib/screens/nur_shield_screen.dart`, protection services, tests and security audit

The inspected commit and tests are repository evidence, not proof that the current app builds or passes all tests. Re-check the current release candidate and CI before publication.

## 10. Implementation status

This document records proposed website copy and claim boundaries only. No website feature cards, screenshots or app functionality have been changed or implemented by this specification.
