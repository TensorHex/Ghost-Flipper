# Ghost Flipper Firmware

**Forked from** [DarkFlippers/unleashed-firmware](https://github.com/DarkFlippers/unleashed-firmware)

### Disclaimer

This software is for educational purposes only and is not intended to be used for any illegal activity. <br> We do not condone illegal activity and strongly encourage keeping transmissions limited to frequencies and protocols allowed by regional law. <br> This software is made without support from Flipper Devices and is in no way associated with the official Flipper project. 

# Installation

Install bundles can be downloaded from the [releases](https://github.com/TensorHex/Ghost-Flipper/releases) page. These can be installed with qFlipper. **If this is your first time installing Ghost Flipper, you must update to the latest version of the official firmware before installing Ghost Flipper.**

# Development

Flipper Zero Firmware is written in C, with some bits and pieces written in C++ and armv7m assembly languages. An intermediate level of C knowledge is recommended for comfortable programming. C, C++, and armv7m assembly languages are supported for Flipper applications.

## Requirements

Supported development platforms:

- Windows 10+ with PowerShell and Git (x86_64)
- macOS 12+ with Command Line tools (x86_64, arm64)
- Ubuntu 20.04+ with build-essential and Git (x86_64)

FBT will take care of all the other dependencies.

## Cloning source code

Make sure you have enough space and clone the source code:

```shell
git clone --recursive https://github.com/TensorHex/Ghost-Flipper.git
```

## Building

Build firmware using Flipper Build Tool:

```shell
./fbt
```

## Flashing firmware using USB

Make sure your Flipper is on, and your firmware is functioning. Connect your Flipper with a USB cable and flash firmware using Flipper Build Tool:

```shell
./fbt flash_usb
```

## Documentation

- [Flipper Build Tool](/documentation/fbt.md) - building, flashing, and debugging Flipper software
- [Applications](/documentation/AppsOnSDCard.md), [Application Manifest](/documentation/AppManifests.md) - developing, building, deploying, and debugging Flipper applications
- [Hardware combos and Un-bricking](/documentation/KeyCombo.md) - recovering your Flipper from the most nasty situations
- [Flipper File Formats](/documentation/file_formats) - everything about how Flipper stores your data and how you can work with it
- And much more in the [documentation](/documentation) folder

# Project structure

- `applications`    - applications and services used in firmware
- `assets`          - assets used by applications and services
- `furi`            - Furi Core: OS-level primitives and helpers
- `debug`           - debug tool: GDB plugins, an SVD file, etc.
- `documentation`   - documentation generation system configs and input files
- `firmware`        - firmware source code
- `lib`             - our and 3rd party libraries, drivers, etc.
- `scripts`         - supplementary scripts and python libraries home

Also, see `ReadMe.md` files inside those directories for further details.
