---
layout: single
title: "Privacy Policy — MediaHarbor"
permalink: /mediaharbor/privacy/
author_profile: true
toc: true
toc_label: "On this page"
---

**Effective date:** July 19, 2026  
**Last updated:** August 3, 2026  

---

## 1. Introduction

MediaHarbor is an independent iOS application developed and maintained by Ian Marrero ("I," "me," or "my"). This Privacy Policy explains what data the app handles, what leaves your device, and your rights as a user.

MediaHarbor is built on a simple principle: **it is a viewer for files you already own, and those files are none of my business.** Your photos, your videos, your server addresses, and your passwords stay on your device and on your own network. There is no account to create, no cloud service behind the app, and no third-party analytics or tracking of any kind.

Only two things ever reach me: a support message you deliberately write and send from inside the app (Section 4), and a handful of anonymous usage counters — app opens and purchases, nothing more — which you can switch off at any time (Section 3).

---

## 2. What the App Does Not Collect

MediaHarbor contains **no third-party analytics or advertising SDKs, no crash-reporting SDK, and no trackers of any kind.** The only measurement it performs is the minimal, anonymous usage counting described in Section 3 — implemented in my own code, sent only to my own server, and controlled by a switch in Settings. The following never leave your device:

- **Your photos and videos.** The app reads them to display them. It never uploads them anywhere.
- **File names, folder names, and directory listings** from your devices or servers.
- **Server addresses, share names, user names, domains, and passwords** for your network connections.
- **Which screens you open, which features you use, which files you view, or how long you watch.** The app counts only *that* a session started (Section 3) — never what you did in it.
- **Your location.** The app does not request location permission. Photos may contain GPS coordinates in their own metadata; those are read on your device to draw a map and are never transmitted.
- **Advertising identifiers (IDFA), the device vendor identifier (IDFV), or your device model.**

Because MediaHarbor collects no data for advertising, shares nothing with any other company, and its usage counters cannot be linked to you, it does not present an App Tracking Transparency prompt and does not track you as Apple defines tracking.

---

## 3. Anonymous Usage Statistics

Starting with version 1.0.1, MediaHarbor counts a small set of anonymous usage statistics so I can tell whether the app is being used and whether its one-time unlock keeps it sustainable. The scope is deliberately tiny, and there is an off switch.

**Exactly four things are counted:**

- That the app was **opened** (at most one count per session).
- That a purchase of the **Lifetime Unlock completed**.
- That a **Restore Purchases** succeeded.
- That an install **has the unlock active** — counted once per install, so I can know how many active users are paid users.

Each count is sent with the app version, a timestamp, and a **random install identifier** generated on your device. That identifier is not derived from your identity, your Apple ID, your name, or any hardware identifier, and it is deliberately a *different* random value than the feedback form's identifier — so a feedback message that carries your email address can never be connected to usage counts. Deleting the app destroys the identifier permanently.

**Nothing else is ever sent.** No file names, folder names, server addresses, screens, features, viewing or playback activity, searches, location, or device model. The receiving server accepts only the four counters above and rejects anything else; it never logs or stores IP addresses.

These counters go to **a server I own and administer personally** — the same self-hosted server that receives feedback messages. No third-party analytics service, SDK, or cloud platform is involved at any point.

**Turning it off:** Settings → Privacy → **Share Anonymous Usage Statistics**. Switching it off stops all counting immediately and discards anything not yet sent. The app works identically either way.

---

## 4. Support and Feedback Submissions

MediaHarbor includes a feedback form at **About → Send Feedback**. It is entirely optional. Nothing is sent unless you type a message and tap Send.

When you send feedback, the following is transmitted to a server I operate personally:

- The **message** you wrote and the **topic** you selected (Bug, Feature Request, Help, or Other).
- Your **email address**, only if you choose to enter one so I can reply. This field may be left blank.
- The **app version** and **iOS version**, so I can reproduce the problem.
- A **random install identifier** — a value generated on your device that is not derived from and cannot be linked to your identity, your Apple ID, your name, or any device hardware identifier. It exists solely to rate-limit abuse of the form. It is erased permanently if you delete the app.
- A **timestamp**.

This data is stored on a server I own and administer. It is **not** processed by Google Forms, Typeform, a helpdesk platform, or any third-party service. It is never shared with, sold to, or made accessible to anyone else. Your email address is used **solely to reply to your message** — never for marketing, and never added to a mailing list.

The app never attaches your photos, videos, file names, server details, or credentials to a feedback submission.

**Please do not include sensitive personal information in a feedback message.** A description of the problem, and your NAS make and model if it is connection-related, is all that is useful.

You may ask me to delete correspondence you have sent at any time — see Section 11.

---

## 5. Network Connections and Credentials

MediaHarbor connects directly to **SMB servers that you specify** — typically a NAS or file server on your own network. These connections go from your device to your server. They do not pass through any server of mine, and I have no visibility into them.

**Credentials.** When you choose to save a password, it is stored in the **iOS Keychain** with device-only accessibility, which means it is encrypted by the system, never included in an iCloud Keychain sync, and never written into the app's own files or settings. Passwords are sent only to the server you entered them for, as part of the SMB authentication the protocol requires. They are never logged, never embedded in URLs, and never transmitted to me.

