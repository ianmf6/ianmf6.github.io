---
layout: single
title: "VA Compensation Calculator — Update 1.26.5"
date: 2026-05-02
categories: posts
tags: [va-disability-calculator, ios, release]
author_profile: true
---

Version 1.26.5 of the [VA Compensation Calculator](/va-disability-calculator-ios-app/) is now available on the App Store. This release adds two of the most-requested features — a **Backpay Calculator** and **Special Monthly Compensation** support — alongside historical rates back to 2018, a corrected 2026 rate table, and a fix for the 0% disability regression.

## What's New

### Backpay Calculator

You can now estimate retroactive compensation across a timeline of rating changes. Build out the timeline of when your ratings changed, and the app calculates the backpay you would be owed for each segment, with full **SMC** support included in the math.

### Special Monthly Compensation (SMC)

The calculator now supports the most common SMC categories — **SMC-K, S, L, R1, and R2** — so you can model compensation for cases that go beyond the standard combined-rating math.

### Historical Rates Back to 2018

The year picker now goes all the way back to **2018**, so you can run calculations against any year's COLA-adjusted rate table. This pairs naturally with the Backpay Calculator when reconstructing compensation for past periods.

### 2026 Rate Correction

The 2026 compensation rates have been corrected to match the latest values published on [VA.gov](https://www.va.gov). If you ran 2026 estimates in an earlier build, re-running them in 1.26.5 will give you the updated numbers.

### 0% Disability Regression Fixed

The 1.26.4 hotfix unintentionally re-broke the ability to add 0% rated disabilities. That regression is fixed in this release — 0% conditions can again be added in any of the Rated, Pending, and Denied statuses.

### Refinements

A few smaller improvements round out the release:

  - The year picker on the main screen now hides automatically outside the December–February COLA window. A Settings toggle lets you keep it visible year-round if you prefer.
  - The Help screen has been reorganized into three sections: **What's New**, **How to Use**, and **Help**. Links to the r/VeteransBenefits community and the Knowledge Base are included for when you want to dig deeper.
  - Some small UI changes and fixes throughout the app.

---

As always, all data remains stored locally on your device and is never transmitted to external servers. The Backpay Calculator, SMC inputs, and historical rate selections all run entirely on-device.

For questions or feedback, use the [contact page](https://www.ianm.tech/contact/).
