# Logitech MX1000 charging dock catalog

The MX1000 charging dock served a dual role: it was simultaneously the **RF receiver** (connected to the host PC via USB or PS/2) and the **charging cradle** for the mouse's Li-ion battery. Every RF-variant MX1000 shipped with one; the Bluetooth variant shipped with a functionally different dock that charged only, with wireless handled separately by the C-UV35 USB Bluetooth dongle. This catalog documents the seven charging docks in the Millennium project's physical collection, alongside all known dock model numbers, part numbers, serial number analysis, manufacturing evidence, and open questions.

For the mice themselves, see [`mx1000-variant-catalog.md`](mx1000-variant-catalog.md). For serial number decoding methodology, see [`mx1000-serial-number-decoding.md`](mx1000-serial-number-decoding.md).

---

## Dock model numbers and part numbers

Two distinct dock models are represented in the collection:

**C-BN34 (P/N 831145-0000)** is the standard MX1000 RF dock. It served as both the RF receiver and charging cradle, connecting to the host PC via USB (or the included PS/2 adapter). Six of the seven collection specimens are C-BN34 units. The dock carried the label marking **C-BN34 REV A0** on the boxed reference unit (Dock 1); whether later production units carry a higher revision marking has not been confirmed. The C-BN34 accepted a **13V DC** external AC adapter and exposed two metal charging contacts on its cradle surface. The USB device ID presented to the host was **VID 046D / PID C50E**, shared with the mouse itself under the RF protocol.[^1]

The C-BN34 has at least **two documented internal wiring configurations**.[^2] An early version ran two black cables directly from the AC adapter input to the charging circuit PCB. A later version introduced a small connector/junction between the adapter wires and the PCB. A user who documented both variants observed that a contact-cleaning fix resolved charging failures on the later version but not the earlier one, suggesting the revision addressed cold solder joints at the charging contact pads — a widely reported failure mode on aged units.

The C-BN34 carries no FCC ID of its own. Receivers operating below 30 MHz are exempt from equipment authorization under 47 C.F.R. § 15.101(b); the transmitting FCC ID (**DZL201758**) belongs to the mouse.[^3]

**C-BO34 (P/N 831231-0000)** is the bundle-variant dock included with the Cordless Desktop MX 3100. The MX 3100 bundle paired the MX1000 mouse with the MX 3000 wireless keyboard; the dock therefore needed to receive from both devices simultaneously. The C-BO34 is externally similar to the C-BN34 but is a functionally distinct product — its main board (P/N 201814-0???, Rev. A) differs from the C-BN34's (P/N 201797-0000, Rev. A) to accommodate simultaneous keyboard and mouse RF reception. The power board is shared with the C-BN34 (see internal PCB section below). The collection contains one C-BO34 specimen (Dock 2, paired with Mouse 2).

---

## Millennium project reference specimens

The Millennium project's physical collection includes **seven charging docks**, designated **Dock 1** through **Dock 7**. Each dock is numbered to match its paired mouse specimen (see [`mx1000-variant-catalog.md`](mx1000-variant-catalog.md)). Docks 1, 2, and 3 were acquired paired with their corresponding mice; Docks 4–7 were acquired together as a lot alongside Mice 4–7, with original pairings unknown. For Docks 4–7, pairing assignments were determined by manufacture-date analysis of dock serial numbers against decoded mouse serial numbers and PIDs, as documented below.

| Shorthand  | P/N         | M/N    | S/N         | Manufacture week             | Main PCB | Main P/N    | Power PCB | Paired mouse | Pairing basis                             | Current status                             |
| ---------- | ----------- | ------ | ----------- | ---------------------------- | -------- | ----------- | --------- | ------------ | ----------------------------------------- | ------------------------------------------ |
| **Dock 1** | 831145-0000 | C-BN34 | LZB44252090 | Week 42, 2004 (Oct 11–17)    | Rev. A   | 201797-0000 | Rev. B    | Mouse 1      | Acquired paired                           | In collection; Mouse 1's boxed retail unit |
| **Dock 2** | 831231-0000 | C-BO34 | LNA50713319 | Week 7, 2005 (Feb 14–20)     | Rev. A   | 201814-0??? | Rev. B    | Mouse 2      | Acquired paired                           | In collection; MX 3100 bundle dock         |
| **Dock 3** | 831145-0000 | C-BN34 | LZB44150762 | Week 41, 2004 (Oct 4–10)     | Rev. A   | 201797-0000 | Rev. B    | Mouse 3      | Acquired paired; serial matches mouse     | In collection                              |
| **Dock 4** | 831145-0000 | C-BN34 | LZ713B1     | Week 13, 2007 (Mar 26–Apr 1) | Rev. A   | 201797-0000 | Rev. A    | Mouse 4      | By elimination; not original pairing      | In collection                              |
| **Dock 5** | 831145-0000 | C-BN34 | LNA45100135 | Week 51, 2004 (Dec 20–26)    | Rev. A   | 201797-0000 | Rev. B    | Mouse 5      | Provisional; condition-matched            | In collection                              |
| **Dock 6** | 831145-0000 | C-BN34 | LZ549BC     | Week 49, 2005 (Dec 5–11)     | Rev. A   | 201797-0000 | Rev. A    | Mouse 6      | Provisional; manufacture-date matched     | In collection                              |
| **Dock 7** | 831145-0000 | C-BN34 | LZ603BC     | Week 3, 2006 (Jan 15–21)     | Rev. A   | 201797-0000 | Rev. A    | Mouse 7      | Manufacture-date matched; high confidence | In collection                              |

