# Nūr Website — Privacy & Trust Section Specification

**Status:** Proposed public copy and disclosure requirements; not implemented  
**Date:** 25 November 2026  
**Website branch:** `feature/website-design-system`  
**App baseline reviewed:** `integration/alpha-readiness` at `055d9cc5d3e8fa0f7bd87fa0fe8defdb819ef9fc`  
**Privacy reconciliation candidate reviewed:** `work/privacy-inventory-reconciliation-2026-11-22` at `0e5b8aadc4f0e7068ac92d32f1b9959baa089589`

## 1. Purpose

Privacy must be a core product explanation, not a decorative promise.

This section should help visitors understand:
- What kinds of information Nūr may handle.
- Which information is stored locally on the device.
- Which features can involve remote services.
- What accountability partners may and may not receive.
- What the user can control.
- What export and deletion currently do—and do not do.

Do not use absolute claims such as "your data never leaves your phone", "we collect nothing", "complete privacy", or "all your data is deleted" unless the exact release architecture and data flows support them.

## 2. Recommended section copy

**Eyebrow:** YOUR DATA. YOUR CHOICES.

**Headline:** Personal growth should not come at the cost of your privacy.

**Supporting copy:**  
Nūr is being built around privacy, transparency and user control. We aim to keep personal activity on your device where practical, explain clearly when a feature uses an online service, and give you meaningful choices about what you share.

**Three principles:**

### Private by design
Personal activity should not be collected just because it can be. Use local processing and storage where practical, and minimise data sent to external services.

### Sharing by choice
Accountability should be deliberate and limited. A trusted person should receive only the information you have chosen to share—not unrestricted access to your device or private activity.

### Clear controls
Understand what is stored, what can be exported, what can be deleted and what requires a separate action with an external service.

This is intended product language. It must be checked against the exact public release build before publication.

## 3. Data handling explanation

### 3.1 Information stored on the device

The inspected app source uses local storage services, including SharedPreferences, for selected app preferences and activity records. Examples include:
- Focus session state and intentions.
- Completed activity and habit records.
- Recovery feedback.
- Protection history and selected protection configuration.
- Islamic Mode preferences and intentions.
- Some accountability cache and activity data.

The exact set of keys changes as features are integrated. The website must not imply this list is complete until the final release inventory has been reconciled across Flutter, Android native storage, SQLite/offline content, notifications and all services.

**Suggested public wording:**  
"Some Nūr settings and activity records are stored locally on your device. The exact information depends on the features you use."

### 3.2 Online services and account data

The inspected integration branch contains Supabase-backed accountability services and related database tables for invitations, partner relationships, events and notifications. Other feature branches contain additional AI consent and processing work, but those changes are not all integrated into the inspected release baseline.

Remote services can involve account identifiers, email addresses, partner details, event records, consent states and other information required to operate a feature.

**Suggested public wording:**  
"Some features may use online services to support accounts or sharing. When they do, Nūr should explain what information is involved and why."

Do not publish a complete list of online data categories or providers until the public release configuration, deployed functions and actual request payloads have been inspected.

### 3.3 Optional AI features

A separate Action Resistance AI implementation branch documents explicit user consent, an optional task/obstacle prompt, server-side consent checking and a Turn off AI control. The privacy/autonomy build notes state that this consent control is not yet integrated into the inspected research/integration branch's Privacy & Data screen.

Do not claim that AI processing is active in the public app, or that all AI data is covered by local deletion, until the feature is integrated and its provider, payload, retention and withdrawal behaviour are verified.

If AI is included in a public release, disclose at minimum:
- What information is sent.
- The purpose of processing.
- Which service provider receives it.
- Whether the user must opt in.
- How consent can be withdrawn.
- Applicable provider retention and deletion limits.

Never send private conversations, Companion memory, reports or faith-related information to AI unless that exact data flow is separately justified, disclosed and explicitly consented to.

## 4. Accountability privacy boundary

The product principle is clear: accountability partners must not receive unrestricted access to browsing history, private conversations or unrelated personal records.

The inspected app screen states that browsing history and private conversations are not shared and that only approved, allowlisted accountability events are exposed. The backend design includes a sanitized shared-events RPC and sharing preferences. However, the complete remote security and two-device lifecycle remains unverified.

**Suggested public wording:**  
"Accountability is intended to share only approved activity that you choose to make available. It is not designed to give another person access to your browsing history or private conversations."

Do not describe the complete partner experience as production-ready until owner, invitee, approved partner, unrelated user and anonymous access tests pass against a disposable Supabase database, including sharing disabled, revocation and post-revocation behaviour.

Do not imply that all accountability sharing is enabled by default.

## 5. Export and deletion: exact boundaries

### 5.1 Current integration baseline

The inspected integration baseline's PrivacyService exports and deletes an explicit set of local Flutter preference keys. The source inventory identifies important omissions in that baseline, including protection history, active Focus session, Tough Hours, accountability cache/events, disable-friction records and prayer records.

The local Privacy screen and service do not provide a complete remote account-data export or account-deletion workflow.

### 5.2 Reconciliation work branch

The newer `work/privacy-inventory-reconciliation-2026-11-22` branch adds missing local personal keys to the export/deletion inventory, separates operational/protection state as export-only, improves partial-deletion reporting and clarifies that native VPN storage and online records are excluded.

This work is documented as authored but not runtime-verified and not merged into the inspected integration baseline. It must not be described as a shipped or verified capability.

### 5.3 Native and remote data boundaries

The Android VPN stores custom blocked domains in a separate native preference namespace. The Flutter PrivacyService does not automatically export or delete that native copy.

Supabase accountability records and Supabase Auth identity are separate from local SharedPreferences deletion. Remote deletion and account deletion require separately authenticated and verified workflows.

