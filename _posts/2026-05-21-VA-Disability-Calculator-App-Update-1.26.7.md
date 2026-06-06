---
layout: single
title: "VA Compensation Calculator — Update 1.26.7"
date: 2026-05-21
categories: posts
tags: [va-disability-calculator, ios, release]
author_profile: true
---

Version 1.26.7 of the [VA Compensation Calculator](/va-compensation-calculator/) is now available on the App Store.

The 38 CFR Diagnostic Codes reference now covers the complete VA schedule — over 700 codes pulled directly from the official eCFR. Plus per-percentage rating criteria, a "Most Claimed" shortcut to the conditions you actually search for, and a cleaner Neurological section.

## The full schedule, not just the curated subset

Previous releases shipped with a hand-curated reference of ~300 diagnostic codes — the ones I'd seen claimed most often. In 1.26.7, the dataset expands to the entire 38 CFR Part 4 schedule: every code across all 15 body systems, ingested directly from the eCFR XML. The curated entries are still there, with their hand-edited copy taking precedence; everything else now fills in around them.

If you've ever opened the lookup, searched for something a little unusual, and come up empty — that should stop happening.

## Per-percentage rating criteria

Each diagnostic code's detail view now shows what the VA actually requires for each rating band. For the most-claimed conditions (PTSD, sleep apnea, hypertension, diabetes, migraines, the full General Rating Formula for Mental Disorders, the Spine formula), the criteria are hand-edited for readability. For the rest of the 700+ codes, the criteria are extracted directly from the regulation.

## "Most Claimed" at the top

Tinnitus. Hearing loss. PTSD. Knee. Back. Sleep apnea. Hypertension. Migraine. Major depressive disorder. Sciatic nerve. Fibromyalgia. Diabetes. Disfiguring scars. Pes planus.

The fifteen codes that account for the bulk of VA claims now appear in a "Most Claimed" section at the top of the lookup, in approximate frequency order. One tap instead of scrolling through 15 body systems to find the one you came in for.

## Tap to add as a disability

From any code's detail view, there's now an "Add to My Disabilities" button. The disability name and DC chip are pre-filled, with a sensible starting rating suggested based on the code's common bands.

## Neurological, grouped by nerve

The Neurological section used to be 119 rows — each peripheral nerve appearing three times for paralysis, neuritis, and neuralgia. It's now 21 expandable nerve-level rows. Tap a nerve, see the three variants. The detail view still shows everything, just without forcing you to scan past it in list form.

A related fix: 86xx and 87xx entries (neuritis and neuralgia) used to read as just "Neuritis" or "Neuralgia" with no nerve identifier in search results. They now display as "Sciatic Nerve, Neuritis" and "Median Nerve, Neuralgia" everywhere they appear.

## Small things

  - A "Back to top" link at the bottom of the How to Use guide
  - The app's display name on the home screen now matches the App Store name (VA Compensation Calculator)
  - Various small UI changes and bug fixes

## Free, ad-free, private. Same as it's always been.

Nothing in this release changes how your data is handled. Everything is still stored locally on your device with complete file protection, no analytics, no accounts. The Tip Jar is optional and unlocks nothing.

---

[Download on the App Store](https://apps.apple.com/us/app/va-compensation-calculator/id6746081239)

For questions or feedback, use the [contact page](/contact/).
