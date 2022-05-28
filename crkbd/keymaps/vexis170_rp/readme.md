# CRKBD (RP2040) Layout 
(adapted from jp230s rp2040, just changed keymap)

## Layers
The four layers:
- BASE Layer: QWERTY
- LOWER Layer: Numbers + Arrows
- RAISE Layer: Symbols
- ADJUST Layer: Numpad + Media Keys + Fn keys

## OLED
- Master: Renders layer state + keylog
- Slave : Renders an animation of a cat that varies its animation speed based on the current WPM

## differences from Pro Micro Board
- Updated `rules.mk`:
  - Set MCU to `RP2040`
  - WS2812 driver to `pio`
  - Serial driver to `pio`
  - Enable warnings
- Updated `config.h`:
  - Set the RP2040 pins for matrix, OLED and RGB
- Added `mcuconf.h` to use I2C1 (for OLED)
- Added `halconf.h` to enable I2C (for OLED)

## Flashing
Flash using `qmk compile -kb crkbd -km vexis170_rp` for Pro Micro


## Keymap
![image](https://user-images.githubusercontent.com/79429306/170833653-0da21553-e7ec-45d0-a1e4-b739e1e8b553.png)