**Local Network permission.** iOS asks for Local Network access the first time the app connects to a server on your network. This is required for SMB to work at all. Declining it does not send any data anywhere; it simply prevents connections from succeeding.

---

## 6. Local Storage and Caching

To make browsing fast, MediaHarbor stores the following in its own sandboxed container on your device:

- **Thumbnails and decoded previews** of images and video poster frames.
- **Downloaded copies of files** you open from a network share, so they don't have to be fetched twice. This cache is capped and evicts the least recently used files automatically.
- **Directory listings**, so a folder you have visited opens instantly next time.
- **Your settings, bookmarks, favorites, recent files, and video resume positions.**

All of this is local. You can remove it at any time in **Settings → Storage → Clear Caches**, which also shows how much space is in use. Uninstalling the app removes everything, including saved passwords in the Keychain.

If you have iCloud Backup enabled, iOS may include portions of the app's container in your device backup. That backup is stored by Apple and governed by **Apple's Privacy Policy**, not by this policy. Cached files are marked as cache data, which iOS generally excludes from backups.

---

## 7. Saving to Photos and Sharing

MediaHarbor can save a photo or video to your Photos library, and can share files through the standard iOS share sheet. Both are user-initiated. Saving requires your permission (iOS will ask). When you share a file to another app, that app's own privacy policy governs what happens to it from that point on.

---

## 8. In-App Purchase

MediaHarbor is free to download. An optional one-time **Lifetime Unlock** removes the free version's limits.

The purchase is processed entirely by **Apple** through the App Store. The app never sees or handles your payment card details, billing address, or Apple ID. I receive only aggregate, anonymized sales and payout reporting through App Store Connect, which never identifies you. Payment processing is governed by **Apple's Privacy Policy**.

The app checks your purchase status through Apple's on-device StoreKit framework. That check does not involve any server of mine.

---

## 9. Data Sharing

I do not sell, rent, or share your data with advertising networks, data brokers, or any other party. There are no third-party SDKs in the app that collect data.

The only external parties involved in MediaHarbor at all are:

- **Apple** — for app distribution and, if you choose to buy the unlock, payment processing. Governed by Apple's Privacy Policy.
- **The servers you configure yourself** — your NAS or file server, which you own and control.

---

## 10. Data Retention and Deletion

- **On your device:** everything the app stores is yours to remove. Clear caches in Settings, or uninstall the app to erase all local data and Keychain entries.
- **Feedback messages:** retained on my server only as long as needed to respond and to track the underlying bug or request. There is no automated retention limit; you may request deletion at any time (Section 11).
- **Usage counters:** stored on my server as anonymous counts. They contain no personal data and cannot be traced back to you or your device, so they are retained as aggregate history (e.g., "daily users over time"). Turning the switch off (Section 3) stops new counts immediately.

I hold no other copy of anything related to your use of the app.

---

## 11. Your Privacy Rights

Because MediaHarbor collects nothing except feedback you deliberately send and anonymous counters that cannot identify you, there is very little data to exercise rights over — but those rights apply fully to what does exist.

If you have sent feedback, you may request a copy of it or ask me to delete it by using the [contact page](https://www.ianm.tech/contact/). Please include enough detail (approximate date, and the email address you used, if any) for me to locate the message.

Residents of California and other states with comprehensive privacy laws should be aware that I do not sell or share personal information, do not engage in targeted advertising, and do not meet the revenue or data-volume thresholds that trigger obligations under the California Consumer Privacy Act (CCPA/CPRA) or similar state laws. The protections in this policy apply to all users regardless of location.

---

## 12. Children's Privacy

MediaHarbor is rated 4+ and does not knowingly collect personal information from anyone, including children under 13. The app has no accounts, no social features, and no advertising. It displays only the files a user chooses to open.

---

## 13. Third-Party AI

MediaHarbor does not send your data to any third-party AI system, machine learning platform, or external service. The scene detection used for smart albums runs entirely on your device using Apple's on-device Vision framework; no image is ever uploaded for analysis.

---

## 14. Open-Source Components

MediaHarbor includes the following open-source libraries, used as dynamically linked, unmodified libraries under the GNU LGPL v2.1:

- **VLCKit** — © VideoLAN and authors
- **AMSMB2** — © Amir Abbas Mousavian
- **libsmb2** — © Ronnie Sahlberg and contributors

These libraries handle video decoding and the SMB protocol on your device. They do not transmit data to their authors or to any third party. Full license text is available in the app under **Settings → About → Third-Party Software**.

---

## 15. Do Not Track

MediaHarbor is a native iOS application. It does not operate a web browser, does not engage in cross-site tracking, and does not respond to browser-based Do Not Track (DNT) signals. DNT is not applicable to this app's functionality.

---

## 16. Changes to This Policy

If I make material changes to this policy, I will update the "Last updated" date at the top of this page. For significant changes, I will also note the update in the app's release notes or in a post on [ianm.tech](https://www.ianm.tech).

Continued use of the app after changes are posted constitutes acceptance of the revised policy.

---

## 17. Governing Law

This Privacy Policy is governed by and construed in accordance with the laws of the State of Maryland, United States, without regard to conflict of law principles.

---

## 18. Contact

If you have questions about this Privacy Policy, use **About → Send Feedback** inside the app, or the [contact page](https://www.ianm.tech/contact/).
