# Battery

The keyboard uses a 1200 mAh lithium-ion battery. It plugs into `JBAT` on the Control Board.

> [!NOTE]
> This is preliminary information for the current prototype. Everything is subject to change.

## CAD

- [Battery.stp](Battery.stp)

## Connector

`JBAT` is a 3-pin Molex PicoBlade header with 1.25 mm pitch, shown on the [power management schematic](../ControlBoard/Schematic/PowerManagementUSBInput.pdf). On the board it is a right-angle, surface-mount part.

To connect the battery to your own board, or to make a cable for `JBAT`, use these Molex PicoBlade parts:

| Part | Molex part number | Notes |
| --- | --- | --- |
| Header | [53047-0310](https://www.molex.com/en-us/products/part-detail/530470310) | Vertical, through hole, for your board |
| Receptacle housing | [51021-0300](https://www.molex.com/en-us/products/part-detail/510210300) | Cable side |
| Crimp terminal | [50079-8000](https://www.molex.com/en-us/products/part-detail/500798000) | 26 to 28 AWG wire |
| Crimp terminal | [50058-8000](https://www.molex.com/en-us/products/part-detail/500588000) | 28 to 32 AWG wire |

For pre-crimped leads, see Molex series 214921.

## Pinout

| Pin | Net | Wire color |
| --- | --- | --- |
| 1 | `VBAT` (+) | Red |
| 2 | `VBAT_NTC` (thermistor) | Yellow |
| 3 | `GND` (−) | Black |

If you use a different battery, check its pin order against this table before you plug it in.

`VBAT_NTC` goes to the `NTC` pin of the nPM1300 PMIC (`U2`). To run without the battery's thermistor, tie `VBAT_NTC` to ground through a 10 kΩ resistor.
