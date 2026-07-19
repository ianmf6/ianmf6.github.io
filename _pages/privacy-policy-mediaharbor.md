---
layout: single
title: "Privacy Policy — MediaHarbor"
permalink: /mediaharbor/privacy/
author_profile: true
toc: true
toc_label: "On this page"
---

**Effective date:** July 19, 2026  
**Last updated:** July 19, 2026  

---

## 1. Introduction

MediaHarbor is an independent iOS application developed and maintained by Ian Marrero ("I," "me," or "my"). This Privacy Policy explains what data the app handles, what leaves your device, and your rights as a user.

MediaHarbor is built on a simple principle: **it is a viewer for files you already own, and those files are none of my business.** Your photos, your videos, your server addresses, and your passwords stay on your device and on your own network. There is no account to create, no cloud service behind the app, and no analytics.

The only information that ever reaches me is a support message you deliberately write and send from inside the app. That is described in Section 3.

---

## 2. What the App Does Not Collect

MediaHarbor contains **no analytics, no advertising SDKs, no crash-reporting SDK, and no third-party trackers of any kind.** Specifically, the following never leave your device:

- **Your photos and videos.** The app reads them to display them. It never uploads them anywhere.
- **File names, folder names, and directory listings** from your devices or servers.
- **Server addresses, share names, user names, domains, and passwords** for your network connections.
- **Which screens you open, which features you use, or how long you use the app.** None of this is measured or transmitted.
- **Your location.** The app does not request location permission. Photos may contain GPS coordinates in their own metadata; those are read on your device to draw a map and are never transmitted.
- **Advertising identifiers (IDFA), the device vendor identifier (IDFV), or your device model.**

Because MediaHarbor collects no data for advertising or measurement, it does not present an App Tracking Transparency prompt and does not track you as Apple defines tracking.

---

## 3. Support and Feedback Submissions

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

You may ask me to delete correspondence you have sent at any time — see Section 10.

---

## 4. Network Connections and Credentials

MediaHarbor connects directly to **SMB servers that you specify** — typically a NAS or file server on your own network. These connections go from your device to your server. They do not pass through any server of mine, and I have no visibility into them.

**Credentials.** When you choose to save a password, it is stored in the **iOS Keychain** with device-only accessibility, which means it is encrypted by the system, never included in an iCloud Keychain sync, and never written into the app's own files or settings. Passwords are sent only to the server you entered them for, as part of the SMB authentication the protocol requires. They are never logged, never embedded in URLs, and never transmitted to me.

**Local Network permission.** iOS asks for Local Network access the first time the app connects to a server on your network. This is required for SMB to work at all. Declining it does not send any data anywhere; it simply prevents connections from succeeding.

---

## 5. Local Storage and Caching

To make browsing fast, MediaHarbor stores the following in its own sandboxed container on your device:

- **Thumbnails and decoded previews** of images and video poster frames.
- **Downloaded copies of files** you open from a network share, so they don't have to be fetched twice. This cache is capped and evicts the least recently used files automatically.
- **Directory listings**, so a folder you have visited opens instantly next time.
- **Your settings, bookmarks, favorites, recent files, and video resume positions.**

All of this is local. You can remove it at any time in **Settings → Storage → Clear Caches**, which also shows how much space is in use. Uninstalling the app removes everything, including saved passwords in the Keychain.

If you have iCloud Backup enabled, iOS may include portions of the app's container in your device backup. That backup is stored by Apple and governed by **Apple's Privacy Policy**, not by this policy. Cached files are marked as cache data, which iOS generally excludes from backups.

---

## 6. Saving to Photos and Sharing

MediaHarbor can save a photo or video to your Photos library, and can share files through the standard iOS share sheet. Both are user-initiated. Saving requires your permission (iOS will ask). When you share a file to another app, that app's own privacy policy governs what happens to it from that point on.

---

## 7. In-App Purchase

MediaHarbor is free to download. An optional one-time **Lifetime Unlock** removes the free version's limits.

The purchase is processed entirely by **Apple** through the App Store. The app never sees or handles your payment card details, billing address, or Apple ID. I receive only aggregate, anonymized sales and payout reporting through App Store Connect, which never identifies you. Payment processing is governed by **Apple's Privacy Policy**.

The app checks your purchase status through Apple's on-device StoreKit framework. That check does not involve any server of mine.

---

## 8. Data Sharing

I do not sell, rent, or share your data with advertising networks, data brokers, or any other party. There are no third-party SDKs in the app that collect data.

The only external parties involved in MediaHarbor at all are:

- **Apple** — for app distribution and, if you choose to buy the unlock, payment processing. Governed by Apple's Privacy Policy.
- **The servers you configure yourself** — your NAS or file server, which you own and control.

---

## 9. Data Retention and Deletion

- **On your device:** everything the app stores is yours to remove. Clear caches in Settings, or uninstall the app to erase all local data and Keychain entries.
- **Feedback messages:** retained on my server only as long as needed to respond and to track the underlying bug or request. There is no automated retention limit; you may request deletion at any time (Section 10).

I hold no other copy of anything related to your use of the app.

---

## 10. Your Privacy Rights

Because MediaHarbor collects nothing except feedback you deliberately send, there is very little data to exercise rights over — but those rights apply fully to what does exist.

If you have sent feedback, you may request a copy of it or ask me to delete it by using the [contact page](https://www.ianm.tech/contact/). Please include enough detail (approximate date, and the email address you used, if any) for me to locate the message.

Residents of California and other states with comprehensive privacy laws should be aware that I do not sell or share personal information, do not engage in targeted advertising, and do not meet the revenue or data-volume thresholds that trigger obligations under the California Consumer Privacy Act (CCPA/CPRA) or similar state laws. The protections in this policy apply to all users regardless of location.

---

## 11. Children's Privacy

MediaHarbor is rated 4+ and does not knowingly collect personal information from anyone, including children under 13. The app has no accounts, no social features, and no advertising. It displays only the files a user chooses to open.

---

## 12. Third-Party AI

MediaHarbor does not send your data to any third-party AI system, machine learning platform, or external service. The scene detection used for smart albums runs entirely on your device using Apple's on-device Vision framework; no image is ever uploaded for analysis.

---

## 13. Open-Source Components

MediaHarbor includes the following open-source libraries, used as dynamically linked, unmodified libraries under the GNU LGPL v2.1:

- **VLCKit** — © VideoLAN and authors
- **AMSMB2** — © Amir Abbas Mousavian
- **libsmb2** — © Ronnie Sahlberg and contributors

These libraries handle video decoding and the SMB protocol on your device. They do not transmit data to their authors or to any third party. Full license text is available in the app under **Settings → About → Third-Party Software**.

---

## 14. Do Not Track

MediaHarbor is a native iOS application. It does not operate a web browser, does not engage in cross-site tracking, and does not respond to browser-based Do Not Track (DNT) signals. DNT is not applicable to this app's functionality.

---

## 15. Changes to This Policy

If I make material changes to this policy, I will update the "Last updated" date at the top of this page. For significant changes, I will also note the update in the app's release notes or in a post on [ianm.tech](https://www.ianm.tech).

Continued use of the app after changes are posted constitutes acceptance of the revised policy.

---

## 16. Governing Law

This Privacy Policy is governed by and construed in accordance with the laws of the State of Maryland, United States, without regard to conflict of law principles.

---

## 17. Contact

If you have questions about this Privacy Policy, use **About → Send Feedback** inside the app, or the [contact page](https://www.ianm.tech/contact/).
