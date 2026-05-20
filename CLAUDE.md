# CLAUDE.md

## What this repository is

Millennium is an open source hardware preservation and restoration project for the Logitech MX1000 Laser Cordless Mouse (2004, M-RAG97). The goal is to create modern drop-in replacement components that enable indefinite serviceability of original hardware while preserving its form factor and functionality. It is not a clone; it is a faithful restoration with modern internals. Where the original can be improved, it should be.

Repository: `jacob-rn-wallace/millennium`  
Licenses: CERN-OHL-S-2.0 (hardware), GPL-3.0 (firmware), CC BY-4.0 (documentation)

---

## Design philosophy

- **Capability over stasis** — improve on the original where possible; do not replicate flaws
- **Improvement over replication** — original behavior is preserved as a firmware profile, not a hardware constraint
- **Original form factor** — all replacement components must fit the original MX1000 shell without modification
- **Drop-in compatibility** — Calibre (replacement PCB) and Reserve (replacement dock) must be mechanically and electrically compatible with original shells and original counterparts

---

## Component naming

The project uses watchmaking-themed subsystem names. Use these terms precisely:

| Name | What it is |
|---|---|
| **Calibre** | Replacement PCB assembly (mouse internals) |
| **Reserve** | Replacement charging dock |
| **Case** | Replacement injection-moulded shells |
| **Regulator** | Cross-platform host configuration software (Tauri-based) |

The target hardware (Logitech MX1000) is referred to as the **specimen**. Physical component names for the MX1000 (buttons, zones, PCBs, housing parts) are defined in `docs/mx1000-physical-description.md`. **Always consult that document before making any claims about appearance or physical construction.** It exists specifically because visual misidentification is a recurring error.

---

## Locked design decisions

These are not open questions. Do not suggest alternatives unless explicitly asked.

- **Sensor:** PAW3395 (pending optical geometry confirmation)
- **MCU:** nRF52840 as an off-the-shelf certified module (daughterboard architecture)
- **Wireless:** Bluetooth HID first; 27 MHz RF subsequently
- **Firmware:** ZMK or Nordic nRF Desktop
- **PCB identifier scheme:** `M1K-PPTTBBVVVV` with ITA2 (CCITT 1932) encoding — see `docs/m1k-identifier-registry.md`

---

## Repository structure

```
millennium/
├── LICENSE-DOCUMENTATION    # CC BY 4.0
├── LICENSE-FIRMWARE         # GPL-3.0
├── LICENSE-HARDWARE         # CERN-OHL-S-2.0
├── README.md
├── docs/                    # Project documentation and reference material
├── electrical/              # PCB photography, scans, schematics, BOM, RF documentation
├── firmware/                # Calibre and Reserve firmware
├── manufacturing/           # Casting, materials, and assembly documentation
├── mechanical/              # Scans, CAD models, print-ready files, dimensioned drawings
└── sourcing/                # Batteries, switches, secondary market guidance
```

Key documents in `docs/`:

| File | Purpose |
|---|---|
| `mx1000-physical-description.md` | **Authoritative** component names and per-colorway visual details — consult before any physical claims |
| `mx1000-variant-catalog.md` | All production SKUs, colorways, part numbers, PCB revisions, bundles, production timeline |
| `mx1000-serial-number-decoding.md` | LZ/LNA prefix analysis, Y+WW date encoding, cross-product validation |
| `mx1000-dock-catalog.md` | Dock specimens, serial analysis, pairing methodology, PCB architecture |
| `millennium-roadmap.md` | Phased development roadmap (Theseus Track and Greenfield Track) |
| `m1k-identifier-registry.md` | PCB identifier scheme specification and assignment tables |

PCB scans live under `electrical/pcb-scans/`, organized by board name and revision (e.g., `roller-pcb-rev-b/`, `thumb-pcb-rev-a/`).

---

## Specimen inventory

### Mice (7 units)

