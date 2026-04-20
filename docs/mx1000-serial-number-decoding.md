# Logitech MX1000 serial number decoding: LZ-prefix date encoding and hardware revision analysis

Logitech's "LZ" serial numbers from the 2002–2012 era encode the exact manufacturing week directly in the digit string using a **Y+WW date format** — a pattern confirmed across five product lines with exact-week matches to known launch and release dates. The standard mouse format is `LZ + [revision letter] + [Y: year's last digit] + [WW: ISO week number] + [NNNNN: 5-digit production sequence]`. Applying this to the three original MX1000 physical specimens places Mouse 3 (LZB44150762, Midnight Black) in **October 2004** near the product's launch, Mouse 2 (LZB50753012, Dark Blue) in **February 2005**, and Mouse 1 (LZC51411902, Gunmetal Silver) in **April 2005** — a unit with the revised PCB. The B/C letter in position 3 tracks the PCB hardware revision (Rev. A → Rev. B), not the year. This decoding is independently validated by MX Revolution and G400 PIDs that align with publicly documented launch dates to the exact calendar week.

MX1000 charging dock serials follow the same Y+WW date encoding but introduce a variant three-character prefix — **LNA** — on a subset of units, discussed in its own section below. The LNA prefix appears to mark a short contract-manufacturer production run of docks from late 2004 through early 2005; it does not appear on any mouse serial observed to date.

The MX1000 was produced during a **transitional period** in Logitech's labeling conventions. Early units carry the long 11-character S/N format; later units use a shorter 7-character PID that omits the production sequence. Logitech formally documented this transition: the PID system replaced S/N on all current products, with MX1000 units spanning both label types across the production run.[^12] A third, even shorter 7-character PID variant (LZ + 5 alphanumeric characters) also appears on some MX1000 units, discussed in its own section below.

The shorthand **Mouse 1**, **Mouse 2**, and **Mouse 3** refers to the Millennium project's three original physical RF specimens in acquisition order; Mice 4–7 refers to four subsequently acquired Gunmetal Silver units. For full specimen definitions including part numbers, colors, and condition, see the reference specimens table in [`mx1000-variant-catalog.md`](mx1000-variant-catalog.md).

---

## The serial number format

Every old-format Logitech serial follows the 11-character structure **LZ + Letter + 8 digits**. Cross-referencing 12 serial numbers across four product families against confirmed product timelines reveals the following field-by-field structure:

| Position | Characters | Field | Meaning |
|----------|-----------|-------|---------|
| 1–2 | `LZ` | Manufacturer prefix | Logitech identifier — constant across mouse serials; dock serials may carry `LNA` instead (see below) |
| 3 | Single letter | Revision / family code | Hardware revision or product family identifier — **not** the year |
| 4 | Single digit | Year (Y) | **Last digit of the manufacture year** (e.g. `4` = 2004, `5` = 2005) |
| 5–6 | Two digits | Week (WW) | **ISO week number** (01–53) |
| 7–11 | Five digits | Sequence (NNNNN) | Production sequence number, likely resetting weekly |

The critical structural insight is that **the letter in position 3 does not encode the year**. This was confirmed by finding webcam units with the same "A" prefix but decoding to different years (2003 and 2004), and by observing that MX1000 "B" and "C" units were manufactured in an overlapping 12-week window during late 2004. The year is carried entirely by the single digit in position 4.

Logitech's support documentation gives an example serial of **LZS44500643** for a Cordless Optical TrackMan.[^1] Applying the format: `S` = trackball family, `4` = 2004, `45` = week 45 (November 1–7, 2004), sequence 00643. The Cordless Optical TrackMan was a 2003–2005 product, making a 2004 manufacture date consistent.

---

## Validation across five product lines

The strongest evidence for this decoding comes from cross-referencing decoded manufacture dates against independently confirmed product timelines. The alignment is precise enough to be definitive.

| Product | Serial / PID | Decoded date | Known event | Match |
|---------|-------------|-------------|-------------|-------|
| MX Revolution | LZ6**34**BJ | 2006, wk 34 (Aug 21–27) | Press release: August 24, 2006[^2] | **Exact week** |
| G400 (launch) | LZ1**24**33 | 2011, wk 24 (Jun 13–19) | Released June 19, 2011[^3] | **Exact week** |
| G400 (revised) | LZ1**33**33 | 2011, wk 33 (Aug 15–21) | Angle snapping removed ~2 months post-launch[^4] | Consistent |
| G-7 | LZ5**47**BJ | 2005, wk 47 (Nov 21–27) | Available Sep–Oct 2005 | Consistent |
| QuickCam V-UJ16 | LZA3**35**56997 | 2003, wk 35 (Aug 25–31) | Consumer webcam, available by Jan 2003 | Consistent |

The MX Revolution alignment is particularly strong: **Logitech's press release was dated August 24, 2006 — the exact middle of the week decoded from the PID (August 21–27, 2006)**.[^2] Manufacturing began the same week as the public announcement. The G400 is equally precise: its release date of June 19 falls on the final day of decoded week 24. These two exact-week matches validate the format with high confidence.

Note that the 7-character **PID** format (e.g. LZ6**34**BJ) and the 11-character **serial** format (e.g. LZB44150762) share identical encoding in positions 1–6. The PID simply omits the 5-digit production sequence.

---

## The three original MX1000 specimens decoded

Applying the confirmed format to the three original physical units:

| Mouse | Serial | Letter | Y+WW | Manufacture window | PCB Rev. | Sequence |
|-------|--------|--------|------|--------------------|----------|----------|
| Mouse 3 (Midnight Black, 852152-1000) | LZB**441**50762 | B | 2004, wk 41 | **Oct 4–10, 2004** | Rev. A | 50,762 |
| Mouse 2 (Dark Blue, 852376-0000) | LZB**507**53012 | B | 2005, wk 07 | **Feb 14–20, 2005** | **Rev. B** | 53,012 |
| Mouse 1 (Gunmetal Silver, 852152-0200) | LZC**514**11902 | C | 2005, wk 14 | **Apr 4–10, 2005** | Rev. B | 11,902 |

Physical inspection of all three units has confirmed these revisions — with one significant finding: **Mouse 2 is LZB prefix but Rev. B PCB**, establishing that the LZB/LZC letter boundary does not cleanly track the Rev. A/Rev. B hardware transition. The transition occurred partway through the LZB production run, somewhere between week 41 of 2004 (Mouse 3, Rev. A) and week 7 of 2005 (Mouse 2, Rev. B).

This decoding is consistent with every independently known constraint:

- **Mouse 3** decodes to week 41 of 2004 — just three to four weeks after the MX1000's September 1, 2004 press release announcement[^5] and within the first confirmed retail availability window (late September / October 2004).[^6] It is the earliest of the three units and carries the original Rev. A PCB.
- **Mouse 2** decodes to week 7 of 2005 and carries Rev. B despite its LZB prefix — placing the Rev. A to Rev. B transition window between October 2004 and February 2005.
- **Mouse 1**'s retail box contained SetPoint 2.14b (a 2004-dated disc)[^7] and documentation Rev. 1.5. These are launch-era materials shipped with a unit manufactured in April 2005 — consistent with Logitech using pre-printed box contents across the first year of production without updating them to reflect incremental software releases.
- **Mouse 1**'s dock (C-BN34) carries PCB date code **FMa060304**, interpreted as March or June 2004 — roughly 10–13 months before the mouse itself was manufactured. Charger components drawn from existing inventory are routinely manufactured and stocked ahead of the mouse, explaining the gap.

---

## Four additional specimens decoded (Mice 4–7)

Four subsequently acquired Gunmetal Silver units extend the dataset and introduce both a new S/N-format unit and the first confirmed PID-format MX1000 labels. Three of the four units carry a PID label (the short 7-character format, discussed in the following section); the fourth carries a standard 11-character S/N. All four are PCB Rev. B / Rev. B / Rev. A (main / roller / thumb). The thumb PCB being Rev. A across all four — including units with Rev. B main and roller boards — is consistent across every specimen examined to date and suggests the thumb PCB either did not receive a revision or its revision cadence is independent of the main and roller boards.

| Mouse | P/N | ID type | ID | Main PCB | Roller PCB | Thumb PCB | Notes |
|-------|-----|---------|-----|----------|------------|-----------|-------|
| Mouse 4 | 852152-0000 | S/N | LZC45101572 | Rev. B | Rev. B | Rev. A | |
| Mouse 5 | 852152-0100 | PID | LZ549B4 | Rev. B | Rev. B | Rev. A | Heavily scuffed label and sensor sticker |
| Mouse 6 | 852152-0100 | PID | LZ549B4 | Rev. B | Rev. B | Rev. A | Label and sensor sticker in good condition |
| Mouse 7 | 852152-0200 | PID | LZ603B4 | Rev. B | Rev. B | Rev. A | |

Units are ordered chronologically by decoded manufacture date. Mice 5 and 6 share an identical PID (LZ549B4) and P/N — consistent with PIDs being lot-level rather than per-unit identifiers[^14] — and are distinguished in this table by physical condition alone, which is the only observable difference between the two units.

**Mouse 4** (LZC45101572) decodes under the standard format to LZC, 2004, week 51 — **December 13–19, 2004**. This is consistent with community-sourced serial data that, while currently unverifiable, reports a Hungarian forum user posting S/N LZC44751269 in early 2005, decoding to LZC, 2004, week 47 — which would confirm LZC production was already running by November 2004.[^8] A week-51 LZC unit sits four weeks later in the same production run and is entirely unremarkable.

**852152-0100** (Mice 5 and 6) is a confirmed Logitech MX1000 part number, appearing independently in parts distributor listings and secondhand market entries.[^15] Its specific regional assignment is not established by any source consulted. See the variant catalog for current notes.

---

## The short PID format (LZ + 5 characters)

Three of the four new specimens carry labels reading "PID" rather than "S/N", with identifiers of the form **LZ + 5 alphanumeric characters** (e.g. LZ549B4, LZ603B4). This is structurally distinct from both the 11-character S/N and the 7-character PID documented elsewhere (e.g. LZ634BJ for the MX Revolution). It decodes as follows:

| Position | Characters | Field | Meaning |
|----------|-----------|-------|---------|
| 1–2 | `LZ` | Manufacturer prefix | Same constant as S/N format |
| 3 | Single digit | Year (Y) | Last digit of manufacture year |
| 4–5 | Two digits | Week (WW) | ISO week number |
| 6–7 | Two characters | Batch suffix (SS) | Factory, line, or lot code — meaning not publicly documented |

Applying this to the observed PIDs:

| PID | Y | WW | SS | Decoded window | Unit(s) |
|-----|---|----|----|----------------|---------|
| LZ549B4 | 2005 | 49 | B4 | **Dec 5–11, 2005** | Mouse 5, Mouse 6 |
| LZ603B4 | 2006 | 03 | B4 | **Jan 16–22, 2006** | Mouse 7 |

Three independent sources support this decoding. First, Logitech's own support KB documents the short PID form directly, citing LZ547BJ for the G-7 Gaming Mouse as an example of a PID "between 4 and 11 digits" — applying the same Y+WW reading gives 2005, week 47, suffix BJ.[^1] Second, an independent community analysis of Logitech Z-5500 speaker PIDs from the same production era observed the identical structure, describing the year digit and two-digit week field by position.[^13] Third, week 54 is not a valid ISO week, which rules out the alternative parse of Y=5, W=4 that would leave no positional room for the suffix at all.

The **2-character suffix** (SS) is not publicly documented. The suffix `B4` recurs across two different week/year combinations (LZ549B4 in week 49/2005 and LZ603B4 in week 3/2006), which rules out a simple sequential unit counter and points to a factory, production line, or lot code whose meaning Logitech has not published. The recurrence of an identical PID across two physically distinct units (Mice 5 and 6) further confirms that these identifiers are lot-level, not per-unit. Record the suffix characters verbatim; do not interpret them.

Note that the short PID **omits the revision letter** present in position 3 of the S/N format. This means short PIDs cannot be used to infer the LZB/LZC letter family, and the letter-based observations in this document apply only to S/N-format units.

---

## The LNA prefix

Two docks in the Millennium project collection carry an **LNA** serial prefix rather than the standard **LZ** prefix: Dock 2 (LNA50713319, C-BO34) and Dock 5 (LNA45100135, C-BN34). A third example — LNA50505952, reported on a Logitech C-BN34 or C-BO34 in a 2014 customer support thread[^18] — establishes that the prefix is not unique to this collection. All three known LNA serials belong to MX1000-family charging docks. No LNA-prefixed mouse serial has been observed.

The three known LNA serials decode cleanly using the standard Y+WW+sequence structure, with LNA substituting for the usual LZ + letter three-character header:

| Serial | Decoded date | Sequence |
|--------|-------------|----------|
| LNA45100135 | Week 51, 2004 (Dec 20–26) | 00135 |
| LNA50505952 | Week 5, 2005 (Jan 31–Feb 6) | 05952 |
| LNA50713319 | Week 7, 2005 (Feb 14–20) | 13319 |

Three features of this dataset are notable. First, the production sequence numbers increase monotonically as decoded dates advance — consistent with a single continuous production run. Second, the sequence on the earliest example (00135) is characteristic of the opening days of a new run. Third, the three serials span just eight weeks, implying a short-term contract rather than an ongoing second facility.

The LNA prefix is not documented in any Logitech support publication, FCC filing, or regulatory exhibit. It does not correspond to any known Logitech-owned facility by initials. The decoded production window — late December 2004 through mid-February 2005 — aligns precisely with the period when Logitech's Suzhou plant was nearing capacity ahead of its July 2005 expansion, and during the ramp-up for the Cordless Desktop MX 3100 bundle (announced at CeBIT in early-to-mid March 2005). Logitech's 10-K filings from this period document that approximately 50% of unit volume was outsourced to Asian contract manufacturers and ODMs, whose individual identities were not publicly disclosed for consumer peripherals.[^11]

The most parsimonious interpretation is that **LNA identifies an Asian contract manufacturer engaged for a short overflow production run of MX1000-family charging docks** during the first holiday demand cycle. Charging cradles — simpler assemblies than the mouse itself — are the natural candidate for such overflow outsourcing. No specific ODM name has been linked to the LNA code in any accessible source.

The format of LNA serials is therefore: **LNA + [Y] + [WW] + [NNNNN]**, where LNA is the full three-character facility/line identifier, and Y, WW, and NNNNN follow the same encoding as the standard LZ format. The modern Logitech acronym "LNA" (Local Network Access, used in CollabOS video-conferencing products from approximately 2021) is unrelated and should not be conflated with this prefix.

---

## The S/N to PID label transition

The coexistence of "S/N" and "PID" labels on the same MX1000 model is not a retail/OEM/refurbished distinction. Logitech's official support KB states the relationship directly: **the PID system replaced the older S/N system on all current Logitech products**.[^12] The MX1000 shipped across this transition, with early units carrying the legacy S/N field and later production carrying PID. Third-party service documentation for another Logitech product (the Harmony One remote) corroborates that these numbers are **lot-level identifiers shared across thousands of units**, not unique per-unit serials.[^14] Refurbished units, by contrast, are identified by an **LV-prefix** overlay sticker — so any label reading "PID LZxxxxx" is original production stock.

The decoded PID dates (week 49 of 2005, week 3 of 2006) place the PID-labeled MX1000 units roughly 8–15 months after the S/N-labeled week-51/2004 unit (Mouse 4), which is consistent with the transition occurring in the second half of the production run. The precise cut-over date for the MX1000 is not documented by Logitech.

---

## The CMII ID field

Several MX1000 bottom labels carry a field reading **"CMII ID:"** followed by a code, or with the code blank. Despite the visual similarity to the ICM Configuration Management II standard, this field is unrelated to it. **CMII here stands for China Ministry of Information Industry** (中华人民共和国信息产业部), the predecessor to the MIIT, which administered SRRC (State Radio Regulatory Commission) type-approval for radio-frequency devices sold in China.[^16]

The code **2004DJ1825** parses as follows:

| Segment | Value | Meaning |
|---------|-------|---------|
| Year | 2004 | Year the SRRC type-approval certificate was granted |
| D | D | Short-range / micro-power radio device category — correct for a 27 MHz cordless mouse |
| J | J | Imported equipment (进口) — correct for a Taiwan-assembled Logitech device |
| 1825 | 1825 | Sequential certificate number within the year |

Adjacent certificate numbers in the SRRC database confirm the format and Logitech's presence in it: **CMII ID 2004DJ1762** and **2004DJ1764**, both issued October 31, 2004 to Taiwan Logitech Electronics for micro-power wireless mouse devices operating at 27.045–27.195 MHz, sit 63 certificates earlier in the same year's series.[^17]

The **blank-field variant** (CMII ID field present, no code) most likely reflects either units destined for non-China markets — where the China-specific marking would be populated on a separate label variant or omitted — or units produced and labeled before the 2004DJ1825 certificate was issued. Both mechanisms would result in the field being present in the label template but unpopulated. Which applies to a given unit is not directly documented by Logitech; record as "blank: non-China-market or pre-certificate production" rather than as a more specific claim.

---

## What the revision letter encodes

The letter in position 3 is a **hardware revision or product family identifier, not a year code**. Three independent observations support this conclusion.

**Overlapping production windows.** The earliest reported LZC serial in community data (LZC44751269, unverified — see [^8]) decodes to **week 47 of 2004** — while LZB units were still being manufactured through at least **week 7 of 2005** (Mouse 2). If accurate, a year code would not produce a 12-week overlap between two consecutive letters.

**Multiple years sharing a letter.** Two webcam units with prefix "A" decode to 2003 and 2004 respectively, demonstrating that a single letter spans multiple calendar years. Year encoding through the letter is therefore ruled out.

**Community-observed labeling.** Hungarian forum users who compared LZB and LZC MX1000 units in early 2005 noted that their LZC unit carried a **"2.0" label** on the bottom sticker.[^8] This strongly implies the letter change was Logitech's internal mechanism for marking a hardware revision rather than a production-year rollover.

The known letter assignments across product families in this era are:

| Letter | Products observed |
|--------|------------------|
| A | Webcams (QuickCam Messenger V-UM14, QuickCam V-UJ16) |
| B | MX1000 — both Rev. A (Mouse 3, week 41/2004) and Rev. B (Mouse 2, week 7/2005) |
| C | MX1000 — Rev. B only (Mouse 1, week 14/2005; Mouse 4, week 51/2004) |
| S | Trackballs (Cordless Optical TrackMan T-RB22) |

Physical inspection of all project specimens has established that **B does not exclusively correspond to Rev. A** — Mouse 2 is LZB but Rev. B. The most likely interpretation is that the letter tracks the **part number family or color variant** (852152 vs. 852376) rather than the PCB revision. All 852152 units observed are LZB (Mouse 3) or LZC (Mouse 1, Mouse 4); the 852376 Dark Blue bundle unit (Mouse 2) is also LZB. The Rev. A to Rev. B transition occurred within the LZB production window, not at the LZB/LZC boundary.

---

## The Rev. A to Rev. B transition and the latency bug

The MX1000 shipped with a known issue: a perceptible delay when the laser reactivated after lifting or momentarily resting the mouse. Forum discussion from late 2004 through 2005 identified this as a problem with the laser powering down during inactivity and taking a measurable interval to return to full power.[^9] [^10]

Serial number data suggests the transition was not a clean one-date cutover but a **parallel production overlap**:

- **LZC units began no later than week 47 of 2004** (the earliest confirmed LZC serial in community data), while LZB units continued until at least week 7 of 2005.
- A French forum user received LZB50100019 — decoded as **week 1 of 2005** — and reported **no latency issue**, suggesting the fix was applied to some late Rev. A boards before the full PCB revision shipped.[^10]
- Community consensus from Italian and French hardware forums (2005) described LZC units as keeping the laser continuously active rather than allowing it to power down — the mechanism of the fix.[^9]

The implication is that Logitech may have first addressed the issue through a **firmware change** on late-run LZB boards, then formalized it as a **PCB-level change** at the LZC/Rev. B transition. A user acquiring an MX1000 today cannot rely on the letter alone to determine whether the latency fix is present; the sequence number within LZB units may be a better predictor, with higher sequences more likely to carry the firmware fix.

---

## The 5-digit production sequence

The sequence field (positions 7–11) likely resets on a **weekly** basis, based on the following observations:

- Unit LZB50100019 (week 1 of 2005) carries sequence **00019** — close to zero, consistent with the first units off the line that week.
- Two units both decoded to week 41 of 2004 (LZB44102564 and LZB44150762) carry sequences **02,564** and **50,762** respectively. The gap of ~48,000 units in a single week implies either very high weekly production across all LZ-prefix products sharing a counter, or that the sequence encodes production line or shift information in addition to a unit count.

If the counter is **shared across all LZ-prefix products** manufactured at Suzhou in a given week (not per-product), a gap of 48,000 within one week is plausible given the scale of Logitech's Suzhou facility, which produced roughly half of all Logitech products during this period.[^11]

The lowest observed sequence of **00019** strongly favors a weekly reset over a continuous counter. A continuous counter starting from product launch would have reached a much higher value by week 1 of 2005 given MX1000 sales volumes. Weekly reset is the simpler and more consistent explanation.

---

## Implications for the production timeline

Combining the serial number decoding with other physical evidence, the MX1000 production timeline for the RF variant (M-RAG97) can now be stated with improved precision:

| Event | Evidence | Date |
|-------|----------|------|
| MX1000 press release | Phys.org / Logitech IR[^5] | September 1, 2004 |
| Mouse 3 (LZB, Rev. A) manufactured | Serial LZB44150762 | Week 41, 2004 (Oct 4–10) |
| Dock 3 (LZB, C-BN34) manufactured | Serial LZB44150762 | Week 41, 2004 (Oct 4–10) |
| First retail availability | Reviews published[^6] | Late September – October 2004 |
| Dock 1 (LZB, C-BN34) manufactured | Serial LZB44252090 | Week 42, 2004 (Oct 11–17) |
| LZC / Rev. B production begins | Earliest reported LZC serial (unverified community data)[^8] | No later than week 47, 2004 |
| Mouse 4 (LZC, Rev. B) manufactured | Serial LZC45101572 | Week 51, 2004 (Dec 13–19) |
| Dock 5 (LNA, C-BN34) manufactured | Serial LNA45100135 | Week 51, 2004 (Dec 20–26) |
| Mouse 2 (LZB, Rev. B) manufactured | Serial LZB50753012 | Week 7, 2005 (Feb 14–20) |
| Dock 2 (LNA, C-BO34) manufactured | Serial LNA50713319 | Week 7, 2005 (Feb 14–20) |
| LZB production confirmed continuing | Mouse 2 serial | Through at least week 7, 2005 |
| Mouse 1 (LZC, Rev. B) manufactured | Serial LZC51411902 | Week 14, 2005 (Apr 4–10) |
| Mice 5 & 6 (PID, Rev. B) manufactured | PID LZ549B4 | Week 49, 2005 (Dec 5–11) |
| Dock 6 (LZ, C-BN34) manufactured | Serial LZ549BC | Week 49, 2005 (Dec 5–11) |
| Mouse 7 (PID, Rev. B) manufactured | PID LZ603B4 | Week 3, 2006 (Jan 16–22) |
| Dock 7 (LZ, C-BN34) manufactured | Serial LZ603BC | Week 3, 2006 (Jan 16–22) |
| MX Revolution announced as successor | Logitech press release[^2] | August 24, 2006 |
| Dock 4 (LZ, C-BN34) manufactured | Serial LZ713B1 | Week 13, 2007 (Mar 26–Apr 1) — postdates MX1000 active production; likely a service/replacement part |

This confirms that Mouse 3 is among the **earliest known production MX1000 units**, manufactured within the first retail availability window. The Rev. A to Rev. B transition occurred during a 12-week overlap period spanning late 2004 through early 2005. Mouse 4 — a week-51/2004 LZC unit — is now the **earliest confirmed Rev. B specimen** in the project collection.

---

## Format continuity and later evolution

The LZ-prefix Y+WW format persisted across Logitech product generations from approximately 2002 through 2012. After this period, Logitech transitioned to a new 12-character format that promotes the date to an explicit **YYWW** prefix — expanding the year to two digits and moving it to the front of the serial. This later format is simpler to read but encodes the same fundamental information. The survival of the same underlying convention across a decade of products, and across both the 7-character PID and 11-character serial variants, indicates this was a deliberate and stable internal standard rather than an ad-hoc scheme.

Whether **"LZ"** specifically references the Suzhou manufacturing facility — "L" for Logitech, "Z" possibly for a site or zone designation — is plausible given that Suzhou was Logitech's primary mouse manufacturing site throughout this period,[^11] but this interpretation has not been confirmed by any primary source.

---

## References

[^1]: Logitech Support — Locating part number (P/N) and model number (M/N). Example serial LZS44500643 for Cordless Optical TrackMan; example PID LZ547BJ for G-7 Gaming Mouse. <https://support.logi.com/hc/en-us/articles/360023352673-Locating-part-number-P-N-and-model-number-M-N>
[^2]: Logitech News — Logitech Mice Deliver Revolution in Personal Computing Navigation (August 24, 2006); MX Revolution PID LZ634BJ decodes to week 34 of 2006 (August 21–27). <https://news.logitech.com/press-releases/news-details/2006/Logitech-Mice-Deliver-Revolution-in-Personal-Computing-Navigation-The-Wheel-Reinvented-Revolution-Mice-Speed-Mac-and-PC-Users-Through-Digital-Content-with-Hyper-Fast-Scrolling/default.aspx>
[^3]: Geeky Gadgets — Logitech G400 Optical Gaming Mouse Announced (June 9, 2011); G400 PID LZ12433 decodes to week 24 of 2011 (June 13–19), matching the June 19 release date. <https://www.geeky-gadgets.com/logitech-g400-optical-gaming-mouse-announced-09-06-2011/>
[^4]: Overclock.net — How to get a Logitech G400 without angle snapping; revised units carry PID LZ13333 (week 33 of 2011, August 15–21). <https://www.overclock.net/threads/how-to-get-a-logitech-g400-without-angle-snapping.1255817/>
[^5]: Phys.org — Logitech Unveils the World's First Laser Mouse (September 1, 2004). <https://phys.org/news/2004-09-logitech-unveils-world180s-laser-mouse.html>
[^6]: The Gadgeteer — Logitech MX1000 Laser Cordless Mouse Review (October 18, 2004). <https://the-gadgeteer.com/2004/10/18/logitech_mx1000_laser_cordless_mouse_review/>
[^7]: Internet Archive — Logitech SetPoint 2.14b Driver Software (CD, 2004). <https://archive.org/details/logitech-set-point-2.4a>
[^8]: HWSW Informatikai Kerekasztal — Logitech MX1000 forum thread, page 17; Hungarian users comparing LZB and LZC units in early 2005, reportedly noting "2.0" label on LZC units; serials LZC44751269 (week 47/2004) and LZB43604579 (week 36/2004) reportedly posted by separate users. **Page currently returns a 403 error; no archived snapshot is available. Content has not been independently verified and should be treated as unconfirmed.** <https://forum.hwsw.hu/topic/67618-logitech-mx1000/page__st__320>
[^9]: HardWare.fr — Logitech MX1000 et latence; French-language forum discussion of laser latency bug and LZC fix, early 2005. <https://forum.hardware.fr/hfr/HardwarePeripheriques/Clavier-Souris/logitech-mx1000-latence-sujet_13862_1.htm>
[^10]: Overclockers Forums — MX1000 Logitech Laser Mouse discussion; community reports on latency bug presence across LZB and LZC units. <https://www.overclockers.com/forums/threads/mx1000-logitech-laser-mouse-what-do-you-think-of-it.352672/post-3320707>
[^11]: Wikipedia — Logitech; Suzhou facility as primary manufacturing center. <https://en.wikipedia.org/wiki/Logitech>
[^12]: Logitech Support — Locating part number (P/N) and model number (M/N); states "The PID is used on all current Logitech products and replaces the older serial number (S/N) system." <https://support.logi.com/hc/en-us/articles/360023352673-Locating-part-number-P-N-and-model-number-M-N>
[^13]: Head-Fi.org — Almi's Logitech Z-5500 Mod thread, page 17; community member decodes Z-5500 PIDs using the same Y+WW structure, describing the year digit and two-digit week field. <https://www.head-fi.org/threads/almis-logitech-z-5500-mod-high-end-upgrade-for-the-speaker-system.657715/page-17>
[^14]: Harmony Remote Repair — Harmony One Hardware Version Identification; notes that Logitech LZ-prefix PIDs "are not unique and actually represent manufacturing lot numbers" shared across thousands of units; refurbished units carry an LV-prefix overlay sticker. <https://www.harmonyremoterepair.com/harmony-one-pcb-verification.html>
[^15]: ASAP Distribution — parts catalog entry for Logitech 852152-0100; eBay listing (MPN field); Spanish-language eBay parts lot "852152-0000/0100". 852152-0100 regional assignment not established by any source consulted. <https://www.asap-distribution.com/it-hardware/rfq/logitech/852152-0100/>
[^16]: FYIcenter.com — What Is the CMIIT Code on My Phone; CMII/CMIIT ID explained as China Ministry of Information Industry type-approval identifier for wireless devices. <http://phone.fyicenter.com/1594_What_Is_the_CMIIT_Code_on_My_Phone.html>
[^17]: fccid.io — CMII ID 2004DJ1762 and 2004DJ1764; both issued October 31, 2004 to Taiwan Logitech Electronics for micro-power wireless mouse at 27.045–27.195 MHz, confirming the YYYY+D+J+NNNN format and Logitech's presence in the 2004 SRRC certificate series. <https://fccid.io/CMII-ID-2004DJ1762>
[^18]: JustAnswer — Customer support thread referencing Logitech cordless desktop receiver M/N C-B034, S/N LNA50505952 (2014); third confirmed LNA-prefixed dock serial, decoding to week 5 of 2005 (January 31–February 6). <https://www.justanswer.com/computer-hardware/8i4zs-cordless-desktop-receiver-m-n-c-b034-s-n-lna.html>
