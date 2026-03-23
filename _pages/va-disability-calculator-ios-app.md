---
permalink: /va-disability-calculator-ios-app/
title: "VA Disability Calculator iOS App"
last_modified_at: 2026-03-22T00:00:00-04:00

toc: true
toc_label: "On this page"
toc_sticky: true

gallery:
  - url: /assets/images/va-disability-app-images/screenshot-1.png
    image_path: /assets/images/va-disability-app-images/screenshot-1.png
    alt: "Home screen showing combined VA rating"
    title: "Home - Combined Rating"
  - url: /assets/images/va-disability-app-images/screenshot-2.png
    image_path: /assets/images/va-disability-app-images/screenshot-2.png
    alt: "Disabilities list with bilateral conditions"
    title: "Disabilities"
  - url: /assets/images/va-disability-app-images/screenshot-3.png
    image_path: /assets/images/va-disability-app-images/screenshot-3.png
    alt: "Dependent information screen"
    title: "Dependents"
  - url: /assets/images/va-disability-app-images/screenshot-4.png
    image_path: /assets/images/va-disability-app-images/screenshot-4.png
    alt: "Compensation breakdown with step-by-step calculation"
    title: "Compensation Breakdown"
  - url: /assets/images/va-disability-app-images/screenshot-5.png
    image_path: /assets/images/va-disability-app-images/screenshot-5.png
    alt: "Share options with privacy redaction"
    title: "Share Options"
  - url: /assets/images/va-disability-app-images/screenshot-6.png
    image_path: /assets/images/va-disability-app-images/screenshot-6.png
    alt: "Saved data viewer with JSON export"
    title: "Saved Data"
  - url: /assets/images/va-disability-app-images/screenshot-7.png
    image_path: /assets/images/va-disability-app-images/screenshot-7.png
    alt: "About screen with changelog and usage guide"
    title: "About This App"
  - url: /assets/images/va-disability-app-images/screenshot-8.png
    image_path: /assets/images/va-disability-app-images/screenshot-8.png
    alt: "Settings screen with data management"
    title: "Settings"

---

## Overview

The VA Disability Calculator helps veterans calculate their combined VA disability rating using the official formula from 38 CFR 4.25 and 4.26. It estimates monthly compensation based on 2025 and 2026 rate tables, shows both raw and VA-rounded percentages, and keeps all data stored locally on your device. No ads, no accounts, no data collection.

[![App Store link](/assets/images/va-disability-app-images/download-on-the-app-store.svg)](https://apps.apple.com/us/app/va-compensation-calculator/id6746081239?mttnsubad=6746081239)

## Key Features

**Official VA Math Engine**
Combines multiple disability ratings step-by-step using the VA Combined Ratings Table, not simple addition.

**Bilateral Factor Support**
Automatically applies the 10% bilateral factor when both sides of an extremity are rated (left knee + right knee, etc.) per 38 CFR 4.26.

**Accurate Compensation Estimates**
Accounts for spouse, spouse Aid & Attendance, parents (0–2), children under 18, and children 18–24 in school.

**Compensation Breakdown**
Step-by-step calculation transparency showing exactly how your rating is combined and your compensation is determined.

**Shareable Breakdown**
Share your rating breakdown with privacy options to redact disability names and hide dependent information.

**Dependents Manager**
Tracks marital status, spouse A&A, parent dependents, and children with links to official VA resources.

**Year Selector**
Supports 2025 and 2026 COLA rates (2.8% increase) with future update capability.

**100% Private**
All data stays on your device. Nothing is uploaded or shared. No accounts, no ads, no tracking.

## Screenshots

<style>
figure.third {
  display: flex !important;
  flex-wrap: wrap !important;
  justify-content: center !important;
  gap: 6px !important;
}
figure.third > a {
  flex: 0 0 30% !important;
  max-width: 30% !important;
  margin: 0 !important;
  width: auto !important;
}
figure.third img {
  border-radius: 8px;
  box-shadow: 0 1px 4px rgba(0,0,0,0.15);
  width: 100% !important;
  height: auto !important;
}
</style>

{% include gallery caption="Screenshots" layout="third" %}

## Version History

<strong>v1.26.2 — March 2026</strong>
  - Share your rating breakdown with privacy options to redact disability names and hide dependent info
  - Cleaner Compensation Breakdown with less clutter and clearer wording
  - Smarter input validation when adding disabilities
  - Fixed breakdown showing incorrect combined percentage before rounding

<strong>v1.26.1 — March 2026</strong>
  - Redesigned bilateral condition entry — each side entered individually for more accurate tracking
  - Bilateral factor only applied when both sides of an extremity group are present
  - Fixed compensation calculation for children ages 18–24 in school
  - Fixed issue where deleting a condition could remove the wrong entry

<strong>v1.26.0 — May 2025</strong>
  - Enhanced settings with JSON data viewer
  - 2026 COLA rate support (2.8% increase)
  - Bilateral factor support (38 CFR 4.26)
  - Improved calculation accuracy

## Technical Details

| Field | Value |
|---|---|
| Current Version | 1.26.2 |
| Platform | iOS 16.6+ |
| Framework | SwiftUI |
| Price | Free |
| Dependencies | None |
| Data Storage | On-device only (JSON) |
| App Store ID | [6746081239](https://apps.apple.com/app/id6746081239) |

## Disclaimer

This app is not affiliated with the U.S. Department of Veterans Affairs. It is an independent tool for estimation purposes only. Always verify your rating and compensation with the VA directly.

**Privacy First**
All data stays on your device and under your control.

## Privacy Policy
[Privacy Policy](/privacy-policy-va-disability-app/)

## Support
For support or to report issues with the app, use the [Contact](/contact/) page.
