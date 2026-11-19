# Framework Wireless Touchpad Keyboard

Documentation for the PCB and other key modules in the [Framework Wireless Touchpad Keyboard](https://frame.work/products/framework-wireless-touchpad-keyboard).

> [!NOTE]
> This is preliminary information for the current prototype. Everything is subject to change and more information will follow.

## Overview

- 68.8 × 85.6 mm precision touchpad with multi-touch gesture support
- 1.5 mm key travel
- Wired, Bluetooth, or USB-A dongle connection, with switching between up to four wireless devices
- Compatible with the USB-A Adapter Expansion Card
- Nordic nRF54LM20A ultra-low-power wireless SoC
- Open-source CAD design and firmware based on [ZMK Firmware](https://zmk.dev)
- Control Board will be available for purchase separately, with breakout pinouts for DIY keyboard builds and custom projects

Get notified when it becomes available: https://frame.work/products/framework-wireless-touchpad-keyboard

## Repository layout

| Path | Contents |
| --- | --- |
| [`ControlBoard/`](ControlBoard/) | Control Board CAD, schematic pages, pinout, and photos. Start with the [Control Board README](ControlBoard/README.md). |
| [`Battery/`](Battery/) | Battery CAD, connector part numbers, and pinout. Start with the [Battery README](Battery/README.md). |
| [`FrameworkWirelessTouchpadKeyboard_dummy_20260605.step`](FrameworkWirelessTouchpadKeyboard_dummy_20260605.step) | Keyboard CAD |
| [`LICENSE`](LICENSE) | CC BY 4.0 license text |

## Mechanical CAD

| Part | File |
| --- | --- |
| Keyboard (dummy model, 2026-06-05) | [FrameworkWirelessTouchpadKeyboard_dummy_20260605.step](FrameworkWirelessTouchpadKeyboard_dummy_20260605.step) |
| Control Board | [ControlBoard.stp](ControlBoard/ControlBoard.stp) |
| Battery | [Battery.stp](Battery/Battery.stp) |

## Control Board

We designed the Control Board to be a repurposable module for keyboard makers and DIYers. The Control Board Developer Program gets pre-production modules into the hands of developers who help test them and give feedback before the module goes on sale. The program is underway with a first group of developers.

Photos, schematic pages, and pinout: [ControlBoard/README.md](ControlBoard/README.md)

## Battery

> [!WARNING]
> Shorting the battery can cause fire or burns. Disconnect the battery and USB cable before working on the board. Never let bare battery wires touch each other or metal. Do not open, crush, puncture, or heat the battery. Stop using it if it is swollen or damaged. Modifying the battery or its wiring is at your own risk.

The battery connects to the Control Board through a 3-pin Molex PicoBlade (1.25 mm pitch) connector, `JBAT` on the [power management schematic](ControlBoard/Schematic/PowerManagementUSBInput.pdf).

| Pin | Net | Wire color |
| --- | --- | --- |
| 1 | `VBAT` (+) | Red |
| 2 | `VBAT_NTC` (thermistor) | Yellow |
| 3 | `GND` (−) | Black |

To run without the battery's thermistor, tie `VBAT_NTC` to ground through a 10 kΩ resistor.
With the resistor in place, the charger can't sense the battery temperature, so it won't stop charging if the battery gets too hot or too cold.

Connector part numbers and mating parts: [Battery/README.md](Battery/README.md)

## Touchpad

Firmware configuration and pinout of the Touchpad to enable re-use: not yet published.

## Keyboard and USB-A Adapter Expansion Card PCBs

Interface schematics and pinout of the PCBs to enable re-use: not yet published.

## Firmware and Bootloader

The keyboard firmware is based on ZMK, which runs on Zephyr, and will be open sourced on GitHub. Zephyr board support for the keyboard is open as [FrameworkComputer/zephyr#2](https://github.com/FrameworkComputer/zephyr/pull/2).

## License

Framework Wireless Touchpad Keyboard © 2026 by Framework Computer Inc is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). The full license text is in [LICENSE](LICENSE).
