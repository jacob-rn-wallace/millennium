# Every known production variant of the Logitech MX1000

The Logitech MX1000 Laser Cordless Mouse — the world's first consumer laser mouse — shipped in **at least five distinct SKU configurations** across two hardware platforms (27 MHz RF and Bluetooth), two documented color finishes (Gunmetal Silver and Onyx Black "Midnight"), and multiple regional part numbers. Logitech's own 2004 press release confirmed two color options at launch, though the Midnight variant was distributed primarily in Europe and has been largely forgotten. This catalog documents every known variant, model number, hardware revision, and bundle configuration from FCC filings, Icecat product data, archived press releases, retail listings, teardown documentation, and community reports.

---

## Two hardware platforms: RF and Bluetooth

The MX1000 existed as two fundamentally different wireless devices sharing an identical ergonomic shell.

**M-RAG97 — Standard 27 MHz RF version.** This was the standalone retail product, using Logitech's proprietary Fast RF protocol in the 27 MHz band. FCC ID **DZL201758**, filed August 10, 2004, tested by TÜV Rheinland Nederland. The C-BN34 base station served a dual role as both the RF receiver (connected to the PC via USB or PS/2) and the charging cradle. Power output was 1 mW max. The USB device ID was **VID 046D / PID C50E**.

**M-RBA97 — Bluetooth 2.0 EDR version.** FCC ID **DZL201945**, filed September 26, 2005, with an updated filing on July 11, 2006 (suggesting a hardware revision between the two submissions — both filings include separate sets of internal and external photographs). This variant used **Bluetooth Class 2** at 2.4 GHz with +4 dBm max power and a theoretical range of 10 meters. The Bluetooth version was **never sold as a standalone product**. Logitech's own support page explicitly states: "The MX 1000 Mouse (stand-alone) does not communicate using the Bluetooth protocol." It shipped exclusively in two bundles and used a separate **C-UV35** USB Bluetooth dongle (FCC ID DZL201986) rather than the integrated dock receiver. The dock still charged the mouse but had no wireless function. The Bluetooth USB device ID was **VID 046D / PID C70E** (via dongle) or **VID 046D / PID B003** (BT HID profile direct).

Both variants received Brazilian ANATEL certification: **00495-06-02347** (M-RAG97) and **00729-06-02347** (M-RBA97), both listing **Suzhou Logitech Electronics Co., Ltd.** as the manufacturer.

### External differences between RF and Bluetooth

The two platforms are visually distinguishable by exactly two external features. The Connect/Reset button on the underside of the M-RBA97 is **red**; on the M-RAG97 it is **black**. The M-RBA97 also carries a **Bluetooth logo** printed on the top shell, absent on the RF version. In all other respects — shell shape, dimensions (**80.9 × 126 × 46 mm**), weight (~**170–171 g**), button layout, scroll wheel, rubberized grips, and battery indicator — the two are externally identical.

Internally, the wireless radio module is entirely different (27 MHz vs. Bluetooth 2.0 EDR), but both use the same **Agilent ADNS-6000** LaserStream sensor at **800 CPI** and the same **L-LB2** lithium-ion battery (3.7V nominal, ~1700–1800 mAh, part numbers 190247-1000, 190247-0000, 190247-B000, NTA2253).

---

## Two color finishes: Gunmetal Silver and Onyx Black "Midnight"

The Logitech press release of September 1, 2004 (reproduced by Macworld, Phys.org, and NBC News) stated the MX1000 was **"available in two colors: gunmetal silver and onyx black."** Macworld's Peter Cohen specifically described these as "gunmetal silver and onyx black finishes." This fact has been almost entirely forgotten in the enthusiast community.

**Gunmetal Silver (SKU 931175-xxxx)** is the widely known standard version. The Gadgeteer's 2004 review described the top shell as a **"sparkly gunmetal bluish color"** with black rubberized side grips. Newegg US listings described it as "Blue/Black" or "2-Tone." This version was sold worldwide.

