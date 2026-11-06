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
| [`Battery/`](Battery/) | Battery CAD |
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

Pinout of the Battery to enable re-use: not yet published.

## Touchpad

Firmware configuration and pinout of the Touchpad to enable re-use: not yet published.

## Keyboard and USB-A Adapter Expansion Card PCBs

Interface schematics and pinout of the PCBs to enable re-use: not yet published.

## Firmware and Bootloader

The keyboard firmware is based on ZMK, which runs on Zephyr, and will be open sourced on GitHub. Zephyr board support for the keyboard is open as [FrameworkComputer/zephyr#2](https://github.com/FrameworkComputer/zephyr/pull/2).

## License

Framework Wireless Touchpad Keyboard © 2026 by Framework Computer Inc is licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). The full license text is in [LICENSE](LICENSE).
