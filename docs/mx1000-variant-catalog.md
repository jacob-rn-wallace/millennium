# Every known production variant of the Logitech MX1000

The Logitech MX1000 Laser Cordless Mouse — the world's first consumer laser mouse — shipped in **at least six distinct SKU configurations** across two hardware platforms (27 MHz RF and Bluetooth), three documented color finishes (Gunmetal Silver, Onyx Black "Midnight", and a Dark Blue bundle variant), and multiple regional part numbers. Logitech's own 2004 press release confirmed two color options at launch, though the Midnight variant was distributed primarily in Europe and has been largely forgotten. This catalog documents every known variant, model number, hardware revision, and bundle configuration from FCC filings, Icecat product data, archived press releases, retail listings, teardown documentation, and community reports.

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

**Gunmetal Silver (SKU 931175-xxxx)** is the widely known standard version. The Gadgeteer's 2004 review described the top shell as a **"sparkly gunmetal bluish color"** with black rubberized side grips.[^9] Newegg US listings described it as "Blue/Black" or "2-Tone."[^10] This version was sold worldwide.

**Onyx Black "Midnight" (SKU 931272-0914 and possibly others)** is the variant that corresponds to the reported "glossy dark gray" version. The Icecat product database lists it as a distinct product entry (Icecat ID 120366) under the full title **"Logitech MX1000 Laser Midnight Cordless Mouse."**[^11] It carried a separate European SKU (931272-0914) distinct from the standard European SKU (931175-0914),[^12] and the only North American retail SKU identified so far is 931272-0403, though this has not yet been confirmed. The hardware label part number **852152-1000** appears to be the consistent identifier for the Midnight variant, observed on units sold in both Europe and North America — distinguishing it from the Gunmetal Silver's -0000, -0100, and -0300 suffixes. This makes 852152-1000 a color variant identifier rather than a regional one. A 2006 Apple Community discussion documented the Midnight as sold by Italian (eprice.it) and French (cdiscount.com, multe-pass.com) retailers at roughly €10 less than the standard Gunmetal Silver.[^13] The same discussion observed that "related pictures look much alike, although they seem to have a different grip, smooth or rough," suggesting the Onyx Black finish may have had a smoother or glossier surface texture compared to the standard's sparkly metallic finish. The Icecat database listed both variants' color as simply "Black," and notably no EAN/GTIN barcode was recorded for the Midnight variant (the standard's EAN is 5099206968493).[^11] [^12] The Midnight accumulated 42,115 product views on Icecat versus 141,162 for the standard, suggesting lower overall production or distribution volume, though not necessarily regional restriction.

**Dark Blue bundle variant (part number 852376-0000)** was produced exclusively for the Cordless Desktop MX 3100 bundle. Contemporary reviewers consistently described this variant as a distinctly darker, more saturated blue than the standard Gunmetal Silver, with one reviewer explicitly noting the bundle's color was "nicer than the dark green on the MX1000" — directly distinguishing the two.[^25] An AnandTech forum user who owned the MX 3100 bundle described the color in person as "very dark blue or even black in the lighting in my room," while another noted they preferred "the metallic grey color to blue of the MX3100 desktop."[^26] The part number 852376-0000 has not been observed on any standalone retail unit and appears to be exclusive to this bundle. No official Logitech color name for this finish has been identified.

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
| **852152-0100** | M-RAG97 (RF) | Gunmetal Silver — variant; relationship to -0000 unclear |
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

## Hardware revisions across the production run

### Mouse PCB revisions

Physical inspection of the Millennium project's three RF specimens has confirmed that the MX1000 RF mouse (M-RAG97) shipped in **at least two distinct PCB revisions**, both marked on the mainboard itself. All three specimens share the mainboard part number **P/N 201758-0000** — the same identifier used in the FCC filing DZL201758, confirming Logitech used a unified numbering system across internal part numbers and regulatory submissions.

| PCB Revision | Serial prefix | Confirmed specimen | Manufacture date |
|-------------|--------------|-------------------|-----------------|
| **Rev. A** | LZB | Mouse 3 (852152-1000, Midnight Black) | Week 41, 2004 (Oct 4–10) |
| **Rev. B** | LZC | Mouse 1 (852152-0200, Gunmetal Silver) | Week 14, 2005 (Apr 4–10) |

Mouse 2 (852376-0000, Dark Blue, LZB prefix) has not yet been inspected at time of writing; its LZB serial prefix predicts Rev. A by analogy with Mouse 3. The PCBs across all three specimens are otherwise **component-for-component identical** on visual inspection — the revision marking is the only observed difference. Component-level differences, if any, have not yet been determined. For the full serial number decoding methodology and production timeline analysis, see [`mx1000-serial-number-decoding.md`](mx1000-serial-number-decoding.md).

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
| **Week 41, 2004 (Oct 4–10)** | Mouse 3 (LZB44150762, 852152-1000, Midnight Black, PCB Rev. A) manufactured — earliest confirmed specimen in Millennium project collection |
| **Early 2005** | Cordless Desktop MX 3100 announced at CeBIT; includes MX1000 RF mouse in dark blue variant (852376-0000)[^25] |
| **Week 7, 2005 (Feb 14–20)** | Mouse 2 (LZB50753012, 852376-0000, Dark Blue) manufactured — PCB revision unconfirmed pending inspection |
| **Week 14, 2005 (Apr 4–10)** | Mouse 1 (LZC51411902, 852152-0200, Gunmetal Silver, PCB Rev. B) manufactured — boxed retail unit with SetPoint 2.14b and documentation Rev. 1.5 |
| **August 16, 2005** | Logitech announces Cordless Desktop MX 5000 Laser (with BT MX1000)[^19] |
| **September 26, 2005** | FCC certification filed for M-RBA97 Bluetooth mouse (DZL201945)[^2] |
| **Late 2005** | MX 5000 bundle ships; BT MX1000 enters market |
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

This catalog identifies **two hardware platforms** (M-RAG97 RF and M-RBA97 Bluetooth), **three color finishes** (Gunmetal Silver standard, Onyx Black "Midnight" with part number 852152-1000, and Dark Blue bundle variant with part number 852376-0000), **at least three regional SKU variants** for the standard RF version (US, Continental Europe, UK), **three confirmed bundles** (one RF, two Bluetooth), and **two confirmed PCB hardware revisions** (Rev. A on LZB-prefix units, Rev. B on LZC-prefix units) with evidence of additional silent revisions to the dock across the production run.

**PCB-level documentation** has been partially addressed by physical inspection of the Millennium project's three specimens, which confirmed the existence of Rev. A and Rev. B PCB designations and their correlation with LZB and LZC serial prefixes respectively. All three boards share part number P/N 201758-0000. Component-level differences between Rev. A and Rev. B have not yet been determined — both are visually identical on inspection, and the functional difference (the laser latency fix) may have been entirely a firmware change rather than a component change. Mouse 2 (Dark Blue, LZB prefix) has not yet been inspected. For the full serial number and hardware revision analysis, see [`mx1000-serial-number-decoding.md`](mx1000-serial-number-decoding.md).

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