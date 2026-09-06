---
layout: single
title: "MediaHarbor — a photo and video player for your own hardware"
date: 2026-07-19T14:00:00-04:00
categories: [MediaHarbor]
tags: [mediaharbor, ios, release]
author_profile: true
header:
  og_image: /assets/images/mediaharbor-images/og-card.png
---

{% assign mh = site.data.apps.mediaharbor %}
{% if mh.app_store_id != "" %}{% assign mh_url = "https://apps.apple.com/us/app/" | append: mh.app_store_slug | append: "/id" | append: mh.app_store_id %}{% endif %}

I've built a second iOS app: **[MediaHarbor](/mediaharbor/)**, a photo and video player for media that lives on hardware you own — a NAS, a home server, or the device in your hand. No account, no cloud service in the middle, nothing uploaded anywhere.

## Why I built it

This one started the way the VA Calculator did: I wanted it, and nothing quite did the job.

My photo and video library lives on a NAS at home. Getting at it from an iPhone left me two unappealing options. The Files app can mount an SMB share, but browsing a few thousand photos through it is miserable — it's a file manager, not a photo app, and thumbnails arrive at a crawl. VLC, on the other hand, plays anything you throw at it but has essentially no photo story; nobody scrolls a family album in a video player.

What I wanted was the obvious combination of the two: browse a network share the way the Photos app browses a library, and play whatever's in it the way VLC would. That's the whole idea.

## Talking to the NAS directly

MediaHarbor implements SMB itself rather than leaning on the Files app. You add a connection — host, port, username, domain — and browse it immediately. Synology, QNAP, TrueNAS, Unraid, a Windows share, anything speaking SMB. Saved passwords go into the iOS Keychain scoped to the device, never into the app's own files, and never into a URL where they'd end up in a log.

Doing the protocol work directly bought a few things worth having. Thumbnails load with the newest visible cells prioritized, so scrolling feels responsive instead of sequential. Files download only when you actually open them, and the cache evicts itself. And when the phone locks mid-scroll and the connection dies — which happens constantly on a real device — the app reconnects on its own rather than silently failing until you back out and try again.

## Two video engines

iOS plays MP4 and MOV natively and refuses most everything else. MediaHarbor uses Apple's player for the formats it handles well, which gets you Picture in Picture and AirPlay, and falls back to a built-in VLC engine for MKV, AVI, WMV, TS, and the rest. The app picks; you don't think about it.

Video streams straight off the share by default — no waiting for a multi-gigabyte download before playback starts. If you'd rather have a local copy for offline viewing (or for PiP and AirPlay), one tap downloads it in the background while the stream keeps playing. It remembers where you stopped, per file, and can move to the next video or shuffle when one finishes.

## The privacy part

> **Update, August 2026:** starting with version 1.1.0, MediaHarbor counts four anonymous usage statistics — app opens and purchases, nothing about your files, servers, or viewing — sent to my own server, with an off switch in Settings. The paragraph below described 1.0 as it shipped; the [privacy policy](/mediaharbor/privacy/) has the full, current details.

This is the piece I care most about, and it's simpler to describe than most privacy policies: the app has no analytics. Not opt-out analytics — none at all. It has no accounts, no third-party SDKs, and no server of mine sitting between you and your files. Your photos never leave your device to be analyzed; even the scene detection behind smart albums runs locally through Apple's on-device Vision framework.

The only thing that ever reaches me is a support message you deliberately type and send from inside the app, and that goes to a server I run personally rather than a Google form.

## Free, with an optional unlock

MediaHarbor is a free download. The free version includes one saved connection and plays the first five minutes of each video — deliberately enough to confirm the app actually works against *your* NAS and *your* files before spending anything, because SMB setups and video containers vary wildly and I'd rather you find out for free. A single $6.99 Lifetime Unlock removes both limits permanently. No subscription, and it's Family Shareable.

{% if mh_url %}
It's available now on the App Store:

[![Download MediaHarbor on the App Store](/assets/images/mediaharbor-images/download-on-the-app-store.svg)]({{ mh_url }})
{% else %}
It's submitted and waiting on App Store review — I'll update this post and the project page with the download link as soon as it's approved.
{% endif %}

Screenshots, the full feature list, and the privacy policy are on the project page:

🎞️ **[MediaHarbor](/mediaharbor/)**
