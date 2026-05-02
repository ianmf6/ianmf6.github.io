---
permalink: /va-disability-calculator-ios-app/
title: "VA Disability Calculator iOS & iPadOS App"
last_modified_at: 2026-05-02T00:00:00-04:00

toc: true
toc_label: "On this page"
toc_sticky: true

---

## Overview

The VA Disability Calculator helps veterans calculate their combined VA disability rating using the official formula from 38 CFR 4.25 and 4.26. It also tracks pending and denied claims alongside rated disabilities and projects what your combined rating could become if pending claims are approved. It estimates monthly compensation against historical rate tables from 2018 onward, supports Special Monthly Compensation (SMC), and includes a Backpay Calculator for estimating retroactive compensation across a timeline of rating changes. All data stays on your device. Available on iPhone and iPad. No ads, no accounts, no data collection.

[![App Store link](/assets/images/va-disability-app-images/download-on-the-app-store.svg)](https://apps.apple.com/us/app/va-compensation-calculator/id6746081239?mttnsubad=6746081239)

## Key Features

**Official VA Math Engine**
Combines multiple disability ratings step-by-step using the VA Combined Ratings Table, not simple addition.

**Bilateral Factor Support**
Automatically applies the 10% bilateral factor when both sides of an extremity are rated (left knee + right knee, etc.) per 38 CFR 4.26.

**Claims Tracking**
Track pending and denied claims alongside rated disabilities, with status filters (Rated, Pending, Denied) for the disabilities list.

**Projected Rating**
See what your combined rating could be if your pending claims are approved, and optionally include pending claims in the shared breakdown.

**In-App "What's New"**
Release notes are shown automatically after each update so you always know what changed.

**Backpay Calculator**
Estimate retroactive compensation across a timeline of rating changes, with full SMC support.

**Special Monthly Compensation (SMC)**
Supports SMC-K, S, L, R1, and R2 alongside the standard combined-rating calculation.

**Accurate Compensation Estimates**
Accounts for spouse, spouse Aid & Attendance, parents (0–2), children under 18, and children 18–24 in school.

**Compensation Breakdown**
Step-by-step calculation transparency showing exactly how your rating is combined and your compensation is determined.

**Shareable Breakdown**
Share your rating breakdown with privacy options to redact disability names, hide dependent information, and optionally include pending claims.

**Dependents Manager**
Tracks marital status, spouse A&A, parent dependents, and children with links to official VA resources.

**Year Selector**
Historical compensation rates from 2018 onward, selectable in the year picker. The picker autohides outside the December–February COLA window, with a Settings toggle to keep it always visible.

**100% Private**
All data stays on your device. Nothing is uploaded or shared. No accounts, no ads, no tracking.

## Screenshots

<style>
.device-tabs {
  display: flex;
  gap: 8px;
  margin: 12px 0 16px;
}
.device-tab {
  padding: 8px 18px;
  background: #f0f0f0;
  border: 1px solid #d0d0d0;
  border-radius: 6px;
  cursor: pointer;
  font-size: 0.95em;
  font-weight: 500;
  color: #333;
}
.device-tab:hover { background: #e6e6e6; }
.device-tab.is-active {
  background: #2c5282;
  color: #fff;
  border-color: #2c5282;
}
.device-pane { display: none; }
.device-pane.is-active { display: block; }

.carousel {
  display: flex;
  align-items: center;
  gap: 10px;
  margin: 0;
}
.carousel-btn {
  flex: 0 0 40px;
  width: 40px;
  height: 40px;
  border: 1px solid #d0d0d0;
  background: #f5f5f5;
  border-radius: 50%;
  font-size: 1.4em;
  line-height: 1;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #333;
  transition: background 0.15s;
}
.carousel-btn:hover:not(:disabled) { background: #e6e6e6; }
.carousel-btn:disabled { opacity: 0.3; cursor: default; }
.carousel-track {
  display: flex;
  overflow-x: auto;
  scroll-behavior: smooth;
  scroll-snap-type: x mandatory;
  gap: 10px;
  flex: 1 1 auto;
  min-width: 0;
  padding: 4px 2px 8px;
  scrollbar-width: none;
}
.carousel-track::-webkit-scrollbar { display: none; }
.carousel-thumb {
  flex: 0 0 calc((100% - 20px) / 3);
  scroll-snap-align: start;
  border: none;
  padding: 0;
  background: none;
  cursor: zoom-in;
  border-radius: 8px;
  overflow: hidden;
  box-shadow: 0 1px 4px rgba(0,0,0,0.15);
}
.carousel-thumb:hover { box-shadow: 0 2px 10px rgba(0,0,0,0.25); }
.carousel-thumb img {
  width: 100%;
  height: auto;
  display: block;
  border-radius: 8px;
}
@media (max-width: 600px) {
  .carousel-thumb { flex: 0 0 calc((100% - 10px) / 2); }
}

.lightbox {
  position: fixed;
  inset: 0;
  background: rgba(0,0,0,0.88);
  display: none;
  align-items: center;
  justify-content: center;
  z-index: 9999;
  padding: 24px;
}
.lightbox.is-open { display: flex; }
.lightbox-img {
  max-width: 100%;
  max-height: 100%;
  object-fit: contain;
  border-radius: 8px;
  box-shadow: 0 4px 20px rgba(0,0,0,0.5);
}
.lightbox-btn {
  position: absolute;
  background: rgba(255,255,255,0.18);
  color: #fff;
  border: none;
  border-radius: 50%;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: background 0.15s;
}
.lightbox-btn:hover { background: rgba(255,255,255,0.32); }
.lightbox-prev,
.lightbox-next {
  top: 50%;
  transform: translateY(-50%);
  width: 52px;
  height: 52px;
  font-size: 2em;
}
.lightbox-prev { left: 16px; }
.lightbox-next { right: 16px; }
.lightbox-close {
  top: 16px;
  right: 16px;
  width: 44px;
  height: 44px;
  font-size: 1.6em;
}
.lightbox-caption {
  position: absolute;
  bottom: 18px;
  left: 50%;
  transform: translateX(-50%);
  color: #fff;
  background: rgba(0,0,0,0.55);
  padding: 6px 14px;
  border-radius: 6px;
  font-size: 0.9em;
  max-width: 80%;
  text-align: center;
}
</style>

<div class="device-tabs" role="tablist">
  <button type="button" class="device-tab is-active" data-target="iphone-pane" role="tab" aria-selected="true">iPhone</button>
  <button type="button" class="device-tab" data-target="ipad-pane" role="tab" aria-selected="false">iPad</button>
</div>

<div id="iphone-pane" class="device-pane is-active" role="tabpanel">
  <div class="carousel">
    <button type="button" class="carousel-btn carousel-prev" aria-label="Previous screenshots">&#8249;</button>
    <div class="carousel-track">
      <button type="button" class="carousel-thumb" data-full="/assets/images/va-disability-app-images/1.26.5/ios/ios-home.png" data-caption="Home — Combined Rating with SMC and Projected Rating"><img src="/assets/images/va-disability-app-images/1.26.5/ios/ios-home.png" alt="Home screen showing 80% rating with projected 90%, SMC-K, and quick-access buttons" loading="lazy"></button>
      <button type="button" class="carousel-thumb" data-full="/assets/images/va-disability-app-images/1.26.5/ios/ios-disabilities.png" data-caption="Disabilities — Rated, Pending, and Denied"><img src="/assets/images/va-disability-app-images/1.26.5/ios/ios-disabilities.png" alt="Disabilities list with mixed Rated, Pending, and Denied statuses including bilateral conditions" loading="lazy"></button>
      <button type="button" class="carousel-thumb" data-full="/assets/images/va-disability-app-images/1.26.5/ios/ios-dependents.png" data-caption="Dependent Information"><img src="/assets/images/va-disability-app-images/1.26.5/ios/ios-dependents.png" alt="Dependent information screen with marital status, A&A, parents, and children inputs" loading="lazy"></button>
      <button type="button" class="carousel-thumb" data-full="/assets/images/va-disability-app-images/1.26.5/ios/ios-smc.png" data-caption="Special Monthly Compensation"><img src="/assets/images/va-disability-app-images/1.26.5/ios/ios-smc.png" alt="Special Monthly Compensation screen showing SMC-K awards and SMC level selection" loading="lazy"></button>
      <button type="button" class="carousel-thumb" data-full="/assets/images/va-disability-app-images/1.26.5/ios/ios-backpay-input.png" data-caption="Backpay — Timeline of Rating Changes"><img src="/assets/images/va-disability-app-images/1.26.5/ios/ios-backpay-input.png" alt="Backpay calculator inputs showing initial rating, rating changes, and SMC configuration" loading="lazy"></button>
      <button type="button" class="carousel-thumb" data-full="/assets/images/va-disability-app-images/1.26.5/ios/ios-backpay-result.png" data-caption="Backpay — Estimate"><img src="/assets/images/va-disability-app-images/1.26.5/ios/ios-backpay-result.png" alt="Backpay estimate showing total backpay broken down by rating period" loading="lazy"></button>
      <button type="button" class="carousel-thumb" data-full="/assets/images/va-disability-app-images/1.26.5/ios/ios-breakdown.png" data-caption="Compensation Breakdown"><img src="/assets/images/va-disability-app-images/1.26.5/ios/ios-breakdown.png" alt="Compensation breakdown with step-by-step calculation, bilateral factor, and SMC" loading="lazy"></button>
      <button type="button" class="carousel-thumb" data-full="/assets/images/va-disability-app-images/1.26.5/ios/ios-share.png" data-caption="Share Options"><img src="/assets/images/va-disability-app-images/1.26.5/ios/ios-share.png" alt="Share options with toggles to redact disability names, hide dependents, and include pending claims" loading="lazy"></button>
      <button type="button" class="carousel-thumb" data-full="/assets/images/va-disability-app-images/1.26.5/ios/ios-settings.png" data-caption="Settings"><img src="/assets/images/va-disability-app-images/1.26.5/ios/ios-settings.png" alt="Settings screen with compensation year picker, projected rating toggle, and Help &amp; About" loading="lazy"></button>
    </div>
    <button type="button" class="carousel-btn carousel-next" aria-label="More screenshots">&#8250;</button>
  </div>
</div>

<div id="ipad-pane" class="device-pane" role="tabpanel">
  <div class="carousel">
    <button type="button" class="carousel-btn carousel-prev" aria-label="Previous screenshots">&#8249;</button>
    <div class="carousel-track">
      <button type="button" class="carousel-thumb" data-full="/assets/images/va-disability-app-images/1.26.5/ipad/ipad-home.png" data-caption="Home — Combined Rating with SMC and Projected Rating"><img src="/assets/images/va-disability-app-images/1.26.5/ipad/ipad-home.png" alt="iPad home screen showing 80% rating with projected 90%, SMC-K, and quick-access buttons" loading="lazy"></button>
      <button type="button" class="carousel-thumb" data-full="/assets/images/va-disability-app-images/1.26.5/ipad/ipad-disabilities.png" data-caption="Disabilities — Bilateral Toggle"><img src="/assets/images/va-disability-app-images/1.26.5/ipad/ipad-disabilities.png" alt="iPad disabilities list with bilateral toggle expanded showing side and extremity group selectors" loading="lazy"></button>
      <button type="button" class="carousel-thumb" data-full="/assets/images/va-disability-app-images/1.26.5/ipad/ipad-add-disability.png" data-caption="Add Disability"><img src="/assets/images/va-disability-app-images/1.26.5/ipad/ipad-add-disability.png" alt="iPad Add Disability form with name, percentage, bilateral toggle, and status fields" loading="lazy"></button>
      <button type="button" class="carousel-thumb" data-full="/assets/images/va-disability-app-images/1.26.5/ipad/ipad-dependents.png" data-caption="Dependent Information"><img src="/assets/images/va-disability-app-images/1.26.5/ipad/ipad-dependents.png" alt="iPad dependent information screen" loading="lazy"></button>
      <button type="button" class="carousel-thumb" data-full="/assets/images/va-disability-app-images/1.26.5/ipad/ipad-smc.png" data-caption="Special Monthly Compensation — Level Picker"><img src="/assets/images/va-disability-app-images/1.26.5/ipad/ipad-smc.png" alt="iPad SMC screen with the SMC level dropdown open showing K, S, L, R1, and R2" loading="lazy"></button>
      <button type="button" class="carousel-thumb" data-full="/assets/images/va-disability-app-images/1.26.5/ipad/ipad-backpay.png" data-caption="Backpay Calculator"><img src="/assets/images/va-disability-app-images/1.26.5/ipad/ipad-backpay.png" alt="iPad backpay calculator showing inputs and computed estimate on a single screen" loading="lazy"></button>
      <button type="button" class="carousel-thumb" data-full="/assets/images/va-disability-app-images/1.26.5/ipad/ipad-breakdown.png" data-caption="Compensation Breakdown"><img src="/assets/images/va-disability-app-images/1.26.5/ipad/ipad-breakdown.png" alt="iPad compensation breakdown sheet with step-by-step calculation" loading="lazy"></button>
      <button type="button" class="carousel-thumb" data-full="/assets/images/va-disability-app-images/1.26.5/ipad/ipad-share.png" data-caption="Share Options"><img src="/assets/images/va-disability-app-images/1.26.5/ipad/ipad-share.png" alt="iPad share options sheet" loading="lazy"></button>
      <button type="button" class="carousel-thumb" data-full="/assets/images/va-disability-app-images/1.26.5/ipad/ipad-help.png" data-caption="How to Use"><img src="/assets/images/va-disability-app-images/1.26.5/ipad/ipad-help.png" alt="iPad How to Use screen with table of contents and detailed sections" loading="lazy"></button>
      <button type="button" class="carousel-thumb" data-full="/assets/images/va-disability-app-images/1.26.5/ipad/ipad-settings.png" data-caption="Settings"><img src="/assets/images/va-disability-app-images/1.26.5/ipad/ipad-settings.png" alt="iPad settings screen with year picker, projected rating, Help &amp; About, and data management" loading="lazy"></button>
    </div>
    <button type="button" class="carousel-btn carousel-next" aria-label="More screenshots">&#8250;</button>
  </div>
</div>

<script>
(function() {
  // Tab toggle
  document.querySelectorAll('.device-tab').forEach(function(btn) {
    btn.addEventListener('click', function() {
      var target = btn.getAttribute('data-target');
      document.querySelectorAll('.device-tab').forEach(function(b) {
        var active = (b === btn);
        b.classList.toggle('is-active', active);
        b.setAttribute('aria-selected', active ? 'true' : 'false');
      });
      document.querySelectorAll('.device-pane').forEach(function(p) {
        p.classList.toggle('is-active', p.id === target);
      });
    });
  });

  // Build lightbox
  var lightbox = document.createElement('div');
  lightbox.className = 'lightbox';
  lightbox.setAttribute('role', 'dialog');
  lightbox.setAttribute('aria-modal', 'true');
  lightbox.innerHTML =
    '<button type="button" class="lightbox-btn lightbox-close" aria-label="Close">&times;</button>' +
    '<button type="button" class="lightbox-btn lightbox-prev" aria-label="Previous">&#8249;</button>' +
    '<img class="lightbox-img" alt="">' +
    '<button type="button" class="lightbox-btn lightbox-next" aria-label="Next">&#8250;</button>' +
    '<div class="lightbox-caption"></div>';
  document.body.appendChild(lightbox);

  var lightboxImg = lightbox.querySelector('.lightbox-img');
  var lightboxCaption = lightbox.querySelector('.lightbox-caption');
  var currentList = [];
  var currentIndex = 0;

  function showCurrent() {
    var item = currentList[currentIndex];
    lightboxImg.src = item.full;
    lightboxImg.alt = item.alt;
    lightboxCaption.textContent = item.caption || '';
  }
  function openLightbox(list, idx) {
    currentList = list;
    currentIndex = idx;
    showCurrent();
    lightbox.classList.add('is-open');
    document.body.style.overflow = 'hidden';
  }
  function closeLightbox() {
    lightbox.classList.remove('is-open');
    document.body.style.overflow = '';
  }
  function navigate(delta) {
    if (!currentList.length) return;
    currentIndex = (currentIndex + delta + currentList.length) % currentList.length;
    showCurrent();
  }

  lightbox.querySelector('.lightbox-close').addEventListener('click', closeLightbox);
  lightbox.querySelector('.lightbox-prev').addEventListener('click', function(e) { e.stopPropagation(); navigate(-1); });
  lightbox.querySelector('.lightbox-next').addEventListener('click', function(e) { e.stopPropagation(); navigate(1); });
  lightbox.addEventListener('click', function(e) { if (e.target === lightbox) closeLightbox(); });
  document.addEventListener('keydown', function(e) {
    if (!lightbox.classList.contains('is-open')) return;
    if (e.key === 'Escape') closeLightbox();
    else if (e.key === 'ArrowLeft') navigate(-1);
    else if (e.key === 'ArrowRight') navigate(1);
  });

  // Wire up each carousel
  document.querySelectorAll('.carousel').forEach(function(carousel) {
    var track = carousel.querySelector('.carousel-track');
    var prev = carousel.querySelector('.carousel-prev');
    var next = carousel.querySelector('.carousel-next');
    var thumbs = [].slice.call(track.querySelectorAll('.carousel-thumb'));
    var images = thumbs.map(function(t) {
      var img = t.querySelector('img');
      return {
        full: t.getAttribute('data-full') || img.src,
        alt: img.alt,
        caption: t.getAttribute('data-caption') || ''
      };
    });

    function pageWidth() {
      // Scroll by 3 thumbs (one page) — fall back to track width if thumbs unsized
      if (thumbs.length === 0) return track.clientWidth;
      var t = thumbs[0];
      return (t.offsetWidth + 10) * 3 || track.clientWidth;
    }
    function updateButtons() {
      prev.disabled = track.scrollLeft <= 1;
      next.disabled = track.scrollLeft + track.clientWidth >= track.scrollWidth - 1;
    }
    prev.addEventListener('click', function() {
      track.scrollBy({ left: -pageWidth(), behavior: 'smooth' });
    });
    next.addEventListener('click', function() {
      track.scrollBy({ left: pageWidth(), behavior: 'smooth' });
    });
    track.addEventListener('scroll', updateButtons);
    window.addEventListener('resize', updateButtons);
    setTimeout(updateButtons, 0);

    thumbs.forEach(function(thumb, idx) {
      thumb.addEventListener('click', function() { openLightbox(images, idx); });
    });
  });
})();
</script>

## Version History

<strong>v1.26.5 — May 2026</strong>
  - Backpay Calculator: estimate retroactive compensation across a timeline of rating changes, with SMC support
  - Special Monthly Compensation (SMC) — supports SMC-K, S, L, R1, and R2
  - Historical compensation rates from 2018 onward, selectable in the year picker
  - Corrected 2026 compensation rates to match the latest [VA.gov](https://www.va.gov) published values
  - Restored ability to add 0% rated disabilities (regression from the 1.26.4 hotfix)
  - Year picker on the main screen now hides automatically outside the December–February COLA window; toggle in Settings to always show it
  - Help reorganized into three sections (What's New, How to Use, Help); added links to the r/VeteransBenefits community and Knowledge Base
  - Some small UI changes and fixes

<details>
<summary><strong>Older releases (v1.26.0 — v1.26.4)</strong></summary>
<p style="margin-top:1em;"><strong>v1.26.4 — April 2026</strong></p>
<ul>
  <li>Hotfix: Allow adding disabilities rated at 0% (Rated, Pending, and Denied)</li>
</ul>

<p><strong>v1.26.3 — April 2026</strong></p>
<ul>
  <li>Track pending and denied claims alongside rated disabilities</li>
  <li>Projected Rating shows what your combined rating could be if pending claims are approved</li>
  <li>Filter the disabilities list by status (Rated, Pending, Denied)</li>
  <li>Optionally include pending claims in the shared breakdown</li>
  <li>Compensation year picker now also available in Settings</li>
  <li>Spouse Aid &amp; Attendance section hidden when not married</li>
  <li>Empty state messages when filtering with no results</li>
  <li>Help section reorganized with clearer sub-sections</li>
  <li>"What's New" automatically displayed after each update</li>
</ul>

<p><strong>v1.26.2 — March 2026</strong></p>
<ul>
  <li>Share your rating breakdown with privacy options to redact disability names and hide dependent info</li>
  <li>Cleaner Compensation Breakdown with less clutter and clearer wording</li>
  <li>Smarter input validation when adding disabilities</li>
  <li>Fixed breakdown showing incorrect combined percentage before rounding</li>
</ul>

<p><strong>v1.26.1 — March 2026</strong></p>
<ul>
  <li>Redesigned bilateral condition entry — each side entered individually for more accurate tracking</li>
  <li>Bilateral factor only applied when both sides of an extremity group are present</li>
  <li>Fixed compensation calculation for children ages 18–24 in school</li>
  <li>Fixed issue where deleting a condition could remove the wrong entry</li>
</ul>

<p><strong>v1.26.0 — May 2025</strong></p>
<ul>
  <li>Enhanced settings with JSON data viewer</li>
  <li>2026 COLA rate support (2.8% increase)</li>
  <li>Bilateral factor support (38 CFR 4.26)</li>
  <li>Improved calculation accuracy</li>
</ul>
</details>

## Disclaimer

This app is not affiliated with the U.S. Department of Veterans Affairs. It is an independent tool for estimation purposes only. Always verify your rating and compensation with the VA directly.

**Privacy First**
All data stays on your device and under your control.

## Privacy Policy
[Privacy Policy](/privacy-policy-va-disability-app/)

## Support
For support or to report issues with the app, use the [Contact](/contact/) page.
