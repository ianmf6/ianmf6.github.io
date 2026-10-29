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
**Last updated:** October 29, 2026  

---

## 1. Introduction

VA Compensation Calculator is an independent iOS application developed and maintained by Ian Marrero ("I," "me," or "my"). This Privacy Policy explains what data the app collects, how it is stored, and your rights as a user.

This app is designed with a privacy-first philosophy: all data you enter stays on your device under your control. I do not collect, transmit, or have access to the VA information you enter into the app. Apart from messages you choose to send me through Contact Me, and, starting with version 1.27.1, what your iPhone shares with your own Apple Watch, the only data the app sends off your device is anonymous, non-identifying usage analytics — described in Section 2 — which never include anything you enter and which you can turn off at any time. The app also checks my server for new pay tables, news, Claim Finder lists, military job lists and app versions (the "Update check" in Section 2); those requests send nothing about you.

---

## 2. Information Collected

### User-entered data

All disability ratings, dependent information, and settings you enter into VA Compensation Calculator are stored locally on your device at `Documents/userData.json` within the app's data container. This data is never transmitted off your device by the app, except what your iPhone shares with your own Apple Watch, starting with version 1.27.1 (see "Apple Watch" below).

That includes **My Profile** (starting with version 1.27.0): your dependents, your Special Monthly Compensation and TDIU, and your military service, meaning the jobs you look up in Military Job Lookup, where you served and what you did. It also includes the answers you give the welcome screen's questions and anything you mark in the Claim Finder or in "What you may be able to claim". The Claim Finder and Military Job Lookup work entirely on your device, from lists that ship with the app or arrive through the update check below. VA never sees any of it, and I don't either.

Starting with version 1.27.1, your saved data also includes what you enter in **Survivor Benefits** under "For your family": the month your 100% or TDIU rating began, the month you married, whether you've been rated that way since you left active duty, whether you're a former prisoner of war, and how many of your children are 18 or older and became disabled before 18. These are stored in `userData.json` with the rest of your data and never sent. The answers you give under "For a survivor" aren't saved at all: they're kept only while that screen is open.

Because data is stored in the app's Documents directory, it may be accessible via iTunes or Finder file sharing when your device is connected to a computer, and may be visible through the iOS Files app depending on your device settings. You can review your stored data at any time within the app via Settings → Data Management → View Saved Data.

I do not collect, receive, or have access to this data at any time.

### Widgets

Starting with version 1.27.0, the app has widgets for your Home Screen and Lock Screen. To draw them, the app saves a small summary in a container on your device that only the app and its widget can read: your combined rating, your monthly pay, your next pay date and your next Claim Tracker event. It never includes a disability's name, a note or an event's title (an event shows only its type, like "C&P exam"), and while App Lock is on it holds no numbers at all, so the widget shows a lock. The widget sends nothing anywhere.

### Apple Watch

Starting with version 1.27.1, the app comes with an Apple Watch app. When the watch app is installed on your paired Apple Watch, your iPhone sends it what it shows, over Apple's WatchConnectivity, the system's own link between an iPhone and its paired watch. It goes only to your own watch, and none of it comes to me.

- **What your iPhone sends your watch:** the same summary the widgets use (your combined rating and monthly pay, and your rating and pay with pending claims), plus the titles and dates of your upcoming Claim Tracker events and the names and diagnostic codes of your disabilities, so you can pick one when you log a symptom episode. It also sends the random IDs of the episodes from the watch that it has already saved.
- **What your watch keeps:** the latest summary your iPhone sent, which each new one replaces; an episode while you're timing it; and the episodes you've logged on the watch, until your iPhone has saved them. They stay on your watch, in storage only the watch app and its complications can read, encrypted until the watch is first unlocked after it starts up.
- **What your watch sends back:** each episode you log on it: which condition it was for, when it started, how long it lasted, how bad it was, whether a migraine was prostrating, any care you sought, and whether the "Log a migraine" shortcut started it. Your iPhone adds it to your Symptom Log, where you can change or delete it like any other episode, and the watch then deletes its copy. The watch also tells your iPhone the last day you opened the watch app, for the count described below.
- **With App Lock on:** your iPhone sends your watch only a lock and those episode IDs: no numbers and no names. The watch app and the watch face show a lock instead, and the "Log a migraine" shortcut won't start an episode. In the watch app, an episode you were timing when App Lock went on still shows, as "Episode" without its condition's name, so you can end it.
- **On your watch face:** the complications show your rating, your monthly pay, your next pay date or your next Claim Tracker date by its type (like "C&P in 6 days"), and an episode's timer while one runs. They never show a disability's name or an event's title.
- **No servers:** the watch app never contacts any server. It talks only to your iPhone.
- **Analytics:** if analytics are on, your iPhone counts, in the anonymous analytics described below, that you used the watch app (once a day), that an episode from the watch reached your Symptom Log, and that the "Log a migraine" shortcut started it. Never what you logged. The watch itself sends no analytics.

