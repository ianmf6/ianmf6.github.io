---
layout: single
title: "VA Compensation Calculator — Update 1.26.13"
date: 2026-10-15
categories: [VA Calculator]
tags: [va-disability-calculator, ios, release]
author_profile: true
---

Version 1.26.13 of the [VA Compensation Calculator](/va-compensation-calculator/) is now available on the App Store. It brings a new main screen — your rating and monthly pay in one summary card, with your tools as cards below — news in the app, new pay tables that arrive without an app update, and the 2027 pay rates with the 3.6% cost-of-living adjustment. It also fixes the pay rates on phones set to a calendar other than the Gregorian one.

## A new main screen

The main screen had grown into a long column of buttons. Now the top of the screen is one summary card: your combined rating and monthly compensation, any SMC, what your pending claims would bring, and how your combined value rounds. **See why** still opens the step-by-step.

Below it, each tool is a card that tells you where things stand before you open it:

- **My Disabilities** — how many conditions, and how many are pending
- **Claim Tracker** — your next event, like a C&P exam in 7 days
- **Symptom Log** — how many episodes, and when you last logged one
- **Dependents & SMC** — your dependents and SMC at a glance
- **Calculators & References** — Backpay, the Increase Finder and the rest

Prefer the old screen? Tap the grid button at the top left to switch to the classic layout, and tap it again to come back. The same switch is in **Settings → Main Screen**. The classic layout is the screen you know from earlier versions.

The new screen also works at the largest text sizes: the rating ring moves above the amount instead of squeezing both into one row. Its labels are darker and easier to read, and a card dims as you tap it, so you know the tap landed. If you're new to the app, the main screen starts with an **Add your first disability** button instead of a 0% ring.

## New pay tables, without an app update

VA's rates change every December 1, and until now new rates took an app update. Starting with 1.26.13, the app checks my server for new pay tables when you open it or come back to it, at most once an hour, and picks them up by itself.

The 2027 rates are already in. Social Security announced a 3.6% cost-of-living adjustment on October 14, and VA disability pay rises by the same 3.6% on December 1. The app switches to the 2027 rates by itself that day; to see yours now, tap the rate year on the main screen and pick 2027. VA hasn't published its own 2027 tables yet, so the app's are built the way VA builds them, a method that reproduces every VA table since 2019 to the cent. If VA's differ anywhere, the corrected tables reach the app without an update.

Each set of tables is signed with a key only I hold, and the app checks the signature and the tables themselves before using them. If anything doesn't check out, it keeps the rates it already has. The check sends nothing about you; the [privacy policy](/va-compensation-calculator/privacy/) has the details.

The rate year now follows the year VA is paying: on December 1 the app switches to the new year's rates by itself. You can still pick any year from 2018 on to compare. If you had picked a year before this update, the app clears it once and starts from the current year.

## News in the app

When there's something worth knowing — the COLA announcement, a VA change, an app update — I'll post it in the app. A megaphone appears at the top left of the main screen when there's a post, with a dot for ones you haven't read. Something important also shows as a banner above your summary card until you read or close it. Some posts have a button straight into the right tool, like the COLA Estimator.

And when a new version of the app is on the App Store, Settings says so, and the gear icon gets a dot.

## Phones set to another calendar

VA's pay rates change every December 1 with the cost-of-living adjustment, and the app picks the rate table by year. On a phone set to the Buddhist calendar — the default in Thailand, where this is the year 2569 — or to the Japanese, Islamic or Persian calendar, the app read the year from the phone's calendar instead of VA's:

- **Backpay** could price every month at the wrong year's rates. On the Buddhist calendar, every month used the newest table, so a 2025 month at 100% came out $3,938.58 instead of $3,831.30.
- The **Pay Date Predictor** could label months in the phone's calendar ("Shawwal 1446" for what is April 2025) and get pay dates wrong.
- On the Japanese, Islamic or Persian calendar, the **main screen** opened on 2025 rates instead of 2026.

All three now use the Gregorian calendar VA uses, whatever your phone is set to. If your phone uses the Gregorian calendar, as almost every phone in the US does, your numbers don't change.

## Also

Various bug fixes and improvements.

As always: your VA information stays on your device and under your control. If something's off or you have an idea, tap **?** → **Contact Me** and tell me.