| Unit | P/N | Colorway | Serial | Mfg week | Status |
|---|---|---|---|---|---|
| Mouse 1 | 852152-0200 | Gunmetal Silver | LZC51411902 | Wk 14/2005 | Functional, boxed; PCBs from Mouse 5 |
| Mouse 2 | 852376-0000 | Dark Blue (MX3100 bundle) | LZB50753012 | Wk 7/2005 | Primary dissection subject; roller PCB fully documented; PCBs from Mouse 4 |
| Mouse 3 | 852152-1000 | Midnight Black | LZB44150762 | Wk 41/2004 | Benched (laser latency bug); **do not dissect** — only Rev. A specimen |
| Mouse 4 | 852152-0000 | Gunmetal Silver | LZC45101572 | Wk 51/2004 | Shell only — PCBs transplanted to Mouse 2 |
| Mouse 5 | 852152-0100 | Gunmetal Silver | LZ549B4 | Wk 49/2005 | Shell only — PCBs transplanted to Mouse 1; heavily scuffed |
| Mouse 6 | 852152-0100 | Gunmetal Silver | LZ549B4 | Wk 49/2005 | Intact, functional, spare |
| Mouse 7 | 852152-0200 | Gunmetal Silver | LZ603B4 | Wk 3/2006 | Intact, functional, spare |

PCB revisions: Mouse 3 is PCB Rev. A (main/roller/thumb). All others examined are PCB Rev. B (main/roller). Thumb PCB is Rev. A on every specimen examined — it appears to version independently.

### Docks (7 units)

| Unit | Model | P/N | Serial | Mfg week | Notes |
|---|---|---|---|---|---|
| Dock 1 | C-BN34 | 831145-0000 | LZB44252090 | Wk 42/2004 | Paired with Mouse 1 |
| Dock 2 | C-BO34 | 831231-0000 | LNA50713319 | Wk 7/2005 | Paired with Mouse 2; **do not dissect** — only C-BO34 specimen |
| Dock 3 | C-BN34 | 831145-0000 | LZB44150762 | Wk 41/2004 | Paired with Mouse 3 |
| Dock 4 | C-BN34 | 831145-0000 | LZ713B1 | Wk 13/2007 | **Designated dissection subject** |
| Dock 5 | C-BN34 | 831145-0000 | LNA45100135 | Wk 51/2004 | Provisionally paired with Mouse 5 |
| Dock 6 | C-BN34 | 831145-0000 | LZ549BC | Wk 49/2005 | Provisionally paired with Mouse 6 |
| Dock 7 | C-BN34 | 831145-0000 | LZ603BC | Wk 3/2006 | Paired with Mouse 7 |

All docks have main board P/N 201797-0000 Rev. A, except Dock 2 (201814-0??? Rev. A). PCB date codes on dock boards (main: 06.28.04, power: 06/24/04) are design revision dates, not manufacture dates.

---

## Documentation standards

**These rules are non-negotiable:**

1. **Distinguish confirmed facts from inferences explicitly.** Use language like "confirmed," "observed," "inferred," or "unverified" where appropriate. Do not state inferences as facts.
2. **Primary sources required for cited claims.** Unverified sources (e.g., links returning 403, forum posts not confirmed accessible) must be softened or flagged.
3. **Consult `mx1000-physical-description.md` before making any claims about appearance or construction.** This document is authoritative. Do not describe colors, finishes, component geometry, or part names from memory.
4. **The README and formal documents reflect only formally completed and documented work.** Incidental observations from conversation are not included without proper measurement or verification.
5. **CAV numbers are injection moulding cavity identifiers, not version indicators.** Do not interpret them as revision data.
6. **Dock PCB date codes are design revision dates, not manufacture dates.**

---

## Development roadmap summary

Two parallel tracks after a shared prerequisite phase:

- **Phase 0** — Physical characterization (prerequisite for both tracks)
- **Theseus Track (Phases 1–3)** — Progressive PCB reproduction and modernization, beginning with exact reproduction of the original design. Gated by complete schematic capture and functional understanding of the original.
- **Greenfield Track (Phases 4–7)** — New internals from scratch using modern components (nRF52840, PAW3395). Largely independent of Theseus after Phase 0; can run in parallel once the Phase 3 gate is met.

See `docs/millennium-roadmap.md` for the full phase definitions and gate conditions.

---

## Commit workflow

- Jake stages and executes commits; Claude proposes the commands but does not assume they have been run
- Commit messages are specific and enumerate individual changes
- Do not assume a commit has been made unless Jake confirms (e.g., "ok done")
- Jake handles `git push` independently
- Frequent, scoped commits — one logical change per commit where practical

---

## Known codenames (silkscreen)

- **KOS** — appears on every PCB with sufficient silkscreen space; interpreted as the system-level platform codename for the MX1000 product
- **SANTORINI** — appears only on the dock power board; interpreted as a sub-project or board-specific codename for the charging subsystem

No public documentation has been found for either codename.