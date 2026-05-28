# Privacy Policy for Glint — Subscription Tracker

**Last updated:** 29 May 2026
**Effective date:** 29 May 2026
**App:** Glint — Subscription Tracker
**Developer:** Nagarajan Seeni
**Contact:** <nagarajanseeni.dev@gmail.com>

This Privacy Policy describes how Glint ("the app", "we", "us", or "our") handles information when you use our mobile application available through the Google Play Store and Apple App Store. By installing or using Glint, you agree to the practices described in this policy.

---

## 1. Summary (Plain English)

- Glint does **not** require an account or sign-in to use the core app. (An optional Google sign-in is used only if you turn on Google Drive backup on Android — see Section 4.4.)
- All your subscription data is stored **only on your device** by default. We do not run servers that store your data.
- Two **optional** features can send limited data off-device, and only when you use them:
  1. **Brand logos** — when you add a subscription, the brand's domain or your typed keyword is sent to a logo service (Brandfetch) so we can show that brand's icon.
  2. **Cloud backup (optional, Pro feature)** — if you turn it on, your subscriptions, categories, and settings are saved to **your own iCloud (iOS) or Google Drive (Android)** account. We never receive a copy.
- We have **no analytics, no advertising SDKs, no behavioural tracking, and no third-party data brokers**.
- Notifications are scheduled and shown **locally on your device** — we do not run any push-notification server.

---

## 2. Information We Collect

### 2.1 Information You Provide

Glint stores the following information **only on your device** in a local database:

- Subscription details you enter: service name, price, currency, billing cycle, renewal date, category, notes, trial information, and cancellation status.
- App settings: preferred currency, theme (light/dark/system), reminder preferences, onboarding completion status, and backup preferences.
- Pro entitlement status (whether you have unlocked the Pro version).

This information **never leaves your device** unless you explicitly enable an optional feature that involves the cloud (see Section 4.4) or back up your device via your operating system's own backup feature (iCloud Backup, Google One Backup, etc.). Those OS-level backups are governed by Apple's and Google's privacy policies.

### 2.2 Information We Do **Not** Collect

We do **not** collect, store on our servers, or process the following:

- Your name, phone number, or any personal identifier (with the limited exception of the Google sign-in flow described in Section 4.4, where Google — not Glint — handles your email).
- Advertising ID, device fingerprint, or location.
- Behavioural analytics, crash reports, screen recordings, or usage statistics.
- Contacts, photos, calendar, microphone, camera, or biometric data. Biometric authentication (Face ID / Touch ID / fingerprint), if used, is handled entirely by your device's operating system; we never receive or store biometric templates.

### 2.3 Information Automatically Processed by Third Parties

When you use specific features, third parties receive limited technical information as required for those features to work:

- **In-app purchase** — purchase transaction token (issued by Google Play / Apple), processed by Google Play Billing / Apple StoreKit and validated through RevenueCat. See Section 4.1–4.3.
- **Brand logos / brand search** — the brand domain or search keyword you enter (e.g. `netflix.com` or `spot`), plus your device's IP address as part of the standard HTTPS request, sent to Brandfetch. See Section 4.5.
- **Currency rates** — a public HTTPS request to ExchangeRate-API containing no personal data. See Section 4.6.
- **Cloud backup (optional, Pro)** — if you enable it, the full backup file is uploaded to **your own** iCloud or Google Drive account. We do not receive a copy. See Section 4.4.

We do **not** maintain identifiers that link these technical requests back to your real identity inside Glint.

---

## 3. How We Use Your Information

The subscription data you enter is used solely to:

- Display your subscriptions, billing cycles, and upcoming renewals inside the app.
- Calculate total monthly and yearly spend in your preferred currency.
- Schedule local reminder notifications before renewals or trial endings.
- Maintain your in-app settings between sessions.
- If you enable cloud backup: serialise your subscriptions, categories, and settings into a JSON backup file that is written to your own cloud storage account (see Section 4.4).

We do **not** sell, rent, lease, share for advertising, or otherwise disclose your subscription data to any third party.

---

## 4. Third-Party Services

Glint uses the minimum third-party services needed to function. Each is listed below with what it receives and a link to its own privacy policy.

### 4.1 Google Play Billing (Android only)

Handles in-app purchases for the Pro upgrade. Google processes the payment and issues a purchase token. Glint does not receive your payment card details or billing address.

- Privacy policy: <https://policies.google.com/privacy>

### 4.2 Apple App Store / StoreKit (iOS only)

Handles in-app purchases for the Pro upgrade on iOS. Apple processes the payment.

- Privacy policy: <https://www.apple.com/legal/privacy/>

### 4.3 RevenueCat

We use RevenueCat (RevenueCat, Inc.) to validate in-app purchase receipts and determine whether your install has an active Pro entitlement. RevenueCat receives:

- The purchase token issued by Google Play / Apple.
- An anonymous installation identifier generated by the RevenueCat SDK.
- Platform information (Android / iOS, app version).

RevenueCat does **not** receive your name, email, subscription data, or any other information from Glint beyond the items above.

- Privacy policy: <https://www.revenuecat.com/privacy>