**Onyx Black "Midnight" (SKU 931272-0914 and possibly others)** is the variant that corresponds to the reported "glossy dark gray" version. The Icecat product database lists it as a distinct product entry (Icecat ID 120366) under the full title **"Logitech MX1000 Laser Midnight Cordless Mouse."** It carried a separate European SKU (931272-0914) distinct from the standard European SKU (931175-0914), and the only North American retail SKU identified so far is 931272-0403, though this has not yet been confirmed. The hardware label part number **852152-1000** appears to be the consistent identifier for the Midnight variant, observed on units sold in both Europe and North America — distinguishing it from the Gunmetal Silver's -0000, -0100, and -0300 suffixes. This makes 852152-1000 a color variant identifier rather than a regional one. A 2006 Apple Community discussion by user Pietro Fortunato documented the Midnight as sold by Italian (eprice.it) and French (cdiscount.com, multe-pass.com) retailers at roughly €10 less than the standard Gunmetal Silver. He observed that "related pictures look much alike, although they seem to have a different grip, smooth or rough," suggesting the Onyx Black finish may have had a smoother or glossier surface texture compared to the standard's sparkly metallic finish. The Icecat database listed both variants' color as simply "Black," and notably no EAN/GTIN barcode was recorded for the Midnight variant (the standard's EAN is 5099206968493). The Midnight accumulated 42,115 product views on Icecat versus 141,162 for the standard, suggesting lower overall production or distribution volume, though not necessarily regional restriction.

---

## Complete SKU and part number registry

### Retail SKUs (on packaging)

| SKU | Variant | Market | Color |
|-----|---------|--------|-------|
| **931175-0403** | MX1000 RF | US / Americas | Gunmetal Silver ("Blue/Black") |
| **931175-0914** | MX1000 RF | Continental Europe | Gunmetal Silver |
| **931175-0120** | MX1000 RF | United Kingdom | Gunmetal Silver ("Silver/Black") |
| **931272-0914** | MX1000 Midnight RF | Europe (primarily) | Onyx Black |
| **931518-0403** | MX1000 Bluetooth | US (in bundles) | — |
| **852384-1000** | MX1000 Bluetooth | International (in bundles) | "Black & Grey" |

Logitech's suffix convention: **-0403** = US/Americas, **-0914** = Continental Europe, **-0120** = United Kingdom.

### Device part numbers (on hardware labels)

| Part Number | Model | Notes |
|-------------|-------|-------|
| **852152-0000** | M-RAG97 (RF) | Commonly observed on US units |
| **852152-0100** | M-RAG97 (RF) | Variant; seen in lot sales alongside -0000 |
| **852152-0300** | M-RAG97 (RF) | Observed on UK/European units |
|         **852152-1000**        |       M-RAG97 (RF)       |                Onyx Black "Midnight" color variant               |
| **852384-1000** | M-RBA97 (BT) | Bluetooth version |
| **831145-0000** | C-BN34 | Charging dock / RF receiver |
| **832243-0000** | C-UV35 | Bluetooth USB transceiver |
| **190247-1000** | L-LB2 | Battery (also 190247-0000, 190247-B000) |

The multiple 852152 suffixes (-0000, -0100, -0300) across the RF mouse suggest regional or production-run sub-variants on the hardware itself.

### "MX1000L" naming

Some eBay listings and packaging reference an **"MX1000L"** or "MX 1000 L" designation, but these carry the same 931175-0403 SKU as the standard MX1000. No separate Icecat or regulatory entry exists. The "L" almost certainly stands for "Laser" and represents a packaging or branding variation — not a distinct hardware variant.

---

## Regional variants and the Japanese market

Beyond the SKU suffixes documented above, the MX1000 was sold in Japan under Logitech's Japanese brand name **Logicool** as the **"MX-1000"** (with a hyphen). PC Watch (Impress) covered the Japanese launch on September 2, 2004. It carried Amazon.co.jp ASIN **B00061OJCS** and was priced around ¥10,000 (open pricing). It received **39 reviews averaging 4.81/5** on Kakaku.com. No Japan-specific hardware differences have been documented — the product appears to have been the standard M-RAG97 with localized packaging and documentation. No Asia-specific SKU suffixes beyond the Japanese listing have been identified.

---

## Hardware revisions across the production run

