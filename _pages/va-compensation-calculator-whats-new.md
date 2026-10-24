---
permalink: /va-compensation-calculator/whats-new/
title: "What's Coming in VA Compensation Calculator 1.27.0"
description: "A 4-minute look at the next update: Rating & Pay, the Claim Finder, Military Job Lookup, My Profile, widgets and more."
header:
  og_image: /assets/images/va-disability-app-images/whats-new-1.27.0.jpg
last_modified_at: 2026-10-24T00:00:00-04:00
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
</style>

The next update to [VA Compensation Calculator](/va-compensation-calculator/) is planned for November. Here's a 4-minute look at what's coming.

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

## What's coming

- **Claim Finder:** conditions often claimed with the ones you have, the ones VA presumes after certain service (like Agent Orange, burn pits, the Gulf War and Camp Lejeune), and the ones linked to what you did in service, like loud noise, combat or asbestos.
- **Military Job Lookup:** the job code from your DD 214, today's or decades old. What the job was, what it became, and the conditions linked to its duties.
- **My Profile:** your dependents, SMC and TDIU, and your military service in one place, with a list of what you may be able to claim and a summary you can share with your VSO.
- **Rating & Pay:** every step of your combined rating and your pay line by line, with switches that show what your pending claims, or the ones you might file, could add.
- **Might file:** a status for a claim you're thinking about, so the main screen can show what it could mean for your rating and pay.
- **Widgets** for your Home Screen and Lock Screen, and **two columns on iPad**.
- **Support & Community:** more places to get help with a claim, your health, caregiving, housing and work.

When it's out, it shows up as an update in the [App Store](https://apps.apple.com/us/app/va-compensation-calculator/id6746081239).

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
</script>
