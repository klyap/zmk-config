# Sweet16 ZMK Config

This repository builds ZMK firmware for a Sweet16 4x4 macropad using a nice!nano v2 controller.

## Files

- `build.yaml` builds `nice_nano_v2` with the `sweet16` shield.
- `config/sweet16.keymap` contains the editable key bindings.
- `config/sweet16.conf` sets the Bluetooth/USB keyboard name.
- `boards/shields/sweet16/sweet16.overlay` defines the 4x4 GPIO matrix.

## Pin Assumption

The matrix uses the Sweet16 v1-style Pro Micro mapping: rows on `F4`, `F5`, `F6`, `F7` and columns on `D7`, `E6`, `B4`, `B5`. If keys respond but are in the wrong positions, update the matrix transform in `boards/shields/sweet16/sweet16.overlay`.

## Flashing

Push this repo to GitHub, let Actions build the firmware artifact, download the `.uf2`, double-tap reset on the nice!nano, and copy the `.uf2` onto the mounted bootloader drive.