### Mouse PCB revisions

Direct evidence of specific PCB revision markings (e.g., "REV A0", "REV B0") has not been publicly documented through community teardowns. However, multiple lines of evidence point to at least one silent hardware revision of the RF version:

**AnandTech forum users** reported that early MX1000 units (purchased at launch in late 2004) suffered a severe **~1 second cursor dead zone** when the mouse was lifted and replaced on a surface, while later purchasers could not reproduce the issue. One user concluded: "I'm betting that there were two different REV models of the MX1000, hence why there's so much confusion and disagreement." The FCC test report for the M-RAG97 is referenced as **AGY-734658-0000.A0** — the ".A0" suffix is consistent with a revision designation scheme.

For the **Bluetooth M-RBA97**, the evidence is stronger: the FCC filing (DZL201945) contains **two distinct sets of internal and external photographs** — the original set from September 2005 and an updated set from July 2006 (referenced as "23868ret101"). This pattern indicates a **Class II Permissive Change**, the FCC's mechanism for documenting hardware modifications to a previously certified device. The 2006 update almost certainly reflects a PCB or component revision.

### The ADNS-6000 sensor's revision architecture

The Agilent **ADNS-6000** sensor used in all MX1000 variants has a built-in **IC revision register** that changes with new silicon revisions, plus a separate **SROM (Shadow ROM) firmware** that is loaded externally by the host microcontroller at boot time. This architecture means Logitech could ship different sensor firmware across production runs **without changing the physical sensor IC** — a plausible mechanism for the tracking improvements observed between early and late units. The sensor's SROM_Load register enables high-speed programming from an external PROM, and the SROM_ID register tracks the downloaded firmware revision. No public record of specific SROM versions shipped in MX1000 production runs exists.

Full ADNS-6000 specifications: **800 CPI**, 30×30 pixel image array, **6,400 frames/second**, 5.8 megapixels/second throughput, 20 inches/second max tracking velocity, 8g max acceleration, SPI serial interface, 18-DIP package. Companion components included the ADNS-6120/6130-001 lens, ADNS-6230-001 clip, and ADNV-6340 VCSEL laser diode (**832–852 nm**, Class 1 eye-safe).

### Charging dock revisions

The C-BN34 dock has at least **two documented internal wiring configurations**. A user on benvallack.com described:

- **Version 1:** Two black cables running straight from the AC adapter input to the charging circuit
- **Version 2:** A small connector/junction joining the two adapter wires before reaching the PCB

The user noted that a contact-cleaning fix worked on the "updated version" but not the original, suggesting the revision addressed **cold solder joints** at the charging contact pads — a widely reported failure mode. The dock label marking **C-BN34 REV A0** is the only documented revision identifier. Whether a "REV A1" or higher exists on later production units remains unconfirmed through public sources but is strongly implied by the wiring change. The dock accepted a **13V DC** external adapter and connected to the host PC via USB (with an included PS/2 adapter).

---

## Bundle configurations that included the MX1000

### Logitech Cordless Desktop MX 5000 Laser

- **SKU:** 967558-0403 (US)
- **MSRP:** ~$199
- **Released:** Late 2005
- **Contents:** MX1000 Bluetooth mouse (M-RBA97) + MX 5000 Bluetooth keyboard with 102×42 pixel LCD display + C-UV35 USB Bluetooth mini-receiver + charging base station + AC adapter + 4 AA batteries + SetPoint and MediaLife software CD + wrist rest
- Pre-paired via Logitech SecureConnect technology

### Logitech diNovo Media Desktop Laser

- **SKU:** 967562-0403 (US)
- **MSRP:** ~$199
- **Released:** 2006
- **Contents:** diNovo Bluetooth keyboard + diNovo MediaPad (remote/numpad with LCD) + MX1000 Bluetooth mouse (M-RBA97) + C-UV35 USB Bluetooth receiver + charging base station + AC adapter + 6 AA batteries + MediaLife software CD
- This was the third generation of the diNovo line (1st gen used MX900 mouse with BT 1.1; 2nd gen "diNovo 2" used BT 1.2; 3rd gen Laser used MX1000 with BT 2.0 EDR)