### Analytics

The app collects a small amount of **anonymous, first-party usage analytics** so I can see which features are used and prioritize improvements. This is **on by default**, and you can turn it off at any time in **Settings → Analytics → Share anonymous usage**.

There are **no third-party analytics tools, advertising networks, crash reporters, or tracking SDKs** in the app. The analytics are sent only to a server I operate, over an encrypted connection through Cloudflare, which carries the traffic to my server; they are never shared with, sold to, or accessible by any third party.

**What is collected:**

- A **random install identifier** — a value generated on your device that is not derived from and cannot be linked to your identity, your Apple ID, your name, or any device hardware identifier. It is stored on your device and is **permanently erased if you delete the app** (reinstalling generates a new, unrelated identifier).
- The **app version**.
- **Which screens and tools you open**, and **which features, choices and settings you use**: for example, that a calculation was run or a PDF was exported, which of the welcome screen's three choices you picked, that a condition was marked in "What you may be able to claim" and with which mark, the status a disability was added with or changed to (rated, pending, might file or denied), that a resource on the Support & Community screen was opened (never which one, and nothing at all for the Veterans Crisis Line), that a date was added in Survivor Benefits (never the date), or that you switched to dark mode. These come from a fixed list of feature names and record only that something was used, never what you entered: not the condition, its rating, your dependents, your SMC or TDIU, your job, where you served or what you did.
- **How long** the app was in use and roughly how long each screen was open (durations in seconds).
- **Anonymous reliability counts** — that a crash, hang, or failed export occurred. Only the count is sent: no stack traces, no error messages, no device details.
- A **timestamp** for each event.

**What is never collected:**

- Anything you enter — disability names, ratings, percentages, dependents, notes, dollar amounts, or your military service (jobs, where you served, what you did).
- Your name, email, Apple ID, or any contact information.
- Your location — neither precise nor general. No IP-based geolocation is performed or stored.
- Advertising identifiers (IDFA), the device vendor identifier (IDFV), or your device model.

Because this data contains no identifying information and is never combined with data from other apps or with data from data brokers, it is **not used to track you** as "tracking" is defined by Apple's App Tracking Transparency framework, and the app does not present a tracking-permission prompt.

**Turning analytics off:** when you switch "Share anonymous usage" off, the app sends a single anonymous signal recording that analytics were disabled, and then sends nothing further. This lets me count how many people opt out without ever identifying them. While analytics are off, no usage data of any kind leaves your device.

### Update check (pay tables, news, lists and app version)

Starting with version 1.26.13, when you open the app, and when you return to it (at most once an hour), the app downloads a small file from a server I operate (apps.ianm.tech). The file says what's newest: the current version of the app on the App Store, the latest compensation pay tables, the latest news posts, and, starting with version 1.27.0, the latest Claim Finder lists (the conditions VA presumes after certain service, and those often claimed together), military job lists (what Military Job Lookup searches), and the Support & Community resources (the phone numbers and links on that screen). When something is newer than what the app already has, the app downloads it too. This is how new VA rates, for example after the yearly cost-of-living adjustment, a change to VA's lists, a changed phone number, and news reach the app without an app update.

These requests **send nothing about you**: no identifier, no analytics, nothing you entered, and no cookies. They are plain downloads of the same public files every user gets. As with any connection to a website, your IP address is visible to the server and to Cloudflare, which carries the traffic to it. The server's logs don't keep IP addresses. The update check runs whether or not analytics are on, because it isn't analytics: it's how the app gets current rates.

