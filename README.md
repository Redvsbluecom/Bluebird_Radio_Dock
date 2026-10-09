# Bluebird RadioDock

### A portable Windows workbench for EdgeTX radios

Bluebird RadioDock brings Lua add-on downloads, model images, radio migration, and custom theme creation into one application.

Built by **Kentucky Bluebird** for the RC community.

## Features

### 🎨 ThemeDock — New in v1.3.0

Create custom EdgeTX color themes with your own photos and colors.

- Start with the original EdgeTX color palette.
- Adjust background crop, zoom, brightness, and image fit.
- Preview sample home screens, menus, and controls.
- Save editable projects with the original photo included.
- Export a theme ZIP ready to copy onto your radio’s SD card.
- Include all five supported color-screen resolutions in one package.
- Preview and export monochrome artwork.

### 🧩 Lua Tools & Add-ons

Browse and download Lua scripts, widgets, themes, and other radio add-ons.

- View available previews.
- Select multiple downloads.
- Choose your destination folder.
- Check for duplicate downloads.
- Review package installation guidance.

### 🖼️ Model Images

Find and download model images with previews and radio-aware formatting.

- Color output: **192 × 114 PNG**.
- Supported X9D-family monochrome output: **64 × 32, 4-bit indexed BMP**.
- Human-readable filenames limited to **9 characters**.
- Choose where images are saved, including your radio’s SD card.

### 🔄 MK2 ↔ MK3 Migration

Convert supported model module settings between MK2 and MK3 configurations using the integrated migration tool.

### ⚠️ Lua Health — Currently Broken

The **Lua Health** tab is included in this build, but it is **not working correctly**. Do not rely on its script detection, update checks, or update actions.

It remains visible in the application, but should be treated as an unfinished feature.

## Getting Started

Download the package from this repository’s **Releases** page.

### Standalone EXE

If the release includes a standalone executable, download and run it. End users do not need Python.

### Windows Build Kit

1. Download and extract the build-kit ZIP.
2. Install **Python 3.10 or newer**.
3. Run `BUILD_FINAL_STANDALONE.bat`.
4. Find the finished executable in the `release` folder.

The first build requires internet access to install dependencies.

## Creating a Theme

1. Open **ThemeDock**.
2. Enter your theme name and author.
3. Add a photo and choose a display resolution.
4. Adjust the photo and palette.
5. Check the previews for each display size you want to support.
6. Export your theme ZIP.
7. Copy its **THEMES** folder to your radio’s SD-card root.
8. Select the new theme in EdgeTX.

Save a `.btheme` project if you want to edit the design again later.

## Theme Display Support

| Display type | Resolution |
|---|---|
| Color, landscape | 320 × 240 |
| Color, portrait | 320 × 480 |
| Color, landscape | 480 × 272 |
| Color, landscape | 480 × 320 |
| Color, landscape | 800 × 480 |
| Monochrome artwork | 128 × 64 |
| Monochrome artwork | 212 × 64 |

Color themes use the modern **EdgeTX 2.6+** theme format. Optional quick-menu color overrides require **EdgeTX 2.12+**.

Monochrome radios do not support selectable color themes. ThemeDock exports monochrome source artwork; startup-image installation depends on the radio and firmware.

## Current Release & Known Issues

**v1.3.0 — ThemeDock Preview Release**

- **Lua Health is included but currently broken.**
- ThemeDock previews use sample values and approximate screen layouts. Actual screens depend on the radio, firmware, and configured widgets.
- Windows standalone build verification and physical-radio testing remain pending.

## Feedback & Issues

Found a problem or have an idea? Open an issue and include:

- Radio model and EdgeTX version.
- RadioDock version.
- What you were trying to do.
- Any error message or screenshot.
- `BUILD_LOG.txt` if the Windows build failed.

## Credits

Created by **Kentucky Bluebird**.

Thanks to the EdgeTX team and the developers behind the scripts, widgets, themes, and image resources used by the RC community.

Bluebird RadioDock is an independent community project and is not affiliated with or endorsed by EdgeTX or RadioMaster. Third-party downloads retain their original licenses.
