---
layout: default
title: Privacy Policy
---

# FORKD — Privacy Policy

**Effective date:** 2026-05-07
**Version:** 2026-05-06

This Privacy Policy explains what data FORKD ("**we**," "**us**," "**our**") collects, why we collect it, how we use it, who we share it with, and the choices you have. It is written to comply with **Apple App Store Review Guideline 5.1.1** and applicable privacy laws (GDPR, CCPA, and similar).

If anything here is unclear, email **szedash@gmail.com**.

---

## 1. Summary (in plain English)

- We collect what is needed to run a social food-review app: your handle, email, photos you post, optional approximate location, and an optional one-way hash of your phone number for friend-finding.
- We **do not** sell your personal data, do not run third-party advertising, and do not track you across other companies' apps or websites.
- You can delete your account from inside the app at any time. Deletion is permanent after a 30-day grace window.

## 2. Data we collect

### Data you provide directly

| Data | Why | Apple "Data Type" |
|---|---|---|
| **Account email** | Sign-in, password recovery, important service notices. | Contact Info → Email Address |
| **Handle and display name** | Identify you to other users. | User Content → Other |
| **Profile photo, bio** | Profile display. | User Content → Photos / Other |
| **Posts: photos, captions, ratings, recipes, lists** | Core app functionality. | User Content → Photos, Other |
| **Comments and likes** | Core app functionality. | User Content → Other |
| **Reports of other users / content** | Safety and moderation. | User Content → Other |

### Data collected automatically

| Data | Why | Apple "Data Type" |
|---|---|---|
| **Approximate location (city-level, ~100m accuracy)** | Discover nearby restaurants and tag posts with a city. We request `When in Use` only and store at coarse resolution. | Location → Coarse Location |
| **Crash and diagnostic data** | Find and fix bugs (Sentry). Excludes user content; PII is scrubbed where possible. | Diagnostics → Crash Data, Performance Data |
| **Device push token** | Send you push notifications you have opted into. | Identifiers → Device ID |
| **Auth session metadata** (timestamp, IP for the session) | Account security. | Identifiers, Usage Data |

### Optional: phone-number hash for friend-finding

If you choose to find friends from your phone book, FORKD computes a **SHA-256 hash** of phone numbers **on your device**. **We never receive or store your real phone numbers or your contact list.** We store only the resulting hashes, and access to the `phone_sha256` column is **revoked from all other users** at the database level — only the matching algorithm can read it. You can disable this feature at any time.

### Data we do NOT collect

- We do not collect precise GPS coordinates.
- We do not collect health data, financial data, browsing history outside FORKD, or contacts list contents.
- We do not use third-party SDKs for advertising or cross-app tracking. The app does not include the AppTrackingTransparency prompt because nothing in FORKD performs tracking as Apple defines it.

## 3. How we use your data

We use the data above only to:

1. Provide the core functionality of FORKD (post, view, follow, comment, like, search, discover).
2. Send service notifications (push, email confirmation, password reset).
3. Keep the app safe (rate-limit abuse, investigate reports, enforce our [Terms](./terms)).
4. Diagnose crashes and improve reliability.
5. Comply with legal obligations.

We do not use your data for advertising, profiling, or training third-party AI models.

## 4. How we share your data

We share data only with the service providers listed below, only to the extent required for them to operate FORKD on our behalf, and only under contractual data-protection terms providing **the same or equivalent protection** required by Apple Guideline 5.1.1.

| Provider | Purpose | Data sent | Region |
|---|---|---|---|
| **Apple, Inc.** | Sign in with Apple, push delivery (APNs) | Apple ID token, device push token | USA |
| **Google LLC** | Google Sign-In | OAuth ID token | USA |
| **Supabase, Inc.** | Database, storage, and edge functions hosting | All app data | Tokyo, ap-northeast-1 |
| **Mapbox, Inc.** | Geocoding lookups (city → coordinates) | City/restaurant query strings | USA |
| **Functional Software, Inc. (Sentry)** | Crash and error reporting | Crash dumps, anonymized identifiers | USA |

We do **not**:

- sell personal data,
- share data with advertisers or data brokers,
- share data with affiliates or related entities for their own marketing.

We may disclose data when required by valid legal process (subpoena, court order) or to protect the rights, property, or safety of our users or the public.

## 5. International transfers

FORKD's primary data is hosted in **Tokyo, Japan (Supabase ap-northeast-1)**. Some service providers (Apple, Google, Sentry, Mapbox) operate from the United States. By using FORKD you consent to the transfer of your data to these jurisdictions, which may have different privacy protections than your country of residence.

## 6. Data retention

| Data | Retention |
|---|---|
| Account, posts, comments | Until you delete them or delete your account. |
| Soft-deleted account | 30 days, then permanent deletion. |
| Backups | Routine rotation, typically deleted within 30 days of a permanent delete. |
| Crash logs | 90 days at Sentry (default). |
| Reports / moderation records | Up to 1 year after resolution, for repeat-offender investigation. |

## 7. Your rights and choices

Depending on where you live, you may have rights to:

- **Access** the data we hold about you.
- **Correct** inaccurate data.
- **Delete** your data (the in-app "Delete Account" path is the fastest way).
- **Export** your data in a portable format.
- **Object to or restrict** certain processing.
- **Withdraw consent** previously given (e.g., disable phone-hash matching, push notifications, or location).

To exercise any of these rights, email **szedash@gmail.com**. We will respond within the period required by applicable law (typically 30 days).

You can also control these directly inside the app:

- **Push notifications:** iOS Settings → Notifications → FORKD.
- **Location:** iOS Settings → Privacy → Location Services → FORKD.
- **Camera / Photos:** iOS Settings → Privacy → Camera / Photos → FORKD.
- **Phone-hash matching:** Settings → Privacy → "Find friends by phone" toggle in FORKD.
- **Account deletion:** Settings → Account → Delete Account in FORKD.

## 8. Security

- All traffic between FORKD and our servers uses **TLS 1.2 or higher** (no `NSAppTransportSecurity` exceptions).
- Authorization is enforced at the database layer with **PostgreSQL Row-Level Security**, so other users cannot read data they should not see, even if there is a bug in the app.
- Photo metadata (EXIF/GPS) is **stripped server-side** before public delivery.
- Phone numbers are **hashed on-device** and the hash column is revoked from all user roles.
- Crash reports are scrubbed of identifying content where feasible.

No system is perfectly secure. If we discover a breach affecting your data, we will notify you and the relevant authorities as required by law.

## 9. Children

FORKD is rated **12+** in the App Store and is not intended for users under **13**. We do not knowingly collect personal information from children under 13. If we learn that we have, we will delete it. If you believe we have collected such information, email **szedash@gmail.com**.

## 10. Third-party content

FORKD displays user-generated content. Other users' posts, comments, and profiles are governed by their own choices. Restaurant data (names, addresses) may be sourced from publicly available datasets and Mapbox.

## 11. Changes to this Policy

We may update this Privacy Policy from time to time. The current version is identified by the **Version** string at the top. Material changes will be communicated in-app, and continued use after the effective date constitutes acceptance.

## 12. Contact

For privacy questions, data requests, or to report a privacy concern: **szedash@gmail.com**.

---

*Last updated: 2026-05-07*
