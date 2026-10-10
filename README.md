# Bluebird RadioDock

<p align="center">
  <img src="Kentucky_Bluebird.png" width="180">
</p>

<p align="center">
  <b>A portable Windows utility for managing EdgeTX radios, model images, Lua add-ons, themes, sounds, and model migration.</b>
</p>

Bluebird RadioDock is designed to make common EdgeTX SD-card tasks easier without trying to replace EdgeTX Companion.

The operator still chooses the radio SD-card location and stays in control of what gets downloaded, installed, converted, or copied.

---

## Main Features

### Model Images

Search for RC aircraft/model images and download them directly to your selected EdgeTX SD card.

RadioDock can:

- Search supported model-image providers
- Preview images before downloading
- Select the radio/display type
- Resize images appropriately for supported radios
- Create EdgeTX-friendly filenames
- Enforce the 9-character model-image naming limit
- Save directly to a selected radio folder
- Reload previews when needed

The goal is to make finding and preparing model images much faster than manually searching, resizing, renaming, and copying files.

---

## EdgeTX Add-ons & Lua Tools

Browse supported EdgeTX Lua scripts, widgets, tools, and add-ons from inside RadioDock.

Features include:

- Add-on browsing
- Publisher screenshots and previews
- Multi-image screenshot galleries
- Links to the original publisher page
- Manual package downloads
- EdgeTX SD-root selection
- Conservative automatic installation for supported packages

RadioDock intentionally does **not** guess when an add-on has an unclear folder structure or radio-specific installation requirement.

If RadioDock cannot confidently determine where something belongs, the package stays manual.

---

## ThemeDock

Create custom themes for EdgeTX color-screen radios using your own photos and color choices.

<p align="center">
  <img src="ThemeDock_preview.png" width="850">
</p>

ThemeDock includes:

- Custom background images
- Image crop and positioning
- Brightness adjustment
- Theme color editing
- Radio/display previews
- Editable ThemeDock project files
- EdgeTX theme export
- Support for multiple EdgeTX color-screen layouts

ThemeDock is intended to make creating a personalized EdgeTX theme much easier without manually assembling all of the theme files.

---

## Sound Tools

RadioDock includes tools for working with EdgeTX sound packs and supported radio sound folders.

The operator chooses the SD-card location, allowing RadioDock to remain portable and avoid making assumptions about drive letters.

---

## MK2 / MK3 Model Migration

RadioDock includes migration tools for moving compatible EdgeTX model files between supported radio generations.

This was originally developed to help with model configuration differences encountered when moving between radios such as the TX16S MK2 and newer MK3 hardware.

The migration system is intentionally separate from EdgeTX Companion and focuses on targeted model-file conversion rather than complete radio management.

---

## Portable by Design

Bluebird RadioDock is designed to remain portable.

Application-owned data is kept with the program rather than being scattered throughout Windows whenever practical.

The finished standalone EXE does not require the end user to install Python.

---

# Installation

## Recommended Method

Go to the **Releases** section and download the latest Bluebird RadioDock package.

If the release contains a ready-to-run standalone EXE:

1. Download the EXE.
2. Place it in a folder of your choice.
3. Run Bluebird RadioDock.
4. When working with your radio, point RadioDock to the correct EdgeTX SD-card root.

## Building from the Build Kit

If you download the source/build kit instead:

1. Extract the ZIP to a normal Windows folder.
2. Run:

```text
BUILD_FINAL_STANDALONE.bat
