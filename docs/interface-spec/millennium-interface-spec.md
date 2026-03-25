# Millennium Interface Specification

**Version:** 0.1 (Draft)
**Status:** Pre-hardware — awaiting physical unit measurement

---

## 1. Overview

This document defines the interface between Millennium Calibre (replacement PCB) and
Millennium Reserve (charging and data dock). All future Calibre and Reserve versions
are guaranteed compatible provided they conform to this specification.

---

## 2. Physical Interface

### 2.1 Contact Geometry
*To be measured from original Logitech MX1000 unit.*
- Contact diameter:
- Contact spacing (center to center):
- Contact material:
- Spring force range:

### 2.2 Mechanical Seating
*To be measured from original Logitech MX1000 unit.*
- Cradle entry angle:
- Seating depth:
- Alignment features:

---

## 3. Electrical Interface

### 3.1 Charging
*To be measured from original Logitech MX1000 cradle.*
- Cradle output voltage (nominal):
- Cradle output voltage (range):
- Maximum charging current:
- Connector polarity:

### 3.2 Data Line
- Protocol: 1-Wire (Dallas/Maxim, now Analog Devices)
- Conductor: Charging positive contact (AC coupled)
- DC isolation: Capacitive (value TBD pending electrical characterization)
- Pull-up voltage: 3.3V
- Pull-up resistor: TBD

---

## 4. Protocol

### 4.1 Base Framing
- Standard 1-Wire timing as defined in Analog Devices 1-Wire protocol specification
- Standard speed: 16.3 kbps
- Overdrive speed: 142 kbps (optional, implementation dependent)

### 4.2 Device Detection
- Reserve pulls up contact and issues reset pulse
- Calibre responds with presence pulse
- Absence of presence pulse indicates original Logitech cradle — charge only mode

### 4.3 Command Space
*Reserved ranges to be allocated as firmware develops.*

| Range | Purpose |
|-------|---------|
| 0x00–0x0F | Reserved |
| 0x10–0x1F | Device identification |
| 0x20–0x2F | Battery and power management |
| 0x30–0x3F | Firmware update |
| 0x40–0x4F | Diagnostics |
| 0x50–0x5F | Configuration |
| 0x60–0xFF | Reserved for future use |

### 4.4 Versioning and Negotiation
- On connection, Calibre reports supported protocol version and capability flags
- Reserve negotiates down to highest mutually supported feature set
- Unknown commands must be ignored gracefully by both sides

---

## 5. Required vs Optional Commands

| Command | Status | Description |
|---------|--------|-------------|
| Device ID | Required | Report Calibre hardware revision |
| Protocol version | Required | Report supported protocol version |
| Battery level | Required | Report charge state (0–100%) |
| Firmware version | Required | Report current firmware version |
| Firmware update | Optional | Accept and flash new firmware |
| Diagnostics dump | Optional | Report event logs and sensor health |
| Configuration write | Optional | Accept button mapping and settings |

---

## 6. Compatibility Guarantee

Any Calibre version is compatible with any Reserve version provided both conform to
this specification. The physical contact geometry, charging voltage envelope, and
base 1-Wire framing defined in sections 2, 3, and 4.1 are permanently fixed and
will not change in future revisions of this document.

---

## 7. Revision History

| Version | Date | Notes |
|---------|------|-------|
| 0.1 | 2026-03-25 | Initial skeleton — pre-hardware |