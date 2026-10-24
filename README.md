# Bluebird RadioDock

![Kentucky Bluebird](Kentucky_Bluebird.png)

**Bluebird RadioDock** is a portable Windows utility for managing, customizing, and maintaining **EdgeTX radios** without trying to replace EdgeTX Companion.

RadioDock brings model images, EdgeTX add-ons, themes, sounds, migration tools, and other useful radio-management features together in one application.

Current release: **v1.4.36**

[Releases](https://github.com/Redvsbluecom/Bluebird_Radio_Dock/releases)

---

## What RadioDock Does

### ImageDock

Search for aircraft model images and prepare them for your radio.

Supported online providers include:

- **SkyRaccoon**
- **AIR-RC**

RadioDock handles radio-specific image conversion, naming, resizing, and saving.

ImageDock has been heavily hardened for real-world provider behavior, including:

- provider switching;
- slow-loading pages;
- first-search recovery;
- empty-result handling;
- failed-page recovery;
- automatic reload attempts;
- Windows proxy support;
- diagnostic logging when something goes wrong.

RadioDock can create:

`Bluebird_RadioDock_Data/ImageDock_Diagnostic.log`

when an ImageDock provider fails, making troubleshooting considerably easier.

---

## EdgeTX Add-ons

Browse the official EdgeTX Lua/add-on catalog directly inside RadioDock.

RadioDock also includes selected **RadioDock Reviewed** community projects that are not yet part of the official EdgeTX catalog.

Examples include:

- AeroGrid
- FPVDash
- EdgeDeck
- UltiDash
- FlightDash
- WingLabs EdgeTX Widgets
- RBCT
- Whoopsie Daisy
- SoarF5J
- Rotorflight RFSuite

When a reviewed project later becomes official, RadioDock automatically prefers the official EdgeTX listing instead of showing duplicates.

### Safe Installation

RadioDock does **not** blindly install arbitrary GitHub repositories.

Automatic installation is offered only when RadioDock can verify the package structure and destination with enough confidence to safely modify the radio SD card.

Unknown or ambiguous packages remain manual.

---

## AeroGrid Support

RadioDock includes dedicated support for installing and updating AeroGrid.

It can:

- download the current stable release;
- install the widget into `/WIDGETS/AeroGrid/`;
- replace the existing widget during an update;
- preserve user layouts and configuration stored under `/AEROGRID/`;
- protect existing files with transactional backup and rollback.

---

## ThemeDock

ThemeDock lets you browse, preview, build, and install EdgeTX color themes.

![ThemeDock Preview](ThemeDock_preview.png)

Features include:

- official EdgeTX theme browsing;
- theme previews;
- local-photo theme creation;
- background crop and positioning;
- brightness adjustment;
- palette editing;
- radio-display previews;
- reusable `.btheme` projects;
- theme ZIP export;
- direct installation to an EdgeTX SD card.

### Startup Media Protection

Normal theme installation will not unexpectedly replace:

- `/IMAGES/splash.png`
- startup `hello.wav`
- startup `tada.wav`

If a package contains startup media, RadioDock requires an explicit choice before replacing it.

---

## Sounds & Voice Packs

RadioDock provides access to EdgeTX-compatible sound and voice resources including:

- GLaDOS Voice Pack
- Joshua Bardwell Voice Pack
- Amber legacy voice resources
- EMAX Satomi Taranis Voice Pack
- Vox-Pack Custom Voice Creator

Current EdgeTX voice packs can be installed where RadioDock can safely verify their layout.

Legacy or external packages remain available for manual review.

---

## Radio-Aware Model Images

RadioDock understands that different EdgeTX radios require different image formats and resolutions.

Supported workflows include:

- color-radio PNG images;
- monochrome radio BMP images;
- automatic resizing;
- radio-aware output;
- human-readable filename handling;
- safe conversion from downloaded source images.

The operator always chooses the radio and destination.

RadioDock does **not** automatically guess which removable drive is your transmitter.

---

## Model Migration Tools

RadioDock includes utilities for moving or converting model resources between supported RadioMaster/EdgeTX radio generations.

These tools are intended to simplify migration while keeping the operator in control of the source and destination.

---

## Portable by Design

RadioDock does not require a traditional Windows installation.

The standalone EXE can be placed wherever you want.

Persistent RadioDock data is stored beside the application in:

`Bluebird_RadioDock_Data`

This keeps settings, update information, and other RadioDock data portable with the program.

---

## Built-In Update Notifications

Starting with **v1.4.36**, RadioDock can check the official GitHub Releases page for a newer stable version.

Features include:

- background update checks;
- manual **Check for updates**;
- visible update notification when a newer version is available;
- release-note preview;
- **Remind me later**;
- **Dismiss this version**.

RadioDock does **not** silently install updates or replace its own executable.

The user remains in control of every RadioDock update.

---

## Windows Networking

RadioDock uses the Windows certificate store for normal HTTPS downloads.

This improves compatibility with:

- GitHub;
- official EdgeTX catalogs;
- themes;
- add-on packages;
- release information;
- publisher resources.

Certificate verification remains enabled.

RadioDock does not silently bypass invalid certificates.

---

## Supported Environment

RadioDock is designed primarily for:

- **Windows 10 / Windows 11**
- **EdgeTX radios**
- RadioMaster color and monochrome radios
- EdgeTX-compatible radios from other manufacturers where the required SD-card structure and formats are supported

Development and testing are currently centered around modern EdgeTX releases and RadioMaster hardware, including TX16S-class radios.

---

## Download

Get the newest standalone release here:

**https://github.com/Redvsbluecom/Bluebird_Radio_Dock/releases**

For normal use, download the latest standalone Windows executable from the Releases page.

Developers can also download the source package included with each release.

---

## Building From Source

The source package includes the Windows build system.

Requirements:

- Python 3.10 or newer
- Windows 10 or 11
- Internet access during the initial build

The current development environment uses **Python 3.13 64-bit**.

Extract the source package and run:

`BUILD_FINAL_STANDALONE.bat`

The build process creates a private temporary Python environment, installs the required dependencies, runs RadioDock's regression checks, and produces the standalone Windows executable.

---

## Safety First

RadioDock is intentionally conservative when modifying an EdgeTX SD card.

Its general rule is:

**If RadioDock cannot confidently determine that an automatic operation is safe, it does not perform it automatically.**

Depending on the package, RadioDock may:

- install automatically;
- ask for confirmation;
- provide a manual download;
- disable automatic installation entirely.

This is intentional.

Protecting an existing radio configuration is more important than pretending every package can be installed automatically.

---

## RadioDock Is Not EdgeTX Companion

Bluebird RadioDock is designed to complement the existing EdgeTX ecosystem.

It focuses on convenient tasks such as:

- model images;
- add-ons;
- themes;
- sounds;
- package management;
- migration;
- radio resources.

It is **not intended to replace EdgeTX Companion**.

---

## Project Philosophy

RadioDock is built around a few simple ideas:

- keep the operator in control;
- make common EdgeTX tasks easier;
- use official publisher sources whenever possible;
- protect existing radio files;
- fail safely when a package is ambiguous;
- keep the program portable;
- improve compatibility without hiding what the application is doing.

---

## Feedback & Issues

If RadioDock behaves unexpectedly, please include as much information as possible when reporting the problem.

For ImageDock problems, include:

`Bluebird_RadioDock_Data/ImageDock_Diagnostic.log`

when available.

GitHub:

**https://github.com/Redvsbluecom/Bluebird_Radio_Dock**

---

## License

See the repository license and individual third-party project licenses for applicable terms.

Bluebird RadioDock does not claim ownership of EdgeTX, publisher add-ons, themes, sounds, aircraft images, or third-party projects listed through the application.