Offline Qur'an content/cache is a separate content database and is not equivalent to user-authored activity history. Its clearing and retention need a separate product decision.

**Required public explanation before launch:**  
"Deleting local app data does not automatically delete information held by online services or other device storage. Where separate deletion steps are required, Nūr must explain them clearly."

Do not advertise "Delete all my data" as complete until local Flutter storage, native Android storage, SQLite/cache decisions, notifications, Supabase records, Auth identity, partner relationships and any AI/provider records have a tested and understandable lifecycle.

## 6. Analytics and tracking

The privacy/autonomy build notes state that the analytics preference is stored locally but does not start tracking because no analytics service is connected in that inspected build.

Do not claim "we never use analytics" as a permanent guarantee. For the exact public website and app release:
- Confirm whether any analytics SDK, crash reporting, advertising, attribution, tracking pixel or third-party script is present.
- Document whether collection is enabled by default or requires opt-in.
- Do not introduce website analytics, fingerprinting or tracking cookies without a documented purpose, privacy review and appropriate consent.
- Keep the website's data collection separate from app data.

If no analytics or tracking is connected in the deployed version, state that narrowly and date the statement.

## 7. Website privacy behaviour

The marketing website itself should follow the approved privacy-first specification:
- Static-first delivery.
- No third-party analytics or advertising trackers by default.
- No fingerprinting.
- No cookies unless a later feature genuinely requires them and receives privacy/legal review.
- No personal data collection in the Hold demonstration.
- No storage of personal-path quiz answers without explicit consent.
- Waitlist collection must be a separate, clearly explained opt-in flow, with double opt-in, minimal fields, access controls, retention and unsubscribe/deletion procedures.
- Do not connect the marketing website to the app's personal activity database.

The website privacy notice must describe the actual hosting, server logs, forms, email provider, waitlist database and any other deployed service. Static hosting does not by itself prove that no server logs or provider metadata exist.

## 8. Design and content structure

The homepage Privacy & Trust section should contain:

1. **Privacy principle:** Personal growth should not cost privacy.
2. **Three principles:** Private by design, sharing by choice, clear controls.
3. **Simple data boundary visual:** On-device information versus information that may use an online service.
4. **Accountability boundary:** Only approved, user-authorised events; no unrestricted browsing history or private conversations.
5. **Export/deletion honesty:** Explain local versus native versus remote boundaries.
6. **Link to detailed Privacy Policy:** Only once legal and technical review is complete.

Do not use a generic padlock illustration as proof of security. Avoid claims such as "military-grade encryption", "zero data", "100% secure" or "complete anonymity" unless specifically substantiated.

## 9. Legal and governance requirements

Before public launch:
- Prepare a privacy notice that matches actual app and website data flows.
- Review applicable Nigerian data protection requirements and any other markets where the service will be offered.
- Identify the data controller/organisation and privacy contact.
- Define purposes, lawful basis, data categories, processors, retention, user rights and complaint route.
- Review international transfers and provider terms where applicable.
- Establish incident response and access-control procedures.
- Ensure consent for optional sensitive processing is specific, informed, revocable and not bundled with unrelated features.
- Obtain qualified legal review. This specification is not legal advice or a certification of compliance.

## 10. Claims that must not appear

Do not publish:
- "Your data never leaves your device."
- "We collect absolutely nothing."
- "Your data is always 100% safe."
- "Delete all data permanently" before every relevant storage and provider path is verified.
- "Your accountability partner can see your progress" without defining the exact consented event types and security boundary.
- "AI never sees personal information" unless the actual payload and provider processing prove it.
- "Fully compliant with every privacy law" without qualified legal review.
- Any claim that website privacy guarantees automatically apply to the app, or vice versa.

## 11. Acceptance criteria

The section is ready for public design review when:
1. Copy distinguishes local device storage from online service processing.
2. Accountability sharing boundaries are explained without implying a verified production system.
3. Export/deletion wording accurately describes current release behaviour.
4. AI and analytics statements match the exact deployed release.
5. Website collection is documented separately from app collection.
6. No absolute or unsubstantiated security claims are used.
7. Privacy Policy and contact details are available before collecting personal data.
8. Technical and legal reviewers approve the final copy against the release configuration.
9. The design remains readable, accessible and fast on mobile.

## 12. Evidence reviewed and limitations

App repository: `hassantaiwo866-dotcom/N-r`.

Baseline:
- Branch: `integration/alpha-readiness`
- Commit: `055d9cc5d3e8fa0f7bd87fa0fe8defdb819ef9fc`

Additional candidate evidence:
- Branch: `work/privacy-inventory-reconciliation-2026-11-22`
- Commit: `0e5b8aadc4f0e7068ac92d32f1b9959baa089589`

Documents reviewed:
- `docs/PHASE_0_DATA_STORAGE_INVENTORY.md`
- `docs/PHASE_0_PRIVACY_INVENTORY_RECONCILIATION_20261122.md`
- `docs/PHASE_1_SUPABASE_SECURITY_DATA_LIFECYCLE_AUDIT_20261122.md`
- `docs/PHASE_0_1_COMPLETION_REVIEW_20261122.md`
- `docs/privacy-user-autonomy-build.md`

The audits are primarily static source reviews. The privacy reconciliation branch explicitly says its tests have not been executed. The Supabase review does not establish passing adversarial role-based RLS tests or a complete remote deletion workflow. No claim in this document should be treated as proof of a deployed or independently verified control.

## 13. Implementation status

This file defines proposed website content, privacy boundaries and publication safeguards. It does not implement privacy controls, change app storage, modify Supabase or certify legal compliance. Re-check the current release branch, source, tests, deployed configuration and legal documents before publication.