---

## Internal PCB architecture

Physical inspection of all seven docks reveals a consistent two-board architecture: a **main board** handling RF reception and USB connectivity, and a **power board** handling the charging circuit. The two boards are **electrically independent** — they operate as separate systems sharing a housing rather than as a unified circuit. This separation is consistent across both the C-BN34 and C-BO34 variants.

### Main board

The main board is **Rev. A** on every specimen in the collection, including Dock 4 (manufactured week 13/2007). No main board revision change has been observed across the entire production run. All C-BN34 specimens carry part number **201797-0000**; the C-BO34 (Dock 2) carries a distinct part number beginning **201814-0** with the suffix obscured by the LED shroud and not yet confirmed.

### Power board

The power board shows a **revision split** across the collection:

| Power PCB | Docks            | Manufacture weeks                 |
| --------- | ---------------- | --------------------------------- |
| Rev. B    | Docks 1, 2, 3, 5 | Week 41/2004 through week 7/2005  |
| Rev. A    | Docks 4, 6, 7    | Week 49/2005 through week 13/2007 |

The earlier production units carry Rev. B and the later units carry Rev. A — an apparent reversal of the expected revision order. The power board therefore has its own independent revision sequence, unrelated to the main board's. The most likely explanation is a design simplification or cost reduction introduced during the production run that reset or restarted the revision designation. The functional implications, if any, are undocumented.

The power board carries no part number visible on any inspected specimen.

### PCB date codes

All inspected boards carry identical date codes regardless of which dock they came from: the main board stamps **06.28.04** and the power board stamps **06/24/04** (note the different separator conventions between the two boards). These dates are consistent across Docks 1–7, including Dock 4 manufactured in 2007. They therefore represent **PCB design revision dates** — the date the board layout was finalised — rather than manufacture dates. Every unit was built from the same unrevised Gerber files throughout the entire production run.

---

## Serial number analysis and pairing methodology

### Dock serial number format

Dock serial numbers follow the same Logitech Y+WW date-encoding scheme established for mice in [`mx1000-serial-number-decoding.md`](mx1000-serial-number-decoding.md). Two serial formats appear across the collection:

**Long format (11-character S/N):** `LZ + [letter] + [Y] + [WW] + [NNNNN]`, where Y is the last digit of the manufacture year and WW is the ISO week number. Docks 1 and 3 use this format. The LNA-prefixed Docks 2 and 5 also follow this structure with LNA substituted for the usual LZ + letter header (see below).

**Short format (7-character PID/S/N):** `LZ + [Y] + [WW] + [XX]`, omitting the 5-digit production sequence and replacing it with a 2-character alphanumeric code. Docks 4, 6, and 7 use this format. This is the same short PID structure observed on later MX1000 mouse units (Mice 5, 6, and 7).

All seven dock serials decode consistently with the known MX1000 production window (2004–2007) and no decode produces an implausible date. The methodology and cross-product validation underpinning this decode are documented fully in [`mx1000-serial-number-decoding.md`](mx1000-serial-number-decoding.md).

### The LNA prefix

Two docks in the collection carry an **LNA** serial prefix rather than the standard **LZ** prefix: Dock 2 (LNA50713319) and Dock 5 (LNA45100135). A third LNA-prefixed dock — LNA50505952 on a C-BN34 or C-BO34 unit — was identified in a 2014 customer support thread during research,[^4] establishing that LNA is not unique to this collection. All three known LNA serials belong to MX1000-family charging docks; no LNA-prefixed mouse serial has been observed.

Decoded, the three known LNA units cluster into a narrow eight-week window:

| Serial      | Decoded date                | Sequence |
| ----------- | --------------------------- | -------- |
| LNA45100135 | Week 51, 2004 (Dec 20–26)   | 00135    |
| LNA50505952 | Week 5, 2005 (Jan 31–Feb 6) | 05952    |
| LNA50713319 | Week 7, 2005 (Feb 14–20)    | 13319    |

The production sequence numbers increase monotonically across all three examples as the decoded dates advance — consistent with a single continuous production run rather than three independent batches. The sequence number on the earliest example (00135) is characteristic of a run's opening days.

The LNA prefix is not documented in any Logitech support publication, FCC filing, or regulatory exhibit. It does not correspond to any Logitech-owned facility by known initials. The weight of available evidence — the eight-week production window, the dock-exclusive product scope, the ~50% outsourcing ratio documented in Logitech's 10-K filings for this period, and the Suzhou plant's capacity expansion in July 2005 — points to **an Asian contract manufacturer (ODM) engaged for a short overflow production run of charging docks during the MX1000's first holiday demand cycle**. Charging cradles are the natural candidate for such overflow work: simpler assemblies than the mouse itself, and readily separable from mouse manufacturing. No specific ODM name has been linked to the LNA code in any accessible source.

