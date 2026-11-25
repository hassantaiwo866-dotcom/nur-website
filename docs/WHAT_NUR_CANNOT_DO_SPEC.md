# Nūr Website — What Nūr Cannot Do

**Status:** Proposed public-facing content and claim boundaries; not implemented  
**Date:** 25 November 2026  
**Website branch:** `feature/website-design-system`  
**App baseline reviewed:** `integration/alpha-readiness` at `055d9cc5d3e8fa0f7bd87fa0fe8defdb819ef9fc`

## 1. Purpose

Nūr should be clear about its limits. It is a tool for supporting self-control, attention, intentional action and personal growth. It is not a substitute for personal judgement, professional care, trusted human support or the user's own decisions.

This page is not an apology for the product. It is part of the product's trust model: explain what Nūr can help with, what it cannot promise, and where responsibility or support must come from elsewhere.

Use plain language. Do not frighten, shame, moralise or make a person feel defective for needing support.

## 2. Recommended public copy

**Eyebrow:** HONEST BY DESIGN

**Headline:** Nūr can support your choices. It cannot make them for you.

**Introduction:**  
Nūr is designed to help you protect your attention, pause before acting, recover after difficult moments and build more intentional routines. It can offer structure and support, but it cannot guarantee outcomes or take the place of your own judgement.

### Nūr cannot guarantee that you will never encounter unwanted content

Protection depends on the device, operating system, network, browser, app and technical paths available. Some traffic and bypass methods may not be covered. Nūr should show its actual protection state and explain limitations rather than promise perfect blocking.

### Nūr cannot make every decision for you

Nūr can help you pause, reflect and choose a next step. It cannot replace your judgement, values or responsibility. You remain in control of the actions you take and the support you choose to use.

### Nūr is not therapy or medical care

Nūr is not a mental-health diagnosis tool, therapist, doctor or emergency service. It does not diagnose or treat addiction, depression, anxiety or any other condition. Its exercises and reflections are general self-support tools, not clinical treatment.

If you are distressed, feel unsafe, or need help beyond what an app can provide, contact a qualified professional or a trusted person. If there is immediate danger, contact local emergency services.

### Nūr cannot erase a difficult moment

A lapse or setback does not erase the effort you have made. Nūr can help you consider a next step, but it cannot change what happened or promise that it will not happen again. You do not owe the app an explanation.

### Nūr is not a religious authority

Islamic Mode is an optional support experience for users who choose it. Nūr does not issue fatwas, replace qualified scholars, or decide what is religiously correct for you. Users should consult knowledgeable and trusted religious authorities for personal religious rulings.

### Nūr cannot promise complete privacy or perfect security

We aim to minimise data collection, explain when features use online services and give users meaningful controls. But no connected app or online service can honestly promise absolute security. Local deletion may not delete information held separately by online services, native device storage or providers.

### Nūr cannot make another person trustworthy

Accountability features are intended to support consent-based sharing, not surveillance. Nūr cannot guarantee that another person will respond well, keep information confidential or provide appropriate support. Only share information with someone you trust, and use available controls to review or revoke sharing.

### Nūr cannot replace real-world support

An app can be useful, but it is not a substitute for healthy relationships, community, professional help, rest, meaningful activity or practical changes in your environment.

## 3. Protection: precise technical boundaries

The inspected integration baseline and protection audits describe Nūr Shield as a DNS-focused filtering foundation with configured exact-IP rules—not a full-device content firewall.

The current documented limitations include:
- Not all device traffic is routed through or inspected by the current DNS-focused engine.
- Direct-IP website traffic is not comprehensively filtered by the current architecture.
- DNS-over-HTTPS and DNS-over-TLS are not comprehensively blocked across all providers and endpoints.
- IPv6 handling is partial and does not establish complete IPv6 leak prevention.
- Android Always-on VPN and system lockdown are not currently enabled by Nūr's inspected baseline.
- Network changes, process termination, reboot, permission revocation, OEM behaviour and competing VPNs require physical-device validation.
- A running VPN packet loop does not mean all device traffic is protected.

**Safe public wording:**  
"Nūr Shield can help filter supported website and DNS requests. Its coverage depends on your device and network settings, and some routes may not be covered. We show protection status as accurately as the platform allows."

Do not claim:
- Unbreakable, bypass-proof or complete blocking.
- Guaranteed blocking of all explicit content across every app and browser.
- Full-device firewall or full traffic inspection.
- Guaranteed protection on every network.
- A working kill switch unless the exact release supports and verifies it.

The protection architecture and supported coverage must be re-audited against the release branch before this copy is published. A source audit is not a physical-device certification.

## 4. Personal growth and recovery boundaries

Nūr can provide prompts, guided actions, optional reflections, Focus sessions and activity records where those features are implemented. It cannot:
- Guarantee a particular habit, outcome, recovery timeline or level of self-control.
- Determine the cause of a person's behaviour from limited app activity.
- Know everything happening in a person's life.
- Treat a lapse as proof of failure or lack of character.
- Require a user to disclose why something happened.
- Replace the user's own goals with an algorithm's priorities.

Avoid medicalised or deterministic language such as "cure", "treatment", "clinically proven" or "guaranteed recovery" unless an appropriate evidence base and regulatory review genuinely support the exact claim.

Do not imply that every planned activity, adaptive suggestion or intelligence feature is already available. Only describe functions that exist in the current public release.

## 5. AI boundaries

AI-related capabilities must remain optional and clearly disclosed where they are included. AI can produce inaccurate, incomplete, unsuitable or context-insensitive suggestions. It does not know the user's full circumstances and must not be presented as a therapist, scholar, emergency responder or final authority.

