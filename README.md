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

* :package: **[Download Latest Release (v1.4.2)](https://github.com/djacidfx/webtoapp-releases/releases/latest)**
* :white_check_mark: **[Complete Feature Checklist & Architecture Capabilities](#feature-checklist)**
* :shield: **[Release Integrity & VirusTotal Scan Verification](#release-integrity)**
* :books: **[Official Documentation & User Guides (Wiki)](https://github.com/djacidfx/webtoapp-releases/wiki)**
* :rocket: **[Quick Start Guide](https://github.com/djacidfx/webtoapp-releases/wiki/Quick-Start-Guide)**
* :balance_scale: **[Legal Disclaimer & Acceptable Use Policy](#legal-disclaimer)**
* :beetle: **[Report an Issue / Request a Feature](https://github.com/djacidfx/webtoapp-releases/issues)**
* :coffee: **[Support on Buy Me a Coffee](https://buymeacoffee.com/wildcatstudio)** | :star: **[Star on GitHub](https://github.com/djacidfx/webtoapp-releases)**

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

5. **:card_file_box: Built-in SQLite & Local Database Bridge**:
   * Embedded native SQLite 3 engine (`Microsoft.Data.Sqlite`) with zero native driver dependencies.
   * Promise-based client API at `window.desktopApp.db` supporting parameterized `query()`, `execute()`, and atomic `executeBatch()` transactions.
   * Security hardening: origin isolation (`https://app.local/*`), path traversal protection, and dangerous PRAGMA blocking.

6. **:link: Custom Deep-Linking (`myapp://`) Protocol Engine**:
   * Cross-platform URL protocol scheme registration (`HKCU\Software\Classes`, Inno Setup, MSIX, and Linux `.desktop`).
   * Single-instance IPC over named pipes (`WebToApp_IPC_<AppName>`) forwards arguments silently without secondary popups.
   * Automatic window focus & restoration (`ShowWindow(SW_RESTORE)` & `SetForegroundWindow`).
   * RFC 3986 scheme validation, reserved scheme blacklist, and argument injection immunity.
   * Client JavaScript bridge via `window.desktopApp.onDeepLink()` and `getLaunchUrl()`.

7. **:zap: Multi-Platform Multi-Build**:
   * Build Windows `.exe`, Microsoft Store `.msix`, Android Studio ZIP, and Ubuntu `.deb` packages all simultaneously in a single click.

8. **:arrows_counterclockwise: 1-Click In-App Auto-Updater**:
   * Remote version manifests, visual changelog modal, and automated in-app updates with SHA-256 cryptographic verification.

---

<a id="feature-checklist"></a>
## :white_check_mark: Complete Feature Checklist & Architecture Capabilities

Comprehensive internal feature checklist and capability tracker reflecting all features, architectures, export platforms, and security controls through **v1.4.2**:

### 1. Dual Source Processing & Asset Pipeline
- [x] **Website URL Mode**:
  - [x] Wraps any live website, SaaS platform, Shopify, WooCommerce, WordPress, or custom web app
  - [x] Automatic offline connection detector with animated retry screen
  - [x] External domain link interception (routes external links to user's default browser)
- [x] **Local Static HTML Folder Mode**:
  - [x] Wraps local HTML5, CSS3, JavaScript (ES6 modules), WebGL, Canvas 2D, and Web Audio
  - [x] Full offline support for `localStorage` and `IndexedDB`
- [x] **Zero-CORS Virtual Host Engine**:
  - [x] Internal virtual host mapping (`https://app.local/`) avoiding `file://` protocol security restrictions
  - [x] Eliminates CORS errors when loading fonts, audio, JSON data, Web Workers, or assets
- [x] **Commercial Binary Sealing & Asset Encryption**:
  - [x] AES-256 binary encryption for all local HTML/CSS/JS/media assets
  - [x] Direct in-memory decryption and streaming into WebView2 / AssetLoader
  - [x] Zero plaintext files exposed on the user's disk
  - [x] Anti-tamper integrity verification and header validation

---

### 2. Multi-Platform Target Export Engines
- [x] **Windows Executables (`.exe`)**:
  - [x] Powered by Microsoft Edge WebView2 runtime (~14 MB footprint vs 150MB+ Electron wrappers)
  - [x] Standalone Edition (self-contained, zero dependencies, runs immediately on any Windows 10/11 PC)
  - [x] Lightweight Edition (compact download utilizing shared .NET 8 Desktop Runtime)
  - [x] Inno Setup installer script generator (`.iss` with desktop shortcuts, start menu, and uninstaller)
  - [x] System tray minimization with custom context menu (Open / Exit)
  - [x] Single-Instance Mutex lock with named pipe IPC
- [x] **Microsoft Store Packages (`.msix`)**:
  - [x] Modern Windows App packaging (`AppxManifest.xml` generator)
  - [x] $0 code signing (automatically re-signed with Microsoft's trusted root certificate upon Partner Center submission)
  - [x] Visual Asset Pipeline: automated generation of 5 scaled tile/splash assets (`StoreLogo`, `Square150x150`, `Square44x44`, `Wide310x150`, `SplashScreen`)
  - [x] 1-Click local sideload trust: RSA 2048 test certificate generator and elevated PowerShell installer script
  - [x] Protocol extension declaration (`windows.protocol`) for custom deep linking
- [x] **Google Play & Android Mobile (`.aab` / `.apk` / Gradle Project)**:
  - [x] Turnkey Android 14 (API 34) Gradle project ready to import into Android Studio or compile via CLI
  - [x] Device compatibility: `minSdk = 24` (supports Android 7.0 through Android 14+, 96.3%+ of all global devices)
  - [x] Modern `WebViewAssetLoader` with zero-CORS secure HTTPS local asset serving
  - [x] Mobile pull-to-refresh (`SwipeRefreshLayout`)
  - [x] Hardware acceleration, screen orientation locking (portrait, landscape, sensor), and Keep-Screen-On (WakeLock)
  - [x] Multi-density icon generator (`mipmap-mdpi`, `hdpi`, `xhdpi`, `xxhdpi`, `xxxhdpi`)
  - [x] Release signing configuration and step-by-step Google Play publishing guide
- [x] **Ubuntu / Debian Linux Packages (`.deb` & Portable AppDir)**:
  - [x] Pure C# Debian binary compiler (generates compliant `.deb` packages on Windows with zero external tools, no Docker/WSL required)
  - [x] Debian package control files, desktop launcher integration (`.desktop` XDG), and scalable icon registration
  - [x] Dual deliverables: installable Debian package (`sudo dpkg -i app.deb`) and portable Linux AppDir (`./run.sh`)
  - [x] Native WebKitGTK Photino runner integration
  - [x] XDG MIME scheme handler registration (`x-scheme-handler/<scheme>;`)

---

### 3. Custom Deep-Linking (`myapp://`) URL Protocol Engine
- [x] **Security Hardening & RFC 3986 Compliance**:
  - [x] Strict protocol scheme validation (`^[a-z][a-z0-9+.-]{1,31}$`)
  - [x] Reserved system protocol blacklist (`http`, `https`, `file`, `javascript`, `data`, `blob`, `chrome`, `edge`, `mailto`, etc.)
  - [x] Argument injection immunity: strictly quoted executable invocations (`"App.exe" "%1"`)
  - [x] Payload sanitization (strips control characters `\r`, `\n`, `\0`, `\t` and enforces 4,096-char safety limit)
- [x] **Single-Instance IPC & Window Restoration**:
  - [x] Asynchronous Named Pipe IPC server (`WebToApp_IPC_<AppName>`)
  - [x] Seamless parameter forwarding from secondary instances with zero duplicate windows or error popups
  - [x] Automatic window focus and restoration (`Win32 ShowWindow(SW_RESTORE)` & `SetForegroundWindow`)
  - [x] Cold-start launch URL preservation and warm-start live event forwarding
- [x] **Frontend JavaScript Bridge**:
  - [x] Injected bridge with `window.desktopApp.onDeepLink(callback)`
  - [x] Synchronous `window.desktopApp.getLaunchUrl()` for startup parameters
  - [x] Standard `desktopapp:deeplink` DOM custom event on `window`
- [x] **Multi-Platform Registration**:
  - [x] Windows HKCU Registry auto-registration for portable executables without UAC prompts
  - [x] Inno Setup installer `[Registry]` keys and `ChangesAssociations=yes`
  - [x] Linux `.desktop` XDG `Exec` `%u` parameter and MIME type association
  - [x] MSIX `AppxManifest.xml` protocol extension declaration

---

### 4. Embedded SQLite Database Engine & Management
- [x] **Client-Side Database Capabilities**:
  - [x] Embedded SQLite engine packaged directly with the application
  - [x] Bidirectional JavaScript bridge: `window.desktopApp.db.query(sql, params)`, `execute(sql, params)`, and transaction support
  - [x] Persistent database storage in isolated application data directory
- [x] **Studio Database Designer (Tab 5)**:
  - [x] Interactive SQL schema editor with syntax highlighting and template presets
  - [x] Direct Database (`.sql` / `.ddl` / `.txt`) file importer via system file dialog
  - [x] Drag-and-drop `.sql` file importing directly onto the editor with visual feedback
  - [x] Real-time schema metrics badge (file name, formatted KB size, line count, detected table count)
  - [x] 1-Click `.sql` schema exporter to save modified database DDL back to disk
  - [x] Configurable SQLite database file name and auto-initialization toggle

---

### 5. Application Branding & Customization
- [x] **Executable & Metadata Customization**:
  - [x] Executable name customization (`.exe`)
  - [x] Window title & Application display name
  - [x] Version, Company Name, Copyright, and Product Description metadata injection
- [x] **Icon Studio & Image Asset Pipeline**:
  - [x] Multi-resolution `.ico` generation (16x16, 24x24, 32x32, 48x48, 64x64, 128x128, 256x256) from source PNG
  - [x] Android multi-density mipmap pipeline (`mdpi` through `xxxhdpi`)
  - [x] MSIX tile assets (`StoreLogo`, `Square150x150`, `Square44x44`, `Wide310x150`, `SplashScreen`)
  - [x] Linux scalable desktop icon packaging
- [x] **Splash Screen & Visual Polish**:
  - [x] Custom borderless splash screen window with smooth alpha fade-out transition
  - [x] Custom User-Agent string override

---

### 6. Window & Display Management
- [x] **Dimensions & Constraints**:
  - [x] Sizing presets (FHD 1080p, HD 720p, Default 1280x800, Compact 1024x768)
  - [x] Custom pixel width/height and minimum width/height constraints
- [x] **Window States & Modes**:
  - [x] Resizable window toggle
  - [x] Start Maximized toggle (for packaged applications)
  - [x] Fullscreen / Kiosk mode toggle
  - [x] Auto-center on display
  - [x] Always-on-top toggle

---

### 7. Commercial Security & Sandbox Controls
- [x] **Hardened Web Runtime**:
  - [x] Disable Developer Tools (F12, Ctrl+Shift+I, Inspect Element shortcuts)
  - [x] Disable Right-Click Context Menu
  - [x] Disable Text Selection (native desktop software feel)
  - [x] Single-Instance Mutex lock (prevents accidental duplicate instances)
  - [x] External domain link routing (opens untrusted URLs in system default browser)
- [x] **Storage & Isolation**:
  - [x] Isolated sandbox profile directory in `%LocalAppData%`
  - [x] Independent cookies, cache, and storage per application
- [x] **Anti-Malware & Integrity Verification**:
  - [x] 70+ Antivirus engine verification clean on VirusTotal
  - [x] Documented heuristic false-positive explanations and guidance for .NET self-contained loaders

---

### 8. Modern Studio Builder Desktop GUI (`WebToExe.Studio`)
- [x] **Interface Design & Workflow**:
  - [x] Linear/Vercel-inspired dark theme UI
  - [x] **Maximized Window Startup by Default** on Windows and Linux with preserved 1340×880 restore bounds (v1.4.1)
  - [x] Interactive Welcome Hub on startup (New Project, Open Project, Recent Projects history)
  - [x] Real-time live window mockup preview with active security badges
  - [x] Tabbed workflow (Source, Branding, Window, Security & Deep-Linking, SQLite Database, Build & Export)
  - [x] Native Windows file and folder picker dialogs
  - [x] Multi-step progress drawer with build stages and detailed build log
  - [x] Post-build modal with 1-click "Open Folder" and "Test Run App"
  - [x] Project configuration management (`.wtp` save/load)
- [x] **Studio Enterprise Security Hardening & Anti-Reverse Engineering (v1.4.2)**:
  - [x] AES-256 encrypted Studio container (`studio.dat`) with in-memory streaming into `https://studio.local/` (zero plaintext HTML/CSS/JS in assembly or on disk)
  - [x] DevTools (`F12`, `Ctrl+Shift+I`) and context menus locked down in Release builds
  - [x] Shortcut interception: blocks `F12`, `Ctrl+Shift+I`, `Ctrl+Shift+J`, `Ctrl+Shift+C`, `Ctrl+U`, and `Ctrl+S`
  - [x] Remote debugging port neutralization (strips malicious `--remote-debugging-port` environment variables)
  - [x] Native Win32 `CheckRemoteDebuggerPresent` and managed anti-debugging defense
  - [x] ReadyToRun (R2R) native ahead-of-time machine code compilation with stripped PDBs and debug symbols

---

### 9. 1-Click Auto-Updater & Ecosystem
- [x] **Built-in Studio Auto-Updater**:
  - [x] Automatic update check against official GitHub release manifest (`version.json`)
  - [x] Cryptographic SHA-256 hash verification before archive extraction
  - [x] Update modal with release changelog and 1-click update deployment
  - [x] Manual "Check for Updates" trigger in header and About dialog
- [x] **Cross-Platform Studio Hosts**:
  - [x] Windows 10/11 Host (WinForms + WebView2)
  - [x] Linux Host (`WebToExe.Studio.Linux` with Photino.NET and WebKitGTK)
- [x] **Documentation & Marketing Assets**:
  - [x] Official Wiki and comprehensive user guides
  - [x] Official product website (`wildcatstudio.us`) with download cards, changelogs, and integrity verification tables
  - [x] CodeCanyon marketplace description and metadata

---

## :rocket: Quick Start

### 1. Download & Run
1. Go to the **[Latest Release](https://github.com/djacidfx/webtoapp-releases/releases/latest)**.
2. Download the distribution ZIP: `WebToApp-Studio-v1.4.2.zip`.
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

| Distribution Package | Target Platform | Security Status | VirusTotal Verification |
|---|---|:---:|:---:|
| **`WebToApp-Studio-v1.4.2.zip`**<br><sub>`a15bbb113218984f8d7c5432626c15dee65a38d707ebd5dc345666d5a84e494b`</sub> | Windows Standalone (Zero-Config Zip) | :white_check_mark: Clean | [Inspect 70+ Engines &rarr;](https://www.virustotal.com/gui/file/a15bbb113218984f8d7c5432626c15dee65a38d707ebd5dc345666d5a84e494b) |
| **`WebToApp-Studio-v1.4.2-Lightweight.zip`**<br><sub>`c9cc4e7f3db5fbb3065415c99471e0cfd007bac46d29d4180b0d027f17860537`</sub> | Windows Lightweight (Requires .NET 8) | :white_check_mark: Clean | [Inspect 70+ Engines &rarr;](https://www.virustotal.com/gui/file/c9cc4e7f3db5fbb3065415c99471e0cfd007bac46d29d4180b0d027f17860537) |
| **`WebToApp-Studio-Pro_1.4.2_amd64.deb`**<br><sub>`c5087894f269acc0a8573c3e4a8f2c4782c76592765809fe86a556cbd31a8cff`</sub> | Ubuntu / Debian (.deb) | :white_check_mark: Clean | [Inspect 70+ Engines &rarr;](https://www.virustotal.com/gui/file/c5087894f269acc0a8573c3e4a8f2c4782c76592765809fe86a556cbd31a8cff) |
| **`WebToApp-Studio-Pro-Linux-x64-v1.4.2-Portable.tar.gz`**<br><sub>`09ca291e9483911f14e25117f23b9ccb6e4d7fd234abdc2f47e33ffb28cf5993`</sub> | Linux x64 (.tar.gz) | :white_check_mark: Clean | [Inspect 70+ Engines &rarr;](https://www.virustotal.com/gui/file/09ca291e9483911f14e25117f23b9ccb6e4d7fd234abdc2f47e33ffb28cf5993) |

---

## :computer: System Requirements & Prerequisites

### Windows Host Environment (Studio Builder)
* **Operating System**: Windows 10 (Build 1809+) or Windows 11 (64-bit)
* **Web Engine**: Microsoft Edge WebView2 Evergreen Runtime (pre-installed on Windows 11 and all updated Windows 10 machines). If missing, install via the official [Microsoft Edge WebView2 Installer](https://go.microsoft.com/fwlink/p/?LinkId=2124703).
* **Architecture**: x64

#### Which Windows Download Should I Choose?
* **:sparkles: Standalone Edition (`WebToApp-Studio-v1.4.2.zip`) [Recommended]**:  
  Completely self-contained with embedded .NET runtime. **Zero installation or runtime dependencies required** — simply extract the zip archive and double-click `WebToExe.Studio.exe` to run immediately on any Windows 10/11 PC without ever seeing a missing .NET runtime prompt!
* **:feather: Lightweight Edition (`WebToApp-Studio-v1.4.2-Lightweight.zip`)**:  
  Ultra-compact download (~33.8 MB). Requires the free [Microsoft .NET Desktop Runtime 8.0 (x64)](https://dotnet.microsoft.com/download/dotnet/8.0/runtime) (Direct installer link: [windowsdesktop-runtime-win-x64.exe](https://aka.ms/dotnet/8.0/windowsdesktop-runtime-win-x64.exe)).

> [!TIP]
> **Saw the "You must install or update .NET to run this application" popup?**  
> If you run the **Lightweight edition** on a computer that does not have .NET 8 Desktop Runtime installed yet, Windows will prompt you to install it:
> 1. Click **"Download it now"** in the Windows dialog (or download directly from [Microsoft .NET 8.0 Desktop Runtime x64](https://aka.ms/dotnet/8.0/windowsdesktop-runtime-win-x64.exe)), run the official Microsoft installer, and then launch `WebToExe.Studio.exe`.
> 2. **Alternatively**, download the **Standalone Edition** (`WebToApp-Studio-v1.4.2.zip`), which has zero prerequisites and works out of the box!

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
* :star: **Star on GitHub**: [github.com/djacidfx/webtoapp-releases](https://github.com/djacidfx/webtoapp-releases)

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