The **LNA prefix functions as the full three-character facility/line identifier**, substituting for the LZ + letter combination of the standard format. The Y+WW+sequence date encoding is otherwise identical. The modern Logitech acronym "LNA" (Local Network Access, used in CollabOS video conferencing products from ~2021) is unrelated and should not be conflated with the 2004–2005 serial prefix.

### Pairing rationale for Docks 4–7

Manufacture-date matching between dock and mouse serials was the primary method for assigning Docks 4–7 to their paired mice.

**Dock 7 (LZ603BC → week 3/2006) paired with Mouse 7 (LZ603B4 → week 3/2006).** The two serials share an identical Y+WW field (603), establishing that dock and mouse were produced in the same ISO week. This is the strongest pairing in the lot and is treated as high-confidence.

**Dock 6 (LZ549BC → week 49/2005) paired with Mouse 6 (LZ549B4 → week 49/2005).** Again the Y+WW field matches exactly (549). However, Mouse 5 also carries the PID LZ549B4 and decodes to the same week, so week-matching alone does not distinguish which of the two identically-dated mice this dock originally shipped with. Condition-matching resolved the ambiguity: Dock 6's label is in relatively good condition, and Mouse 6's label and sensor sticker are likewise in good condition. The pairing is provisional but internally consistent.

**Dock 5 (LNA45100135 → week 51/2004) paired with Mouse 5 (LZ549B4 → week 49/2005).** This is the weakest pairing in the collection. The dock predates the mouse by approximately one year, so week-matching gives no positive signal. The assignment is by condition: Dock 5's label is scuffed, and Mouse 5's label and sensor sticker are also heavily scuffed. The dock was almost certainly not Mouse 5's original retail pairing; it may have originally shipped with an earlier mouse now absent from the collection. The assignment reflects physical grouping rather than production-date evidence, and the documentation treats it as provisional accordingly.

**Dock 4 (LZ713B1 → week 13/2007) paired with Mouse 4 (LZC45101572 → week 51/2004).** Dock 4 is assigned by elimination — it is the only remaining unassigned dock for the only remaining unassigned mouse. The dock postdates the mouse by over two years, making an original retail pairing essentially impossible. This dock was almost certainly separated from its original mouse at some point before the lot was acquired.

### Dock 3 serial note

Dock 3's S/N (LZB44150762) is identical to Mouse 3's S/N (LZB44150762). This is not a transcription error — it indicates the dock and mouse were **serialized together as a unit** at the factory, sharing a production sequence number. This is consistent with retail packaging of the dock and mouse as a matched set and provides strong corroborating evidence that both identifiers were applied at final assembly rather than at separate sub-assembly stages.

## Open questions

Whether the **C-BN34 REV A0** label marking on Dock 1 is the only revision ever produced, or whether later units carry higher revision designations, has not been established. The internal wiring variant documented in community sources[^2] suggests at least a silent revision occurred, but no label evidence for a formal REV A1 or later has been observed.

The **FCC exhibit photos** for DZL201758 (the MX1000 mouse filing) and associated receiver documents on fcc.gov and fccid.io may contain label photographs showing dock serial numbers. If any LNA-prefixed serial appears in those exhibits, it would provide a contemporaneous Logitech-internal record of the prefix in context. These exhibits were not successfully retrieved during initial research.

The **total population of LNA-prefixed docks** is unknown. Only three examples have been identified across all sources consulted. Additional eBay listings or community teardown threads showing clear dock label photographs would be the most accessible path to further examples.

No ODM or contract manufacturer name has been linked to the LNA prefix in any publicly accessible source. **Logitech's 10-K filings from this period do not name individual contract manufacturers for consumer peripheral components.**

---

## References

[^1]: fcc.report — FCC ID DZL201758 (M-RAG97 RF Cordless Mouse, Logitech Inc.). <https://fcc.report/FCC-ID/DZL201758>

[^2]: benvallack.com — Easy fix for Logitech MX Revolution not charging (documents both C-BN34 wiring variants). <https://benvallack.com/notebook/easy-fix-for-logitech-mx-revolution-not-charging/>

[^3]: 47 C.F.R. § 15.101(b) (2004). Only receivers operating in the 30–960 MHz range, CB receivers, and radar detectors are subject to equipment authorization under Subpart B; the C-BN34, operating at 27 MHz, falls below the lower bound of that range. <https://www.ecfr.gov/current/title-47/chapter-I/subchapter-A/part-15/subpart-B/section-15.101>

[^4]: JustAnswer — Customer support thread referencing Logitech cordless desktop receiver M/N C-B034, S/N LNA50505952 (2014). <https://www.justanswer.com/computer-hardware/8i4zs-cordless-desktop-receiver-m-n-c-b034-s-n-lna.html>
