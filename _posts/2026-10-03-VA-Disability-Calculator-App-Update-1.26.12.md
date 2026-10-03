---
layout: single
title: "VA Compensation Calculator — Update 1.26.12"
date: 2026-10-03
categories: [VA Calculator]
tags: [va-disability-calculator, ios, release]
author_profile: true
---

Version 1.26.12 of the [VA Compensation Calculator](/va-compensation-calculator/) is now available on the App Store. It rates arm and hand conditions the way 38 CFR does — differently for your dominant and non-dominant arm — shows the regulation's own notes in the diagnostic-code reference, and corrects the rating criteria for about 200 codes.

## Dominant and non-dominant arm

For 74 arm and hand codes, the rating schedule has two columns: one for your dominant arm and a lower one for the other arm. They cover shoulder, elbow, wrist, hand and finger conditions; arm, hand and finger amputations; paralysis of the arm's nerves (DC 8510–8519); and muscle injuries of the shoulder, arm and forearm (muscle groups I–VIII, DC 5301–5308).

Through 1.26.11 the app showed only the dominant column. On a non-dominant arm that meant seeing ratings you can't get, and the Increase Finder could point at the wrong next step. Take limitation of motion of the arm (DC 5201): motion limited to midway between the side and shoulder level is 30% for the dominant arm but 20% for the other, so a non-dominant arm rated 20% doesn't move up until motion is limited to 25° from the side (30%).

Now:

- A code's page in the 38 CFR reference has a **Dominant / Non-dominant** switch above the criteria.
- When you add one of these conditions or give it a code, the app asks **Which arm?**, and the rating choices follow your answer. You can change it later from the code tag on the disability's row.
- The **Increase Finder** uses that arm's ratings and says which arm it used. If a condition has no arm set yet, it asks right there.

VA decides which arm is dominant from your records or a VA exam, and your decision letter or C&P exam usually says. If you're ambidextrous, the injured arm counts as dominant (38 CFR 4.69).

## The regulation's own notes, and the codes they point to

A veteran wrote in that their diverticulitis is rated under DC 7329, but the app only listed DC 7327. They were right. The regulation's note to 7327 says that after a colectomy or colostomy, it's rated under 7327 or 7329 (resection of the large intestine), whichever gives the higher rating — and the app had been dropping every note like that.

Now 416 codes carry the regulation's own notes, and a code's page links every code its notes point to under **Related codes**. Searching "diverticulitis", "colectomy" or "colostomy" finds 7329, and you can type a code the way your decision letter prints it, like "DC 7329" or "5299-5237".

## About 200 rating criteria corrected

The criteria in the 38 CFR reference come from the official schedule, and the tool that reads it had two bugs. Rating levels marked with a footnote were skipped (breast surgery, DC 7626, showed only its 0% level), and a shared rating formula leaked into codes it doesn't cover (the eye-episode ladder showed up on ectropion, DC 6020). Fixing them changed 194 codes: 91 gained criteria they never had, and 44 lost levels that were never theirs.

One hand-written entry was out of date, too. Erectile dysfunction (DC 7522) is rated 0% under the current schedule, not 20%. The money is SMC-K for loss of use of a creative organ, which is paid even at 0%. The Increase Finder had been suggesting a 0% → 20% step that doesn't exist.

## Contact Me: a check before you send without an email

Leaving the email blank is fine, and your message still arrives. But without an email I can't reply, or let you know what came of your message — a fix, an answer or a decision. Tapping Send with the email blank now says so, and lets you add your email or send anyway. The [contact page](/contact/) on this site does the same.

## Tip Jar

The Tip Jar says why again: tips keep this app free and ad-free for the next veteran who needs it. On the US App Store, it also offers a way to tip on the web. Tips are optional, as always, and unlock nothing.

## Also

Various bug fixes and improvements.

As always: your VA information stays on your device and under your control. If something's off or you have an idea, tap **?** → **Contact Me** and tell me.
