# ZMK Config for Hitsuki46 with Latest DYA Studio Support

This repository provides ZMK firmware configuration for the Hitsuki46 split keyboard, adapted to support the latest [DYA Studio](https://studio.dya.cormoran.works/) based on [cormoran/zmk-keyboard-dya2 v2.0](https://github.com/cormoran/zmk-keyboard-dya2/releases/tag/v2.0).

## Features
- Dual trackball support (PMW3610)
- NiMH battery support
- WS2812 LED status
- Full DYA Studio compatibility (keymap, trackball settings, macros, combos, OS detection, battery history, BLE management, etc.)
- Based on ZMK main+dya (v0.4 era) + cormoran modules

## Hardware
- MCU: Seeed XIAO nRF52840 (xiao_ble)
- Based on DYA Dash schematic (cormoran)
- 46 keys split

## Build
GitHub Actions will build on push. Download UF2 from Actions artifacts.

Or local:
```
west init -l config
west update
west zmk-build  # or use the build matrix
```

## Notes
- This is an initial adaptation. Trackball runtime processors and some LED animation may need further tuning for dual trackball + Studio.
- Refer to gohanda11/zmk-config-hitsuki46 for original pinouts and to cormoran/zmk-keyboard-dya2 for Studio features.
- Flash left/right UF2 accordingly. Use settings_reset if needed.
- Unlock Studio with &studio_unlock key if locking is enabled.

## Credits
- Original Hitsuki46 ZMK: gohanda11
- DYA / DYA Studio / modules: cormoran
- PMW3610: badjeff / cormoran custom