Before describing an AI feature publicly, verify the release implementation and disclose:
- Whether AI is present in that release.
- What exact input is sent and why.
- Which provider processes it.
- Whether consent is required and how to withdraw it.
- What data is excluded from the request.
- What provider retention and deletion terms apply.

Do not claim that AI is integrated, available to every user, or processes no personal data based solely on a separate development branch. Do not imply that turning off AI deletes records already held by a provider.

## 6. Accountability boundaries

Accountability is meant to be chosen by the user and limited to defined information. It is not a monitoring product.

Nūr cannot guarantee that:
- A partner will be available, supportive or discreet.
- A partner will interpret shared information correctly.
- Every invitation, approval, revocation or deletion will succeed until the complete lifecycle has been tested.
- A partner will never misuse information they have legitimately received.

The intended product boundary is that partners do not receive unrestricted browsing history or private conversations. The inspected backend design uses approved sharing settings and a sanitized event path, but the full two-device lifecycle and adversarial access-control tests remain incomplete.

Do not market accountability as fully production-ready until the relevant owner, invitee, partner, unrelated-user and anonymous-access tests pass, including revocation and post-revocation access.

## 7. Faith and Islamic Mode boundaries

Islamic Mode is optional. Nūr is not exclusively for Muslims and must not imply that every user should enable it.

Nūr can offer user-selected faith-related intentions or supportive features where implemented. It cannot:
- Issue fatwas or settle scholarly differences.
- Claim religious authority.
- Judge a person's faith or worth.
- Replace Qur'an study with generated religious rulings.
- Present a particular madhhab or interpretation as universal unless explicitly and accurately scoped.

Keep faith support respectful, transparent and user-controlled. Do not use guilt or fear to drive engagement.

## 8. Privacy and security boundaries

Use this page together with the Privacy & Trust section and the detailed Privacy Policy. Do not repeat a simplified promise that contradicts the data inventory.

At the time of the source review:
- The integration baseline has local export/deletion functionality for an explicit set of Flutter preference keys.
- A separate privacy reconciliation branch adds missing local keys and clearer partial-deletion reporting, but its tests were not executed and it was not merged into the inspected integration baseline.
- Native Android VPN preferences are separate from Flutter preference storage.
- Supabase account and accountability records are not automatically deleted by local preference deletion.
- A complete remote account export/deletion workflow was not verified.
- Local deletion is not a guarantee of erasure from external AI or other providers.

Do not state that "Delete all data" removes every record unless every applicable storage location and provider lifecycle has been tested.

## 9. Suggested page structure

1. Hero: "Nūr can support your choices. It cannot make them for you."
2. Short introduction: useful support, not a guarantee.
3. Six to eight concise limit cards:
   - No guaranteed blocking.
   - No guaranteed outcomes.
   - Not therapy or medical care.
   - Not a religious authority.
   - No absolute privacy/security promise.
   - Accountability is not surveillance.
   - AI is not an authority.
   - Not a replacement for real-world support.
4. A short "What Nūr is here to do" section to rebalance the page: help users pause, protect attention, recover without shame, and build intentional routines.
5. Links to Privacy & Trust, Help & Safety, and the Privacy Policy when those pages are ready.

Use the approved visual system: deep forest green, calm light, refined serif headings and restrained glass cards. Keep the copy readable and calm. Do not use warning-red styling or alarming imagery for ordinary product limitations.

## 10. Content rules

- Say "can help", "is designed to support" and "where supported" when outcomes depend on conditions.
- Explain the relevant limitation beside the feature claim, not only in a distant disclaimer.
- Do not describe planned features as available.
- Do not use shame, blame, fear or moral judgement.
- Do not imply that a person has failed because they need support.
- Do not make clinical, religious, security or legal guarantees.
- Keep the page useful, not defensive. Every limitation should help the user make an informed decision.

## 11. Publication checklist

Before publishing:
- Re-check the current app release branch, relevant source, tests and CI.
- Re-check the current protection architecture and supported-device matrix.
- Confirm which Focus, Recovery, Insights, Accountability, Islamic Mode and AI features are actually in the release.
- Confirm the current privacy/export/deletion implementation and remote data lifecycle.
- Verify that any professional-support language and emergency guidance is appropriate for the countries served.
- Obtain legal review for health-related positioning and applicable consumer-protection requirements.
- Have product and technical reviewers approve each claim against evidence.
- Review the page on low-end Android devices, with reduced motion and accessible contrast.

## 12. Evidence reviewed and limitations

App repository: `hassantaiwo866-dotcom/N-r`.

Baseline:
- Branch: `integration/alpha-readiness`
- Commit: `055d9cc5d3e8fa0f7bd87fa0fe8defdb819ef9fc`

Documents reviewed:
- `docs/NUR_BUILD_ROADMAP.md`
- `docs/PROTECTION_SECURITY_AUDIT.md`
- `docs/protection/p4-hardening-assessment.md`
- `docs/lapse-recovery-build.md`
- `docs/privacy-user-autonomy-build.md`

The roadmap explicitly separates planned work from implemented work and requires protection claims to match tested behaviour. Protection audits are source-level assessments and state that runtime/physical-device verification remains necessary. Recovery and privacy notes also record pending automated validation. This document is therefore a proposed website content specification, not a certification of current product capability.

## 13. Implementation status

This file defines public-facing content and claim boundaries. It does not change app behaviour, provide medical or legal advice, or certify security. Re-check the exact public release before publishing.
