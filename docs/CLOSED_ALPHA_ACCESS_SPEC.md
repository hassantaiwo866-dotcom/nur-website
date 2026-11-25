# Nūr Website — Closed Alpha Access Specification

**Status:** Proposed access flow; closed-state status copy implemented on homepage; request flow not implemented
**Date:** 25 November 2026
**Website branch:** `feature/website-design-system`
**App baseline checked:** `integration/alpha-readiness` at `055d9cc5d3e8fa0f7bd87fa0fe8defdb819ef9fc`

---

## 1. Purpose and release boundary

The Join Alpha journey should let interested people request consideration for a limited early release without implying that access is immediate, guaranteed or currently open.

This document specifies the experience and backend requirements. It does **not** mean a waitlist, registration form, email service, invitation system or app distribution channel currently exists.

Until the complete flow is implemented, tested and approved:
- Do not display an active submission form.
- Do not collect email addresses through an improvised contact form, public issue, social-media comment or direct message.
- Do not describe the alpha as open.
- Use a non-interactive status message such as: **“Nūr is in development. Closed-alpha access details will be announced here when applications open.”**
- A CTA may link to a clearly marked updates page only if that destination exists and does not collect data unexpectedly.

## 2. Recommended alpha policy

### Audience

For the first closed alpha, the recommended policy is **adults aged 18 or older only**. The app is intended to handle sensitive personal routines and protection settings; an adult-only pilot reduces the complexity of consent, safeguarding and data handling while the product is immature.

This is a proposed product policy, not a statement of legal compliance. Confirm it with qualified legal advice for Nigeria and any other launch market before collecting applications. Do not ask for date of birth or identity documents merely to verify age; use a minimal age-eligibility confirmation and define a proportionate verification process if legally required.

### Access model

- Requesting access is not acceptance.
- Alpha places may be limited by device compatibility, support capacity and test objectives.
- Invitations are issued in controlled batches.
- A person may decline an invitation without penalty.
- Access can be paused if a serious safety, security or reliability issue is found.
- Alpha software may contain bugs, incomplete features and data-loss risks; explain these before installation.
- Do not charge for alpha access unless a separate, reviewed paid-pilot policy is explicitly approved.

## 3. Proposed page copy

**Eyebrow:** EARLY ACCESS

**Headline:** Help shape what Nūr becomes.

**Body:**
Nūr is being built to help people protect their attention, practise self-control and keep growing without shame. The closed alpha will be a small, carefully supported opportunity to try early versions, report problems and help us understand what needs to improve.

**Status while applications are closed:**
Nūr is still in development. Closed-alpha applications are not open yet. We will publish the access process here when the experience is ready.

**Status when applications are open:**
Applications are open for a limited test group. Sending a request does not guarantee an invitation. We will contact you only about your request and the alpha process, in line with the privacy notice.

**CTA while closed:** Alpha updates
Only show if an actual, privacy-reviewed updates channel exists. Otherwise show no button.

**CTA while open:** Request alpha access

Avoid “Join now”, “Get instant access” or “Download now” unless that action truly works.

## 4. Application form — minimum data

When the backend is ready, keep the form short.

Required fields:
1. **Email address** — used for verification and alpha-related contact.
2. **Age eligibility** — checkbox confirming the applicant is 18 or older.
3. **Privacy notice acknowledgement** — explicit acknowledgement that the applicant has read the relevant notice.

Optional field:
- **Country or region** — only if it materially helps determine device support, legal availability or test logistics. Prefer a short country selector; do not request a street address.

Do not collect in the initial application:
- Full name, phone number, date of birth or identity documents.
- Sexual history, explicit-content use, addiction history or other intimate disclosures.
- Religious affiliation or Islamic Mode preference.
- Detailed health, mental-health or diagnostic information.
- Contacts, social handles, browsing history or app usage records.
- Free-text “tell us your struggle” answers.
- Accountability partner details.

If a later research study genuinely needs additional information, make it a separate optional consent flow with a clear purpose, data scope and retention period. Never make sensitive disclosure a condition of alpha access.

## 5. Consent and email verification

The application must distinguish:
- **Request processing:** permission to use the email address to process the alpha request and send necessary status messages.
- **Optional product updates:** separate, unchecked consent for occasional product news beyond the request itself.

Do not bundle marketing consent with the access request. Refusing optional updates must not reduce alpha eligibility.

Recommended flow:
1. Applicant completes the minimal form and submits over HTTPS.
2. Server validates and rate-limits the request.
3. Server stores a pending, unverified request.
4. A verification email is sent with a single-use, expiring token.
5. Applicant verifies the address.
6. The application enters the review queue.
7. The applicant receives an outcome only when a decision is made.
8. Invitation emails contain an expiry date and a safe, official next step.
9. Every optional marketing email includes a working unsubscribe mechanism.

Do not expose whether an email address is already on the list in a way that enables account or membership enumeration. Use a neutral confirmation response.

## 6. Submission and confirmation copy

**Form helper:**
We only need the information required to process your request. Please do not include personal or sensitive details about your habits or experiences.

**Submit button:** Send access request

**Neutral success state:**
If the address can receive mail, a verification message will be sent shortly. Check your inbox and spam folder. If you requested access before, follow the latest message you received.

**Verified state:**
Your email is verified. Your request can now be considered for a future alpha group. Verification does not guarantee an invitation.