### 4.4 Cloud Backup — Apple iCloud and Google Drive (optional, Pro feature)

**This feature is off by default.** It is only activated when you turn on "Cloud backup" in Settings.

When enabled, Glint serialises a JSON backup file containing your **subscriptions, categories, and app settings** and uploads it to:

- **On iOS** — your own **iCloud** account, in an app-private container ("AppData" scope) that is not visible in your iCloud file browser. No additional sign-in step is required; the OS uses your existing iCloud login.
- **On Android** — your own **Google Drive**, in the hidden, app-private `appDataFolder` ("Drive AppData" scope) that is not visible in your normal Drive view. Enabling this feature requires a one-time Google sign-in. The sign-in is provided by Google's official Google Sign-In SDK and gives Glint a short-lived OAuth access token plus your Google account email. Glint requests **only the drive.appdata scope** — we cannot read or write any other file in your Drive.

**Important points:**

- **We never receive a copy of your backup.** It is stored in your own cloud account and governed by Apple's or Google's privacy policy for that account.
- **You can turn cloud backup off** at any time in Settings. You can also delete the backup file directly from iCloud or Drive (the file is named `glint-backup.json` in the app's AppData area).
- **Signing out** of Google on Android (Settings → Cloud backup → Sign out) revokes our OAuth token immediately.
- Apple and Google may retain backup file metadata according to their own policies.

Third-party policies that apply to data while it is in your own cloud:

- Apple iCloud privacy: <https://www.apple.com/legal/privacy/>
- Google Drive / Google Sign-In privacy: <https://policies.google.com/privacy>
- Google API Services User Data Policy (which Glint complies with for `drive.appdata` use, including the Limited Use requirements): <https://developers.google.com/terms/api-services-user-data-policy>

**Glint's use of Google user data complies with the Google API Services User Data Policy, including the Limited Use requirements.** Specifically: data obtained from Google APIs is used only to provide the cloud backup feature, is not transferred to other parties except as needed to provide that feature, is not used for advertising, and is not read by humans except (a) with your explicit consent, (b) for security purposes, or (c) where required by law.



### 4.5 Brandfetch — Brand Logos and Brand Search

To display recognisable icons for your subscriptions, Glint fetches brand logos from Brandfetch (a brand-asset CDN). Brandfetch receives:

- The brand's **domain name** (e.g. `netflix.com`) or your typed **search keyword** (e.g. `spot`) when you are adding or editing a subscription's brand.
- A Brandfetch client identifier owned by Glint.
- Standard HTTPS request metadata, including your device's IP address.

Brandfetch does **not** receive your subscription prices, renewal dates, notes, identity, or any other information from inside Glint. Search results are cached locally on your device for 24 hours to minimise repeat requests. Logo image responses are also cached by your operating system's image cache.

You may use Glint without ever triggering a Brandfetch request by leaving the brand/domain fields empty when adding a subscription — Glint will fall back to a coloured initials tile in that case.

- Brandfetch privacy policy: <https://brandfetch.com/privacy>

### 4.6 ExchangeRate-API

Glint fetches public foreign exchange rates from exchangerate-api.com to display your subscription costs in your chosen currency. These requests contain **no personal data** — only a standard HTTPS request for the latest rate table. The fetched rates are cached locally on your device and refreshed at most once every 24 hours.

- Privacy policy: <https://www.exchangerate-api.com/terms>

### 4.7 Expo / Expo Notifications

Glint is built with the Expo framework. Local notifications are scheduled and delivered by the device's operating system — no notification content is sent to Expo's or any external server. Glint does **not** use push notifications, so no push token is ever generated or transmitted.

- Privacy policy: <https://expo.dev/privacy>

We do **not** use Google Analytics, Firebase Analytics, Facebook SDK, AppsFlyer, Adjust, Branch, Sentry, Crashlytics, or any advertising / attribution SDK of any kind.

---

## 5. Data Storage and Security

- All on-device app data is stored in a local SQLite database inside the OS-managed app sandbox.
- We do not operate any servers that store your subscription data, so there is no central cloud database that could be breached.
- All outbound network requests (in-app purchase validation, Brandfetch, ExchangeRate-API, cloud backup) are transmitted over HTTPS (TLS 1.2+).
- OAuth tokens used for Google Drive backup are short-lived and stored only in the secure keystore provided by the Google Sign-In SDK; we do not log or transmit them elsewhere.
- Cloud backup files are stored in app-private scopes (iCloud AppData / Drive AppData) that are not visible to other apps or to your own normal file browser, in addition to the security controls applied by Apple and Google to your cloud account.

No method of transmission or storage is 100% secure, but we minimise risk by storing data on-device by default, using app-private cloud scopes for optional backup, and using industry-standard encryption for all outbound requests.

---

## 6. Data Retention and Deletion

Because the primary copy of your data lives on your device, **you control retention entirely**:

**On-device data:**

- To delete an individual subscription: open it inside Glint and tap Delete.
- To delete all app data: uninstall Glint, or on Android use **Settings → Apps → Glint → Storage → Clear data**.
- On iOS, deleting the app removes all associated data.

**Cloud backup file (if you enabled it):**

- Turn off cloud backup in Glint Settings — this stops new uploads. The existing file remains in your cloud until you delete it.
- To delete the file itself: it lives at `glint-backup.json` in the app's AppData scope. On Android you can use Google Drive's "Manage apps" screen (Drive → Settings → Manage apps → Glint → Delete hidden app data). On iOS, deleting Glint from your device removes its iCloud AppData container.
- On Android, sign out of Google Drive in Glint Settings to revoke our OAuth token.

**Data held by third-party processors:**

- **RevenueCat / Google Play / Apple purchase records:** retained by those processors for accounting, tax, refund, and fraud-prevention purposes for the period required by law. Request deletion directly from RevenueCat at <https://www.revenuecat.com/privacy> or via Google / Apple support.
- **Brandfetch / ExchangeRate-API:** receive only transient HTTPS request metadata and do not retain user-identifiable records about you on Glint's behalf.

If you wish to confirm full erasure of anything we control, email <nagarajanseeni.dev@gmail.com> and we will respond within 30 days.

---

## 7. Permissions Requested

Glint requests the following device permissions; each is optional and used only as described:

- **Notifications** — to show local renewal reminders. You can disable this in your device settings or inside Glint's Settings screen at any time. Glint never sends push notifications from a server.
- **Internet access** — required to fetch brand logos, currency exchange rates, process in-app purchases, and upload to your own cloud account if you enable cloud backup. The app's core functionality works offline.
- **Google account access (Android only, optional)** — requested only the first time you enable Google Drive backup. Limited to the `drive.appdata` scope so Glint can only write to a hidden app-private folder.
- **Biometric authentication (optional, if enabled)** — handled entirely by the OS; Glint never sees or stores biometric data.

Glint does **not** request access to: contacts, photos, camera, microphone, calendar, location, SMS, call logs, or any other sensitive data.

---

## 8. Children's Privacy

Glint is intended for users aged **18 and over**. The app is not directed to children under 13 (or under 16 in jurisdictions where that threshold applies), and we do not knowingly collect personal data from children.

If you believe a child has somehow provided information through the app, please contact us at <nagarajanseeni.dev@gmail.com> and we will take prompt action.

This complies with:

- The Children's Online Privacy Protection Act (COPPA) in the United States.
- The General Data Protection Regulation — Article 8 (GDPR-K) in the European Union and United Kingdom.
- Google Play's Families Policy.

---

## 9. Your Rights

Because Glint stores your primary data on your device and any cloud backup is stored in **your own** iCloud or Google Drive account, most data-subject rights (access, rectification, erasure, portability, restriction, objection) are exercised by you directly — through the app and through your cloud provider.

For data processed by our third-party providers (RevenueCat, Google Play, Apple, Brandfetch, ExchangeRate-API), please use their respective privacy contact channels listed in Section 4.

Residents of California (CCPA / CPRA), the EU/EEA (GDPR), the United Kingdom (UK GDPR), Brazil (LGPD), and other privacy-protected jurisdictions have additional statutory rights. To the extent we hold any personal data under those laws, you may exercise those rights by contacting <nagarajanseeni.dev@gmail.com>.

We do **not** "sell" or "share" personal information as those terms are defined under California law.

---

## 10. International Data Transfers

Your subscription data is stored locally on your device by default, so no international transfer occurs for that data.

When you use optional features, limited technical data may be processed by servers operated by the relevant third party in the United States or other countries:

- Brandfetch (logo / brand search requests).
- ExchangeRate-API (currency rate requests).
- RevenueCat (purchase validation).
- Google / Apple (in-app purchase processing, cloud sign-in, cloud storage of backup files in your own account).

These transfers occur under those providers' published data-transfer frameworks (e.g. Standard Contractual Clauses, EU-US Data Privacy Framework). Refer to their privacy policies for details.

---

## 11. Changes to This Policy

We may update this Privacy Policy from time to time to reflect changes in the app, third-party services, or legal requirements. The "Last updated" date at the top of this page indicates the most recent revision. Significant changes will be highlighted in the app's release notes on Google Play and the App Store.

Continued use of Glint after a policy update constitutes acceptance of the revised terms.

---

## 12. Contact

For questions, complaints, or data-related requests:

**Email:** <nagarajanseeni.dev@gmail.com>
**Developer:** Nagarajan Seeni
**App:** Glint — Subscription Tracker

We respond to all privacy enquiries within 30 days.

---

## 13. Compliance Statement

This Privacy Policy is intended to satisfy the disclosure requirements of:

- Google Play Developer Program Policies (Data safety, User Data, Families, and Limited Use of Google API user data)
- Google API Services User Data Policy and the Limited Use requirements applicable to the `drive.appdata` scope
- Apple App Store Review Guidelines (5.1 Privacy)
- EU / UK General Data Protection Regulation (GDPR)
- California Consumer Privacy Act (CCPA) and California Privacy Rights Act (CPRA)
- Brazilian General Data Protection Law (LGPD)
- Children's Online Privacy Protection Act (COPPA)

If any provision of this policy conflicts with applicable law in your jurisdiction, the law of your jurisdiction prevails to the extent of the conflict.

