# Millennium

**Millennium** is an open source preservation and restoration project for the **Logitech MX1000 laser mouse** — the world's first laser mouse, released in 2004, and still regarded by many as the finest mouse ever made.

The MX1000 is no longer manufactured. Official software support has ended. Batteries degrade. Shells wear. The laser sensor is irreplaceable through normal channels. Millennium exists to change that.

This README intentionally avoids implementation specifics. Hardware design decisions, firmware architecture, and manufacturing processes are documented in their respective directories and in `docs/interface-spec/millennium-interface-spec.md`.

---

## Project Vision

The goal of Millennium is to make the MX1000 **indefinitely serviceable** — not merely repairable with whatever parts remain, but supported by a complete, open library of reproducible components and documented processes.

This means:

- A replacement PCB built from modern, readily sourceable components
- A replacement charging and data dock compatible with the original cradle interface
- Replacement shells with permanent, wear-proof markings
- A parts archive sufficient to rebuild a functional MX1000 from scratch

---

## Design Philosophy

Millennium is guided by the following principles:

- **Compatibility as a guarantee** — all Calibre (PCB) versions are compatible with all Reserve (dock) versions, enforced by a permanent interface specification
- **Improvement over replication** — replacement components are not constrained by the original manufacturing process and should be measurably better where possible
- **Open by default** — all design files, measurements, and documentation are published under open licenses so the community can build on them without restriction
- **Buildability** — every process should be executable by a motivated individual with access to hobbyist tools, not just specialist equipment

---

## Components

**Calibre** — the replacement PCB. Implements Bluetooth HID as an initial wireless target, with 27MHz protocol compatibility (matching the original receiver) as a subsequent goal. Where possible, builds on existing open source mouse hardware designs. Designated by revision as Calibre M1K###.

**Reserve** — the replacement charging and data dock. Electrically compatible with the original Logitech cradle's charging behavior. Adds a 1-Wire data channel over the existing charging contacts for firmware updates, diagnostics, and configuration. The original Logitech cradle remains fully functional for charging. Designated by revision as Reserve M1K###.

**Case** — replacement top and bottom shells, cast in urethane with double-shot legend inserts for permanent, wear-proof markings. A parametric process for applying custom graphics allows users to choose their own markings.

**Parts documentation** — a complete open archive of every measurable and reproducible component: PCB photography, schematics, dimensional drawings, material specifications, and sourcing guides.

---

## Repository Structure
```
millennium/
├── CONTRIBUTING.md          # Contribution guidelines and code of conduct
├── LICENSE-DOCUMENTATION    # CC BY 4.0 (documentation)
├── LICENSE-FIRMWARE         # GPL-3.0 (firmware)
├── LICENSE-HARDWARE         # CERN-OHL-S-2.0 (hardware)
├── README.md                # This file
├── docs/                    # Interface specification and project documentation
├── electrical/              # PCB photography, schematics, BOM, RF protocol documentation
├── firmware/                # Calibre and Reserve firmware
├── manufacturing/           # Casting, materials, and assembly documentation
├── mechanical/              # Scans, CAD models, print-ready files, dimensioned drawings
└── sourcing/                # Batteries, switches, secondary market guidance
```
---

## Current Status

The project is in its earliest stage. A unit is en route for physical characterization. No hardware has been produced yet.

Immediate priorities upon receiving the unit:

- Full internal photography and dimensional measurement
- PCB tracing and component identification
- Charging contact voltage and current characterization
- RF capture of 27MHz protocol traffic
- Shell geometry scan

---

## Contributing

The project currently needs people with experience in:

- RF reverse engineering and SDR capture (27MHz protocol documentation)
- KiCad PCB design
- nRF52840 / Bluetooth HID firmware
- Urethane casting and silicone mold making
- 3D scanning and Fusion 360

If you have an MX1000 and are willing to contribute measurements, photographs, or disassembly documentation, that is equally valuable.

Please open an issue or discussion before proposing major architectural changes so that design intent can be preserved.

---

## Prior Art and Related Work

The MX1000 community has kept these mice alive for over twenty years. Work this project builds on:

- [iFixit MX1000 disassembly guide](https://www.ifixit.com/Guide/Logitech+Mouse+MX1000+Disassembly/139371)
- [Bitbuilt MX1100 3D scans](https://bitbuilt.net/forums/threads/logitech-mx1100.6785/) — high-poly shell scans of the closely related MX1100, useful as geometric reference
- [NewPower99 battery replacement kit](https://newpower99.com/products/logitech-mx1000-cordless-mouse-battery-replacement-kit-with-special-installation-tools-and-one-year-money-back-guarantee) — the established battery replacement solution
- [Solaar](https://github.com/pwr-Solaar/Solaar) — Linux manager for Logitech devices, partial HID++ protocol documentation
- [logiops](https://github.com/PixlOne/logiops) — unofficial Linux driver for HID++ 2.0+ devices; useful firmware architecture reference though the MX1000 predates its supported protocol range
- [MouseJack research](https://www.bastille.net/research/vulnerabilities/mousejack) — Bastille Security's disclosure of Logitech Unifying receiver vulnerabilities, useful RF protocol context

---

## License

Millennium uses a split license model:

- **Hardware designs and mechanical documentation** are licensed under the **CERN Open Hardware License Version 2 – Strongly Reciprocal (CERN-OHL-S-2.0)** (see `LICENSE-HARDWARE`)
- **Firmware** is licensed under the **GNU General Public License v3.0 (GPL-3.0)** (see `LICENSE-FIRMWARE`)
- **Documentation** is licensed under **Creative Commons Attribution 4.0 International (CC BY 4.0)** (see `LICENSE-DOCUMENTATION`)

Unless otherwise noted, files are licensed according to the category they fall under.