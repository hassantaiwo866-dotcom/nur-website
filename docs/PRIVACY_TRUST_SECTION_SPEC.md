# Nūr Website — Privacy & Trust Section Specification

**Status:** Initial homepage implementation committed; build and browser verification pending  
**Date:** 25 November 2026  
**Website branch:** `feature/website-design-system`  
**App baseline reviewed:** `hassantaiwo866-dotcom/N-r`, `integration/alpha-readiness`, commit `055d9cc5d3e8fa0f7bd87fa0fe8defdb819ef9fc`

## 1. Purpose

Privacy must be a core product explanation, not a decorative promise. Explain what may be stored locally, what may involve online services, what accountability is intended to share, and the real boundaries of export and deletion.

Never use absolute claims such as "your data never leaves your phone", "we collect nothing", "complete privacy", or "all your data is deleted" unless the exact release architecture proves them.

## 2. Homepage copy

**Eyebrow:** YOUR DATA. YOUR CHOICES.

**Headline:** Personal growth should not come at the cost of your privacy.

**Supporting copy:** Nūr is being built around privacy, transparency and user control. We aim to keep personal activity on your device where practical, explain clearly when a feature uses an online service, and give you meaningful choices about what you share.

### Three principles

- **Private by design:** Personal activity should not be collected simply because it can be. Use local processing and storage where practical, and minimise data sent to external services.
- **Sharing by choice:** Accountability should be deliberate and limited. A trusted person should receive only information deliberately made available—not unrestricted access to a device or private activity.
- **Clear controls:** Explain what is stored, what can be exported, what can be deleted and what requires a separate action with an external service.

## 3. Data location explanation

The inspected integration branch uses local storage services, including SharedPreferences, for selected app preferences and activity records. Examples include Focus session state and intentions, completed activity and habit records, recovery feedback, selected protection configuration, and optional Islamic Mode preferences.

The source inventory also identifies Android-native protection preferences, operational metadata, local notification state and an offline Qur'an content database. The website's examples are intentionally illustrative, not exhaustive.

**Approved wording:** "Some Nūr settings and activity records are stored locally on your device. The exact information depends on the features you use."

The inspected integration includes Supabase-backed accountability services and tables for invitations, partner relationships, events and notifications. Remote services can involve account identifiers, email addresses, partner details, event records and consent/sharing state.

**Approved wording:** "Some features may use online services to support accounts or sharing. When they do, Nūr should explain what information is involved and why."

Do not publish a complete provider or remote-data list until the public release configuration, deployed functions and actual request payloads have been inspected.

## 4. Accountability boundary

The product principle is that accountability partners must not receive unrestricted access to browsing history, private conversations or unrelated personal records. The inspected app screen and backend design describe approved/allowlisted shared events and sharing preferences.

**Approved wording:** "Accountability is intended to share only approved activity that you choose to make available. It is not designed to give another person access to your browsing history or private conversations."

The complete remote security and two-device lifecycle remain unverified. Do not describe the complete partner experience as production-ready until owner, invitee, approved partner, unrelated user and anonymous access tests pass against a disposable Supabase database, including sharing disabled, revocation and post-revocation behaviour.

## 5. Export and deletion limits

The inspected integration baseline's `PrivacyService` exports and deletes an explicit set of local Flutter preference keys. The source inventory identifies omissions in that baseline, including protection history, active Focus session, Tough Hours, accountability cache/events, disable-friction records and prayer records.

A separate reconciliation branch proposes broader local export/deletion coverage, but it is not the inspected integration baseline and was not runtime-verified in the source review. Do not describe that work as shipped.

The current local Privacy screen/service does not provide a complete remote account-data export or account-deletion workflow. Android VPN custom-domain preferences are stored in a separate native preference namespace. Supabase accountability records and Supabase Auth identity are separate from local SharedPreferences deletion. Offline Qur'an content/cache is also a separate content database.

**Required public explanation:** "Deleting local app data does not automatically delete information held by online services or other device storage. Where separate deletion steps are required, Nūr must explain them clearly."

Do not advertise "Delete all my data" as complete until local Flutter storage, native Android storage, SQLite/cache decisions, notifications, Supabase records, Auth identity, partner relationships and any AI/provider records have a tested lifecycle.

## 6. AI and analytics

Do not claim AI processing is active in the public app, or that all AI data is covered by local deletion, until the feature is integrated and its provider, payload, retention and withdrawal behaviour are verified. If AI is included, disclose information sent, purpose, provider, opt-in requirements, withdrawal and retention/deletion limits.

Do not claim "we never use analytics" as a permanent guarantee. Confirm SDKs, crash reporting, advertising, attribution, tracking pixels and third-party scripts for the exact release. The website implementation should not introduce analytics, fingerprinting or tracking cookies without a documented purpose, privacy review and appropriate consent.

## 7. Visual and interaction direction

- Use clean, solid surfaces for long-form privacy information.
- Use concise principles, a local/online comparison and a clear accountability boundary.
- No decorative privacy seals, absolute guarantees or unsupported compliance badges.
- Keep the content static and readable without JavaScript.
- Maintain responsive layouts, keyboard accessibility, visible focus and WCAG 2.2 AA contrast.
- Do not collect visitor data in this section.

## 8. Acceptance criteria

- [x] Three privacy principles explained.
- [x] Local and online data categories distinguished with examples.
- [x] Examples explicitly described as non-exhaustive.
- [x] Accountability sharing principle and verification limitation disclosed.
- [x] Local export/deletion limitations explained.
- [x] AI and analytics claims kept within evidence.
- [x] Static responsive homepage component implemented.
- [ ] Build and browser rendering verified.
- [ ] Accessibility and contrast checks completed.
- [ ] Exact public release inventory and legal copy reviewed before launch.

## 9. Implementation

Implemented in `src/components/home/PrivacyTrust.astro` and imported into `src/pages/index.astro` after the feature grid. The section uses static Astro markup and CSS; it adds no client script, analytics or visitor-data collection. Build, browser and device verification remain pending.
