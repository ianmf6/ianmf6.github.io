---
layout: single
title: "Privacy Policy — VA Compensation Calculator"
permalink: /va-compensation-calculator/privacy/
# Old privacy URLs are kept alive as redirects — the App Store listing and any
# external links still point at them. Revisit removing after ~July 2027.
redirect_from:
  - /privacy-policy-va-compensation-app/
  - /privacy-policy-va-disability-app/
author_profile: true
toc: true
toc_label: "On this page"
---

**Effective date:** November 7, 2025  
**Last updated:** July 14, 2026  

---

## 1. Introduction

VA Compensation Calculator is an independent iOS application developed and maintained by Ian Marrero ("I," "me," or "my"). This Privacy Policy explains what data the app collects, how it is stored, and your rights as a user.

This app is designed with a privacy-first philosophy: all data you enter stays on your device under your control. I do not collect, transmit, or have access to any information you enter into the app. The only data the app sends off your device is anonymous, non-identifying usage analytics — described in Section 2 — which never include anything you enter and which you can turn off at any time.

---

## 2. Information Collected

### User-entered data

All disability ratings, dependent information, and settings you enter into VA Compensation Calculator are stored locally on your device at `Documents/userData.json` within the app's data container. This data is never transmitted off your device by the app.

Because data is stored in the app's Documents directory, it may be accessible via iTunes or Finder file sharing when your device is connected to a computer, and may be visible through the iOS Files app depending on your device settings. You can review your stored data at any time within the app via Settings → Data Management → View Saved Data.

I do not collect, receive, or have access to this data at any time.

### Analytics

The app collects a small amount of **anonymous, first-party usage analytics** so I can see which features are used and prioritize improvements. This is **on by default**, and you can turn it off at any time in **Settings → Analytics → Share anonymous usage**.

There are **no third-party analytics tools, advertising networks, crash reporters, or tracking SDKs** in the app. The analytics are sent only to a server I operate; they are never shared with, sold to, or accessible by any third party.

**What is collected:**

- A **random install identifier** — a value generated on your device that is not derived from and cannot be linked to your identity, your Apple ID, your name, or any device hardware identifier. It is stored on your device and is **permanently erased if you delete the app** (reinstalling generates a new, unrelated identifier).
- The **app version**.
- **Which screens and tools you open**, and a few in-app actions (for example, that a calculation was run or a PDF was exported), drawn from a fixed list of feature names.
- **How long** the app was in use and roughly how long each screen was open (durations in seconds).
- **Anonymous reliability counts** — that a crash, hang, or failed export occurred. Only the count is sent: no stack traces, no error messages, no device details.
- A **timestamp** for each event.

**What is never collected:**

- Anything you enter — disability names, ratings, percentages, dependents, notes, or dollar amounts.
- Your name, email, Apple ID, or any contact information.
- Your location — neither precise nor general. No IP-based geolocation is performed or stored.
- Advertising identifiers (IDFA), the device vendor identifier (IDFV), or your device model.

Because this data contains no identifying information and is never combined with data from other apps or with data from data brokers, it is **not used to track you** as "tracking" is defined by Apple's App Tracking Transparency framework, and the app does not present a tracking-permission prompt.

**Turning analytics off:** when you switch "Share anonymous usage" off, the app sends a single anonymous signal recording that analytics were disabled, and then sends nothing further. This lets me count how many people opt out without ever identifying them. While analytics are off, no usage data of any kind leaves your device.

### Crash reporting

I do not integrate any crash-reporting SDK. The app uses Apple's on-device **MetricKit** framework solely to *count* crashes and hangs; those counts are part of the anonymous analytics described above and carry no stack traces, no error contents, and no device details — and they stop entirely if you turn analytics off. Separately, Apple may provide me with aggregate, anonymized crash statistics through App Store Connect if you have opted in to sharing diagnostics with developers in your iOS settings; that data is collected and anonymized by Apple, governed by **Apple's Privacy Policy**, and I never receive information that identifies you.

### Support and feedback submissions

