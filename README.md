Bluebird RadioDock
Bluebird RadioDock is a portable Windows utility for some of the EdgeTX SD-card jobs I kept finding myself doing over and over.
It is not intended to replace EdgeTX Companion. The goal is to make model images, themes, sounds, migration work, and finding useful EdgeTX add-ons a little easier while keeping the operator in control.
Current release: v1.4.44
Download the latest release · RC Groups discussion and feedback
---
Model Images
RadioDock can search SkyRaccoon and AIR-RC for aircraft/model images, preview the results, prepare them for the selected radio, save them to the SD card, and assign them directly to an EdgeTX model YAML.
It also scans the model files already on the radio and can point out:
models with no image assigned;
models whose assigned image is missing;
valid existing assignments;
images in `/IMAGES` that are not currently used by models on that radio.
![Bluebird RadioDock Model Images search](docs/images/model_images_search.png)
Work with images already on the SD card
You do not have to download an image again just to use it.
The image-library review can preview existing files in `/IMAGES`, and Assign to model... can connect one of those existing images directly to a current model YAML.
The assignment workflow backs up the model file first and verifies the change afterward.
![Assign an existing SD-card image to an EdgeTX model](docs/images/model_image_assignment.png)
Conservative image cleanup
A lot of us keep one big image collection and carry it from radio to radio, so RadioDock does not assume that an image is junk just because the current radio is not using it.
The review screen describes those files as not used on this radio and leaves the decision to the operator.
Selected removals are backup-first. `splash.png` is protected, archived YAML references are considered, and nothing is automatically selected for deletion.
---
EdgeTX Add-ons / Lua Browser
RadioDock provides one place to browse EdgeTX Lua scripts, widgets, tools, and other useful add-ons.
It combines the official EdgeTX catalog with selected community projects and can show descriptions, publisher information, screenshots, and download links.
![Bluebird RadioDock EdgeTX Add-ons and Lua browser](docs/images/addons_lua_search.png)
Why Lua installation is conservative
Different Lua projects are packaged in very different ways. Some use Tools, Widgets, Function scripts, shared libraries, sounds, configuration files, or other package-specific locations and setup steps.
Earlier development experimented with broader automatic Lua installation and scanning. Testing showed that guessing wrong could create false detections or install files incorrectly.
For that reason, Lua/widget automatic installation is currently disabled unless a package-specific installation method has been fully verified. The browser remains useful for finding projects and getting to the correct publisher/download source.
I'd rather RadioDock leave something alone than confidently modify the wrong files.
---
ThemeDock
ThemeDock can browse, preview, build, and install EdgeTX color themes.
It supports things such as:
theme previews;
local-photo backgrounds;
crop and positioning controls;
brightness and palette adjustments;
radio-display previews;
reusable theme projects;
theme ZIP export;
installation to the selected EdgeTX SD card.
Personalized startup media is protected
A theme can carry its own splash or startup sound without automatically replacing the files you already use.
Replacement of the active splash image or startup `hello.wav` / `tada.wav` is optional and off by default. If you explicitly choose to replace an active startup asset, RadioDock backs up the existing file first.
---
Sounds & Voice Packs
RadioDock includes access to supported EdgeTX sound and voice resources.
Where the package structure is known and predictable, supported sound packs can be installed automatically. The currently active personalized startup sound is preserved by default unless the operator explicitly chooses to replace it.
---
Model Migration
RadioDock includes utilities to help move or convert model resources between supported EdgeTX radio generations.
The operator chooses the source and destination. RadioDock is not intended to become a Companion replacement or automatically rewrite a radio configuration behind the user's back.
---
Portable by Design
RadioDock is intended to run as a portable Windows application.
Persistent application data is kept beside the program under:
```text
Bluebird_RadioDock_Data
```
The operator manually selects the EdgeTX SD-card root. RadioDock does not guess which removable drive belongs to the transmitter.
---
Updates
RadioDock can check the project's GitHub Releases page for a newer stable version and show the release information inside the application.
It does not silently replace its own executable.
View all Bluebird RadioDock releases
---
Project Notes
This is a hobby/community project.
A lot of the development has been AI-assisted — or, more accurately, a fair amount of vibe coding — followed by testing on real radios, finding what breaks, fixing it, and adding regression tests so the same problem is less likely to come back.
Development/testing has centered heavily on modern EdgeTX color radios, including the RadioMaster TX16S MK3 and Jumper V16, while trying to keep the underlying workflows based on EdgeTX structures rather than one specific radio.
If you try RadioDock on another radio or find something strange, feedback is welcome.
RC Groups discussion:  
https://www.rcgroups.com/forums/showthread.php?4960605-EdgeTX-file-assistant-Standalone-program#post55204319
Downloads / releases:  
https://github.com/Redvsbluecom/Bluebird_Radio_Dock/releases
---
Safety
Back up your SD card before using any program that writes to it.
RadioDock's general rule is simple:
> If an operation cannot be performed with enough confidence to protect the existing radio files, it should not be automatic.
---
License
See the repository license and the individual licenses of third-party projects and resources referenced by RadioDock.
Bluebird RadioDock does not claim ownership of EdgeTX, publisher add-ons, themes, sound packs, aircraft images, or other third-party projects surfaced through the application.
