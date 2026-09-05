<p align="center">
  <img src="app_icon.png" width="100" alt="CineVerse Prime" />
</p>
<h1 align="center">CineVerse Prime</h1>
<p align="center">
  <strong>Open-source Android streaming client</strong><br>
  Movies · Series · Anime · Live TV
</p>

<p align="center">
  <a href="https://github.com/singaporecool4-cyber/cineverse-prime/releases/latest"><img src="https://img.shields.io/github/v/release/singaporecool4-cyber/cineverse-prime?style=flat-square&color=2997ff" alt="Release" /></a>
  <a href="https://github.com/singaporecool4-cyber/cineverse-prime/releases"><img src="https://img.shields.io/github/downloads/singaporecool4-cyber/cineverse-prime/total?style=flat-square&color=34c759" alt="Downloads" /></a>
  <a href="https://github.com/singaporecool4-cyber/cineverse-prime/blob/main/LICENSE"><img src="https://img.shields.io/github/license/singaporecool4-cyber/cineverse-prime?style=flat-square" alt="License" /></a>
  <a href="https://t.me/CineVersePrime"><img src="https://img.shields.io/badge/Telegram-Channel-0088cc?style=flat-square&logo=telegram" alt="Telegram" /></a>
</p>

---

## Overview

CineVerse Prime is a native Android app built with Kotlin, Jetpack Compose, and a custom AGSL glass shader system. It aggregates publicly available streaming sources into a single interface with no ads, no account required.

---

## Features

- **Glass UI** — Frosted glass panels rendered with AGSL shaders. Real-time blur on every card, navbar, and overlay.
- **Gesture Player** — Swipe for brightness/volume, long-press for 2x, tap to play/pause. Zero button clutter.
- **Resume Playback** — Watch history with per-title progress. Pick up exactly where you left off.
- **Offline Downloads** — Download movies and episodes for offline viewing via the built-in download manager.
- **Multi-Server** — Multiple streaming providers with automatic fallover. Switch sources instantly.
- **Live TV** — Stream live television channels directly in-app.
- **DNS-over-HTTPS** — All network traffic routed through Cloudflare DoH with connection pooling.
- **120fps Support** — Requests highest available display refresh rate on compatible devices.

---

## Screenshots

<p align="center">
  <img src="screenshots/home.png" width="200" />
  <img src="screenshots/detail.png" width="200" />
  <img src="screenshots/player.png" width="200" />
  <img src="screenshots/search.png" width="200" />
</p>

---

## Tech Stack

| Layer | Technology |
|---|---|
| Language | Kotlin, Java |
| UI | Jetpack Compose, XML Views |
| Shaders | AGSL (Android Graphics Shading Language) |
| Networking | OkHttp + Retrofit, DNS-over-HTTPS |
| Player | WebView + HLS.js (bundled locally) |
| Image Loading | Coil |
| Data | SharedPreferences, TMDB API |
| Build | Gradle (Kotlin DSL), JDK 17 |

---

## Build

```bash
# Clone
git clone https://github.com/singaporecool4-cyber/cineverse-prime.git
cd cineverse-prime

# Build debug APK
./gradlew assembleDebug

# Build release APK
./gradlew assembleRelease
```

> Requires JDK 17 and Android SDK 34+.

---

## Project Structure

```
app/src/main/java/com/cineverseprime/app/
├── api/              # Network layer (Retrofit, OkHttp, DoH tunnel)
├── models/           # Data models, caches, managers
├── adapters/         # RecyclerView adapters
├── ui/
│   ├── components/   # Glass cards, navbar, hero banner, shaders
│   ├── screens/      # Compose screens (Home, Search, Downloads, Live TV)
│   └── theme/        # Color system, typography
├── MainActivity.kt   # App entry point
├── DetailActivity.java
├── CinefyPlayerActivity.kt
└── SplashActivity.kt
```

---

## Download

Get the latest APK from [Releases](https://github.com/singaporecool4-cyber/cineverse-prime/releases/latest) or visit [CineVerse Prime Web](https://cineverse-prime.pages.dev).

---

## Disclaimer

This application does not host, store, or distribute any media content. All streams are sourced from publicly available third-party APIs. All rights to the content belong to their respective owners.

CineVerse Prime does not claim ownership or responsibility for any material displayed. The app functions solely as an aggregator of publicly accessible resources.

If you are a copyright holder and believe any content infringes your rights, please [contact us](https://t.me/CineVersePrime) for prompt removal.

---

## License

This project is licensed under the [MIT License](LICENSE).

---

<p align="center">
  Built by <a href="https://github.com/singaporecool4-cyber">Developer</a>
</p>