**Waitlist/full state:**
Requests are currently paused while we support the existing test group. We will update this page when the next application window is confirmed.

**Decline state:**
Thank you for your interest. We are not able to offer you a place in this test group. This is not a judgement about you or your goals. You may apply again if a future application window is announced.

Do not disclose internal screening scores or sensitive inferences.

## 7. Invitation and onboarding

An invitation should explain:
- That this is an early test build, not a finished product.
- Supported operating systems and minimum versions, based on verified testing.
- Known limitations, especially protection reliability and incomplete features.
- Installation source and how to verify it is official.
- What feedback is useful and where to send it.
- How to report a security or privacy concern.
- How to leave the alpha and request deletion of application information.
- Whether any separate research activity is optional.

Do not ask alpha users to disable Android security settings or install an APK from an unverified mirror. Provide checksums or signed distribution details where appropriate and technically available.

Alpha feedback must be optional. Do not require participants to disclose intimate behaviour or submit screenshots containing personal information.

## 8. Backend and security requirements

The waitlist must be a separate service from the Nūr app's user-data systems.

Required controls before launch:
- Dedicated database/project or clearly isolated schema and credentials.
- Server-side validation; never trust client-side checks alone.
- HTTPS for all submissions and verification links.
- Rate limiting and abuse protection that does not rely on invasive tracking or fingerprinting.
- Email verification tokens stored securely (hash tokens at rest where practical), single-use and expiring.
- Least-privilege service credentials; no secrets in browser JavaScript or public repository files.
- Row-level access controls or equivalent server-side authorisation for every administrative read/write path.
- No public endpoint that lists applicants or reveals whether a specific email is registered.
- Admin access restricted to named, authorised operators with strong authentication.
- Audit records for administrative access and status changes, without copying unnecessary applicant data into logs.
- Backups, restoration testing and a documented incident-response process.
- Dependency and configuration review before deployment.
- A documented deletion and retention job with tests.
- No connection to app browsing/activity, protection, recovery, accountability or Islamic Mode data.

A CAPTCHA or bot service may itself process visitor data. Evaluate its privacy impact before selection; prefer low-data rate limiting and email verification first. Do not promise “no tracking” if the selected abuse-prevention service uses tracking or fingerprinting.

## 9. Data lifecycle and retention

Before implementation, choose and document exact periods. Do not leave retention indefinite by default.

Recommended policy to review:
- Unverified requests: automatically delete after 7 days unless the person requests a new verification email.
- Verified, non-invited requests: retain only while the current alpha recruitment cycle is active; set a published review/expiry date.
- Declined or withdrawn requests: delete promptly, subject to narrowly defined security/legal retention needs.
- Invited applicants: retain the minimum invitation and onboarding status needed for the alpha; do not merge the waitlist record with app activity.
- Optional marketing list: separate consent state and separate unsubscribe handling.
- Security logs: short, documented retention; avoid storing full email addresses or verification tokens in logs.

These are proposed defaults, not an adopted retention policy. Confirm actual periods, backup deletion behaviour and legal obligations before collecting data.

Provide a simple privacy contact and process for access, correction, withdrawal and deletion requests before launch. Explain any data that cannot immediately be removed from immutable backups and when it expires.

## 10. Alpha capacity and fairness

- State clearly when applications are open, paused or closed.
- Do not fabricate a queue position, remaining-place counter or scarcity message.
- Do not promise selection order unless a published policy actually uses it.
- Define selection criteria internally before review begins; keep them relevant to device compatibility, test coverage and support capacity.
- Avoid selecting people based on intimate disclosures, religion, disability or other sensitive characteristics.
- Provide a route for people who are not selected to receive future announcements only if they separately consent.
- Do not sell, rent or share the list with advertisers, partners or unrelated services.

## 11. Operational readiness checklist

Do not open applications until all are complete:

- [ ] Adult-only alpha policy reviewed and approved.
- [ ] Supported device/Android requirements and known issues documented.
- [ ] Privacy notice and terms reviewed for Nigeria and intended markets.
- [ ] Data controller/contact identity and privacy contact confirmed.
- [ ] Data map, lawful basis, purpose and retention schedule approved.
- [ ] Waitlist storage isolated from app user data.
- [ ] Server validation, rate limits, email verification and admin access tested.
- [ ] Deletion, unsubscribe, backup expiry and restoration procedures tested.
- [ ] Email templates, sender domain and deliverability checked.
- [ ] No sensitive free-text fields or unnecessary tracking included.
- [ ] Security review and incident-response owner assigned.
- [ ] Invitation and installation route tested end-to-end.
- [ ] Alpha limitations and support expectations shown before installation.
- [ ] Accessibility, mobile, slow-network and failure states tested.
- [ ] Final copy matches the actual deployed system.

## 12. Implementation boundary

This specification does not implement a form, waitlist database, email integration, admin dashboard, invitation service, CAPTCHA, analytics, app distribution or legal compliance. Do not collect real applicant data until the full operational and privacy review is complete.


## 11. Current homepage status implementation

The homepage closing callout in `src/components/home/AlphaCallout.astro` and the shared footer state that Nūr is in development and closed-alpha applications are not open. The callout links to the existing How Nūr Works section only.

No email address, age confirmation or other personal information is collected. There is no waitlist, application submission, email verification, invitation workflow or download link. This is a status display, not an alpha access system.

The status must be changed only after the application process, privacy notice, legal review, support ownership and distribution method are implemented and verified.