The website's contact and feedback form is powered by **Google Forms**, a third-party service operated by Google LLC. When you submit a form, your response is transmitted to and stored on Google's servers, governed by **Google's Privacy Policy** and terms of service. I do not control Google's data infrastructure or retention practices.

You may voluntarily provide personal information in a form submission, including your name, email address, or written messages. Because this app serves veterans managing disability-related information, some users have chosen to include sensitive details such as disability ratings, health conditions, or other personal information in their messages. The form includes an explicit notice advising users not to submit sensitive personal or medical information beyond what is necessary. **You are not required to share this information.**

Your email address is used solely to reply to your message. It is not used for marketing, stored in any system I own or operate, or shared with any third party. I do not store submission content in any personally owned database or storage system beyond what Google Forms retains.

---

## 3. iCloud Backup and File Access

If you have iCloud Backup enabled on your device (the iOS default), Apple will include your app's `Documents/userData.json` file as part of your device backup. This backup is stored on Apple's servers and governed entirely by **Apple's Privacy Policy**, not by this policy.

The app does not control whether your data is included in iCloud backups. You can manage backup settings at any time in **Settings → [Your Name] → iCloud → iCloud Backup**, or exclude this app specifically in **Settings → [Your Name] → iCloud → Show All** and toggling off VA Compensation Calculator.

Additionally, because data is stored in the app's Documents directory, it may be transferable via iTunes or Finder file sharing when your device is connected to a computer. This is an iOS system-level behavior outside the app's control.

I do not have access to your iCloud backup data or any file transfers you make under any circumstances.

---

## 4. Sharing and Copying Your Data

### Compensation Breakdown Share

The app includes an optional feature that allows you to share a summary of your compensation breakdown using the native iOS share sheet. This feature is entirely user-initiated and user-controlled. The app does not transmit any data to me or any third party — you choose where the output goes (Messages, Mail, clipboard, etc.).

Before sharing, you are presented with a **Share Options screen** that gives you control over what is included:

- **Redact disability names** (enabled by default) — replaces your specific condition names with generic labels (e.g., "Disability 1") in the shared output
- **Include dependent information** (enabled by default) — includes marital status, spouse Aid & Attendance, and dependent counts in the shared output

The shared output may contain sensitive health information including disability ratings, percentages, dependent status, and estimated monthly compensation. **You are responsible for where you direct this information once it leaves the app.** Once shared to a third-party service (such as Messages, Mail, or any other app), that service's own privacy policy governs the data.

I recommend using the "Redact disability names" toggle if you are sharing with anyone other than a trusted individual such as a VSO or benefits attorney.

### Saved Data Copy

The Settings → Data Management → View Saved Data screen includes a **Copy** button that copies your full saved data — including disability names, ratings, dependent information, and raw JSON — to your device's clipboard. Clipboard contents on iOS may be accessible to other apps. Exercise caution when copying sensitive data if untrusted apps are installed on your device.

---

## 5. Tips (In-App Purchases)

The app includes an optional **Tip Jar** that lets you support development through Apple's **In-App Purchase** system. Tipping is entirely optional, unlocks no features, and can be ignored — the app remains free and ad-free either way.

Tips are processed by **Apple**. The app never sees or handles your payment card details, billing address, or Apple ID. I receive only aggregate, anonymized sales and payout information through App Store Connect (for example, how many tips of each amount were purchased), which never identifies you. All payment processing and any personal information involved are governed by **Apple's Privacy Policy**.

---

## 6. Data Sharing

I do not sell, rent, or share your personal data with advertising networks, data brokers, or other external services for commercial purposes. There are no third-party SDKs embedded in the app that collect data.

Aside from the anonymous usage analytics described in Section 2 — which are sent to a server I operate, contain no identifying information, and can be turned off — the app does not transmit your data off your device. In addition, two third-party services are accessible through this app and its associated website:

- **Google Forms** (support/feedback contact): Form responses are stored on Google's servers. Google's privacy policy governs this data.
- **Apple In-App Purchase** (optional Tip Jar): tips are processed by Apple; your payment details are handled entirely by Apple and governed by Apple's privacy policy.

