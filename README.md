<img width="1254" height="170" alt="ThemeDock_preview" src="https://github.com/user-attachments/assets/e73dd1da-2ad8-4942-a750-373b135f573c" />
<img width="1386" height="1326" alt="Kentucky_Bluebird" src="https://github.com/user-attachments/assets/c9fd3b46-600b-40fa-92e5-7465c55eb0ed" />
[README.md](https://github.com/user-attachments/files/33288373/README.md)
# Bluebird RadioDock

<p align="center">
  <img src="Kentucky_Bluebird.png" width="180" alt="Kentucky Bluebird">
</p>

<p align="center">
  <strong>A portable Windows utility for managing common EdgeTX radio tasks.</strong>
</p>

<p align="center">
  Model Images • Lua Add-ons • ThemeDock • Sound Packs • Model Migration
</p>

---

## About Bluebird RadioDock

Bluebird RadioDock is a Windows utility built to simplify some of the repetitive jobs involved with managing EdgeTX radios and SD cards.

It is **not intended to replace EdgeTX Companion**.

Instead, RadioDock focuses on tasks that often require manually searching websites, resizing images, renaming files, navigating SD-card folders, downloading Lua packages, building themes, or converting model files.

The operator remains in control of the radio and chooses the SD-card location manually.

---

## Model Images

Search supported model-image providers directly from RadioDock and download aircraft images for your EdgeTX radio.

Features include:

- Search supported model-image providers
- Preview images before saving
- Radio/display-aware image sizing
- Automatic image conversion when required
- EdgeTX-compatible filenames
- 9-character model-image filename handling
- Direct download to a selected radio folder
- Preview reload support
- Provider switching
- Portable image workflow

RadioDock is designed to eliminate much of the manual work normally involved in finding, resizing, converting, renaming, and copying model images.

---

## EdgeTX Add-ons & Lua Tools

Browse EdgeTX Lua scripts, widgets, utilities, and add-ons from inside RadioDock.

Features include:

- Add-on browsing
- Publisher screenshots
- Screenshot galleries
- Publisher website access
- Manual package downloads
- EdgeTX SD-root selection
- Conservative automatic installation where supported
- Package layout validation
- Transactional file replacement
- Rollback protection during supported installs

RadioDock intentionally uses a **fail-closed** approach.

If an add-on has an unclear folder structure, unsupported dependency, radio-specific variant, or ambiguous installation requirement, RadioDock will leave that package as a manual installation instead of guessing.

---

## Add-on Preview Galleries

Publisher screenshots are shown directly inside the Add-ons tab.

Multi-image galleries include navigation controls and image counters such as:

```text
2 / 6
```

Single-image previews do not display an unnecessary `1 / 1` counter.

The preview system also adjusts correctly when RadioDock is maximized or running fullscreen.

---

## ThemeDock

Create custom themes for EdgeTX color-screen radios using your own images and color selections.

<p align="center">
  <img src="ThemeDock_preview.png" width="850" alt="ThemeDock Preview">
</p>

ThemeDock includes:

- Custom background photos
- Crop and positioning controls
- Zoom controls
- Brightness adjustment
- Theme color editing
- Radio/display previews
- Editable `.btheme` project files
- EdgeTX theme export
- Support for multiple color-screen layouts

ThemeDock is intended to make creating personalized EdgeTX themes easier without manually assembling all of the theme assets yourself.

---

## Sound Packs

RadioDock includes tools for working with supported EdgeTX sound packs.

The operator selects the radio SD-card root, allowing RadioDock to remain portable and avoiding assumptions about Windows drive letters.

---

## Model Migration

RadioDock includes tools for converting supported EdgeTX model files between radio generations.

This functionality originally grew from migration work involving radios such as:

- RadioMaster TX16S MK2
- RadioMaster TX16S MK3
- HelloRadioSky V16

The migration tools are focused specifically on compatible model-file changes and are not intended to replace full radio-management software.

---

## Portable by Design

Bluebird RadioDock is designed to remain portable.

Where practical, application-owned files and settings stay beside the application instead of being scattered throughout Windows.

The finished standalone EXE does **not** require Python to be installed on the end user's computer.

---

## Download

The easiest way to get RadioDock is through the GitHub **Releases** page.

Download the latest release package and follow the instructions included with that release.

---

## Building the Standalone EXE

The source/build kit includes:

```text
BUILD_FINAL_STANDALONE.bat
```

To build RadioDock:

1. Download the latest build kit.
2. Extract the ZIP to a normal Windows folder.
3. Run:

```text
BUILD_FINAL_STANDALONE.bat
```

4. The builder creates a temporary private Python environment.
5. Required dependencies are installed automatically.
6. Regression tests are run before the application is packaged.
7. If all required tests pass, the standalone EXE is created in:

```text
release
```

The first build requires an internet connection.

End users only need the finished EXE.

---

## Using an EdgeTX SD Card

RadioDock does not assume a specific Windows drive letter.

Connect the radio or SD card to your computer and choose the correct **EdgeTX SD root** when requested.

A typical EdgeTX SD card may contain folders such as:

```text
MODELS
RADIO
SCRIPTS
WIDGETS
THEMES
SOUNDS
IMAGES
```

The exact folder layout depends on the radio, EdgeTX version, and installed packages.

---

## Automatic Lua Installation

Automatic Lua/add-on installation is intentionally conservative.

RadioDock only offers automatic installation when the package layout and destination can be determined with enough confidence.

Automatic installation may be unavailable for packages with:

- Unknown folder structures
- Radio-specific variants
- Ambiguous publisher instructions
- Unsupported dependencies
- Unverified package layouts
- Hardware-specific requirements

When RadioDock cannot prove that an automatic installation is safe, manual download remains available.

This behavior is intentional.

---

## Package Health

Lua / Package Health functionality remains experimental.

EdgeTX Lua packages do not all use a single universal installation or version-tracking system, especially older manually installed scripts.

Package Health should not yet be treated as a universal update checker.

---

## Current Version

### Bluebird RadioDock v1.4.16

Recent improvements include:

- Cleaner Model Images interface
- Removed unnecessary Cancel Downloads control
- Improved Model Images preview spacing
- Improved Reload Preview positioning
- Better maximized/fullscreen Add-ons previews
- Multi-image gallery counters
- Single-image counter cleanup
- Publisher-page control moved beside SD-root selection
- Improved ImageDock search/preview timing
- Hardened Windows GUI regression testing

See the **Releases** section for detailed version history.

---

## Project Philosophy

RadioDock is built around a few simple ideas:

- Keep the operator in control
- Do not guess about radio files
- Prefer manual behavior when automatic behavior is uncertain
- Keep the application portable
- Avoid modifying unrelated SD-card files
- Make repetitive EdgeTX tasks easier
- Preserve working functionality while the project evolves

---

## Backup Your Radio

Before making significant changes to an EdgeTX SD card, keep a backup.

RadioDock includes safety checks for supported operations, but a current backup of your SD card is always recommended.

---

## Disclaimer

Bluebird RadioDock is an independent community project.

It is not affiliated with or endorsed by EdgeTX, RadioMaster, HelloRadioSky, model-image providers, Lua developers, or other referenced manufacturers and projects.

EdgeTX, manufacturer names, logos, software, artwork, add-ons, and other referenced properties remain the property of their respective owners.

---

<p align="center">
  <strong>Bluebird RadioDock</strong><br>
  Built for the EdgeTX community.
</p>
