# Every known production variant of the Logitech MX1000

The Logitech MX1000 Laser Cordless Mouse — the world's first consumer laser mouse — shipped in **at least six distinct SKU configurations** across two hardware platforms (27 MHz RF and Bluetooth), three documented color finishes (Gunmetal Silver, Onyx Black "Midnight", and a Dark Blue bundle variant), and multiple regional part numbers. Logitech's own 2004 press release confirmed two color options at launch, though the Midnight variant was distributed primarily in Europe and has been largely forgotten. This catalog documents every known variant, model number, hardware revision, and bundle configuration from FCC filings, Icecat product data, archived press releases, retail listings, teardown documentation, and community reports.

---

## Millennium project reference specimens

The Millennium project's physical collection includes seven RF variant specimens, referred to throughout this document and in [`mx1000-serial-number-decoding.md`](mx1000-serial-number-decoding.md) by the shorthand **Mouse 1** through **Mouse 7**. Mice 1–3 are numbered in acquisition order; Mice 4–7 are numbered in manufacture order (chronological by decoded serial/PID date). Mouse 3 is the oldest unit in the original trio; Mouse 4 is the earliest confirmed Rev. B specimen in the full collection.

All PCB revision data reflects physical inspection of main, roller, and thumb PCBs. All seven specimens share main board part number **P/N 201758-0000**. The thumb PCB is Rev. A on every specimen examined to date, suggesting it either did not receive a revision or its revision cadence is independent of the main and roller boards.

**PCB transplant convention:** the three PCBs of any given mouse (main, roller, and thumb) are treated as an inseparable unit for both documentation and physical transplant purposes. The main and roller PCBs are effectively inseparable in practice — desoldering them without lifting pads has proven unreliable — and the thumb PCB is kept with them for consistency. Any transplant operation moves all three boards together. When a transplant has occurred, the PCB origin column records which mouse the boards originated from, preserving full traceability of manufacture date, serial/PID, and revision data independently of the chassis they currently occupy.

| Shorthand | Part number | Color | ID | ID type | Main PCB | Roller PCB | Thumb PCB | PCB origin | Manufacture date | Current status |
|-----------|-------------|-------|----|---------|----------|------------|-----------|------------|-----------------|----------------|
| **Mouse 1** | 852152-0200 | Gunmetal Silver | LZC51411902 | S/N | Rev. B | Rev. B | Rev. A | Mouse 5 (LZ549B4, week 49/2005) | Week 14, 2005 (Apr 4–10) | Functional; PCB transplant April 19, 2026 |
| **Mouse 2** | 852376-0000 | Dark Blue (MX 3100 bundle) | LZB50753012 | S/N | Rev. B | Rev. B | Rev. A | Mouse 4 (LZC45101572, week 51/2004) | Week 7, 2005 (Feb 14–20) | Functional; PCB transplant April 19, 2026 |
| **Mouse 3** | 852152-1000 | Midnight Black | LZB44150762 | S/N | Rev. A | Rev. A | Rev. A | Original | Week 41, 2004 (Oct 4–10) | Benched; exhibits laser latency bug |
| **Mouse 4** | 852152-0000 | Gunmetal Silver | LZC45101572 | S/N | Rev. B | Rev. B | Rev. A | Donated to Mouse 2 (April 19, 2026) | Week 51, 2004 (Dec 13–19) | Shell only |
| **Mouse 5** | 852152-0100 | Gunmetal Silver | LZ549B4 | PID | Rev. B | Rev. B | Rev. A | Donated to Mouse 1 (April 19, 2026) | Week 49, 2005 (Dec 5–11) | Shell only; heavily scuffed label and sensor sticker |
| **Mouse 6** | 852152-0100 | Gunmetal Silver | LZ549B4 | PID | Rev. B | Rev. B | Rev. A | Original | Week 49, 2005 (Dec 5–11) | Functional; label and sensor sticker in good condition |
| **Mouse 7** | 852152-0200 | Gunmetal Silver | LZ603B4 | PID | Rev. B | Rev. B | Rev. A | Original | Week 3, 2006 (Jan 16–22) | Functional |

Mice 5 and 6 share an identical PID (LZ549B4) and part number — consistent with PIDs being lot-level identifiers rather than per-unit serials, as documented in [`mx1000-serial-number-decoding.md`](mx1000-serial-number-decoding.md). They are distinguished by physical condition. PCB revision data for Mice 4 and 5 was confirmed prior to transplant and remains in the record; their boards now reside in Mice 2 and 1 respectively.

Mouse 1's dock (C-BN34) carries PCB date code FMa060304, indicating it was manufactured approximately one year before the mouse itself — consistent with charger components being stocked ahead of the mouse launch.

