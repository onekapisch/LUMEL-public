<div align="center">

<img src="docs/icon.png" alt="LUMEL Mac brightness booster and dimmer app icon" width="120" height="120" />

# LUMEL

### Make your Mac brighter than macOS allows, or dimmer than its minimum.

**LUMEL** is a tiny macOS menu-bar app that unlocks the brightness range your Mac already has but hides. Boost a supported **XDR display toward ~1600 nits** for sunlight, or **dim below the macOS floor** for dark rooms at night. Free to download; a one-time **$2.99** unlocks full-screen boost. No subscription, no account, no data collected.

[![macOS 13+](https://img.shields.io/badge/macOS-13%2B-111111?logo=apple&logoColor=white)](https://apps.apple.com/us/app/lumel/id6776136831)
[![Mac App Store: Free + $2.99 Pro](https://img.shields.io/badge/Mac%20App%20Store-Free%20%2B%20%242.99%20Pro-0D96F6?logo=apple&logoColor=white)](https://apps.apple.com/us/app/lumel/id6776136831)
[![Telemetry: none](https://img.shields.io/badge/telemetry-none-2ea44f)](SECURITY.md)
[![Website](https://img.shields.io/badge/website-getlumel.app-ff7a00)](https://getlumel.app)
[![GitHub stars](https://img.shields.io/github/stars/onekapisch/LUMEL-public?style=social)](https://github.com/onekapisch/LUMEL-public/stargazers)

**[⬇️ Download on the Mac App Store](https://apps.apple.com/us/app/lumel/id6776136831)&nbsp; · &nbsp;[🌐 getlumel.app](https://getlumel.app)&nbsp; · &nbsp;[🐞 Report a bug / request a feature](https://github.com/onekapisch/LUMEL-public/issues/new/choose)**

<br />

<img src="docs/hero.png" alt="LUMEL boosting a MacBook XDR display brighter than macOS allows, from the menu bar" width="820" />

</div>

> [!NOTE]
> **LUMEL is a commercial, closed-source Mac app.** This repository hosts its **docs, release notes, and issue tracker**, not the source code. Found a bug or want a feature? [Open an issue](https://github.com/onekapisch/LUMEL-public/issues/new/choose). They're read and welcomed.

---

## Why

macOS quietly caps two things:

- **Brightness tops out around 500 nits** for everyday (SDR) content, even on MacBook Pro displays rated for 1000 nits sustained and ~1600 peak. Step into sunlight and the screen washes out.
- **The brightness slider won't go below a fixed floor.** In a dark room at night, even the lowest setting can feel harsh, a common cause of eye strain. (Apple's own 2024 MacBook Pro displays were widely covered for going *"even dimmer in low light"*, proof both ends of the range matter.)

LUMEL fixes **both**, from the menu bar, using Apple's public Extended Dynamic Range rendering. No private APIs, no system hacks.

## What you get

- ☀️ **Boost beyond the cap:** push a supported XDR display toward its ~1600-nit peak so it stays readable in direct sunlight.
- 🌙 **Eclipse: dim below the minimum.** Go darker than macOS allows for night reading and dark rooms. *Free and unlimited.*
- ↔️ **Both directions, one app:** the only Mac brightness app that brightens **and** dims. No second app for night.
- ⌨️ **Global shortcut (⌃⌥⌘B):** toggle boost from any app. **No Accessibility permission required.**
- 🔋 **Battery-aware:** set a 10-50% threshold and boost switches off automatically; Low Power Mode disables it too.
- ⏲️ **Optional auto-off timer:** 30 min / 1 h / 2 h, so sustained brightness never sneaks up on you.
- 🖥️ **Per-display memory:** on/off per screen, remembered across reconnects, sleep, and hot-plug.
- 🔒 **Private by architecture:** sandboxed, no network entitlement, collects nothing. See **[SECURITY.md](SECURITY.md)**.

<div align="center">
<img src="docs/eclipse.png" alt="LUMEL Eclipse mode dimming a Mac below the system minimum brightness for night" width="410" />&nbsp;
<img src="docs/two-way.png" alt="LUMEL Boost and Eclipse, brighten and dim a Mac display from one app" width="410" />
</div>

## Supported Macs

| Display | Boost (brighter than max) | Eclipse (dim below min) |
|---|:--:|:--:|
| 14″ / 16″ MacBook Pro (Apple silicon, XDR) | ✅ | ✅ |
| Pro Display XDR · Studio Display | ✅ | ✅ |
| Other Macs / external monitors | No *(needs EDR headroom)* | ✅ |

Boost requires a display that reports Extended Dynamic Range headroom. On displays without it, LUMEL still runs and **Eclipse dimming still works**, so the boost controls simply stay inactive until a compatible display is connected.

## How it compares

An honest look at the apps people ask about: differences, not trash-talk.

| | **LUMEL** | Vivid | BrightIntosh | LumiMax |
|---|:--:|:--:|:--:|:--:|
| **Direction** | **Brighten + dim** | Brighten only | Brighten only | Brighten only |
| **Dim below minimum** | ✅ Eclipse | ❌ | ❌ | ❌ |
| **Price** | **Free + $2.99 once** | ~$15 once | $1.99 once | $16.35 + fee |
| **Free tier** | ✅ Compare boost + full Eclipse | Watermark demo | 3‑day trial | 3‑day trial |
| **Native brightness keys** | ❌ *(sandbox trade-off)* | ✅ | ✅ | ✅ |
| **Collects no data** | ✅ | ✅ | ✅ | ✅ |
| **Open source** | ❌ | ❌ | ✅ | ❌ |

**Where others win:** Vivid, BrightIntosh, and LumiMax hook into your Mac's **native brightness keys**; LUMEL trades that away to stay sandboxed and permission-free. BrightIntosh is also **open-source and $1.99**, so it's cheaper. If below-minimum dimming, a free tier that never expires, and a single app for both directions matter more to you, that's LUMEL. *Competitor prices verified June 2026. Check each store for current pricing.*

## Privacy & security

LUMEL is **sandboxed with no network entitlement**, so it cannot send data off your Mac. No analytics, no telemetry, no accounts, no ads. The $2.99 purchase is handled by the App Store (StoreKit), not by LUMEL. Full details in **[SECURITY.md](SECURITY.md)**.

## Install

1. Open the **[Mac App Store listing](https://apps.apple.com/us/app/lumel/id6776136831)** and click **Get**.
2. Launch LUMEL. It lives in your **menu bar**.
3. Click the icon, choose **Boost** or **Eclipse**, and drag the slider.
4. *(Optional)* Tap **Full screen** to unlock **LUMEL Pro** ($2.99) for whole-display boost across every screen.

- **Update:** via the Mac App Store → Updates (auto-updates if enabled).
- **Uninstall:** quit LUMEL, then remove it from the App Store (Uninstall) or `/Applications`. It leaves nothing behind but a small preferences file in `~/Library`.
- **Requirements:** macOS 13 (Ventura) or later. Boost requires an EDR/XDR-capable display.

## Roadmap & feedback

Have a bug, a Mac that should be supported, or a feature idea? **[Open an issue](https://github.com/onekapisch/LUMEL-public/issues/new/choose)**. This tracker is the official place for it, and it shapes the roadmap.

## FAQ

**Is LUMEL open source?**
No. LUMEL is a commercial, closed-source app on the Mac App Store. This repository hosts its docs, release notes, and issue tracker. (Prefer open source? [BrightIntosh](https://brightintosh.de/) is a solid GPL-licensed, brighten-only option.)

**Why pay $2.99 when BrightIntosh is $1.99 (and free apps exist)?**
Because LUMEL is the only one that also **dims below the minimum**, and its free tier (Compare boost plus **unlimited Eclipse dimming**) never expires. You're paying for two-way control and a lasting free tier, not just a brightness boost. If you only ever brighten, a cheaper brighten-only app may suit you better, and that's fine.

**Does it collect any data?**
No. Sandboxed, no network entitlement, no analytics or accounts. Your preferences stay on your Mac. See [SECURITY.md](SECURITY.md).

**Which Macs work?**
Boost needs an EDR/XDR display (14″/16″ MacBook Pro Apple silicon, Pro Display XDR, Studio Display). Eclipse dimming works on **any** Mac running macOS 13+.

---

<div align="center">

**If LUMEL makes your Mac better, [⭐ star this repo](https://github.com/onekapisch/LUMEL-public). It helps others find it.**

[Download](https://apps.apple.com/us/app/lumel/id6776136831) · [Website](https://getlumel.app) · [Report an issue](https://github.com/onekapisch/LUMEL-public/issues/new/choose) · [Security](SECURITY.md) · [Changelog](CHANGELOG.md)

<sub>Not affiliated with Apple Inc. macOS, MacBook, and Mac are trademarks of Apple Inc.</sub>

</div>
