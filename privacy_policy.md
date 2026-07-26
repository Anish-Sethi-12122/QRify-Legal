# QRify — Privacy Policy

**Effective Date:** July 26, 2026



## Introduction

QRify is a mobile application developed by **Anish Sethi** ("the developer", "us") based in India. QRify is designed to help you understand and evaluate the content encoded in QR codes before you act on them.

This Privacy Policy explains what information QRify ("the app") processes, how it handles that information, and what choices you have. QRify is built on a **local-first, privacy-first** philosophy — your data stays on your device unless you explicitly choose otherwise.

If you have questions or concerns about this policy, you can reach us at **support.qrify@gmail.com**.



## Information QRify Processes

When you scan a QR code, QRify decodes and interprets its contents. This may include:

- **URLs** — web addresses and deep links
- **WiFi configurations** — network names, encryption types, and passwords encoded in QR format
- **UPI payment data** — payee identifiers, amounts, and transaction references encoded in QR format
- **Plain text, contact information, calendar events, geographic locations, Wi-Fi configurations, UPI payment requests, and other standard QR-encoded data**

All of this information is processed **locally on your device**. QRify does not transmit scanned QR content outside your device. The only exception is optional, user-initiated External Verification described below.



## Local Processing

QRify performs all of its core analysis entirely on your device. This includes:

- **URL parsing** — breaking down web addresses into their structural components
- **Semantic interpretation** — understanding what a QR code is trying to do
- **Identity analysis** — examining domain names, brand indicators, and trust signals
- **Call-to-action (CTA) analysis** — identifying what the QR code is asking you to do
- **Explanation synthesis** — generating human-readable summaries of QRify's findings

None of these operations require an internet connection. None of them send data off your device. The QR code you scan and the analysis QRify produces both remain entirely local.



## External Verification (Optional, User-Initiated Only)

QRify offers an **optional** external verification feature for URLs. Here's how it works:

1. After QRify completes its local analysis, you may be presented with the option to verify a URL against an external safety database.  

2. **This verification is never automatic.** It only happens if you explicitly choose to initiate it. Although QRify may recommend external verification in certain situations, the decision always remains yours.  

3. When you initiate verification, the URL is sent to a **Firebase Cloud Function** operated by QRify, which forwards it to the **Google Web Risk API** for evaluation, which is accessible only to the developer(s) via **Google Cloud Portal**.  

4. The result (no known reports, potential threat detected, or inconclusive) is returned to your device and displayed alongside QRify's own local analysis.  

5. External verification is **supplementary** — it adds an additional data point but does not override QRify's local interpretation.  


**To be clear:** QRify will never silently upload, transmit, or share the QR codes you scan. External verification is entirely optional, entirely user-initiated, and performed only after your explicit consent.



## User Consent

Before QRify sends any URL for external verification, it asks for your **explicit consent** through an in-app dialog.

- You can **accept** to proceed with verification for that URL.
- You can **decline** to skip verification entirely and rely on QRify's local analysis alone.
- You can choose **"Do not show again"** to remember your preference for future scans. This preference is stored locally on your device and can be reset at any time from within the app.




## Internet Usage

QRify requires an internet connection for the optional external verification feature, retrieving dynamic configuration updates, and displaying advertisements.

Core functionality — scanning, decoding, analyzing, and explaining QR codes — works entirely offline.



## Third-Party Services

QRify integrates with the following third-party services under the above stated condition:

### Google Web Risk API
- **Purpose:** Evaluates URLs against Google's database of unsafe web resources.
- **When used:** Only when you choose to verify a URL after scanning.
- **What is sent:** The URL you chose to verify.
- **Provider's privacy policy:** [Google APIs Privacy Policy](https://developers.google.com/terms/api-services-user-data-policy)

### Firebase Cloud Functions
- **Purpose:** Acts as a secure gateway between QRify and the Google Web Risk API.
- **When used:** Only when you choose to verify a URL after scanning.
- **What is sent:** The URL you chose to verify.
- **Why a gateway:** API keys are stored server-side in the Cloud Function, not in the app itself. This means no sensitive credentials are embedded in the app on your device.
- **Provider's privacy policy:** [Google Firebase Privacy Policy](https://firebase.google.com/support/privacy)

### Google AdMob
- **Purpose:** Serves advertisements within the application.
- **When used:** During general application usage and scanning.
- **What is collected:** Device identifiers and usage data as governed by Google to provide relevant or non-personalized ads.
- **Provider's privacy policy:** [Google Privacy & Terms](https://policies.google.com/technologies/ads)

QRify also integrates **Firebase Analytics**, **Firebase Crashlytics**, **Firebase App Check**, and **Firebase Remote Config** to improve application reliability, understand aggregate feature usage, remotely manage configurations, and protect backend services. These services operate within the privacy principles described throughout this Privacy Policy.




## Analytics & Diagnostics

QRify uses a limited set of Google Firebase services to help improve the application's stability and usability.  


### Firebase Analytics

QRify collects a small number of aggregate application events, such as:

- application launches
- scan sessions
- QR code categories (for example, URL, Wi-Fi, UPI payment, text, contact information, calendar event, or geographic location)
- local analysis outcomes
- optional external verification usage
- theme preference changes
- opening the Privacy Policy or Terms & Conditions

