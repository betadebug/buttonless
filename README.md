# Buttonless – Volume Control

> **Control without buttons.**  
> A modern Android app that makes volume control easier on phones with broken or difficult-to-use physical volume buttons.

Buttonless – Volume Control provides an alternative way to access volume controls through Android's Quick Settings panel. Instead of relying entirely on physical buttons, users can access volume controls directly from the notification shade.

Built with Kotlin and Jetpack Compose, the app combines a modern interface with a practical purpose: making everyday audio controls more accessible and convenient.

## Badges

![Platform](https://img.shields.io/badge/platform-Android-3DDC84?logo=android&logoColor=white)
![Language](https://img.shields.io/badge/language-Kotlin-7F52FF?logo=kotlin&logoColor=white)
![UI](https://img.shields.io/badge/UI-Jetpack%20Compose-4285F4?logo=jetpackcompose&logoColor=white)

## Table of Contents

- [Why](#why)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Demo](#demo--live-preview)
- [Install and Run](#install-and-run)
- [Usage](#usage)
- [Configuration](#configuration)
- [Customize](#customize)
- [Contributing](#contributing)
- [Testing](#testing)
- [Roadmap](#roadmap)
- [Changelog](#changelog)
- [License](#license)
- [Contact](#contact)

## Why

**Your volume buttons should not be the only way to control your volume.**

Physical volume buttons can become unreliable or stop working entirely. Replacing them may be inconvenient, but controlling audio should remain straightforward.

Buttonless offers an alternative by bringing volume-control access to Android's Quick Settings panel. It is designed for people dealing with damaged buttons as well as anyone who prefers convenient, software-based access to volume controls.

The goal is simple: provide a practical solution with a clean interface and minimal friction.

## Features

- **Quick Settings integration:** Access volume controls from Android's notification shade.
- **Alternative to physical buttons:** Reduce reliance on hardware volume keys.
- **Modern interface:** A clean, minimalist design with a vibrant blue gradient.
- **Jetpack Compose UI:** A modern declarative approach to Android interface development.
- **System volume controls:** Access the supported Android volume-control interface.
- **Convenient access:** Launch the relevant control from a Quick Settings tile.
- **Scalable visual assets:** Use vector-based graphics for crisp rendering at different sizes.
- **Focused experience:** Keep the primary purpose clear without unnecessary interface clutter.

Feature availability depends on the installed version, Android version, and device behavior. Buttonless does not replace Android's audio system or guarantee identical behavior across every device.

## Tech Stack

| Technology | Purpose |
|---|---|
| Kotlin | Application development |
| Jetpack Compose | Declarative UI |
| Android SDK | Platform integration |
| Android Studio | Development and debugging |
| Gradle | Build automation |
| Git and GitHub | Version control and collaboration |

## Demo / Live Preview

Buttonless is an Android application, so the primary demo is the app running on a compatible device or emulator.

To preview the experience:

1. Open the application.
2. Add its Quick Settings tile if prompted or required by the installed version.
3. Open the notification shade.
4. Tap the Buttonless tile and explore the available volume controls.

Screenshots and a demonstration video can be added to this section as the project develops.

## Install and Run

### Prerequisites

Before building the project, install:

- Android Studio
- A compatible Android SDK
- Git
- A physical Android device or Android emulator

### 1. Clone the repository

```bash
git clone <YOUR_REPOSITORY_URL>
cd <YOUR_REPOSITORY_DIRECTORY>
```

Replace the two values with your actual GitHub repository URL and directory name.

### 2. Open the project

Open the cloned project in Android Studio and allow Gradle synchronization to finish. Resolve any SDK or dependency requirements reported by the IDE.

### 3. Build the debug APK

On macOS or Linux:

```bash
./gradlew assembleDebug
```

On Windows:

```powershell
.\gradlew.bat assembleDebug
```

The standard Gradle output location for the debug APK is:

```text
app/build/outputs/apk/debug/app-debug.apk
```

This path assumes the application module is named `app`.

### 4. Install the application

Connect an Android device with USB debugging enabled, or start an emulator.

```bash
adb install -r app/build/outputs/apk/debug/app-debug.apk
```

Alternatively, run the app directly from Android Studio.

## Usage

1. Install and launch Buttonless.
2. Follow any in-app instructions for enabling its Quick Settings tile.
3. Open the Android notification shade and expand Quick Settings.
4. Enter Quick Settings edit mode if necessary.
5. Add the Buttonless tile to your active tiles.
6. Tap the tile to open the volume-control interface provided by the app.

The exact tile setup and resulting interface can vary by Android version and device manufacturer.

If a tile does not appear or behave as expected, verify that the installed build supports your Android version and that the tile has been added to the active Quick Settings panel.

## Configuration

Buttonless is designed to work through Android's platform APIs rather than requiring a web service.

Configuration is managed through the Android project, including its Gradle files, application resources, and manifest.

Key configuration areas include:

- **Application ID:** The unique identifier defined in the Android app module.
- **Minimum SDK:** The minimum Android version supported by the project.
- **Target SDK:** The Android API level targeted by the application.
- **Build types:** Debug and release build configurations.
- **Quick Settings integration:** The service and metadata used to register the application's tile.

Refer to the project's Gradle configuration and Android manifest for the actual values. No environment variables or external API credentials are assumed to be required.

## Customize

Buttonless uses a modern visual style that can be adapted while preserving its core purpose.

### Theme and branding

Customize the Compose theme and Android resources to change the application's appearance.

Example brand colors:

```kotlin
val PrimaryBlue = Color(0xFF0787F9)
val PrimaryBlueDark = Color(0xFF1557F5)
val SurfaceLight = Color(0xFFF8FAFC)
```

These are suggested design values, not a guarantee of the exact colors currently defined in the project.

### Extension points

Potential improvements include:

- Additional theme options.
- Improved accessibility labels and touch targets.
- More explanatory onboarding.
- Device compatibility improvements.
- Better handling of Quick Settings tile states.

Keep the interface focused, and test visual changes on different screen sizes and Android versions.

## Contributing

Contributions are welcome! Bug fixes, accessibility improvements, documentation updates, and focused UI enhancements can all make Buttonless more useful.

### Contribution workflow

1. Check the existing issues before starting.
2. Open an issue to discuss significant changes.
3. Fork the repository.
4. Create a feature branch.
5. Implement and test your changes.
6. Submit a pull request describing the problem, solution, and verification steps.

Example workflow:

```bash
git checkout -b feature/your-improvement
git add .
git commit -m "feat: improve volume control experience"
git push origin feature/your-improvement
```

When submitting UI changes, include screenshots where possible. For device-specific bugs, provide the Android version, device model, reproduction steps, and expected behavior.

Please keep contributions focused and follow the existing code style. Be respectful and constructive when reviewing others' work.

## Testing

Testing should cover both application behavior and Android platform integration.

Run the project's configured unit tests:

```bash
./gradlew test
```

Build the debug application:

```bash
./gradlew assembleDebug
```

On Windows, use `.\gradlew.bat` instead of `./gradlew`.

If the project includes connected Android instrumentation tests, run:

```bash
./gradlew connectedAndroidTest
```

Verify the following before submitting changes:

- The project builds successfully.
- The application launches without crashing.
- The Quick Settings tile can be added and activated.
- Volume controls behave as expected on the tested device.
- The interface remains readable at different screen sizes.
- No unnecessary permissions or sensitive credentials are introduced.

Instrumentation tests require a configured Android test environment and a connected device or emulator.

## Roadmap

Potential future improvements include:

- [ ] Add application screenshots and a short demonstration video.
- [ ] Improve onboarding and Quick Settings setup guidance.
- [ ] Expand device and Android-version compatibility testing.
- [ ] Strengthen accessibility and usability.
- [ ] Add automated checks for builds and tests.
- [ ] Publish versioned releases with installation instructions.
- [ ] Evaluate additional volume-control shortcuts based on user feedback.

Roadmap items are proposals rather than guarantees and may change as the project evolves.

## Changelog

### Unreleased

- Develop the Buttonless volume-control experience.
- Provide an alternative entry point to volume controls through Quick Settings.
- Establish the project's documentation and contribution workflow.

Update this section with verified changes whenever a new version is released. Use Git tags and GitHub Releases to distinguish published versions from development builds.

## License

Buttonless – Volume Control is licensed under the **MIT License**.

You are free to use, copy, modify, merge, publish, distribute, sublicense, and sell copies of the software, subject to the terms of the MIT License.

The software is provided "as is", without warranty of any kind, express or implied.

See the [`LICENSE`](LICENSE) file for the complete license terms.

## Contact

For bug reports, feature requests, or project-related questions, use the repository's GitHub issue tracker.

- **Project:** Buttonless – Volume Control
- **Repository:** Your GitHub repository
- **Bug reports:** Open an issue in the repository
- **Contributions:** Submit a pull request

When reporting a bug, include your Android version, device model, steps to reproduce the issue, and any relevant screenshots or logs.

---

**Buttonless — Control without buttons.**

If Buttonless helps you access volume controls when your physical buttons are unreliable, consider starring the repository and contributing improvements that make the experience better for everyone.
