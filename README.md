# numpad-lcd-encoders

## 📻 Project Description

A wired numberpad in 5×3 layout, with 3× rotary encoders, and a 128×64 LCD display.

![Photo of first prototype](images/photos/20220527-IMG_1333.jpg)

## 🧰 Features

- 5×3 programmable keys
- 3× rotary encoders (rotate and click)
- 128×64 3.25" LCD display
- Micro-USB connector
- Cut-outs for MCU boot select switch, and trimpot for LCD brightness 

## ⏳ Issues

> ⚠ Not suitable for actual use. Use at your own risk!

- LCD12864 in BOM has a trimpot and capacitors on the rear of the PCB between the centerlines of two of the screws. Standoffs are required here.
- Spacing for switches is tight, to the point that the plate will warp and might snap (printer tolerances may vary)
- Switches next to the bottom two M3 holes will possibly hit pan head screws before bottoming out.
- The entire build flexes significantly when pressing the encoder switches, or pressing the top middle 3 switches in a chording fashion. Probably needs an additional pair of standoffs between the encoders and the switches.
- Flex is also an issue when using the magnetic tenting legs.
- Spacing around encoders on top plate is too wide (ø19mm cutout for ø18mm knobs)
- Encoders might fit with 10mm standoffs between middle and bottom plate, but it will be tight. 12mm is easier to work with.

See: [Photo Gallery](photos.md)

## 🛒 Bill of Materials (BOM)

> ⚠ Dimensions for screws still to be finalised

| Item | Size | Qty | Store |
| ---- | ---- | --- | ----- |
| Raspberry Pi Pico | N/A | 1 | [Raspberry official](https://www.raspberrypi.com/products/raspberry-pi-pico/)
| EC11 Rotary Encoder | ø6×20mm shaft | 3 | [Robotics.org.za](https://www.robotics.org.za/EC11-VER-20)
| LCD Display 128×64 | 93×70mm OD | 1 | [Robotics.org.za](https://www.robotics.org.za/12864-WH-33V)
| ~~LCD I2C Interface Module~~<sup>1</sup> | N/A | ~~1~~ | [Robotics.org.za](https://www.robotics.org.za/6970622931577)
| Switches | MX | 15 |
| Diodes, 1N4148 | N/A | 18 |
| Standoffs | M3×10mm | 6 | [Robotics.org.za](https://www.robotics.org.za/M3-NYLON-KIT)
| Standoffs | M3×6mm | 8 |
| Screws | M3×6mm | 6 |
| Screws | M2×?mm | 4 |
| Nuts | M3 | 6 |
| Nuts | M2 | 4 |
| 3D printed shell | N/A | 3 pcs |
| Encoder knobs | ø18×16mm | 3 pcs |
| JST-SH male breakout (optional) | JST-SH 6 pin | 4 pcs | [Robotics.org.za](https://www.robotics.org.za/4772), [Pololu](https://www.pololu.com/product/4772)
| JST-SH female connectors (optional) | JST-SH 6 pin | 4 pcs | [Robotics.org.za](https://www.robotics.org.za/JST-XH-6P-KIT) |

Notes:
1. I2C interface not required for the ST7920 controller version of the LCD as it already utilises SPI.

---

![Render of the numberpad pad (transparent)](images/renders/Render-Transparent-Iso.png)
## 🔗 References

- [KMK firmware](https://github.com/KMKfw/kmk_firmware)
- [Raspberry Pi Pico Datasheet](https://datasheets.raspberrypi.com/pico/pico-datasheet.pdf)
- [CircuitPython UF2 for Pico](https://circuitpython.org/board/raspberry_pi_pico/)