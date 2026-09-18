---
layout: single
title: "VA Compensation Calculator — Update 1.26.11"
date: 2026-09-17
categories: [VA Calculator]
tags: [va-disability-calculator, ios, release]
author_profile: true
---

Version 1.26.11 of the [VA Compensation Calculator](/va-compensation-calculator/) was submitted to the App Store today and will roll out as soon as Apple approves it. This one adds **Backup & Restore**, an **Increase Finder**, and an **SMC Eligibility Screener** — and it comes out of the most thorough accuracy audit the app has had, with several fixes worth knowing about.

## Backup & Restore

Everything in this app lives in one file on your device with no account and no cloud sync. That's the privacy promise — but it also meant a lost or reset phone erased years of conditions and symptom-log evidence with no way back.

**Settings → Data Management → Export Backup** now saves everything — disabilities, dependents, SMC, TDIU, claim events, and your symptom log — to a single file *you* keep: Files, iCloud Drive, AirDrop to a computer, wherever you like. **Restore from Backup** brings it back on a new phone. Nothing is uploaded anywhere; where the file goes is entirely your pick.

## Increase Finder

A veteran asked for this almost word for word: *"I want to track all my disabilities so I can see which ones I want to apply for an increase."*

For each rated condition with a diagnostic code, the **Increase Finder** shows what the next rating step requires under 38 CFR — the paraphrased criteria — and what that one change would do to your combined rating and monthly pay, using the real Table I math and rate tables, sorted by impact. If a condition has no code yet, you can add one right from the screen. It's honest about its limits, too: a code the schedule rates from tables (hearing) or a retired code gets a plain explanation instead of a confident guess, and the footer carries the standard VSO warning — filing for an increase re-opens the rating.

## SMC Eligibility Screener

Special Monthly Compensation is the most under-claimed benefit in the system. Veterans carry SMC-K-qualifying conditions for years without knowing SMC exists, because nothing in the normal rating flow mentions it.

The **SMC Eligibility Screener** asks a handful of plain-language questions and points to the levels worth asking about — K, L and above, S, T — with the reason and the next step (usually VA Form 21-2680). One check is automatic: if your ratings contain a single 100% disability plus others that independently combine to 60%, that's the statutory-housebound formula under 38 U.S.C. 1114(s), and the app tells you so. Educational only — it never sets a level; only the VA can grant SMC.

## The math, explained where you're looking

"Your math is wrong" is the app's number-one support question, and it is almost always 38 CFR 4.25's round-to-nearest-10. The main screen now says it plainly — *"Combined value 83% rounds to 80%"* — and **See why** opens the step-by-step breakdown. It shows at 100% too, which was the case people asked about most ("95% rounds to 100%").

## Backpay: only the difference you're owed

Retro pay for an increase is the difference between the new rate and what the VA kept paying you meanwhile. A new **"Already being paid at"** option deducts the old rating month by month, so a 30% → 70% increase no longer shows the full 70% rate as backpay. Leave it at "Nothing yet" for an original claim and nothing changes. The notes about estimated months — before the 2018 rate table, or future months at today's rates — now travel with shared text and PDFs, not just the screen.

## Diagnostic codes, easier

- Add or change a disability's diagnostic code from its row on the Disabilities screen — previously a code could only be attached when a disability was first added.
- The code search now understands the names veterans actually use: **PTSD**, GERD, TBI, COPD, sleep apnea, carpal tunnel, flat feet, sciatica, "lumbar spine strain" — none of which appear in the schedule's formal titles.

## Contact Me

The in-app form now matches the website's: **Name** (optional), **Email** (optional), **Topic**, **Message**, with the same topic list everywhere. Leave the name and email blank to stay anonymous.

## Accuracy fixes

This release followed a full audit of the app's math, data, and law. The ones that changed a number:

- **Combined value vs. official rating.** The breakdown and the "need X% more" line were re-deriving the combined value with decimal math while the official rating uses the VA's integer table. Across a rounding boundary they could disagree — the app could show 93.59% under a 100% rating. Every displayed value now comes from the same table math.
- **SMC-K and the 1114(o) cap.** K awards are paid "in no event to exceed" the SMC-O rate, so K never adds on top of SMC-O and N½ + K awards stop at O. The app was stacking past the cap.
- **CRDP / CRSC** now show the *waived* retired pay being restored, not the full retired pay; CRSC also requires being a retiree.
- **38 CFR reference.** Eleven codes carried another code's name (for example 7326 is Crohn's disease, not diverticulitis; 6063 is loss of *one* eye), the heart criteria still showed pre-2021 text, and several formulas were corrected — spine, interstitial lung disease, flat foot, and the median/ulnar nerve ladders.
- **Reminders** now tell you when notifications are turned off for the app in iOS Settings, instead of silently never firing.

## Also

Various bug fixes and improvements throughout, including a safer data loader (a file from a newer version of the app no longer wipes your data on an older one).

As always: your VA information stays on your device and under your control. If something's off or you have an idea, tap **?** → **Contact Me** and tell me.
