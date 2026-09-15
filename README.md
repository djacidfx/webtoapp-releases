# WebToApp Studio Pro 🚀

> **Commercial Cross-Platform Web-to-Desktop & Mobile Packaging Engine**  
> Turn any Website URL or Local Static HTML5/CSS/JS Folder into Standalone Windows Executables, Google Play Android Apps, and Ubuntu Linux Debian Packages.

[![Latest Release](https://img.shields.io/github/v/release/djacidfx/webtoapp-releases?style=flat-square&color=success&label=Latest%20Release)](https://github.com/djacidfx/webtoapp-releases/releases/latest)
[![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Android%20%7C%20Ubuntu%20Linux-blue?style=flat-square)](#)
[![Engines](https://img.shields.io/badge/Engines-WebView2%20%7C%20Android%20WebView%20%7C%20WebKitGTK-orange?style=flat-square)](#)
[![Documentation](https://img.shields.io/badge/Documentation-Official%20Wiki-purple?style=flat-square)](https://github.com/djacidfx/webtoapp-releases/wiki)
[![License](https://img.shields.io/badge/License-Commercial-green?style=flat-square)](https://github.com/djacidfx/webtoapp-releases/releases)

---

## ⚡ Quick Navigation

* 📥 **[Download Latest Release (v1.1.4)](https://github.com/djacidfx/webtoapp-releases/releases/latest)**
* 📚 **[Official Documentation & User Guides (Wiki)](https://github.com/djacidfx/webtoapp-releases/wiki)**
* 🚀 **[Quick Start Guide](https://github.com/djacidfx/webtoapp-releases/wiki/Quick-Start-Guide)**
* 🐛 **[Report an Issue / Request a Feature](https://github.com/djacidfx/webtoapp-releases/issues)**
* ☕ **[Support on Buy Me a Coffee](https://buymeacoffee.com/wildcatstudio)** | ❤️ **[Support on Patreon](https://www.patreon.com/c/wildcatstudio)**

---

## 📖 Overview

**WebToApp Studio Pro** is a high-performance commercial utility designed for web developers, software entrepreneurs, SaaS creators, game developers, and digital agencies. It transforms any **Live Website URL** or **Local Static HTML5/CSS/JS Folder** into standalone, production-ready software across three major operating systems:

1. **🪟 Windows Executables (`.exe`)**:
   * Powered by **Microsoft Edge WebView2** with ultra-compact resource footprint (~14 MB vs 150MB+ Electron wrappers).
   * **Virtual HTTPS Host (`https://app.local/`)**: Eliminates `file://` protocol CORS restrictions — Canvas, Web Audio API, IndexedDB, and ES6 modules run seamlessly offline.
   * **Commercial Binary Sealing**: HTML/JS/CSS assets can be encrypted with AES-256 and streamed in-memory with zero plaintext files exposed on the user's disk.
   * Multi-resolution `.ico` icon injection, splash screens, system tray minimization, single instance mutex, and full window customization.

2. **📱 Google Play Android Apps (`.aab` / `.apk` / Gradle Project)**:
   * Turnkey **Android 14 (API 34)** Gradle project ready to import into Android Studio or publish directly to Google Play.
   * **Modern WebViewAssetLoader**: Zero-CORS offline static assets served via secure HTTPS scheme.
   * Mobile pull-to-refresh (`SwipeRefreshLayout`), hardware acceleration, screen orientation locking, and Keep-Screen-On (WakeLock).
   * Integrated release signing and step-by-step Google Play publishing guide.

3. **🐧 Ubuntu Linux Debian Packages (`.deb` / Portable AppDir)**:
   * Pure C# Debian binary compiler — generates compliant `.deb` installer packages directly on Windows with **zero external dependencies** (no WSL, Docker, or Linux VMs required).
   * Dual deliverables: Installable Debian package (`sudo dpkg -i app.deb`) and standalone portable AppDir (`./run.sh`).
   * WebKitGTK runner with Chromium kiosk fallback and embedded localhost web server with ephemeral session tokens.

4. **⚡ Tri-Platform Multi-Build**:
   * Build Windows `.exe`, Android Studio ZIP, and Ubuntu `.deb` packages all simultaneously in a single click.

5. **🔄 1-Click In-App Auto-Updater**:
   * Remote version manifests, visual changelog modal, and automated in-app updates with SHA-256 cryptographic verification.

---

## 🚀 Quick Start

### 1. Download & Run
1. Go to the **[Latest Release](https://github.com/djacidfx/webtoapp-releases/releases/latest)**.
2. Download the distribution ZIP: `WebToApp-Studio-Pro-vX.X.X.zip`.
3. Extract the ZIP archive on your Windows machine.
4. Open the `01-WebToApp-Studio/` directory and double-click **`WebToExe.Studio.exe`**.

### 2. Packaging Your Application
1. **Choose Target Platform**: Select **Windows (.exe)**, **Android App**, **Ubuntu Linux**, or **Multi-Build**.
2. **Select Source**:
   - **Website URL**: Enter your live website (e.g. `https://myawesomeapp.com`).
   - **Local HTML5 Folder**: Select your static folder containing `index.html` (e.g. HTML5 game, React, Vue, Vite, or static site export).
3. **Branding & Sizing**: Set your App Name, Executable Name, Version, Window Dimensions, and upload your icon.
4. **Platform-Specific Settings**: Customize package names, permissions, and orientations.
5. Click **BUILD EXECUTABLE** (or **MULTI-BUILD**).
6. Click **Test Run App** or **Open Output Folder** to distribute your software!

---

## 📚 Official Wiki Documentation

Comprehensive guides, tutorials, and technical references are hosted in the **[Official Wiki](https://github.com/djacidfx/webtoapp-releases/wiki)**:

| Guide | Description |
|---|---|
| 🚀 **[Quick Start Guide](https://github.com/djacidfx/webtoapp-releases/wiki/Quick-Start-Guide)** | 5-minute setup and packaging walkthrough |
| 🪟 **[Windows Executable Packaging](https://github.com/djacidfx/webtoapp-releases/wiki/Windows-Executable-Packaging)** | WebView2 engine, virtual HTTPS host, window styling, and tray icons |
| 📱 **[Android & Google Play Guide](https://github.com/djacidfx/webtoapp-releases/wiki/Android-Google-Play-Publishing)** | AssetLoader, Gradle configuration, permissions, and Google Play submission |
| 🐧 **[Ubuntu Linux Packaging](https://github.com/djacidfx/webtoapp-releases/wiki/Ubuntu-Linux-Debian-Packaging)** | Pure C# Debian compiler, WebKitGTK runner, and desktop integration |
| 🛡️ **[Enterprise Security Hardening](https://github.com/djacidfx/webtoapp-releases/wiki/Enterprise-Security-Hardening)** | AES-256 asset encryption, anti-debugging, and memory streaming |
| 🔄 **[In-App Auto-Updater Setup](https://github.com/djacidfx/webtoapp-releases/wiki/1-Click-Auto-Updater-Guide)** | Manifest configuration, SHA-256 verification, and update deployment |
| ❓ **[Troubleshooting & FAQ](https://github.com/djacidfx/webtoapp-releases/wiki/Troubleshooting-and-FAQ)** | Solutions for common questions, edge cases, and runtime issues |

---

## 💻 System Requirements

### Host Environment (Studio Builder)
* **Operating System**: Windows 10 (Build 1809+) or Windows 11 (64-bit)
* **Runtime**: Microsoft Edge WebView2 Evergreen Runtime (included with Windows 11 and modern Windows 10)
* **Architecture**: x64

### Target Output Environments
* **Windows Executables**: Windows 10 / 11 (64-bit) with WebView2 Runtime
* **Android Apps**: Android 7.0 (API 24) through Android 14 (API 34+)
* **Linux Packages**: Ubuntu 20.04+, Debian 11+, Linux Mint 20+, or compatible Debian-based distributions with GTK3 / WebKit2GTK

---

## 🐛 Feedback, Bug Reports & Feature Requests

Encountered an issue or have an idea to make WebToApp Studio Pro even better?

* 📝 **[Submit an Issue or Request](https://github.com/djacidfx/webtoapp-releases/issues)**
* When submitting bugs, please include:
  * Your version number (e.g. `v1.1.4`)
  * Windows OS version
  * Target output platform (Windows / Android / Linux)
  * Any error logs or screenshots

---

## ☕ Support the Creator

If **WebToApp Studio Pro** accelerates your workflows and helps you deliver client apps, games, or SaaS wrappers, consider supporting ongoing development:

* ☕ **Buy Me a Coffee**: [buymeacoffee.com/wildcatstudio](https://buymeacoffee.com/wildcatstudio)
* ❤️ **Patreon**: [patreon.com/c/wildcatstudio](https://www.patreon.com/c/wildcatstudio)

---

## 📄 Commercial License

WebToApp Studio Pro is distributed under commercial terms. For licensing details, please refer to the license agreement included with your purchase.

Copyright © 2026 **Wildcat Studio**. All rights reserved.
