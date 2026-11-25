# Nūr Website — Homepage Feature Grid

**Status:** Initial implementation committed; browser/build verification pending  
**Date:** 25 November 2026  
**Website branch:** `feature/website-design-system`  
**App evidence reviewed:** `hassantaiwo866-dotcom/N-r`, branch `integration/alpha-readiness`, commit `055d9cc5d3e8fa0f7bd87fa0fe8defdb819ef9fc`

## Purpose and message

Introduce six areas of support without implying every planned capability is production-ready.

**Headline:** The tools to protect your attention—and build beyond it.

**Supporting copy:** Nūr brings together tools for protection, focus, recovery and reflection. Use the parts that help you. Your progress remains yours to shape.

## Six feature cards and evidence boundaries

1. **Nūr Shield — Protection.** The website says the protection system is being developed to help limit access to selected websites. The app contains a DNS-focused filtering foundation and native VPN work, but this is not a full-device firewall or guaranteed bypass-proof adult-content blocking. Physical-device reliability and transport coverage remain limitations. Do not claim unbreakable protection.
2. **Focus.** The website describes setting an intention, choosing a session length and making time for a task. The inspected app service persists/restores sessions and optional intentions; tests cover restoration, pause/resume and activity recording. Do not claim guaranteed productivity or every planned Focus mode.
3. **Reset & Recovery.** The website describes recovery activities and optional helpfulness feedback. The inspected app flow records completed recovery activity and permits feedback to be saved or skipped. Do not describe this as therapy, clinical treatment or a complete adaptive recovery journey.
4. **Insights & Growth.** The website describes reviewing recorded Focus, recovery and growth activity. The app contains local reporting foundations. Do not imply complete phone monitoring, comprehensive behavioural analysis or mature adaptive AI.
5. **Accountability.** The website describes the intended user-controlled sharing principle, while explicitly stating that the complete two-person experience and security need verification. App service and Supabase paths exist, but this does not prove a secure two-device workflow. Do not market it as production-ready or imply partners see browsing history.
6. **Islamic Mode — Optional.** The website describes an optional space for faith-oriented intentions and carefully sourced content. The inspected service stores enabled state and intentions locally; tests cover persistence and enable/disable behaviour. Do not present Nūr as a mufti, religious authority or Qur'an interpreter. Never imply Islamic Mode is required.

## Availability note

Use this clear note below the cards:

"Some Nūr features are still being developed and tested. Availability may vary during the closed alpha. We'll be clear about what is ready, what is limited and what is still on the way."

Do not publish a feature-by-feature release status until the alpha scope and supported app build are fixed.

## Visual and accessibility direction

- Six cards: three columns on wide screens, two on medium screens, one on narrow mobile.
- Restrained glass surface with a solid readable fallback.
- Abstract CSS symbols only; no fabricated screenshots or metrics.
- No status-badge clutter, streaks, scores or gamification.
- Static content; no JavaScript or visitor data collection required.
- Maintain accessible contrast and readable type at narrow widths.

## Acceptance criteria

- [x] Six feature areas included in the agreed order.
- [x] Copy uses qualified claims aligned to inspected implementation evidence.
- [x] Protection, accountability, insights and Islamic Mode limitations are explicit.
- [x] Optional Islamic Mode is not positioned as defining all of Nūr.
- [x] Responsive grid authored.
- [x] No fabricated screenshots, testimonials, metrics or working signup.
- [ ] Build, browser, contrast and real-device checks completed.

## Evidence inspected

App repository branch and commit above; relevant documentation:
- `docs/NUR_BUILD_ROADMAP.md`
- `docs/NUR_GITHUB_IMPLEMENTATION_AUDIT.md`
- `docs/PROTECTION_SECURITY_AUDIT.md`
- `docs/PHASE_0_DATA_STORAGE_INVENTORY.md`

Relevant source and tests:
- `lib/services/focus_session_service.dart`, `test/focus_intention_test.dart`
- `lib/services/recovery_feedback_service.dart`, `test/recovery_feedback_test.dart`
- `lib/services/accountability_service.dart`
- `lib/services/islamic_mode_service.dart`, `test/islamic_mode_test.dart`
- Insights service and local activity reporting implementation.

This is a website content/implementation review, not a claim that app CI or tests were run in this task.