The Bluetooth MX1000 was **not available outside these two bundle configurations**. Both bundles were succeeded by the MX 5500 Revolution desktop set, which replaced the MX1000 with the MX Revolution Bluetooth mouse around 2008.

### Not a bundle: Cordless Desktop MX 3100 Laser

Sometimes confused with MX1000 bundles, the **MX 3100 Laser** set included the **MX600** laser mouse (AA battery powered, ~6 months battery life), not the MX1000. Mentioned here to prevent misidentification.

---

## Production timeline

| Date | Event |
|------|-------|
| **June 15, 2004** | FCC testing of M-RAG97 completed (test lab: TÜV Rheinland, Netherlands) |
| **August 10, 2004** | FCC certification filed for M-RAG97 (DZL201758) |
| **August 20, 2004** | First Newegg listing appears for 931175-0403 |
| **September 1, 2004** | Logitech officially announces MX1000 — "world's first laser mouse" — in two colors |
| **September 2, 2004** | PC Watch (Japan) covers the launch; Logicool MX-1000 available in Japan |
| **Late September – October 2004** | Retail availability in US and Europe; first reviews published |
| **August 16, 2005** | Logitech announces Cordless Desktop MX 5000 Laser (with BT MX1000) |
| **September 26, 2005** | FCC certification filed for M-RBA97 Bluetooth mouse (DZL201945) |
| **Late 2005** | MX 5000 bundle ships; BT MX1000 enters market |
| **2006** | diNovo Media Desktop Laser ships with BT MX1000 |
| **July 11, 2006** | Updated FCC filing for M-RBA97 with new internal/external photos (hardware revision) |
| **August 24, 2006** | Logitech announces MX Revolution as MX1000 successor ($99.99 MSRP) |
| **Late 2006** | MX1000 effectively discontinued; MX Revolution takes over |
| **~2008** | MX 5000 and diNovo bundles discontinued; succeeded by MX 5500 Revolution |

---

## Complete model and regulatory ID summary

| Component | Model | FCC ID | ANATEL | Key Part Numbers |
|-----------|-------|--------|--------|-----------------|
| Mouse (RF) | M-RAG97 | DZL201758 | 00495-06-02347 | 852152-0000/-0100/-0300/-1000 |
| Mouse (Bluetooth) | M-RBA97 | DZL201945 | 00729-06-02347 | 852384-1000 |
| Dock / RF Receiver | C-BN34 | None (receive-only) | — | 831145-0000 |
| Bluetooth USB Dongle | C-UV35 | DZL201986 | — | 832243-0000; also 830-000003, 830-000021 |
| Battery | L-LB2 | N/A | N/A | 190247-1000 |

The FCC grantee code for all MX1000 filings is **DZL** (Logitech Inc., Newark, CA), not JNZ (Logitech Far East Ltd.). The C-BN34 dock has no FCC ID because receive-only devices operating under Part 15 do not require FCC certification.

## Conclusion: what remains undocumented

This catalog identifies **two hardware platforms** (M-RAG97 RF and M-RBA97 Bluetooth), **two color finishes** (Gunmetal Silver standard and Onyx Black "Midnight"), **at least three regional SKU variants** for the standard RF version (US, Continental Europe, UK), **two confirmed bundles** containing the Bluetooth variant, and evidence of **silent hardware revisions** to both the mouse and dock across the production run.

The most significant gap for hardware preservation is **PCB-level documentation**. The FCC's internal photo PDFs for both DZL201758 (4 parts) and DZL201945 (2 submission rounds) are publicly downloadable and would reveal PCB revision markings, date codes, and component-level differences — but no community member has yet published a comparative analysis. The ADNS-6000's SROM firmware versioning adds another invisible layer of variation that would require reading the sensor's SROM_ID register from live hardware. Finally, the physical differences between the Midnight and standard finishes have never been photographed side-by-side; whether the Onyx Black shell was truly glossy versus the standard's sparkly metallic remains based on a single user's observation of "smooth or rough" grip differences. For a preservation project, acquiring specimens of both the 931175 and 931272 SKUs and performing direct comparison would be the definitive next step.