Your use of these services is voluntary. I do not receive personal information from either service in any storage I own or operate.

---

## 7. Data Security

Data is stored in a local JSON file within the app's sandboxed data container. The app applies iOS **Complete File Protection** to this file, so it is **encrypted at rest whenever your device is locked** and cannot be read — even with physical access to the device — until it is unlocked with your passcode, Face ID, or Touch ID.

The app also offers an optional **biometric lock** (Settings → Privacy) that requires Face ID or Touch ID to open the app and re-locks it whenever it moves to the background.

Device-level security remains the foundation, and I strongly recommend using a passcode together with Face ID or Touch ID. Because Complete File Protection keeps the file readable only while the device is unlocked, the main residual risk is a device that is lost or stolen *while already unlocked*; that risk is managed at the device level.

---

## 8. Data Retention and Deletion

Your data persists on your device until you delete it. You have full control:

- **Delete individual entries** within the app using the app's data management tools (Settings → Data Management).
- **Clear all app data** using the clear data options in the app's Settings view.
- **Uninstall the app** to permanently remove all locally stored data from your device.

I do not retain any copy of your data. Deleting the app removes all locally stored data from your device. If iCloud Backup has previously backed up your data, you can manage or delete those backups through Apple's iCloud settings.

---

## 9. Children's Privacy

Because VA Compensation Calculator does not collect any personal data from any user, no personal data is collected from children under 13. The app is intended for use by veterans and their families and does not knowingly target children.

---

## 10. Do Not Track

VA Compensation Calculator is a native iOS application. It does not operate a web browser, does not engage in cross-site tracking, and does not respond to or honor browser-based Do Not Track (DNT) signals. DNT signals are not applicable to this app's functionality.

---

## 11. Your Privacy Rights

The anonymous usage analytics described in Section 2 contain no information that identifies you, so there is no way to link them back to an individual to access, correct, export, or delete on a per-person basis; you control whether they are collected at all using the opt-out in **Settings → Analytics**, and deleting the app erases the random identifier entirely. Apart from those anonymous analytics, VA Compensation Calculator does not collect or hold any personal data, so there is no personal data held by me to access, correct, export, or delete. All data you enter into the app is under your direct control on your device.

If you have submitted a support inquiry through the website contact form, you may request that I delete any correspondence I have on file by contacting me through the [contact page](https://www.ianm.tech/contact/).

Residents of California and other states with comprehensive privacy laws should be aware that I do not sell or share personal information, do not engage in targeted advertising, and do not meet the revenue or data volume thresholds that trigger obligations under the California Consumer Privacy Act (CCPA/CPRA) or similar state laws. The privacy protections in this policy apply to all users regardless of location.

---

## 12. Third-Party AI

VA Compensation Calculator does not share your data with any third-party AI systems, machine learning platforms, or external services. All calculations are performed locally on your device using the official VA incremental formula.

---

## 13. Disclaimer of Accuracy

VA Compensation Calculator is provided for **informational and estimation purposes only**. It is not affiliated with, endorsed by, or officially connected to the U.S. Department of Veterans Affairs.

Compensation estimates produced by this app are approximations based on publicly available VA rate tables and calculation formulas. The VA's official determination of your disability rating and compensation amount is authoritative. Do not make legal, financial, or medical decisions based solely on results from this app. For official ratings and benefits determinations, contact the VA directly at [va.gov](https://www.va.gov).

---

## 14. Changes to This Policy

If I make material changes to this policy, I will update the "Last updated" date at the top of this page. For significant changes, I will also note the update in the app's "What's New" section or in a post on [ianm.tech](https://www.ianm.tech).

Continued use of the app after changes are posted constitutes acceptance of the revised policy.

---

## 15. Governing Law

This Privacy Policy is governed by and construed in accordance with the laws of the State of Maryland, United States, without regard to conflict of law principles.

---

## 16. Contact

If you have questions about this Privacy Policy, please use the [contact page](https://www.ianm.tech/contact/).
