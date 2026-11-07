# andr36oid

*Philosophy: Trying to answer the question*
> What if the cheapest handheld on the shelf ran software that actually respected the hardware?

andr36oid is a custom Android for the R36S and the whole family of ultra-cheap RK3326 clones, plus the R36 Ultra. It is based on LineageOS 18.1 (Android 11) on a 4.19 kernel, with the UI reworked for a 640x480 console and its game controls.

One image serves them all. The R36S, the many panel and board variants of the clones, and the R36 Ultra boot from the same build, which detects the console and loads the right panel, DTB and device profile at runtime. No picking the wrong image for your board.

### Install via the **[andr36oid SD flasher](https://github.com/andr36oid/andr36oid_sdflasher/releases/)**
Install should be simple. Download the flasher, put your SD card in, and let it write the latest release. It picks the right profile for your console, and if your board is not auto-detected it walks you through choosing one. An existing andr36oid card keeps your games and settings when you update.

## What works
- The R36S, R36 Ultra, and a large and growing list of clones from one image, with per-board panel, DTB and charging profiles
- Performance profiles and overclocking, with a low-voltage warning when a console throttles
- Kernel Tweaks: tune CPU/GPU/stick/charging behaviour per console, export and import profiles
- Custom screen refresh rates, with a safe preview and a smoothness test
- Missing or extra buttons handled per board, with a user-picked Fn stand-in and bindable extras
- Per-stick sensitivity, and RGB stick rings on the consoles that have them
- USB device modes: present the console as a keyboard, gamepad, flash drive, CD-ROM or sound card over a single USB-C cable
- eMMC install for consoles that have internal storage, with backup and restore
- Optional root with Magisk, pinned to the shipped version so an app update cannot brick it
- Hotfixes applied from the card at boot, with no reflash
- **The dArkOSen Subsystem for Linux** (see below)

## dArkOSen Subsystem for Linux
Run a full Linux desktop stack (dArkOSen, with EmulationStation and PortMaster) right alongside Android, no reflashing. Android lets go of the GPU and the Linux frontend takes it over, so it runs close to native speed, and you can drop cleanly back to Android when you are done. This is early (alpha), and it pairs with [djparentx's dArkOSen](https://github.com/djparentx), whose work the subsystem is built around.

## What doesn't (yet)
- The dArkOSen subsystem is alpha and has rough edges
- Vulkan and on-device updates from the console itself are in progress
- Found a bug? Tell us in GitHub issues

## Help
Running into issues? Report a problem via [GitHub issues](https://github.com/andr36oid/issue_tracker/issues).

Status: public releases are stable daily drivers; the Linux subsystem is an opt-in alpha.

## Links
Official sister project to [haretic](https://github.com/haretic), a custom OS for the rabbit r1.