Pay tables, news, the Claim Finder lists, the job lists and the support resources are all signed with a key only I hold, and the app checks the signature and the contents before using any of them. If anything doesn't check out, the app ignores the download and keeps what it already has.

### Crash reporting

I do not integrate any crash-reporting SDK. The app uses Apple's on-device **MetricKit** framework solely to *count* crashes and hangs; those counts are part of the anonymous analytics described above and carry no stack traces, no error contents, and no device details — and they stop entirely if you turn analytics off. Separately, Apple may provide me with aggregate, anonymized crash statistics through App Store Connect if you have opted in to sharing diagnostics with developers in your iOS settings; that data is collected and anonymized by Apple, governed by **Apple's Privacy Policy**, and I never receive information that identifies you.

### Support and feedback submissions

You can write to me from the app (**? → Contact Me**) or from the [contact page](https://www.ianm.tech/contact/) on this website. Both send your message to a server I operate, not to Google or any other form service. It travels over an encrypted connection through Cloudflare, which carries the traffic to my server.

A message carries what you type into the form: your message, its topic, your name, and your email address if you give one (in the app, the name is optional too). A message from the app also carries the app's version, your iOS version, and a one-way ID that groups your own messages together. That ID is deliberately separate from the analytics ID described above, so a message can't be linked to how you use the app. A message from the website form carries a random ID that changes with every message instead.

Messages are stored on my server, and only I have access to them. When one arrives, I get a notification through Discord that says which app it's about, its topic and the app version, never its text, your name or your email address.

Your email address is used only to reply to you. It is never used for marketing or shared with anyone. Because this app serves veterans, please don't include medical details or anything from your VA file in a message. **You are not required to share any of this.** Section 8 says how long messages are kept, and Section 11 how to have yours deleted.

---

## 3. iCloud Backup and File Access

If you have iCloud Backup enabled on your device (the iOS default), Apple will include your app's `Documents/userData.json` file as part of your device backup. This backup is stored on Apple's servers and governed entirely by **Apple's Privacy Policy**, not by this policy.

The app does not control whether your data is included in iCloud backups. You can manage backup settings at any time in **Settings → [Your Name] → iCloud → iCloud Backup**, or exclude this app specifically in **Settings → [Your Name] → iCloud → Show All** and toggling off VA Compensation Calculator.

Additionally, because data is stored in the app's Documents directory, it may be transferable via iTunes or Finder file sharing when your device is connected to a computer. This is an iOS system-level behavior outside the app's control.

I do not have access to your iCloud backup data or any file transfers you make under any circumstances.

---

## 4. Sharing and Copying Your Data

### Sharing as Text or PDF

The app can share what you've entered as text or a PDF using the native iOS share sheet: from **Rating & Pay** ("Share as text or PDF"), from **My Profile** ("Share a summary", a summary for a VSO, an attorney or your family), from the **Backpay** results and from the **Symptom Log** report. Sharing is entirely user-initiated and user-controlled. The app does not transmit any data to me or any third party — you choose where the output goes (Messages, Mail, Files, a printer, etc.).

Before sharing, you see a live preview of exactly what will be shared, and you choose what goes in:

- **Rating & Pay:** **Redact disability names** (off by default) replaces your condition names with generic labels (e.g., "Disability 1"), and **Include dependent information** (on by default) includes marital status, spouse Aid and Attendance and dependent counts. What's shared follows the screen: if you switched on your pending claims or the claims you might file there, they're included.
- **Share a summary:** a switch for each part that has something in it: your disabilities and claims, your rating and pay, your dependents, your military service (your jobs, where you served and what you did), your Claim Tracker dates (with the titles and places you entered), a summary of the last 90 days of your Symptom Log, and your notes on each disability (off by default).

A PDF is written to the app's temporary folder with the same file protection as your saved data and deleted when the share sheet closes.

The shared output may contain sensitive health information including disability ratings, percentages, claims, dependent status, military service and estimated monthly compensation. **You are responsible for where you direct this information once it leaves the app.** Once shared to a third-party service (such as Messages, Mail, or any other app), that service's own privacy policy governs the data.

I recommend using the "Redact disability names" switch, or leaving parts of the summary out, if you are sharing with anyone other than a trusted individual such as a VSO or benefits attorney.

### Saved Data Copy

The Settings → Data Management → View Saved Data screen includes a **Copy** button that copies your full saved data — including disability names, ratings, dependent information, and raw JSON — to your device's clipboard. Clipboard contents on iOS may be accessible to other apps. Exercise caution when copying sensitive data if untrusted apps are installed on your device.

---

## 5. Tips (In-App Purchases)

The app includes an optional **Tip Jar** that lets you support development through Apple's **In-App Purchase** system. Tipping is entirely optional, unlocks no features, and can be ignored — the app remains free and ad-free either way.

Tips are processed by **Apple**. The app never sees or handles your payment card details, billing address, or Apple ID. From Apple, I receive only aggregate, anonymized sales and payout information through App Store Connect (for example, how many tips of each amount were purchased), which never identifies you. All payment processing and any personal information involved are governed by **Apple's Privacy Policy**.

If the anonymous usage analytics described in Section 2 are on, the app also records the Tip Jar steps you take, such as opening it, choosing an amount, or cancelling Apple's payment sheet, and, starting with version 1.26.13, which size of tip was completed (Small, Coffee, Lunch or Dinner). These are anonymous events like the rest: they carry no payment details and nothing that identifies you, and they stop when analytics are off.

---

## 6. Data Sharing

I do not sell, rent, or share your personal data with advertising networks, data brokers, or other external services for commercial purposes. There are no third-party SDKs embedded in the app that collect data.

Aside from what Section 2 describes, the app does not transmit your data off your device. That's the anonymous usage analytics (no identifying information, and you can turn them off), the update check (which sends nothing about you), and any message you choose to send me. All three go to a server I operate. One third-party service is accessible through this app:

- **Apple In-App Purchase** (optional Tip Jar): tips are processed by Apple; your payment details are handled entirely by Apple and governed by Apple's privacy policy.

Your use of it is voluntary. I do not receive personal information from Apple in any storage I own or operate.

### Links and videos

Some screens and News posts link to websites, like VA.gov and this one. They open in your browser, the app sends them nothing, and each has its own privacy policy.

The page on this website that previews new versions ([What's coming in VA Compensation Calculator](/va-compensation-calculator/whats-new/)) shows a video hosted on YouTube. Nothing loads from YouTube until you press play. Once you do, the video plays in YouTube's own player: YouTube (Google) receives your IP address and browser details and may set cookies, under [Google's Privacy Policy](https://policies.google.com/privacy). The same applies if you watch the video in the YouTube app or on youtube.com.

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

I do not retain any copy of the data you keep in the app. Deleting the app removes all locally stored data from your device. If iCloud Backup has previously backed up your data, you can manage or delete those backups through Apple's iCloud settings.

Messages you send me through Contact Me or the contact page are the exception. They're kept on my server so I can read and answer them, until I delete them. A deleted message also leaves my server's backups as those rotate out.

---

## 9. Children's Privacy

Because VA Compensation Calculator does not collect any personal data from any user, no personal data is collected from children under 13. The app is intended for use by veterans and their families and does not knowingly target children.

---

## 10. Do Not Track

VA Compensation Calculator is a native iOS application. It does not operate a web browser, does not engage in cross-site tracking, and does not respond to or honor browser-based Do Not Track (DNT) signals. DNT signals are not applicable to this app's functionality.

---

## 11. Your Privacy Rights

The anonymous usage analytics described in Section 2 contain no information that identifies you, so there is no way to link them back to an individual to access, correct, export, or delete on a per-person basis; you control whether they are collected at all using the opt-out in **Settings → Analytics**, and deleting the app erases the random identifier entirely. Apart from those anonymous analytics and any message you send me, VA Compensation Calculator does not collect or hold any personal data, so there is no other personal data held by me to access, correct, export, or delete. All data you enter into the app is under your direct control on your device.

If you have sent me a message through Contact Me in the app or the website's contact page, you may ask me what I have on file from you, or ask me to delete it, through the [contact page](https://www.ianm.tech/contact/).

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