Mouse 2's arrival confirmed its PCB as Rev. B despite its LZB serial prefix — establishing that the LZB/LZC letter boundary does not cleanly track the Rev. A/Rev. B hardware transition. The revision transition occurred partway through the LZB production run. Mouse 3 (LZB, week 41/2004) is Rev. A; Mouse 2 (LZB, week 7/2005) is Rev. B — meaning the transition occurred somewhere between those two manufacture dates. The letter change from LZB to LZC appears to track the part number family or color variant rather than the PCB revision. Mouse 4 (LZC, week 51/2004) is the earliest confirmed Rev. B specimen in the collection, predating Mouse 2 by approximately ten weeks despite carrying a later serial prefix letter. For the full serial number and hardware revision analysis, see [`mx1000-serial-number-decoding.md`](mx1000-serial-number-decoding.md).

On **April 7, 2025**, Mouse 3 arrived and was initially used as a daily driver in preference to Mouse 1 due to more responsive button feel. The batteries of the two units were swapped at this point: Mouse 3 received the HXJNLDC 2100mAh unit originally installed in Mouse 1, and Mouse 1 received Mouse 3's original battery (which had held a charge despite being unreplaced across the unit's life). On **April 8, 2025**, cursor jumping behavior was observed on Mouse 3 during use and both units were benched; the Logitech MX Anywhere 2S was returned to daily driver duty.

The cursor jumping on Mouse 3 is consistent with the laser reactivation latency bug documented in community reports from 2004–2005 and discussed in [`mx1000-serial-number-decoding.md`](mx1000-serial-number-decoding.md). Mouse 3's Rev. A PCB and LZB serial place it squarely in the affected production window.