These events are used only to understand how QRify is used and to improve the application over time.  


**QRify never sends the contents of scanned QR codes, URLs, domains, Wi-Fi passwords, contact details, calendar data, payment information, geographic coordinates, or any other QR payload to Firebase Analytics.**


### Firebase Crashlytics

QRify uses Firebase Crashlytics to receive crash reports and diagnostic information when the application unexpectedly fails.

Crash reports help identify software defects and improve application stability.

QRify does not intentionally include scanned QR contents, URLs, or other user-generated content in crash reports.

Crash reports are limited to diagnostic information necessary to investigate application failures. QRify does not intentionally attach custom logs, user identifiers, scanned QR contents, or external verification results to crash reports.


### Firebase App Check

QRify uses Firebase App Check to help protect its backend infrastructure from unauthorized or automated abuse.

App Check verifies that requests originate from a genuine QRify application without collecting or exposing the contents of scanned QR codes.

App Check is used solely to verify legitimate application instances before optional backend requests are processed. It is not used for analytics, advertising, or user tracking.



## Permissions

QRify requests the following device permission:

### Camera
- **Purpose:** Required to scan QR codes using your device's camera.
- **Usage:** The camera feed is processed locally and in real-time to detect and decode QR codes. QRify does not record, store, or transmit camera images or video.  


### Gallery Access
QRify allows you to scan QR codes from images in your device's gallery. This relies on the native system photo picker, meaning QRify does not require or request persistent access to your entire photo library.

QRify does not request any other permissions.



## Data Storage

QRify uses **SharedPreferences** (Android's local key-value storage) and a local **SQLite database** to store data on your device. This includes:

- Your consent dialog preference (e.g., whether you selected "Do not show again")
- Your **selected application theme** (Light, Dark, or System)
- Your **language preference**
- Cached external verification policies and results

This data is stored **locally on your device only**. It is not transmitted to any server, is explicitly excluded from Android cloud backups, and is not accessible to any third party. You can clear this data at any time by clearing the app's data through your device settings.



## What QRify Does NOT Collect

QRify is designed to respect your privacy. To be explicit, QRify does **not**:

- Collect or transmit the **contents of scanned QR codes**, URLs, domains, Wi-Fi SSIDs, Wi-Fi passwords, UPI IDs, Aadhaar-linked payment destinations, bank account numbers, contact details, calendar information, geographic coordinates, or any other QR payload, contact information, payment information, or other QR-encoded content for analytics purposes
- Collect **personally identifiable information** such as your name, email address, phone number, precise location, or government-issued identifiers
- Use analytics to profile individual users or track browsing activity across apps or websites
- Associate analytics or diagnostic information with your identity\
- Require or support **user accounts**, logins, or registration
- Use **cloud sync** or cloud storage for your data
- Offer or require **subscriptions** or in-app purchases
- Track your **browsing history** or app usage patterns
- Collect **personal information** such as your name, email, phone number, or location
- Build **user profiles** or share data with data brokers
- Use **fingerprinting**, device identification, or cross-app tracking



## Data Collection

QRify collects minimal required data to **report crashes**, understand **app usage** and ensure continually improving services. Precisely:

- Collect limited, aggregate application usage metrics to understand how QRify's features are used and to improve the application's reliability
- Collect crash diagnostics when the application unexpectedly terminates in order to improve stability



## Security

QRify takes the following measures to protect the data it handles:

- **HTTPS transport:** When external verification is used, all communication between QRify, Firebase Cloud Functions, and Google Web Risk occurs over encrypted HTTPS connections.
- **Server-side API keys:** Sensitive API credentials are stored in the Firebase Cloud Function environment, not in the app binary on your device. This prevents key extraction or misuse.
- **No client-side secrets:** QRify does not embed API keys, tokens, or other secrets in the application itself.
- **Minimal data exposure:** QRify sends only the specific URL being verified — nothing more. No device identifiers, no metadata, no additional context.



## User Choices

You have full control over how QRify operates:

- **Decline external verification:** You can always choose not to verify a URL externally. QRify's local analysis is fully functional without it.
- **Reset consent preferences:** If you previously selected "Do not show again," you can reset this preference at any time by clearing the app's data through your device settings.
- **Revoke camera permission:** You can revoke camera access through your device settings at any time, though this will prevent QRify from scanning QR codes.
- **Uninstall:** You can uninstall QRify at any time. Because all data is stored locally, uninstalling the app removes all associated data from your device.



## Children's Privacy

QRify does not knowingly collect personal information from children under the age of 13. Since QRify does not collect personal information from any user, this is inherently the case.



## Contact Information

If you have questions, concerns, or feedback about this Privacy Policy or QRify's privacy practices, please contact:

- **Developer:** Anish Sethi
- **Email:** support.qrify@gmail.com
- **Location:** India
- **Website:** Coming Soon



## Future Updates to This Policy

This Privacy Policy may be updated from time to time to reflect changes in QRify's functionality or applicable regulations.

- The **in-app version** of this Privacy Policy is the authoritative version until a dedicated website is available.
- Material changes will be communicated through an update to this in-app document.
- The "Effective Date" at the top of this policy will be updated to reflect the date of the most recent revision.

Your continued use of QRify after changes to this policy constitutes your acceptance of the updated terms.  

**© 2026 Anish Sethi. All rights reserved.**
