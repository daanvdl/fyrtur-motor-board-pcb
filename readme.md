# IKEA Fyrtur Motorboard Replacement (Drop-In Replica)

Within just a few years, more than 50% of all IKEA Fyrtur blinds I bought had a defective motorboard.
After some investigation, I discovered that the *motor itself* is perfectly fine — it’s the motor control PCB that tends to fail.

This project is a reverse-engineered replica of the original Fyrtur motorboard: a drop-in replacement designed to bring your blinds back to life.

## ✳️ Motivation

After multiple failures, it became clear that the Fyrtur’s weakest point is the control electronics, not the mechanics or the motor.
I wanted a way to repair and reuse the blinds without relying on scarce or unreliable spare parts — so I designed a new, fully compatible board.

------

## 🧠 Inspiration

This work was inspired by two excellent community projects:

- **Riesinger’s custom firmware research**
   https://riesinger.dev/posts/silencing-fyrtur-blinds-with-custom-firmware/
   →  This was the first detailed article I came across showing how mjuhanne’s custom firmware was successfully applied to the IKEA Fyrtur blinds.
- **mjuhanne’s open hardware design**
   https://github.com/mjuhanne/fyrtur-motor-board
   → The foundation and inspiration for my own schematic improvements and hardware layout.

------

## 🧩 Improvements over the original design

Compared to mjuhanne’s schematic, several design improvements were implemented to enhance reliability and compatibility:

- Removed unnecessary parts
- Cleaned silkscreen layout and labeling for easier assembly
- Added silkscreen labeling for reprogramming

The updated and verified schematic is included in this repository.

------

## 🏭 Fabrication

- Manufacturer: JLCPCB
- Files used: `Gerber/` directory
- Thickness: 1.6 mm
- Finish: HASL (recommended) or ENIG (better for hand-soldering heat tolerance)
- Result: Tested and confirmed fully functional
- 100% drop-in replacement — no firmware modification required.

------

## ⚙️ Compatibility

- Fits the original IKEA Fyrtur blinds (tested on multiple units)
- Uses the same connectors and mounting holes as the factory PCB
- Fully compatible with the existing motor, sensors, and ZigBee control board

------

## 🔧 Soldering

This project requires SMD soldering skills. Hand soldering is possible, but using hot-air reflow is recommended for best results.
The board is hardwired at IO2, which connects to the ZigBee button board. The RED labeled wire is RX0.
The motor itself connects via the standard motor connector, just like the original board.

------

## 🧱 Gerber

- **Board thickness:** 1.6 mm
- **Surface finish:** HASL is sufficient, but **ENIG** withstands more heat during manual soldering.
- **Manufacturer:** JLCPCB (personally tested and verified)
- Other PCB manufacturers should also work fine using the included Gerbers.

------

## 🧩 Parts

See `bom.txt` for the complete Bill of Materials.
All components are standard SMD packages (mainly 0603, SOT-23, and SOIC-8).

------

## 🧾 Schematic

I became enthusiastic and motivated to fully reproduce the motor board thanks to the great work by [mjuhanne](https://github.com/mjuhanne/fyrtur-motor-board).
With this project and my own reverse enginering of the controllerboard PCB i was able to bring five electric blinds back to life.

The schematic is based on mjuhanne’s version, extended with the missing and corrected components. You can find it in the `Schematic/` directory.

------

## 💾 Firmware

This project includes the **original IKEA firmware**, located in the `Firmware/` directory.
It allows the board to function identically to the factory version.

For those interested in **enhanced and modified firmware**, including versions that make the blinds **operate completely silently**, please refer to the excellent work by
 👉 [mjuhanne’s Fyrtur Motor Board repository](https://github.com/mjuhanne/fyrtur-motor-board).

------

## 📁 Repository structure

```
├── Firmware/     → Original firmware binaries / data
├── Gerber/       → PCB production files (JLCPCB-ready)
├── Schematic/    → Updated schematic and design source
├── bom.txt       → Bill of Materials
└── README.md     → This documentation
```

------

## 🧑‍🔬 Author Notes

This is a personal repair and improvement project — **not affiliated with IKEA**.
Shared in the hope that it helps others revive their Fyrtur blinds instead of throwing them away.

------

## 📜 License

Open-source hardware. See `LICENSE` for details.
You are free to reuse, modify, and improve — please credit the original authors and references.
