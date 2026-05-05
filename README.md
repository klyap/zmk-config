# Sweet16 ZMK Config

This repository builds ZMK firmware for a Sweet16 4x4 macropad using a nice!nano v2 controller.

## Files

- `build.yaml` builds `nice_nano_v2` with the `sweet16` shield.
- `config/sweet16.keymap` contains the editable key bindings.
- `config/sweet16.conf` sets the Bluetooth/USB keyboard name.
- `boards/shields/sweet16/sweet16.overlay` defines the 4x4 GPIO matrix.

## Pin Assumption

The matrix uses the Pro Micro silk labels `D7`, `E6`, `B4`, `B5`, `B6`, `B2`, `B3`, plus inferred `B1` as the missing eighth matrix pin. If one full row or column does not respond after flashing, confirm the eighth pin on the PCB photo and update the last `col-gpios` entry in `boards/shields/sweet16/sweet16.overlay`.

## Flashing

Push this repo to GitHub, let Actions build the firmware artifact, download the `.uf2`, double-tap reset on the nice!nano, and copy the `.uf2` onto the mounted bootloader drive.
