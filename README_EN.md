<div align="center">

# RemTV

### A modern home screen for Android TV and Google TV

**tvOS-inspired design · Liquid Glass · Deep customization · Remote-first**

[Features](#features) · [Compatibility](#compatibility) · [Installation](#installation) · [Build](#build-from-source) · [Security](#security)

[Русский](README.md)

</div>

---

RemTV is a customizable launcher for Android TVs and streaming devices. It combines two home-screen styles — **Night Scenes** and **Classic** — with a personalized dock, useful system tools, and navigation designed for a standard TV remote.

The project is written in Java and uses the Android SDK. Build scripts are provided for Windows and macOS/Linux; Gradle is not required.

## Features

### Home screen & personalization
- **Night Scenes** — atmospheric backgrounds, clock, date, greeting, and weather.
- **Classic** — app grid and a centered tvOS-inspired dock.
- **Liquid Glass Dock** — configurable size and app order, plus an Other Apps folder.
- Custom wallpapers, multiple wallpaper slots, and folder-based shuffle.
- App renaming and icon editing, hidden apps, and user profiles.

### TV controls
- Quick Settings panel over the home screen and other apps.
- Recent Apps switcher and RAM usage display.
- **Button Mapper** for single, double, and triple remote-button actions.
- Custom button actions, including Android KeyEvent dispatch.
- Sleep options, Ambient Mode, and a built-in lock screen.

### Content & everyday tools
- **Continue Watching**, based on information exposed by media apps and Android TV system services.
- App and content search, recommendations, and a news feed.
- Multi-day weather forecast.
- Multiple user profiles.

### Utilities & maintenance
- First-run setup and permission assistant.
- Secure ADB Mode and Persistent ADB Mode.
- **CleanYourTV (Beta)** — TV profiles, stock-launcher controls, and system-app management.
- In-app update checks and APK installation.
- Settings backup and restore.

### Languages
The interface includes Russian, English, Turkish, Swedish, Hindi, Spanish, French, German, Italian, Portuguese, Arabic, Japanese, Chinese, and Korean.

## Compatibility

- **Android TV / Google TV:** Android 7.0 (API 24) and later.
- Designed for TV remote navigation (DPAD).
- Feature availability depends on the device manufacturer, Android version, and available system services.
- Some advanced features require special permissions or ADB setup.

## Installation

When a release is published, download the APK from **[Releases](../../releases)**.

1. Download the APK from Releases.
2. Install it on your Android TV or Google TV device.
3. Open RemTV and complete the first-run setup.
4. Follow the on-screen instructions to set RemTV as your home app.

If no release is available yet, build the APK from source using the instructions below.

## Build from source

### Requirements
- JDK 17 or newer.
- Android SDK.
- `platforms;android-34`.
- `build-tools;34.0.0`.

Set `JAVA_HOME` and `ANDROID_HOME` (or `ANDROID_SDK_ROOT`) if the tools are not detected automatically.

**Windows (PowerShell):**
```powershell
powershell -ExecutionPolicy Bypass -File .\build.ps1
```

**macOS / Linux:**
```bash
chmod +x ./build.sh
./build.sh
```

The resulting APK is written to `build/RemTV.apk`.

Install with ADB:
```bash
adb connect <TV-IP-address>:5555
adb install -r build/RemTV.apk
```

Network ADB availability depends on the device and its developer settings. Do not leave ADB enabled unless needed.

## Security

- Grant only the permissions required by the features you use.
- Review the package list carefully before using CleanYourTV: disabling system components may affect TV functionality.
- Secure ADB Mode is designed to grant required permissions during setup and then turn off network ADB.
- **Never commit keystores, passwords, tokens, or other secrets.** Keep release-signing keys outside the public repository.
- Do not use ADB over untrusted networks.

## Project layout

```text
.
├── assets/          App icons, fonts, and resources
├── res/             Android resources and XML configuration
├── src/             Java source code
├── AndroidManifest.xml
├── build.ps1        Windows build script
└── build.sh         macOS / Linux build script
```

## Acknowledgements

The project uses ideas and selected components from [Hume Launcher](https://github.com/petrobot-admin/hume-launcher), [Couch TV](https://github.com/Seagey/couch-tv), [CleanYourTV](https://github.com/Gathin23/cleanyourtv), [Inter](https://github.com/rsms/inter), and [Project Nayuki QR Code Generator](https://github.com/nayuki/QR-Code-generator).

Weather data is also provided by Open-Meteo, MET Norway, and wttr.in. Refer to the project notices for third-party component and license details.

---

<div align="center">

**RemTV — make your TV feel like home.**

</div>