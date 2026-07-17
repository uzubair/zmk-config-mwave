# ZMK Config for the Kinesis mWave

This repository contains the keymap files for the Kinesis mWave Mechanical Keyboard. There are 3 discrete keymap files, one for each variant: ANSI Windows, ANSI Mac, ISO Windows (not in production) so please choose the appropriate .keymap file. Power users who prefer not to customize their device with Kinesis Clique (https://clique.kinesis-ergo.com/) or ZMK Studio (https://zmk.studio/) can use a graphical keymap editor (example: https://nickcoutsos.github.io/keymap-editor/) or edit their keymap files directly on GitHub.

Kinesis does not officially support installing custom firmware on this device and no documentation, support or troubleshooting is offered. Proceed at your own risk. If you were to brick your keyboard with custom firmware that would invalidate your warranty.


## File Structure

[config/mwave_33.conf](config/mwave_33.conf): This file contains local Kconfig override flags

[config/mwave_33.keymap](config/mwave_33.keymap): This file contains the ANSI Windows keymap

[config/mwave_33_mac.keymap](config/mwave_33_mac.keymap): This file contains the ANSI Mac keymap

[config/mwave_33_iso.keymap](config/mwave_33_iso.keymap): This file contains the ISO keymap

All other files in the [config/](config/) folder should not be edited. They contain crucial configuration information for the functionality of the device.

## Flashing Firmware

After pushing changes to `main`, GitHub Actions builds the firmware automatically. Download the `firmware` artifact from the latest Actions run.

**The file to flash for the Mac layout is `ansi-mac.uf2`.**

### Steps

1. Double-press the reset button on the keyboard — a `MWAVE` drive will appear on your Mac.
2. Copy the firmware file to the drive:
   ```
   cp ~/Downloads/firmware/ansi-mac.uf2 /Volumes/MWAVE/
   ```
3. The keyboard reboots automatically. The "disk not ejected properly" warning is expected — ignore it.

### Keys not working after flashing?

ZMK Studio stores keymap edits persistently in flash. These stored settings override the compiled firmware even after reflashing. To fix:

1. Double-press reset to enter bootloader.
2. Flash the settings reset firmware first:
   ```
   cp ~/Downloads/firmware/ansi-settings-reset.uf2 /Volumes/MWAVE/
   ```
3. Double-press reset again when the keyboard reboots.
4. Flash the mac firmware:
   ```
   cp ~/Downloads/firmware/ansi-mac.uf2 /Volumes/MWAVE/
   ```

This clears all stored ZMK settings and loads the compiled keymap from scratch.

## Layer Reference

See [docs/mwave_33_mac_layers.md](docs/mwave_33_mac_layers.md) for a full breakdown of every layer, key binding, and behavior.

