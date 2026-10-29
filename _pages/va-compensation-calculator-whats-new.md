---
permalink: /va-compensation-calculator/whats-new/
title: "What's Coming in VA Compensation Calculator"
description: "A 4-minute look at 1.27.0: Rating & Pay, the Claim Finder, Military Job Lookup, My Profile, widgets and more. After it: Survivor Benefits and an Apple Watch app."
header:
  og_image: /assets/images/va-disability-app-images/whats-new-1.27.0.jpg
last_modified_at: 2026-10-29T00:00:00-04:00
---

<style>
.vp{position:relative;aspect-ratio:16/9;margin:0 0 1.4em;border-radius:10px;overflow:hidden;background:#0f2c4f}
.vp-thumb{display:block;position:relative;width:100%;height:100%;color:#fff;text-decoration:none}
.vp-thumb img{display:block;width:100%;height:100%;object-fit:cover}
.vp-play{position:absolute;left:50%;bottom:7%;transform:translateX(-50%);display:inline-flex;align-items:center;gap:.55em;padding:.5em 1.05em;border-radius:999px;background:#0a7ea4;box-shadow:0 4px 16px rgba(0,0,0,.35);font-size:.85em;font-weight:600;white-space:nowrap;transition:background .15s}
.vp-play::before{content:"";border-style:solid;border-width:.42em 0 .42em .7em;border-color:transparent transparent transparent #fff}
.vp-thumb:hover .vp-play{background:#086b8c}
.vp-thumb:focus-visible{outline:3px solid #0a7ea4;outline-offset:3px}
.vp iframe{position:absolute;inset:0;width:100%;height:100%;border:0}
.page__content ul.vp-chapters{list-style:none;margin:0 0 1.6em;padding:0;font-size:.9em}
.page__content ul.vp-chapters li{margin:0 0 .35em}
.page__content ul.vp-chapters span{display:inline-block;min-width:3.2em;color:#5f6b76;font-variant-numeric:tabular-nums}

/* Screenshots: the project page's carousel and lightbox, with a label under each one */
.carousel{display:flex;align-items:center;gap:10px;margin:0 0 1.4em}
.carousel-btn{flex:0 0 40px;width:40px;height:40px;border:1px solid #d0d0d0;background:#f5f5f5;border-radius:50%;font-size:1.4em;line-height:1;cursor:pointer;display:flex;align-items:center;justify-content:center;color:#333;transition:background .15s}
.carousel-btn:hover:not(:disabled){background:#e6e6e6}
.carousel-btn:disabled{opacity:.3;cursor:default}
.carousel-btn:focus-visible{outline:3px solid #0a7ea4;outline-offset:2px}
.carousel-track{display:flex;align-items:flex-start;gap:10px;flex:1 1 auto;min-width:0;overflow-x:auto;scroll-behavior:smooth;scroll-snap-type:x mandatory;scroll-padding:0 2px;padding:4px 2px 8px;scrollbar-width:none}
.carousel-track::-webkit-scrollbar{display:none}
.page__content figure.shot{display:block;margin:0}
.carousel .shot{flex:0 0 calc((100% - 20px) / 3);scroll-snap-align:start}
.carousel .shot.is-ipad{flex-basis:calc((100% - 20px) / 3 * 1.63)}
.shot-thumb{display:block;width:100%;padding:0;border:none;background:none;cursor:zoom-in;border-radius:8px;overflow:hidden;box-shadow:0 1px 4px rgba(0,0,0,.15)}
.shot-thumb:hover{box-shadow:0 2px 10px rgba(0,0,0,.25)}
.shot-thumb:focus-visible{outline:3px solid #0a7ea4;outline-offset:-3px}
.page__content .shot-thumb img{display:block;width:100%;height:auto;margin:0;border-radius:0}
.page__content .shot figcaption{margin:.45em 0 0;font-family:inherit;font-size:.75em;line-height:1.35;color:#5f6b76}
.shot-grid{display:grid;grid-template-columns:repeat(3,minmax(0,1fr));gap:12px;margin:0 0 1.4em}
.shot-grid.is-watch{grid-template-columns:repeat(4,minmax(0,1fr))}
.shot-grid.is-watch .shot-thumb{border-radius:14%;background:#000}
@media (max-width:600px){
  .carousel .shot{flex-basis:calc((100% - 10px) / 2)}
  .carousel .shot.is-ipad{flex-basis:calc((100% - 10px) / 2 * 1.63)}
  .shot-grid{gap:8px}
  .shot-grid.is-watch{grid-template-columns:repeat(2,minmax(0,1fr))}
}
.lightbox{position:fixed;inset:0;z-index:9999;display:none;align-items:center;justify-content:center;padding:68px 16px 100px;background:rgba(0,0,0,.88)}
.lightbox.is-open{display:flex}
.lightbox-img{max-width:100%;max-height:100%;object-fit:contain;border-radius:8px;box-shadow:0 4px 20px rgba(0,0,0,.5)}
.lightbox-btn{position:absolute;display:flex;align-items:center;justify-content:center;border:1px solid rgba(255,255,255,.45);border-radius:50%;background:rgba(0,0,0,.6);color:#fff;cursor:pointer;transition:background .15s}
.lightbox-btn:hover{background:rgba(0,0,0,.8)}
.lightbox-btn:focus-visible{outline:3px solid #fff;outline-offset:2px}
.lightbox-prev,.lightbox-next{top:50%;transform:translateY(-50%);width:52px;height:52px;font-size:2em}
.lightbox-prev{left:16px}
.lightbox-next{right:16px}
.lightbox-close{top:16px;right:16px;width:44px;height:44px;font-size:1.6em}
.lightbox-caption{position:absolute;bottom:18px;left:16px;right:16px;width:fit-content;max-width:760px;margin:0 auto;padding:6px 14px;border-radius:6px;background:rgba(0,0,0,.55);color:#fff;font-size:.9em;line-height:1.4;text-align:center}
</style>

The next update to [VA Compensation Calculator](/va-compensation-calculator/), 1.27.0, is planned for November. Here's a 4-minute look at what's coming. Further down are screenshots, and what comes after it.

<div class="vp" id="vp">
  <a class="vp-thumb" href="https://www.youtube.com/watch?v=eNAiKTJv8SI" aria-label="Play the 4-minute preview of VA Compensation Calculator 1.27.0">
    <img src="/assets/images/va-disability-app-images/whats-new-1.27.0.jpg" alt="VA Compensation Calculator: What's new in 1.27.0" width="1280" height="720">
    <span class="vp-play" aria-hidden="true">Watch the preview · 4:08</span>
  </a>
</div>

## In the video

<ul class="vp-chapters">
  <li><span>0:00</span> <a href="https://www.youtube.com/watch?v=eNAiKTJv8SI" data-start="0">One main screen</a></li>
  <li><span>0:29</span> <a href="https://www.youtube.com/watch?v=eNAiKTJv8SI&amp;t=29s" data-start="29">Rating &amp; Pay</a></li>
  <li><span>1:04</span> <a href="https://www.youtube.com/watch?v=eNAiKTJv8SI&amp;t=64s" data-start="64">Claim Finder</a></li>
  <li><span>1:47</span> <a href="https://www.youtube.com/watch?v=eNAiKTJv8SI&amp;t=107s" data-start="107">Military Job Lookup</a></li>
  <li><span>2:23</span> <a href="https://www.youtube.com/watch?v=eNAiKTJv8SI&amp;t=143s" data-start="143">My Profile</a></li>
  <li><span>3:01</span> <a href="https://www.youtube.com/watch?v=eNAiKTJv8SI&amp;t=181s" data-start="181">Might file</a></li>
  <li><span>3:22</span> <a href="https://www.youtube.com/watch?v=eNAiKTJv8SI&amp;t=202s" data-start="202">Widgets and iPad</a></li>
  <li><span>3:43</span> <a href="https://www.youtube.com/watch?v=eNAiKTJv8SI&amp;t=223s" data-start="223">More help in Support &amp; Community</a></li>
</ul>

## What's coming in 1.27.0

- **Claim Finder:** conditions often claimed with the ones you have, the ones VA presumes after certain service (like Agent Orange, burn pits, the Gulf War and Camp Lejeune), and the ones linked to what you did in service, like loud noise, combat or asbestos.
- **Military Job Lookup:** the job code from your DD 214, today's or decades old. What the job was, what it became, and the conditions linked to its duties.
- **My Profile:** your dependents, SMC and TDIU, and your military service in one place, with a list of what you may be able to claim and a summary you can share with your VSO.
- **Rating & Pay:** every step of your combined rating and your pay line by line, with switches that show what your pending claims, or the ones you might file, could add.
- **Might file:** a status for a claim you're thinking about, so the main screen can show what it could mean for your rating and pay.
- **Widgets** for your Home Screen and Lock Screen, and **two columns on iPad**.
- **Support & Community:** more places to get help with a claim, your health, caregiving, housing and work.

### Screenshots

<div class="carousel" data-gallery>
  <button type="button" class="carousel-btn carousel-prev" aria-label="Previous screenshots">&#8249;</button>
  <div class="carousel-track">
    <figure class="shot">
      <button type="button" class="shot-thumb" data-caption="One main screen: your rating and pay up top, your tools as cards below"><img src="/assets/images/va-disability-app-images/1.27.0/ios/main-screen.png" alt="The main screen: a 90% combined rating, 100% with pending claims, and $2,942.17 a month with one SMC-K at 2026 rates. Below it, My Disabilities with 13 conditions, 1 pending and 1 might file, and cards for the Claim Finder, Increase Finder, Claim Tracker, Symptom Log, My Profile and Calculators &amp; References" width="800" height="1738" loading="lazy"></button>
      <figcaption>One main screen</figcaption>
    </figure>
    <figure class="shot">
      <button type="button" class="shot-thumb" data-caption="Rating &amp; Pay: your pay line by line, and how your ratings combine, step by step"><img src="/assets/images/va-disability-app-images/1.27.0/ios/rating-and-pay.png" alt="Rating &amp; Pay: the 90% rate for a veteran, a spouse and a child, $2,704.30, plus an additional child and SMC-K, for a total of $2,942.17 a month. Below it, how the rating is combined, highest first: PTSD 70%, sleep apnea 50%, both legs with the bilateral factor and four more, for a combined value of 94 that rounds to 90%" width="800" height="1738" loading="lazy"></button>
      <figcaption>Rating &amp; Pay</figcaption>
    </figure>
    <figure class="shot">
      <button type="button" class="shot-thumb" data-caption="Claim Finder: conditions often claimed with the ones you have"><img src="/assets/images/va-disability-app-images/1.27.0/ios/claim-finder.png" alt="Claim Finder, with the conditions you have: for a back or neck condition, lumbar spine strain, it lists radiculopathy in an arm and bladder or bowel problems, both rated separately under 38 CFR, and reflux or ulcers from pain relievers, which needs a doctor's opinion, each with an Add button" width="800" height="1738" loading="lazy"></button>
      <figcaption>Claim Finder</figcaption>
    </figure>
    <figure class="shot">
      <button type="button" class="shot-thumb" data-caption="Military Job Lookup: what the job was, its earlier codes, and what was often part of it"><img src="/assets/images/va-disability-app-images/1.27.0/ios/military-job-lookup.png" alt="Military Job Lookup's page for Army MOS 11B, Infantryman: the official description, its earlier codes 11H and 11M, used until 2002, and what's often part of the job, like loud noise and blasts and explosions" width="800" height="1738" loading="lazy"></button>
      <figcaption>Military Job Lookup</figcaption>
    </figure>
    <figure class="shot">
      <button type="button" class="shot-thumb" data-caption="My Profile: Dependents, SMC &amp; TDIU, and Military service in one place"><img src="/assets/images/va-disability-app-images/1.27.0/ios/my-profile.png" alt="My Profile: Dependents, married with 2 children; SMC &amp; TDIU, 1 SMC-K with TDIU off; and Military service: the job, MOS 11B, where they served, burn pits and other toxic exposures and Gulf War illnesses, and what they did, loud noise and combat or hostile fire" width="800" height="1738" loading="lazy"></button>
      <figcaption>My Profile</figcaption>
    </figure>
    <figure class="shot">
      <button type="button" class="shot-thumb" data-caption="Share a summary: pick what goes in, then share it as text or a PDF"><img src="/assets/images/va-disability-app-images/1.27.0/ios/share-a-summary.png" alt="Share a Summary: switches for disabilities and claims, rating and pay, dependents, military service, Claim Tracker dates and the Symptom Log's last 90 days, all on, and notes on each disability, off, above a preview of the Veteran Summary and a Share as Text button" width="800" height="1738" loading="lazy"></button>
      <figcaption>Share a summary</figcaption>
    </figure>
    <figure class="shot">
      <button type="button" class="shot-thumb" data-caption="Widgets on your Home Screen: your rating, pay, next pay date and next Claim Tracker date"><img src="/assets/images/va-disability-app-images/1.27.0/ios/widgets-home-screen.jpg" alt="A Home Screen with two VA Compensation Calculator widgets: a 90% rating, $2,942.17 a month, 100% with pending claims, the next pay date, Fri, Oct 30, and a C&amp;P exam in 6 days from the Claim Tracker" width="800" height="1738" loading="lazy"></button>
      <figcaption>Home Screen widgets</figcaption>
    </figure>
    <figure class="shot">
      <button type="button" class="shot-thumb" data-caption="Widgets on your Lock Screen"><img src="/assets/images/va-disability-app-images/1.27.0/ios/widgets-lock-screen.jpg" alt="A Lock Screen with VA 90% and $2,942.17 a month above the clock, and under it the rating, the monthly pay, the next pay date and a gauge at 90" width="800" height="1738" loading="lazy"></button>
      <figcaption>Lock Screen widgets</figcaption>
    </figure>
    <figure class="shot is-ipad">
      <button type="button" class="shot-thumb" data-caption="iPad: your rating and cards on the left, each card's screen beside them"><img src="/assets/images/va-disability-app-images/1.27.0/ipad/two-columns.png" alt="An iPad in two columns: the main screen's rating, pay and cards on the left, and the Increase Finder on the right, with the next rating step for each condition and what it would mean for the combined rating and pay" width="1200" height="1600" loading="lazy"></button>
      <figcaption>iPad: two columns</figcaption>
    </figure>
  </div>
  <button type="button" class="carousel-btn carousel-next" aria-label="More screenshots">&#8250;</button>
</div>

When it's out, it shows up as an update in the [App Store](https://apps.apple.com/us/app/va-compensation-calculator/id6746081239).

## Coming after 1.27.0

Two more things come in an update after 1.27.0. There's no date yet.

### Survivor Benefits (DIC)

Dependency and Indemnity Compensation (DIC) is a tax-free monthly payment VA makes to a veteran's survivors. Survivor Benefits estimates it for a surviving spouse and children, two ways:

- **For your family:** what your spouse and children could receive, line by line, from the dependents in My Profile. It also shows when each of VA's rules would apply: a service-connected death at any time, almost any cause of death after 10 years rated 100% or TDIU without a break, and the 8-year provision, which pays a spouse more. If you're rated 100% or TDIU, add the month that rating began and the month you married to see when.
- **For a survivor:** an estimate from a survivor's own answers, with who qualifies and a link to apply on VA.gov.

It's an estimate. It never says anyone qualifies: VA decides that, and whether a death was service-connected. It doesn't cover DIC for parents, which depends on their income, or deaths before 1993. You'll find it in Calculators & References, and in My Profile under Dependents.

<div class="shot-grid" data-gallery>
  <figure class="shot">
    <button type="button" class="shot-thumb" data-caption="Survivor Benefits, For your family: what your spouse and children could receive, line by line"><img src="/assets/images/va-disability-app-images/1.27.1/ios/survivor-for-your-family.png" alt="Survivor Benefits, For your family: $2,900.36 a month at 2026 rates, tax-free, and $2,541.36 after DIC's first 2 years, for a married veteran rated 90% with 2 children under 18. It adds up the spouse's basic rate, $1,699.36, 2 children under 18, $842.00, and the transitional benefit, $359.00" width="800" height="1734" loading="lazy"></button>
    <figcaption>For your family</figcaption>
  </figure>
  <figure class="shot">
    <button type="button" class="shot-thumb" data-caption="Survivor Benefits: when each of VA's rules would apply"><img src="/assets/images/va-disability-app-images/1.27.1/ios/survivor-when-it-applies.png" alt="Survivor Benefits, When it would apply: a service-connected death, at any time; any cause of death, only after 10 years rated 100% or TDIU without a break; and the 8-year provision, $360.85 more, only after 8 years rated 100% or TDIU while married. Below it, Good to know, about Survivors Pension and the Survivor Benefit Plan" width="800" height="1734" loading="lazy"></button>
    <figcaption>When it would apply</figcaption>
  </figure>
  <figure class="shot">
    <button type="button" class="shot-thumb" data-caption="Survivor Benefits, For a survivor: an estimate from the survivor's own answers"><img src="/assets/images/va-disability-app-images/1.27.1/ios/survivor-for-a-survivor.png" alt="Survivor Benefits, For a survivor: an estimated $2,900.36 a month, with who's applying, a surviving spouse or children only, how DIC would apply, died in service or of a service-connected condition, rated 100% or TDIU for the 10 years before death, or not sure, and a switch for DIC's first 2 years" width="800" height="1734" loading="lazy"></button>
    <figcaption>For a survivor</figcaption>
  </figure>
</div>

### Apple Watch

The app gets an Apple Watch app. It comes with the iPhone app and needs watchOS 10 or later.

- **Your rating and pay:** your rating, monthly pay and next pay date on your wrist and on your watch face.
- **Symptom Log:** log an episode the moment it starts. When it's over, tap End and say how bad it was, whether a migraine made you stop and lie down, and any care you needed. It goes to the Symptom Log on your iPhone, which keeps the record.
- **Claim Tracker:** your upcoming exams, hearings and deadlines.
- **Log a migraine:** say "Log a migraine in VA Compensation" to Siri on your watch, and it starts timing one without opening the app.

With App Lock on, the watch shows a lock, not your numbers. The watch face never shows a disability's name or an event's title.

<div class="shot-grid is-watch" data-gallery>
  <figure class="shot">
    <button type="button" class="shot-thumb" data-caption="Apple Watch: your rating and monthly pay"><img src="/assets/images/va-disability-app-images/1.27.1/watch/va-rating.png" alt="Apple Watch, VA Rating: a 90% ring, $2,942.17 a month, and with pending claims, 100% and $4,567.97" width="416" height="496" loading="lazy"></button>
    <figcaption>Your rating and pay</figcaption>
  </figure>
  <figure class="shot">
    <button type="button" class="shot-thumb" data-caption="Apple Watch: timing a migraine for the Symptom Log"><img src="/assets/images/va-disability-app-images/1.27.1/watch/symptom-log-timing.png" alt="Apple Watch, Symptom Log: a migraine being timed, 42 minutes in, since 7:55 AM, with an End button" width="416" height="496" loading="lazy"></button>
    <figcaption>Timing a migraine</figcaption>
  </figure>
  <figure class="shot">
    <button type="button" class="shot-thumb" data-caption="Apple Watch: when it ends, how bad it was"><img src="/assets/images/va-disability-app-images/1.27.1/watch/end-how-bad-was-it.png" alt="Apple Watch, End: How bad was it? Moderate, 3 of 5, with minus and plus buttons. It lasted 42 minutes. A Next button" width="416" height="496" loading="lazy"></button>
    <figcaption>How bad was it?</figcaption>
  </figure>
  <figure class="shot">
    <button type="button" class="shot-thumb" data-caption="Apple Watch: your Claim Tracker dates"><img src="/assets/images/va-disability-app-images/1.27.1/watch/claim-tracker.png" alt="Apple Watch, Claim Tracker: a migraine C&amp;P exam on Wed, Nov 4, in 6 days, a neurology follow-up on Wed, Nov 11, in 13 days, and an HLR informal conference on hypertension" width="416" height="496" loading="lazy"></button>
    <figcaption>Claim Tracker</figcaption>
  </figure>
</div>

## Tell me what you think

I'd like to hear what you think of what's coming: what looks useful, what's missing, or anything that's unclear. [Send me a note](/contact/?topic=va-feedback), and leave your email if you'd like a reply.

— Ian

<script>
(function () {
  var box = document.getElementById("vp");
  if (!box) return;
  // The regular YouTube player, loaded only when someone presses play (or a chapter).
  function play(start) {
    var f = document.createElement("iframe");
    f.src = "https://www.youtube.com/embed/eNAiKTJv8SI?autoplay=1&rel=0&playsinline=1" + (start ? "&start=" + start : "");
    f.title = "What's Coming in VA Compensation Calculator 1.27.0";
    f.allow = "accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share";
    f.setAttribute("allowfullscreen", "");
    f.referrerPolicy = "strict-origin-when-cross-origin";
    box.innerHTML = "";
    box.appendChild(f);
  }
  box.querySelector(".vp-thumb").addEventListener("click", function (e) {
    e.preventDefault();
    play(0);
  });
  Array.prototype.forEach.call(document.querySelectorAll(".vp-chapters a[data-start]"), function (a) {
    a.addEventListener("click", function (e) {
      e.preventDefault();
      play(parseInt(a.getAttribute("data-start"), 10));
      box.scrollIntoView({ behavior: "smooth", block: "center" });
    });
  });
})();

(function () {
  // The screenshots open in one lightbox: Escape closes it, the arrow keys
  // step through that group, Tab stays on its buttons, and focus goes back
  // to the screenshot that opened it.
  var lightbox = document.createElement("div");
  lightbox.className = "lightbox";
  lightbox.setAttribute("role", "dialog");
  lightbox.setAttribute("aria-modal", "true");
  lightbox.setAttribute("aria-label", "Screenshot");
  lightbox.innerHTML =
    '<button type="button" class="lightbox-btn lightbox-close" aria-label="Close">&times;</button>' +
    '<button type="button" class="lightbox-btn lightbox-prev" aria-label="Previous screenshot">&#8249;</button>' +
    '<img class="lightbox-img" alt="">' +
    '<button type="button" class="lightbox-btn lightbox-next" aria-label="Next screenshot">&#8250;</button>' +
    '<div class="lightbox-caption"></div>';
  document.body.appendChild(lightbox);

  var img = lightbox.querySelector(".lightbox-img");
  var caption = lightbox.querySelector(".lightbox-caption");
  var closeBtn = lightbox.querySelector(".lightbox-close");
  var prevBtn = lightbox.querySelector(".lightbox-prev");
  var nextBtn = lightbox.querySelector(".lightbox-next");
  var buttons = [closeBtn, prevBtn, nextBtn];
  var list = [];
  var index = 0;
  var opener = null;

  function show() {
    var item = list[index];
    img.src = item.full;
    img.alt = item.alt;
    caption.textContent = item.caption;
  }
  function open(items, i, from) {
    list = items;
    index = i;
    opener = from;
    show();
    lightbox.classList.add("is-open");
    document.body.style.overflow = "hidden";
    closeBtn.focus();
  }
  function close() {
    lightbox.classList.remove("is-open");
    document.body.style.overflow = "";
    if (opener) opener.focus();
  }
  function step(delta) {
    index = (index + delta + list.length) % list.length;
    show();
  }

  closeBtn.addEventListener("click", close);
  prevBtn.addEventListener("click", function () { step(-1); });
  nextBtn.addEventListener("click", function () { step(1); });
  lightbox.addEventListener("click", function (e) { if (e.target === lightbox) close(); });
  document.addEventListener("keydown", function (e) {
    if (!lightbox.classList.contains("is-open")) return;
    if (e.key === "Escape") { e.preventDefault(); close(); }
    else if (e.key === "ArrowLeft") { e.preventDefault(); step(-1); }
    else if (e.key === "ArrowRight") { e.preventDefault(); step(1); }
    else if (e.key === "Tab") {
      e.preventDefault();
      var at = buttons.indexOf(document.activeElement);
      buttons[(at + (e.shiftKey ? -1 : 1) + buttons.length) % buttons.length].focus();
    }
  });

  // Each group (the carousel, or a grid) steps through its own screenshots.
  Array.prototype.forEach.call(document.querySelectorAll("[data-gallery]"), function (gallery) {
    var thumbs = [].slice.call(gallery.querySelectorAll(".shot-thumb"));
    var items = thumbs.map(function (t) {
      var pic = t.querySelector("img");
      var label = t.parentNode.querySelector("figcaption");
      return {
        full: pic.getAttribute("src"),
        alt: pic.alt,
        caption: t.getAttribute("data-caption") || (label ? label.textContent : "")
      };
    });
    thumbs.forEach(function (t, i) {
      t.addEventListener("click", function () { open(items, i, t); });
    });
  });

  // The carousel's arrows scroll it one view at a time.
  Array.prototype.forEach.call(document.querySelectorAll(".carousel"), function (carousel) {
    var track = carousel.querySelector(".carousel-track");
    var prev = carousel.querySelector(".carousel-prev");
    var next = carousel.querySelector(".carousel-next");
    function update() {
      var hadFocus = document.activeElement;
      prev.disabled = track.scrollLeft <= 1;
      next.disabled = track.scrollLeft + track.clientWidth >= track.scrollWidth - 1;
      // An arrow that just turned off hands the focus to the other one.
      if (hadFocus === next && next.disabled && !prev.disabled) prev.focus();
      if (hadFocus === prev && prev.disabled && !next.disabled) next.focus();
    }
    prev.addEventListener("click", function () { track.scrollBy({ left: -track.clientWidth, behavior: "smooth" }); });
    next.addEventListener("click", function () { track.scrollBy({ left: track.clientWidth, behavior: "smooth" }); });
    track.addEventListener("scroll", update);
    window.addEventListener("resize", update);
    update();
  });
})();
</script>