On **April 19, 2026**, PCB transplants were performed on Mice 1 and 2. Mice 1 and 2 had the best cosmetic condition of the collection but were non-functional: Mouse 1's roller PCB pads had lifted during a desoldering attempt, and Mouse 2 had previously been dissected for documentation. Mice 4–7, acquired subsequently, were in poor cosmetic condition but all functional with batteries capable of holding at least some charge. Since all mice except Mouse 3 share identical PCB revisions, the transplants paired donors by manufacture date proximity: Mouse 4's PCBs (week 51/2004, closest to Mouse 2's week 7/2005) were installed in Mouse 2, and Mouse 5's PCBs (week 49/2005, closest to Mouse 1's week 14/2005) were installed in Mouse 1. Both transplants were successful. Mice 4 and 5 are retained as shells. Mice 6 and 7 remain intact and functional as spares.

---

## Two hardware platforms: RF and Bluetooth

The MX1000 existed as two fundamentally different wireless devices sharing an identical ergonomic shell.

**M-RAG97 — Standard 27 MHz RF version.** This was the standalone retail product, using Logitech's proprietary Fast RF protocol in the 27 MHz band. FCC ID **DZL201758**, filed August 10, 2004, tested by TÜV Rheinland Nederland.[^1] The C-BN34 base station served a dual role as both the RF receiver (connected to the PC via USB or PS/2) and the charging cradle. Power output was 1 mW max. The USB device ID was **VID 046D / PID C50E**.

**M-RBA97 — Bluetooth 2.0 EDR version.** FCC ID **DZL201945**, filed September 26, 2005, with an updated filing on July 11, 2006 (suggesting a hardware revision between the two submissions — both filings include separate sets of internal and external photographs).[^2] This variant used **Bluetooth Class 2** at 2.4 GHz with +4 dBm max power and a theoretical range of 10 meters. The Bluetooth version was **never sold as a standalone product**. Logitech's own support page explicitly states: "The MX 1000 Mouse (stand-alone) does not communicate using the Bluetooth protocol."[^3] It shipped exclusively in two bundles and used a separate **C-UV35** USB Bluetooth dongle (FCC ID DZL201986) rather than the integrated dock receiver. The dock still charged the mouse but had no wireless function. The Bluetooth USB device ID was **VID 046D / PID C70E** (via dongle) or **VID 046D / PID B003** (BT HID profile direct).

Both variants received Brazilian ANATEL certification: **00495-06-02347** (M-RAG97) and **00729-06-02347** (M-RBA97), both listing **Suzhou Logitech Electronics Co., Ltd.** as the manufacturer.[^4]

### External differences between RF and Bluetooth

The two platforms are visually distinguishable by exactly two external features. The Connect/Reset button on the underside of the M-RBA97 is **red**; on the M-RAG97 it is **black**.[^3] The M-RBA97 also carries a **Bluetooth logo** printed on the top shell, absent on the RF version. In all other respects — shell shape, dimensions (**80.9 × 126 × 46 mm**), weight (~**170–171 g**), button layout, scroll wheel, rubberized grips, and battery indicator — the two are externally identical.[^5]

Internally, the wireless radio module is entirely different (27 MHz vs. Bluetooth 2.0 EDR), but both use the same **Agilent ADNS-6000** LaserStream sensor at **800 CPI** and the same **L-LB2** lithium-ion battery (3.7V nominal, ~1700–1800 mAh, part numbers 190247-1000, 190247-0000, 190247-B000, NTA2253).[^6]

---

## Color finishes: Gunmetal Silver, Onyx Black "Midnight", and Dark Blue bundle variant

The Logitech press release of September 1, 2004 stated the MX1000 was **"available in two colors: gunmetal silver and onyx black."**[^7] Macworld's Peter Cohen specifically described these as "gunmetal silver and onyx black finishes."[^8] A third color variant — a darker, more saturated blue — was produced exclusively for the Cordless Desktop MX 3100 bundle.

**Gunmetal Silver (SKU 931175-xxxx)** is the widely known standard version. The Gadgeteer's 2004 review described the top shell as a **"sparkly gunmetal bluish color"** with black rubberized side grips.[^9] Newegg US listings described it as "Blue/Black" or "2-Tone."[^10] The finish is matte metallic, in contrast to the Midnight variant's glossy finish. The scroll wheel assembly surround — the moulded frame around the scroll wheel and its cruise control rocker buttons — is **silver/chrome** on Gunmetal Silver units, so the entire scroll wheel zone reads as one continuous silver element. This is confirmed by promotional imagery and contrasts with the Midnight variant's black surround, which makes the silver rocker buttons read as discrete elements against a dark field. This version was sold worldwide.

**Onyx Black "Midnight" (SKU 931272-0914 and possibly others)** is the darker, glossy variant. The Icecat product database lists it as a distinct product entry (Icecat ID 120366) under the full title **"Logitech MX1000 Laser Midnight Cordless Mouse."**[^11] It carried a separate European SKU (931272-0914) distinct from the standard European SKU (931175-0914),[^12] and the only North American retail SKU identified so far is 931272-0403, though this has not yet been confirmed. The hardware label part number **852152-1000** appears to be the consistent identifier for the Midnight variant, observed on units sold in both Europe and North America — distinguishing it from the Gunmetal Silver's -0000, -0100, and -0300 suffixes. This makes 852152-1000 a color variant identifier rather than a regional one.

Physical inspection of Mouse 3 (852152-1000) confirms the Midnight finish is **glossy**, in contrast to the Gunmetal Silver and Dark Blue variants which use a matte metallic finish. This is consistent across all promotional photography of the Midnight variant. A further distinguishing feature confirmed by physical inspection and promotional imagery is the **scroll wheel assembly surround**: the moulded frame surrounding the scroll wheel and its cruise control rocker buttons is **black** on Midnight units, so the silver rocker buttons read as discrete elements against a dark field. On Gunmetal Silver units the same surround piece is **silver/chrome**, causing the entire scroll wheel zone — frame and rockers — to read as one continuous silver assembly.

A 2006 Apple Community discussion documented the Midnight as sold by Italian (eprice.it) and French (cdiscount.com, multe-pass.com) retailers at roughly €10 less than the standard Gunmetal Silver.[^13] The Icecat database listed both variants' color as simply "Black," and notably no EAN/GTIN barcode was recorded for the Midnight variant (the standard's EAN is 5099206968493).[^11] [^12] The Midnight accumulated 42,115 product views on Icecat versus 141,162 for the standard, suggesting lower overall production or distribution volume, though not necessarily regional restriction.

**Dark Blue bundle variant (part number 852376-0000)** was produced exclusively for the Cordless Desktop MX 3100 bundle. Physical inspection of Mouse 2 confirms the top shell finish is **matte metallic**, identical in character to the Gunmetal Silver finish. The scroll wheel surround moulding is **silver/chrome**, identical to the Gunmetal Silver variant — the Dark Blue and Gunmetal Silver variants are effectively identical in every respect except the top shell color. Contemporary reviewers consistently described this variant as a distinctly darker, more saturated blue than the standard Gunmetal Silver, with one reviewer explicitly noting the bundle's color was "nicer than the dark green on the MX1000" — directly distinguishing the two.[^25] An AnandTech forum user who owned the MX 3100 bundle described the color in person as "very dark blue or even black in the lighting in my room," while another noted they preferred "the metallic grey color to blue of the MX3100 desktop."[^26] The part number 852376-0000 has not been observed on any standalone retail unit and appears to be exclusive to this bundle. No official Logitech color name for this finish has been identified.

---

## Complete SKU and part number registry

### Retail SKUs (on packaging)

| SKU | Variant | Market | Color |
|-----|---------|--------|-------|
| **931175-0403** | MX1000 RF | US / Americas | Gunmetal Silver ("Blue/Black") |
| **931175-0914** | MX1000 RF | Continental Europe | Gunmetal Silver |
| **931175-0120** | MX1000 RF | United Kingdom | Gunmetal Silver ("Silver/Black") |
| **931272-0914** | MX1000 Midnight RF | Europe | Onyx Black |
| **931518-0403** | MX1000 Bluetooth | US (in bundles) | — |
| **852384-1000** | MX1000 Bluetooth | International (in bundles) | "Black & Grey" |

Logitech's suffix convention: **-0403** = US/Americas, **-0914** = Continental Europe, **-0120** = United Kingdom.

### Device part numbers (on hardware labels)

| Part Number | Model | Notes |
|-------------|-------|-------|
| **852152-0000** | M-RAG97 (RF) | Gunmetal Silver — commonly observed on US units |
| **852152-0100** | M-RAG97 (RF) | Gunmetal Silver — two confirmed specimens (Mice 5 and 6); regional assignment not established |
| **852152-0300** | M-RAG97 (RF) | Gunmetal Silver — observed on UK/European units |
| **852152-1000** | M-RAG97 (RF) | Onyx Black "Midnight" — observed on units sold in both North America and Europe |
| **852376-0000** | M-RAG97 (RF) | Dark Blue — MX 3100 bundle variant; not observed in standalone retail |
| **852384-1000** | M-RBA97 (BT) | Bluetooth version |
| **831145-0000** | C-BN34 | Charging dock / RF receiver |
| **832243-0000** | C-UV35 | Bluetooth USB transceiver |
| **190247-1000** | L-LB2 | Battery (also 190247-0000, 190247-B000) |

The multiple 852152 suffixes (-0000, -0100, -0300) across the RF mouse suggest regional or production-run sub-variants on the hardware itself.

### "MX1000L" naming

Some eBay listings and packaging reference an **"MX1000L"** or "MX 1000 L" designation, but these carry the same 931175-0403 SKU as the standard MX1000.[^14] No separate Icecat or regulatory entry exists. The "L" almost certainly stands for "Laser" and represents a packaging or branding variation — not a distinct hardware variant.

---

## Regional variants and the Japanese market

Beyond the SKU suffixes documented above, the MX1000 was sold in Japan under Logitech's Japanese brand name **Logicool** as the **"MX-1000"** (with a hyphen). No Japan-specific hardware differences have been documented — the product appears to have been the standard M-RAG97 with localized packaging and documentation. No Asia-specific SKU suffixes beyond the Japanese listing have been identified.

---

## Retail packaging revision

The MX1000 retail box underwent at least one documented design revision during the production run. Early boxes had a **plastic window on the back panel** through which the underside of the mouse — including the hardware label and serial number — was visible. This was a deliberate design choice consistent with Logitech's practice on the MX700 and other contemporary products, allowing customers to inspect the unit before purchase.[^27] [^28]

A January 2005 HardForum thread documents the transition directly. A user purchasing an MX1000 at Best Buy found that **the new box design prevented seeing the serial number**, and specifically drove to Sam's Club to find the old box design where the underside remained visible — in order to verify the serial prefix before buying.[^27] Sam's Club was simultaneously stocking both box designs at that point, with one LZB unit remaining and eight LZC units behind it on the shelf.

The packaging revision therefore occurred sometime between the product's launch in late 2004 and January 2005, consistent with the LZB-to-LZC hardware transition window. The Millennium project's **Mouse 1 (LZC, April 2005)** box lacks the window, confirming that later production units shipped in the revised packaging. Whether the packaging change and the hardware revision were coordinated or coincidental is not established by available evidence.

The early windowed box was also noted in contemporary reviews: the Phoronix review of the MX1000 and MX518 described both boxes as having the mice "easily seen through the plastic portion of the packaging."[^28]

---

## Hardware revisions across the production run

### Mouse PCB revisions

Physical inspection of the Millennium project's seven RF specimens has confirmed that the MX1000 RF mouse (M-RAG97) shipped in **at least two distinct PCB revisions**, both marked on the mainboard itself. All specimens share the mainboard part number **P/N 201758-0000** — the same identifier used in the FCC filing DZL201758, confirming Logitech used a unified numbering system across internal part numbers and regulatory submissions.

| PCB Revision | Serial/PID | Confirmed specimens | Manufacture date(s) |
|-------------|------------|---------------------|---------------------|
| **Rev. A** | LZB (S/N) | Mouse 3 (852152-1000, Midnight Black) | Week 41, 2004 (Oct 4–10) |
| **Rev. B** | LZB, LZC (S/N); LZ549B4, LZ603B4 (PID) | Mouse 2 (852376-0000, Dark Blue, LZB); Mouse 4 (852152-0000, LZC); Mouse 1 (852152-0200, LZC); Mice 5 & 6 (852152-0100, PID); Mouse 7 (852152-0200, PID) | Week 7, 2005 through week 3, 2006 |

The thumb PCB is **Rev. A on every specimen where it has been inspected** (Mice 4, 5, 6, and 7). It has not yet been inspected on Mice 1, 2, or 3. Whether the thumb PCB received any revision during the production run is unknown.

Mouse 2's confirmed Rev. B PCB despite its LZB serial prefix establishes that the LZB/LZC letter boundary does **not** cleanly correspond to the Rev. A/Rev. B hardware transition. The transition occurred partway through the LZB production run — Mouse 3 (LZB, week 41/2004) is Rev. A while Mouse 2 (LZB, week 7/2005) is Rev. B, placing the transition window between October 2004 and February 2005. Mouse 4 (LZC, week 51/2004) is the earliest confirmed Rev. B specimen and predates Mouse 2 by approximately ten weeks. The letter change from LZB to LZC appears to track the part number family (852152 vs. 852376) or color variant rather than the PCB revision. The PCBs across all specimens are otherwise **component-for-component identical** on visual inspection. Component-level differences between Rev. A and Rev. B have not yet been determined. For the full serial number and hardware revision analysis, see [`mx1000-serial-number-decoding.md`](mx1000-serial-number-decoding.md).

AnandTech forum users reported that early MX1000 units (purchased at launch in late 2004) suffered a severe **~1 second cursor dead zone** when the mouse was lifted and replaced on a surface, while later purchasers could not reproduce the issue.[^15] One user concluded: "I'm betting that there were two different REV models of the MX1000, hence why there's so much confusion and disagreement." The serial number evidence now confirms this intuition was correct — the Rev. A / Rev. B split aligns with the latency bug reports, with LZC/Rev. B units consistently associated with the fix. The FCC test report for the M-RAG97 is referenced as **AGY-734658-0000.A0** — the ".A0" suffix is consistent with the Rev. A designation observed on early production boards.[^1]

For the **Bluetooth M-RBA97**, the evidence is stronger: the FCC filing (DZL201945) contains **two distinct sets of internal and external photographs** — the original set from September 2005 and an updated set from July 2006.[^2] This pattern indicates a **Class II Permissive Change**, the FCC's mechanism for documenting hardware modifications to a previously certified device. The 2006 update almost certainly reflects a PCB or component revision.

### The ADNS-6000 sensor's revision architecture

The Agilent **ADNS-6000** sensor used in all MX1000 variants has a built-in **IC revision register** that changes with new silicon revisions, plus a separate **SROM (Shadow ROM) firmware** that is loaded externally by the host microcontroller at boot time.[^16] This architecture means Logitech could ship different sensor firmware across production runs **without changing the physical sensor IC** — a plausible mechanism for the tracking improvements observed between early and late units. No public record of specific SROM versions shipped in MX1000 production runs exists.

Full ADNS-6000 specifications: **800 CPI**, 30×30 pixel image array, **6,400 frames/second**, 5.8 megapixels/second throughput, 20 inches/second max tracking velocity, 8g max acceleration, SPI serial interface, 18-DIP package. Companion components included the ADNS-6120/6130-001 lens, ADNS-6230-001 clip, and ADNV-6340 VCSEL laser diode (**832–852 nm**, Class 1 eye-safe).[^16]

### Charging dock revisions

The C-BN34 dock has at least **two documented internal wiring configurations**.[^17] A user described:

- **Version 1:** Two black cables running straight from the AC adapter input to the charging circuit
- **Version 2:** A small connector/junction joining the two adapter wires before reaching the PCB

The user noted that a contact-cleaning fix worked on the "updated version" but not the original, suggesting the revision addressed **cold solder joints** at the charging contact pads — a widely reported failure mode. The dock label marking **C-BN34 REV A0** is the only documented revision identifier (confirmed by physical inspection of the boxed reference unit in the Millennium project collection). Whether a "REV A1" or higher exists on later production units remains unconfirmed through public sources. The dock accepted a **13V DC** external adapter and connected to the host PC via USB (with an included PS/2 adapter).[^18]

---

## Bundle configurations that included the MX1000

### Logitech Cordless Desktop MX 3100

- **SKU:** unconfirmed
- **MSRP:** ~$120
- **Released:** Early 2005[^25] [^26]
- **Contents:** MX1000 RF mouse (M-RAG97, 852376-0000) + MX 3000 wireless keyboard + C-BN34 charging dock / RF receiver + AC adapter + 2 AA batteries (for keyboard) + software CD
- Uses Logitech proprietary 2.4GHz Fast RF wireless, not Bluetooth
- Mouse color is a distinctly darker blue than the standalone Gunmetal Silver variant; pre-paired with keyboard at factory
- The dock serves as both RF receiver and charging cradle, as in the standalone MX1000

### Logitech Cordless Desktop MX 5000 Laser

- **SKU:** 967558-0403 (US)
- **MSRP:** ~$199
- **Released:** Late 2005[^19]
- **Contents:** MX1000 Bluetooth mouse (M-RBA97) + MX 5000 Bluetooth keyboard with 102×42 pixel LCD display + C-UV35 USB Bluetooth mini-receiver + charging base station + AC adapter + 4 AA batteries + SetPoint and MediaLife software CD + wrist rest
- Pre-paired via Logitech SecureConnect technology

### Logitech diNovo Media Desktop Laser

- **SKU:** 967562-0403 (US)
- **MSRP:** ~$199
- **Released:** 2006[^20]
- **Contents:** diNovo Bluetooth keyboard + diNovo MediaPad (remote/numpad with LCD) + MX1000 Bluetooth mouse (M-RBA97) + C-UV35 USB Bluetooth receiver + charging base station + AC adapter + 6 AA batteries + MediaLife software CD
- This was the third generation of the diNovo line (1st gen used MX900 mouse with BT 1.1; 2nd gen "diNovo 2" used BT 1.2; 3rd gen Laser used MX1000 with BT 2.0 EDR)

The Bluetooth MX1000 was **not available outside the MX 5000 and diNovo bundle configurations**.[^3] Both bundles were succeeded by the MX 5500 Revolution desktop set, which replaced the MX1000 with the MX Revolution Bluetooth mouse around 2008.[^21]

---

## Production timeline

| Date | Event |
|------|-------|
| **June 15, 2004** | FCC testing of M-RAG97 completed (test lab: TÜV Rheinland, Netherlands)[^1] |
| **August 10, 2004** | FCC certification filed for M-RAG97 (DZL201758)[^1] |
| **August 20, 2004** | First Newegg listing appears for 931175-0403[^10] |
| **September 1, 2004** | Logitech officially announces MX1000 — "world's first laser mouse" — in two colors[^7] |
| **Late September – October 2004** | Retail availability; first reviews published[^9] [^23] |
| **Week 41, 2004 (Oct 4–10)** | Mouse 3 (LZB44150762, 852152-1000, Midnight Black, PCB Rev. A) manufactured — earliest known production specimen in Millennium project collection |
| **Week 51, 2004 (Dec 13–19)** | Mouse 4 (LZC45101572, 852152-0000, Gunmetal Silver, PCB Rev. B) manufactured — earliest confirmed Rev. B specimen in collection |
| **Early 2005** | Cordless Desktop MX 3100 announced at CeBIT; includes MX1000 RF mouse in dark blue variant (852376-0000)[^25] |
| **Week 7, 2005 (Feb 14–20)** | Mouse 2 (LZB50753012, 852376-0000, Dark Blue, PCB **Rev. B**) manufactured — establishes that LZB serial prefix does not exclusively correspond to Rev. A hardware |
| **Week 14, 2005 (Apr 4–10)** | Mouse 1 (LZC51411902, 852152-0200, Gunmetal Silver, PCB Rev. B) manufactured — boxed retail unit with SetPoint 2.14b and documentation Rev. 1.5 |
| **August 16, 2005** | Logitech announces Cordless Desktop MX 5000 Laser (with BT MX1000)[^19] |
| **September 26, 2005** | FCC certification filed for M-RBA97 Bluetooth mouse (DZL201945)[^2] |
| **Week 49, 2005 (Dec 5–11)** | Mice 5 & 6 (PID LZ549B4, 852152-0100, Gunmetal Silver, PCB Rev. B) manufactured — identical PIDs confirm lot-level identifier system |
| **Late 2005** | MX 5000 bundle ships; BT MX1000 enters market |
| **Week 3, 2006 (Jan 16–22)** | Mouse 7 (PID LZ603B4, 852152-0200, Gunmetal Silver, PCB Rev. B) manufactured |
| **2006** | diNovo Media Desktop Laser ships with BT MX1000[^20] |
| **July 11, 2006** | Updated FCC filing for M-RBA97 with new internal/external photos (hardware revision)[^2] |
| **August 24, 2006** | Logitech announces MX Revolution as MX1000 successor ($99.99 MSRP)[^24] |
| **Late 2006** | MX1000 effectively discontinued; MX Revolution takes over |
| **~2008** | MX 5000 and diNovo bundles discontinued; succeeded by MX 5500 Revolution[^21] |

---

## Complete model and regulatory ID summary

| Component | Model | FCC ID | ANATEL | Key Part Numbers |
|-----------|-------|--------|--------|-----------------|
| Mouse (RF) | M-RAG97 | DZL201758 | 00495-06-02347 | 852152-0000/-0100/-0300/-1000; 852376-0000 |
| Mouse (Bluetooth) | M-RBA97 | DZL201945 | 00729-06-02347 | 852384-1000 |
| Dock / RF Receiver | C-BN34 | None (receive-only) | — | 831145-0000 |
| Bluetooth USB Dongle | C-UV35 | DZL201986 | — | 832243-0000 |
| Battery | L-LB2 | N/A | N/A | 190247-1000 |

The FCC grantee code for all MX1000 filings is **DZL** (Logitech Inc., Newark, CA), not JNZ (Logitech Far East Ltd.). The C-BN34 dock has no FCC ID because receive-only devices operating under Part 15 do not require FCC certification.

---

## What remains undocumented

This catalog identifies **two hardware platforms** (M-RAG97 RF and M-RBA97 Bluetooth), **three color finishes** (Gunmetal Silver standard, Onyx Black "Midnight" with part number 852152-1000, and Dark Blue bundle variant with part number 852376-0000), **at least three regional SKU variants** for the standard RF version (US, Continental Europe, UK), **three confirmed bundles** (one RF, two Bluetooth), and **two confirmed PCB hardware revisions** (Rev. A on LZB-prefix units manufactured through at least week 41/2004, Rev. B confirmed from week 51/2004 onward) with evidence of additional silent revisions to the dock across the production run. The regional assignment of part number **852152-0100** (two confirmed specimens, Mice 5 and 6) has not been established by any source consulted.

**PCB-level documentation** has been partially addressed by physical inspection of the Millennium project's seven specimens. The thumb PCB has been confirmed as Rev. A on Mice 4–7; it has not yet been inspected on Mice 1, 2, or 3, and it is unknown whether the thumb PCB ever received a revision at all. Component-level differences between Rev. A and Rev. B main boards have not yet been determined — both are visually identical on inspection, and the functional difference (the laser latency fix) may have been entirely a firmware change rather than a component change. For the full serial number and hardware revision analysis, see [`mx1000-serial-number-decoding.md`](mx1000-serial-number-decoding.md).

The FCC's internal photo PDFs for both DZL201758 (4 parts) and DZL201945 (2 submission rounds) are publicly downloadable and reveal PCB layout and component-level details, though no comparative analysis between RF and Bluetooth variants has been published. The ADNS-6000's SROM firmware versioning adds another invisible layer of variation that would require reading the sensor's SROM_ID register from live hardware. The physical differences between the Midnight and standard finishes have never been photographed side-by-side; whether the Onyx Black shell was truly glossy versus the standard's sparkly metallic remains based on a single user's observation. The MX 3100 bundle mouse (852376-0000) represents a third M-RAG97 color variant whose precise color name has not been confirmed by any Logitech primary source — contemporary reviews describe it as a darker, more saturated blue than the standard finish, but no official color designation has been found. The retail SKU for the MX 3100 bundle has not been confirmed. For a preservation project, performing direct side-by-side comparison of all three color variants and a detailed component-level diff between Rev. A and Rev. B PCBs would be the definitive next steps.

---

## References

[^1]: fcc.report — FCC ID DZL201758 (M-RAG97 RF Cordless Mouse). <https://fcc.report/FCC-ID/DZL201758>
[^2]: fccid.io — FCC ID DZL201945 (M-RBA97 Bluetooth Mouse). <https://fccid.io/DZL201945>
[^3]: Logitech Support — Bluetooth support for my MX 1000. <https://support.logi.com/hc/en-001/articles/360023212594-Bluetooth-support-for-my-MX-1000>
[^4]: fccid.io — DZL201945 Operational Description: General Information. <https://fccid.io/DZL201945/Operational-Description/General-Information-585552>
[^5]: Logitech Support — MX 1000 Technical Specifications. <https://support.logi.com/hc/en-us/articles/360023305394-MX-1000-Technical-Specifications>
[^6]: Amazon — FITHOOD Replacement Battery for LOGITECH M-RAG97 MX1000 (190247-1000, L-LB2). <https://www.amazon.com/Replacement-Battery-LOGITECH-Cordless-190247-1000/dp/B07XRKJVP7>
[^7]: Phys.org — Logitech Unveils the World's First Laser Mouse (September 1, 2004). <https://phys.org/news/2004-09-logitech-unveils-world180s-laser-mouse.html>
[^8]: Macworld — Logitech introduces MX 1000 Laser Cordless Mouse. <https://www.macworld.com/article/172164/mx1000.html>
[^9]: The Gadgeteer — Logitech MX1000 Laser Cordless Mouse Review (October 18, 2004). <https://the-gadgeteer.com/2004/10/18/logitech_mx1000_laser_cordless_mouse_review/>
[^10]: Newegg — Logitech MX1000 931175-0403 Blue/Black Laser Mouse. <https://www.newegg.com/logitech-931175-0403-mx1000/p/N82E16826104158>
[^11]: Icecat — Logitech MX1000 Laser Midnight Cordless Mouse (931272-0914). <https://icecat.biz/us/p/logitech/931272-0914/mice-mx1000+midnight-120366.html>
[^12]: Icecat — Logitech MX1000 mouse RF Wireless Laser (931175-0914). <https://icecat.biz/us/p/logitech/931175-0914/mice-5099206968493-mx1000-120351.html>
[^13]: Apple Community — Logitech MX1000 'midnight' mouse discussion. <https://discussions.apple.com/thread/417077>
[^14]: eBay — Logitech MX1000L Laser Cordless RF Wireless Mouse (931175-0403). <https://www.ebay.com/itm/224564727188>
[^15]: AnandTech Forums — New Logitech MX1000 Review discussion. <https://forums.anandtech.com/threads/new-logitech-mx1000-review.1443895/>
[^16]: Digi-Key — ADNS-6000 Datasheet by Broadcom Limited. <https://www.digikey.com.au/htmldatasheets/production/663849/0/0/1/adns-6000.html>
[^17]: benvallack.com — Easy fix for Logitech MX Revolution not charging (documents both C-BN34 dock wiring variants). <https://benvallack.com/notebook/easy-fix-for-logitech-mx-revolution-not-charging/>
[^18]: Amazon — UpBright 13V AC/DC Adapter for Logitech C-BN34 831145-0000. <https://www.amazon.com/UPBRIGHT-Logitech-831145-0000-8311450000-Cordless/dp/B00GYSAUSY>
[^19]: Logitech IR — Keyboard LCD a Smart Addition to Logitech Cordless Desktop MX 5000 Laser (2005). <https://ir.logitech.com/press-releases/press-release-details/2005/Keyboard-LCD-a-Smart-Addition-to-Logitech-Cordless-Desktop-MX-5000-Laser/default.aspx>
[^20]: Amazon — Logitech diNovo Media Desktop Laser (967562-0403). <https://www.amazon.com/Logitech-diNovo-Media-Desktop-Laser/dp/B000AY0IT4>
[^21]: Hardware Canucks — Logitech MX5500 Revolution review. <https://hardwarecanucks.com/forum/threads/logitech-mx5500-review.21387/>
[^22]: APH Networks — Logitech MX3000 Review (MX3000 bundle uses MX600, not MX1000). <https://aphnetworks.com/reviews/logitech_mx3000>
[^23]: Trusted Reviews — Logitech MX1000 Laser Cordless Mouse Review. <https://www.trustedreviews.com/reviews/logitech-mx1000-laser-cordless-mouse>
[^24]: Logitech News — Logitech Mice Deliver Revolution in Personal Computing Navigation (August 24, 2006). <https://news.logitech.com/press-releases/news-details/2006/Logitech-Mice-Deliver-Revolution-in-Personal-Computing-Navigation-The-Wheel-Reinvented-Revolution-Mice-Speed-Mac-and-PC-Users-Through-Digital-Content-with-Hyper-Fast-Scrolling/default.aspx>
[^25]: ASE Labs — Logitech Cordless Desktop MX3100 preview (documents color distinction from standard MX1000). <http://www.prop.aselabs.com/articles.php?id=172>
[^26]: AnandTech Forums — Logitech Cordless Desktop MX 3100 deal discussion (documents in-person color description). <https://forums.anandtech.com/threads/hot-or-not-logitech-cordless-desktop-mx-3100-w-mx1000-laser-mouse-115-33-shipped-buy-com.1567695/>
[^27]: HardForum — "New version of Logitech MX1000?" thread (January 14–15, 2005); documents box design revision hiding serial number, LZB/LZC color distinction ("bluish hue" vs. "dark charcoal pearlescent"), and LZC lag-free behavior. <https://hardforum.com/threads/new-version-of-logitech-mx1000.854762/>
[^28]: Phoronix — Logitech MX518 and MX1000 review; describes early packaging with plastic window allowing mice to be "easily seen." <https://www.phoronix.com/review/383>