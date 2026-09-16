# WebToApp Studio Pro :rocket:

> **Commercial Cross-Platform Web-to-Desktop & Mobile Packaging Engine**  
> Turn any Website URL or Local Static HTML5/CSS/JS Folder into Standalone Windows Executables, Google Play Android Apps, and Ubuntu Linux Debian Packages.

[![Latest Release](https://img.shields.io/github/v/release/djacidfx/webtoapp-releases?style=flat-square&color=success&label=Latest%20Release)](https://github.com/djacidfx/webtoapp-releases/releases/latest)
[![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Android%20%7C%20Ubuntu%20Linux-blue?style=flat-square)](#)
[![Engines](https://img.shields.io/badge/Engines-WebView2%20%7C%20Android%20WebView%20%7C%20WebKitGTK-orange?style=flat-square)](#)
[![Documentation](https://img.shields.io/badge/Documentation-Official%20Wiki-purple?style=flat-square)](https://github.com/djacidfx/webtoapp-releases/wiki)
[![License](https://img.shields.io/badge/License-Commercial-green?style=flat-square)](https://github.com/djacidfx/webtoapp-releases/releases)

---

## :zap: Quick Navigation

* :package: **[Download Latest Release (v1.2.0)](https://github.com/djacidfx/webtoapp-releases/releases/latest)**
* :shield: **[Release Integrity & VirusTotal Scan Verification](#release-integrity)**
* :books: **[Official Documentation & User Guides (Wiki)](https://github.com/djacidfx/webtoapp-releases/wiki)**
* :rocket: **[Quick Start Guide](https://github.com/djacidfx/webtoapp-releases/wiki/Quick-Start-Guide)**
* :balance_scale: **[Legal Disclaimer & Acceptable Use Policy](#legal-disclaimer)**
* :beetle: **[Report an Issue / Request a Feature](https://github.com/djacidfx/webtoapp-releases/issues)**
* :coffee: **[Support on Buy Me a Coffee](https://buymeacoffee.com/wildcatstudio)** | :heart: **[Support on Patreon](https://www.patreon.com/c/wildcatstudio)**

---

## :book: Overview

**WebToApp Studio Pro** is a high-performance commercial utility designed for web developers, software entrepreneurs, SaaS creators, game developers, and digital agencies. It transforms any **Live Website URL** or **Local Static HTML5/CSS/JS Folder** into standalone, production-ready software across three major operating systems:

1. **:window: Windows Executables (`.exe`)**:
   * Powered by **Microsoft Edge WebView2** with ultra-compact resource footprint (~14 MB vs 150MB+ Electron wrappers).
   * **Virtual HTTPS Host (`https://app.local/`)**: Eliminates `file://` protocol CORS restrictions -- Canvas, Web Audio API, IndexedDB, and ES6 modules run seamlessly offline.
   * **Commercial Binary Sealing**: HTML/JS/CSS assets can be encrypted with AES-256 and streamed in-memory with zero plaintext files exposed on the user's disk.
   * Multi-resolution `.ico` icon injection, splash screens, system tray minimization, single instance mutex, and full window customization.

2. **:department_store: Microsoft Store Packages (`.msix`)**:
   * **$0 Code Signing Expense**: Microsoft automatically re-signs packages with its trusted root certificate for free upon submission to Partner Center.
   * **Automated Visual Asset Pipeline**: Renders 5 scaled Store/Start Menu tile assets (`StoreLogo`, `Square150x150`, `Square44x44`, `Wide310x150`, `SplashScreen`).
   * **1-Click Local Sideload Trust**: Built-in RSA 2048 test cert generator and elevated PowerShell installer for instant local testing.

3. **:iphone: Google Play Android Apps (`.aab` / `.apk` / Gradle Project)**:
   * Turnkey **Android 14 (API 34)** Gradle project ready to import into Android Studio or publish directly to Google Play.
   * **Device Compatibility (`minSdk = 24`)**: Runs on **Android 7.0 through Android 14+** (covering 96.3%+ of all global devices).
   * **Modern WebViewAssetLoader**: Zero-CORS offline static assets served via secure HTTPS scheme.
   * Mobile pull-to-refresh (`SwipeRefreshLayout`), hardware acceleration, screen orientation locking, and Keep-Screen-On (WakeLock).
   * Integrated release signing and step-by-step Google Play publishing guide.

4. **:penguin: Ubuntu Linux Debian Packages (`.deb` / Portable AppDir)**:
   * Pure C# Debian binary compiler -- generates compliant `.deb` installer packages directly on Windows with **zero external dependencies** (no WSL, Docker, or Linux VMs required).
   * Dual deliverables: Installable Debian package (`sudo dpkg -i app.deb`) and standalone portable AppDir (`./run.sh`).
   * WebKitGTK runner with Chromium kiosk fallback and embedded localhost web server with ephemeral session tokens.

5. **:zap: Multi-Platform Multi-Build**:
   * Build Windows `.exe`, Microsoft Store `.msix`, Android Studio ZIP, and Ubuntu `.deb` packages all simultaneously in a single click.

6. **:arrows_counterclockwise: 1-Click In-App Auto-Updater**:
   * Remote version manifests, visual changelog modal, and automated in-app updates with SHA-256 cryptographic verification.

---

## :rocket: Quick Start

### 1. Download & Run
1. Go to the **[Latest Release](https://github.com/djacidfx/webtoapp-releases/releases/latest)**.
2. Download the distribution ZIP: `WebToApp-Studio-v1.1.5.zip`.
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

## :books: Official Wiki Documentation

Comprehensive guides, tutorials, and technical references are hosted in the **[Official Wiki](https://github.com/djacidfx/webtoapp-releases/wiki)**:

| Guide | Description |
|---|---|
| :rocket: **[Quick Start Guide](https://github.com/djacidfx/webtoapp-releases/wiki/Quick-Start-Guide)** | 5-minute setup and packaging walkthrough |
| :window: **[Windows Executable Packaging](https://github.com/djacidfx/webtoapp-releases/wiki/Windows-Executable-Packaging)** | WebView2 engine, virtual HTTPS host, window styling, and tray icons |
| :iphone: **[Android & Google Play Guide](https://github.com/djacidfx/webtoapp-releases/wiki/Android-Google-Play-Publishing)** | AssetLoader, Gradle configuration, permissions, and Google Play submission |
| :penguin: **[Ubuntu Linux Packaging](https://github.com/djacidfx/webtoapp-releases/wiki/Ubuntu-Linux-Debian-Packaging)** | Pure C# Debian compiler, WebKitGTK runner, and desktop integration |
| :shield: **[Enterprise Security Hardening](https://github.com/djacidfx/webtoapp-releases/wiki/Enterprise-Security-Hardening)** | AES-256 asset encryption, anti-debugging, and memory streaming |
| :arrows_counterclockwise: **[In-App Auto-Updater Setup](https://github.com/djacidfx/webtoapp-releases/wiki/1-Click-Auto-Updater-Guide)** | Manifest configuration, SHA-256 verification, and update deployment |
| :question: **[Troubleshooting & FAQ](https://github.com/djacidfx/webtoapp-releases/wiki/Troubleshooting-and-FAQ)** | Solutions for common questions, edge cases, and runtime issues |

<a id="release-integrity"></a>
## :shield: Release Integrity & Anti-Malware Verification

All release binaries are cryptographically signed, SHA-256 hashed, and independently verified clean against **70+ security engines via VirusTotal**:

| Distribution Package | Platform | SHA-256 Checksum | VirusTotal Scan Verification | Status |
|---|---|---|---|:---:|
| `WebToApp-Studio-v1.2.0.zip` | Windows (Portable Zip) | `97b1449f12c3492a70a746d148c6e04d5d25fb12ca6d3eba49dad0210ba2ba21` | [Inspect on VirusTotal (70+ Engines)](https://www.virustotal.com/gui/file/97b1449f12c3492a70a746d148c6e04d5d25fb12ca6d3eba49dad0210ba2ba21) | âœ… Clean |
| `WebToApp-Studio-Pro_1.2.0_amd64.deb` | Ubuntu / Debian (.deb) | `60321a7aef3c619db781da66fa576acf79b19010b4a0b8ade477f4944b23cb71` | [Inspect on VirusTotal (70+ Engines)](https://www.virustotal.com/gui/file/60321a7aef3c619db781da66fa576acf79b19010b4a0b8ade477f4944b23cb71) | âœ… Clean |
| `WebToApp-Studio-Pro-Linux-x64-v1.2.0-Portable.tar.gz` | Linux x64 (.tar.gz) | `ec28f63a9f736a4379b6cf142d27dbeee3201aa58b61a7cf703203f0d1a8d711` | [Inspect on VirusTotal (70+ Engines)](https://www.virustotal.com/gui/file/ec28f63a9f736a4379b6cf142d27dbeee3201aa58b61a7cf703203f0d1a8d711) | âœ… Clean |

---

## :computer: System Requirements

### Host Environment (Studio Builder)
* **Operating System**: Windows 10 (Build 1809+) or Windows 11 (64-bit)
* **Runtime**: Microsoft Edge WebView2 Evergreen Runtime (included with Windows 11 and modern Windows 10)
* **Architecture**: x64

### Target Output Environments
* **Windows Executables**: Windows 10 / 11 (64-bit) with WebView2 Runtime
* **Android Apps**: Android 7.0 (API 24) through Android 14 (API 34+)
* **Linux Packages**: Ubuntu 20.04+, Debian 11+, Linux Mint 20+, or compatible Debian-based distributions with GTK3 / WebKit2GTK

---

## :beetle: Feedback, Bug Reports & Feature Requests

Encountered an issue or have an idea to make WebToApp Studio Pro even better?

* :memo: **[Submit an Issue or Request](https://github.com/djacidfx/webtoapp-releases/issues)**
* When submitting bugs, please include:
  * Your version number (e.g. `v1.1.5`)
  * Windows OS version
  * Target output platform (Windows / Android / Linux)
  * Any error logs or screenshots

---

## :coffee: Support the Creator

If **WebToApp Studio Pro** accelerates your workflows and helps you deliver client apps, games, or SaaS wrappers, consider supporting ongoing development:

* :coffee: **Buy Me a Coffee**: [buymeacoffee.com/wildcatstudio](https://buymeacoffee.com/wildcatstudio)
* :heart: **Patreon**: [patreon.com/c/wildcatstudio](https://www.patreon.com/c/wildcatstudio)

---

<a id="legal-disclaimer"></a>
## :balance_scale: Legal Disclaimer & Acceptable Use Policy

### 1. Important Legal Notice
**WebToApp Studio Pro** is a software utility developed to help developers, creators, and website owners package **their own** web applications, static websites, and games into native executables for Windows, Android, and Ubuntu Linux.

The author/maintainers of WebToApp Studio Pro do not own, control, host, review, or endorse any third-party websites, applications, assets, or content packaged or distributed by end users of this software.

### 2. Prohibited Uses & Unacceptable Conduct
By downloading, running, or using WebToApp Studio Pro, you explicitly agree that you will **NOT** use this software to:

* **Impersonate or Phish**: Create applications that impersonate financial institutions, government agencies, social networks, or third-party brands, or engage in credential harvesting, fraud, or social engineering.
* **Infringe Intellectual Property**: Package, distribute, or monetize websites, web applications, media, games, or trademarks that you do not own or for which you have not obtained explicit written authorization and licensing from the rightful copyright holder.
* **Distribute Malicious Software**: Package or inject malware, spyware, ransomware, keyloggers, unauthorized tracking scripts, cryptominers, or any code designed to disrupt, damage, or gain unauthorized access to any system or user data.
* **Bypass Access Controls or Paywalls**: Circumvent authentication mechanisms, digital rights management (DRM), paywalls, or terms of service of third-party platforms.
* **Violate Platform & Store Policies**: Submit applications to the Microsoft Store, Google Play Store, or Linux package repositories that violate their respective developer distribution agreements, privacy guidelines, or content policies.

### 3. Limitation of Liability & Warranty Disclaimer
* **"AS-IS" Provision**: This software is provided *"as is"*, without warranty of any kind, express or implied, including but not limited to the warranties of merchantability, fitness for a particular purpose, and non-infringement.
* **Zero Liability**: In no event shall the authors, copyright holders, or contributors be liable for any claim, damages, legal actions, criminal prosecution, civil liability, loss of data, loss of profits, or regulatory penalties arising from, out of, or in connection with the software, its use, or the packaging and distribution of any third-party applications created with it.
* **User Indemnification**: The user of this tool assumes 100% full legal responsibility and liability for all applications, packages, domains, and assets generated, signed, or distributed using WebToApp Studio Pro.

### 4. Trademark Attribution
* "Windows", "Microsoft Store", "WebView2", and "MSIX" are trademarks of Microsoft Corporation.
* "Android", "Google Play", and "Chromium" are trademarks of Google LLC.
* "Ubuntu" is a registered trademark of Canonical Ltd.
* All trademarks, logos, and brand names mentioned are the property of their respective owners and are used strictly for identification and compatibility purposes. Their mention does not imply endorsement or affiliation.

---

## :page_facing_up: Commercial License

WebToApp Studio Pro is distributed under commercial terms. For licensing details, please refer to the license agreement included with your purchase.

Copyright (c) 2026 **Wildcat Studio**. All rights reserved.
