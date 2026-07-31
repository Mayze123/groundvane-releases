# Groundvane

A native macOS ground station for ArduPilot aircraft.

This repository carries the downloads and the update feed, and nothing else. The source is private.

## Download

**[Download the latest release](https://github.com/Mayze123/groundvane-releases/releases/latest)**

Every version is listed on the [releases page](https://github.com/Mayze123/groundvane-releases/releases), tagged `v<version>-<build>`, with the notarized `.zip` attached.

### Requirements

- **macOS 14 (Sonoma) or later**
- **Apple Silicon** — M1 or newer. Intel Macs are not supported and the app will not open on one.

### Installing

1. Download and unzip the `.zip`.
2. Drag `Groundvane.app` into your Applications folder.
3. Open it.

The app is signed with an Apple Developer ID and notarized by Apple, so it opens normally the first time. There is no "unidentified developer" warning to click past and no need to right-click → Open.

If macOS does refuse to open it, that is a fault in the release rather than something to work around — please report it instead of disabling security settings.

## Updates

Groundvane checks for updates once a day and can also check on request from its menu.

- **It never installs an update on its own.** Installing relaunches the application, and it is sometimes the only thing holding a link to an aircraft in the air. Updating is always a decision you make.
- **It does not check in the background while a vehicle is connected**, so a dialog cannot appear mid-flight. A check you ask for from the menu always runs.
- **Update checks send no profiling information** about your machine.

Updates are verified against a key built into the application before anything is installed, so a tampered download is rejected rather than run.

The feed itself is `appcast.xml` in this repository, served at
`https://mayze123.github.io/groundvane-releases/appcast.xml`

## Publishing

Archives are uploaded to a Release **before** `appcast.xml` is pushed. A feed that names a file which is not yet uploaded advertises a download that 404s to everyone who checks in the interval.
