---
permalink: /mediaharbor/
title: "MediaHarbor"
description: "Photo and video player for your NAS on iPhone and iPad — browse SMB shares directly, view RAW and Live Photos, and stream MKV, AVI, and MP4 without uploading anything to the cloud."
header:
  og_image: /assets/images/mediaharbor-images/og-card.png
last_modified_at: 2026-07-19T13:00:00-04:00

toc: true
toc_label: "On this page"
toc_sticky: true

---

{% assign mh = site.data.apps.mediaharbor %}
{% if mh.app_store_id != "" %}{% assign mh_url = "https://apps.apple.com/us/app/" | append: mh.app_store_slug | append: "/id" | append: mh.app_store_id %}{% endif %}

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "MobileApplication",
  "name": "MediaHarbor",
  "operatingSystem": "iOS",
  "applicationCategory": "MultimediaApplication",
  "url": "https://www.ianm.tech/mediaharbor/",
  {% if mh_url %}"downloadUrl": "{{ mh_url }}",
  {% endif %}"author": { "@type": "Person", "name": "Ian Marrero" },
  "offers": { "@type": "Offer", "price": "0", "priceCurrency": "USD" }
}
</script>

## Overview

Your photos and videos live on a NAS, an external drive, or right on your iPhone. **MediaHarbor** makes them feel like they're in the Photos app — without uploading a single file to anyone's cloud.

Save SMB connections to Synology, QNAP, TrueNAS, Unraid, or any Windows share and browse them directly. No mounting in the Files app first, no accounts, no sync service in the middle. Photos render in a fast thumbnail grid; video plays through a two-engine player that handles the MKV and AVI files iOS normally refuses to open.

{% if mh_url %}
[![Download MediaHarbor on the App Store](/assets/images/mediaharbor-images/download-on-the-app-store.svg)]({{ mh_url }})
{% else %}
**Status:** {{ mh.status }} — submitted for App Store review. Check back shortly for the download link.
{: .notice--info }
{% endif %}

