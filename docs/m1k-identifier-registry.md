# M1K identifier registry

This document defines the identifier scheme used for all Millennium PCB designs and maintains the registry of assigned identifiers.

---

## Identifier format

```
M1K-PPTTBBVVVV
```

All identifiers begin with the family prefix `M1K`, followed by a hyphen, followed by a ten-digit numeric string with no internal separators. The ten digits are divided into four fixed-width segments:

| Segment | Digits | Width | Meaning |
|---------|--------|-------|---------|
| PP | 1–2 | 2 | Peripheral |
| TT | 3–4 | 2 | Track |
| BB | 5–6 | 2 | Board |
| VVVV | 7–10 | 4 | Version |

Segment boundaries are implicit and fixed — no separators appear within the numeric string. An identifier can be parsed unambiguously by position alone.

---

## Encoding

Segment values are derived from the ITA2 character encoding (International Telegraph Alphabet No. 2), the international teleprinter standard ratified by the CCITT in 1932. Each character is represented as a five-bit value with the most significant bit on the left, rendered as a two-digit decimal number (zero-padded where necessary).

The ITA2 standard is publicly documented and requires no proprietary reference to decode. A complete character table is available at: https://en.wikipedia.org/wiki/Baudot_code

### Peripheral (PP)

Identifies the Millennium subsystem the board belongs to.

| Value | ITA2 character | Subsystem |
|-------|---------------|-----------|
| 14 | C | Calibre (replacement PCB) |
| 10 | R | Reserve (replacement dock) |
| 05 | S | Case (replacement shells) |
| 16 | T | Regulator (host configuration software) |

### Track (TT)

Identifies the development track the design belongs to.

| Value | ITA2 character | Track |
|-------|---------------|-------|
| 16 | T | Theseus Track |
| 26 | G | Greenfield Track |

### Board (BB)

Identifies the specific PCB within the subsystem.

| Value | ITA2 character | Board |
|-------|---------------|-------|
| 28 | M | Main board |
| 10 | R | Roller board |
| 16 | T | Thumb board |
| 18 | L | Laser board |

The board segment may be allocated differently by subsystems whose board taxonomy differs from Calibre's. In all cases the encoding method remains the same: a two-digit ITA2 decimal value. Allocations for Reserve, Case, and Regulator boards will be documented here as those subsystems develop.

### Version (VVVV)

A four-digit sequential number assigned in order of design creation within a given peripheral/track/board combination. Version numbers begin at 0001 and increment by one for each new design revision. Each distinct design — however minor the change from its predecessor — receives its own version number. There are no sub-variants; one design, one number.

---

## Assigned identifiers

Identifiers are reserved here before design work begins. A row must be added to this table before committing any new board design to the repository.

| Identifier | Peripheral | Track | Board | Description | Status |
|------------|-----------|-------|-------|-------------|--------|

---

## Assignment log

| Identifier | Date reserved | Reserved by | Notes |
|------------|--------------|-------------|-------|