<style>
.feature-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 14px;
  margin: 28px 0 32px;
}
.feature-card {
  background: #fafafa;
  border: 1px solid #e5e5e5;
  border-radius: 10px;
  padding: 18px 16px;
  display: flex;
  flex-direction: column;
  gap: 6px;
  transition: box-shadow 0.15s, transform 0.15s;
}
.feature-card:hover {
  box-shadow: 0 4px 14px rgba(0,0,0,0.08);
  transform: translateY(-1px);
}
.feature-card .fc-icon {
  font-size: 1.7em;
  color: #2c5282;
  line-height: 1;
  margin-bottom: 4px;
}
.feature-card .fc-title {
  font-weight: 600;
  font-size: 1.02em;
  color: #1a202c;
}
.feature-card .fc-summary {
  font-size: 0.9em;
  color: #4a5568;
  line-height: 1.4;
}
@media (prefers-color-scheme: dark) {
  .feature-card {
    background: #2d3748;
    border-color: #4a5568;
  }
  .feature-card .fc-title { color: #f7fafc; }
  .feature-card .fc-summary { color: #cbd5e0; }
  .feature-card .fc-icon { color: #63b3ed; }
}
</style>

<section class="feature-grid" aria-label="Feature highlights">
  <div class="feature-card">
    <span class="fc-icon"><i class="fas fa-server" aria-hidden="true"></i></span>
    <span class="fc-title">Direct SMB</span>
    <span class="fc-summary">Connect straight to a NAS or Windows share — no Files app mount needed.</span>
  </div>
  <div class="feature-card">
    <span class="fc-icon"><i class="fas fa-th" aria-hidden="true"></i></span>
    <span class="fc-title">Real Photo Grid</span>
    <span class="fc-summary">Adaptive thumbnails, pinch to resize, sort, search, and favorites.</span>
  </div>
  <div class="feature-card">
    <span class="fc-icon"><i class="fas fa-film" aria-hidden="true"></i></span>
    <span class="fc-title">MKV &amp; AVI Playback</span>
    <span class="fc-summary">A built-in VLC engine plays what iOS can't open natively.</span>
  </div>
  <div class="feature-card">
    <span class="fc-icon"><i class="fas fa-broadcast-tower" aria-hidden="true"></i></span>
    <span class="fc-title">Stream, Don't Wait</span>
    <span class="fc-summary">Video plays straight off the share, or download it for offline.</span>
  </div>
  <div class="feature-card">
    <span class="fc-icon"><i class="fas fa-camera-retro" aria-hidden="true"></i></span>
    <span class="fc-title">RAW &amp; Live Photos</span>
    <span class="fc-summary">DNG, ARW, CR2, CR3, NEF, HEIC, GIF — plus Live Photo playback.</span>
  </div>
  <div class="feature-card">
    <span class="fc-icon"><i class="fas fa-tv" aria-hidden="true"></i></span>
    <span class="fc-title">PiP &amp; AirPlay</span>
    <span class="fc-summary">Native player for MP4 and MOV with Picture in Picture.</span>
  </div>
  <div class="feature-card">
    <span class="fc-icon"><i class="fas fa-user-shield" aria-hidden="true"></i></span>
    <span class="fc-title">Privacy First</span>
    <span class="fc-summary">No accounts, no cloud, no trackers. Passwords stay in the Keychain.</span>
  </div>
  <div class="feature-card">
    <span class="fc-icon"><i class="fas fa-map-marked-alt" aria-hidden="true"></i></span>
    <span class="fc-title">Metadata &amp; Maps</span>
    <span class="fc-summary">Full EXIF, GPS map view, and on-device scene detection.</span>
  </div>
</section>

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
      <button type="button" class="carousel-thumb" data-full="/assets/images/mediaharbor-images/1.0/ios/ios-gallery.png" data-caption="Gallery — thumbnails loaded straight from an SMB share"><img src="/assets/images/mediaharbor-images/1.0/ios/ios-gallery.png" alt="MediaHarbor photo grid on iPhone showing a full screen of landscape thumbnails loaded from a network share" loading="lazy"></button>
      <button type="button" class="carousel-thumb" data-full="/assets/images/mediaharbor-images/1.0/ios/ios-home.png" data-caption="Home — saved connections and favorite folders"><img src="/assets/images/mediaharbor-images/1.0/ios/ios-home.png" alt="MediaHarbor home screen on iPhone with Open Folder and Open File tiles, a favorited Photo Library folder, and a saved Living Room NAS connection" loading="lazy"></button>
      <button type="button" class="carousel-thumb" data-full="/assets/images/mediaharbor-images/1.0/ios/ios-viewer.png" data-caption="Viewer — file name, size, dimensions, and zoom"><img src="/assets/images/mediaharbor-images/1.0/ios/ios-viewer.png" alt="MediaHarbor full screen photo viewer on iPhone showing file name, file size, pixel dimensions, zoom level, and image position in the folder" loading="lazy"></button>
      <button type="button" class="carousel-thumb" data-full="/assets/images/mediaharbor-images/1.0/ios/ios-player.png" data-caption="Video — streaming straight off the NAS"><img src="/assets/images/mediaharbor-images/1.0/ios/ios-player.png" alt="MediaHarbor video playback on iPhone streaming an MP4 file directly from a network share" loading="lazy"></button>
    </div>
    <button type="button" class="carousel-btn carousel-next" aria-label="More screenshots">&#8250;</button>
  </div>
</div>

<div id="ipad-pane" class="device-pane" role="tabpanel">
  <div class="carousel">
    <button type="button" class="carousel-btn carousel-prev" aria-label="Previous screenshots">&#8249;</button>
    <div class="carousel-track">
      <button type="button" class="carousel-thumb" data-full="/assets/images/mediaharbor-images/1.0/ipad/ipad-gallery.png" data-caption="Gallery — the grid scales up on iPad"><img src="/assets/images/mediaharbor-images/1.0/ipad/ipad-gallery.png" alt="MediaHarbor photo grid on iPad showing large thumbnails from a network share" loading="lazy"></button>
      <button type="button" class="carousel-thumb" data-full="/assets/images/mediaharbor-images/1.0/ipad/ipad-home.png" data-caption="Home — connections and favorites"><img src="/assets/images/mediaharbor-images/1.0/ipad/ipad-home.png" alt="MediaHarbor home screen on iPad with open tiles, a favorited folder, and a saved NAS connection" loading="lazy"></button>
      <button type="button" class="carousel-thumb" data-full="/assets/images/mediaharbor-images/1.0/ipad/ipad-viewer.png" data-caption="Viewer — full screen photo with details"><img src="/assets/images/mediaharbor-images/1.0/ipad/ipad-viewer.png" alt="MediaHarbor full screen photo viewer on iPad with file details and toolbar" loading="lazy"></button>
      <button type="button" class="carousel-thumb" data-full="/assets/images/mediaharbor-images/1.0/ipad/ipad-player.png" data-caption="Video — playback on iPad"><img src="/assets/images/mediaharbor-images/1.0/ipad/ipad-player.png" alt="MediaHarbor video playback on iPad streaming from a network share" loading="lazy"></button>
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

## Key Features

### Network Shares (SMB)

  - Save connections to Synology, QNAP, TrueNAS, Unraid, Windows shares, or any SMB server
  - Direct SMB implementation — no need to mount the share in the Files app first
  - Host, port, username, domain, and default share are all configurable
  - Passwords stored in the iOS Keychain, scoped to your device
  - Favorite individual folders for one-tap access from the home screen
  - Files download only when you open them, and the local cache cleans up after itself

### Photo Browsing

  - Adaptive thumbnail grid, 2–6 columns, with pinch-to-resize
  - Sort by name, date, or size, with date-grouped section headers
  - Search by file name, favorites, and multi-select for batch actions
  - JPEG, HEIC, PNG, GIF, TIFF, WebP, and RAW (DNG, ARW, CR2, CR3, NEF, ORF, RW2, RAF and more)
  - Live Photos play with a long press
  - Pinch and double-tap zoom in the full-screen viewer
  - Smart albums from on-device scene detection — no photo ever leaves the device to be analyzed

### Video Playback

  - Two engines, chosen automatically: the native iOS player for MP4 and MOV, and a built-in VLC engine for MKV, AVI, WMV, TS, and other containers
  - Picture in Picture and AirPlay on the native player
  - Stream video straight off the share, or download it for offline playback
  - Resume where you left off, tracked per file
  - Double-tap to skip, hold for 2× speed, drag for brightness and volume
  - Play Next or Shuffle when a video ends
  - Audio and subtitle track selection, plus `.srt` sidecar files

### Metadata

  - Full EXIF, TIFF, GPS, and IPTC data
  - Map view for photos with GPS coordinates
  - File name, size, dimensions, and format badges

### Privacy

  - No accounts, no ads, no third-party SDKs, no trackers
  - Nothing is uploaded — the app talks to your server and nobody else's
  - SMB passwords live in the iOS Keychain, device-scoped
  - The only data that ever reaches the developer: support messages you explicitly send, and four anonymous usage counters (app opens and purchases — with an off switch in Settings, full details in the [privacy policy](/mediaharbor/privacy/))

## Pricing

MediaHarbor is a **free download**. The free version includes one saved network connection and plays the first five minutes of each video — enough to confirm it works with your NAS and your files before spending anything.

A single **Lifetime Unlock** ($6.99, one time) removes both limits permanently. No subscription, and it's Family Shareable.

## Version History

<strong>v1.0 — July 2026</strong>
  - Initial release: direct SMB browsing, photo grid with RAW and Live Photo support, two-engine video playback with streaming, resume positions, favorites, metadata with GPS maps, and on-device smart albums

## Open Source Notice

MediaHarbor includes open-source software: **VLCKit** (© VideoLAN and authors), **AMSMB2** (© Amir Abbas Mousavian), and **libsmb2** (© Ronnie Sahlberg and contributors), each used under the GNU LGPL v2.1 as dynamically linked, unmodified libraries. Full license text is included in the app under Settings → About → Third-Party Software.

## Privacy Policy

[Privacy Policy](/mediaharbor/privacy/)

## Support

Send feedback directly from inside the app — **About → Send Feedback**. No email account needed. You can also use the [Contact](/contact/) page.
