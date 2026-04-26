# Millennium project: development roadmap

This roadmap organizes the Millennium project across four parallel tracks — **Documentation**, **Calibre** (replacement PCB), **Case** (replacement shells), and **Reserve** (dock) — and eight sequential phases. Phases represent meaningful capability gates: work within a phase can proceed in any order, but phase boundaries reflect dependencies that must be resolved before the next phase begins. **Regulator** (host configuration software) development is noted within phases but treated as a running parallel track rather than a gated deliverable, since its development is loosely coupled to hardware until functional firmware exists.

Calibre development follows two named tracks that diverge after Phase 3:

- **Theseus Track** (Phases 1–3) — reproduces and progressively modernizes the original PCB design, beginning with exact reproduction and culminating in a board that preserves original functionality while substituting modern drop-in components. Priority track: directly supports existing hardware.
- **Greenfield Track** (Phases 4–7) — designs new internals from scratch using modern components, working toward full replication of original MX1000 functionality as a firmware profile on new silicon. Largely independent of the Theseus Track; both tracks share Phase 0 as a prerequisite and the Phase 3 gate condition as a dependency.

The two tracks can proceed in parallel once the Phase 3 gate is met, and are suited to different contributor profiles: the Theseus Track is accessible to hardware generalists familiar with the original; the Greenfield Track requires firmware and RF expertise. They converge at the same long-term goal — a fully characterized original design and a fully working modern replacement — and are not in conflict.

The roadmap reflects current project state: Mouse 1 (Gunmetal Silver, Rev. B), Mouse 2 (Dark Blue, Rev. B), and Mouse 3 (Midnight Black, Rev. A) are in hand. No Calibre PCB has been designed. No Case geometry exists. Reserve dock design has not begun.

---

## Phase 0 — Physical characterization

_Gate: complete physical documentation of all hardware before any design work is committed_

This phase is the foundation for everything downstream. Decisions made in Calibre, Case, and Reserve are only as good as the measurements they're based on. Phase 0 work should be committed to the repository as it is completed. Phase 0 feeds both the Theseus and Greenfield tracks.

**Status: in progress**

### Documentation track

- [ ] **External photography** — all units, standardized lighting, all angles; side-by-side color comparison across colorways
- [ ] **Shell measurements** — all external dimensions: length, width, height at multiple points, button surface geometry, grip panel positions, scroll wheel recess, logo placement, foot positions and dimensions
- [ ] **Internal measurements** — PCB dimensions and mounting point positions, battery compartment geometry, charging contact positions and spacing, light pipe geometry, button mechanism travel and actuation positions, scroll wheel encoder dimensions
- [ ] **Mass and inertia** — total mass of all units (with and without battery), center of mass, moment of inertia via trifilar pendulum; document and compare Rev. A and Rev. B
- [ ] **PCB tracing** — trace at minimum one mainboard revision (Rev. B preferred, two specimens available); identify all components, map signal routing for sensor, switches, scroll encoder, battery management, RF module, indicator LEDs; document Rev. A differences if dissection of Mouse 3 is later authorized
- [ ] **Component identification** — identify all ICs and passives; cross-reference with datasheets; document sensor mount geometry relative to shell window; PCB photography and component catalogue already in progress for Mouse 2
- [ ] **Charging contact characterization** — voltage and current profile during a full charge cycle on a known-good unit; contact resistance measurement; pin assignments
- [ ] **Battery connector** — pinout, connector family/pitch, dimensions
- [ ] **Scroll wheel encoder** — type (mechanical vs. optical), dimensions, mounting, detent count per revolution
- [ ] **Switch identification** — measure existing switches (travel, actuation force, dimensions, footprint); identify manufacturer and part number where possible
- [ ] **Light pipe experiment** — powered mouse in darkened room; photograph and document LED propagation through light pipes; assess light bleed at boundaries; informs whether Case requires a redesigned light divider
- [ ] **3D scanning** — obtain foot powder spray; scan shell exterior with CR-Scan Ferret SE; export meshes to repository
- [ ] **Dock characterization** — measure C-BN34 dock dimensions; document charging contact geometry and alignment relative to mouse contacts; confirm power input spec
- [ ] **Optical geometry** — measure sensor-to-lens distance, lens-to-surface distance, window geometry; confirm PAW3395 compatibility with MX1000 optical path

### Calibre track

- [ ] Review PAW3395 datasheet against optical geometry measurements — confirm or revisit sensor selection (Greenfield Track dependency)
- [ ] Begin Greenfield component shortlist: MCU (nRF52840 module), sensor (PAW3395), battery management IC, USB interface IC, haptic driver (DRV2605L or equivalent — future), inductive position sensor (TI LDC series — future)

### Case track

- [ ] Identify Logitech-era white TPE reference specimen for grip color matching (M-BJ58 or equivalent)
- [ ] Obtain Midnight Black and Gunmetal Silver Pantone reference matches from physical specimens; document in repository
- [ ] Review 3D scan data for surface quality and geometry fidelity

### Reserve track

- [ ] Measure dock interior volume and PCB mounting constraints
- [ ] Document charging contact alignment tolerance

### Regulator track

- [ ] Define initial HID feature report schema — design for extensibility from the start; parameters to include at minimum: sensor CPI, report rate, button assignments, scroll detent strength (future), scroll mode (future)

---

## Phase 1 — Theseus Track: PCB reproduction

_Gate: PCB tracing complete for target revision; component catalogue complete; fabrication files verified_

Phase 1 produces a reproducible Calibre PCB that allows a builder to transfer components from an original MX1000 mainboard to a new substrate, extending the life of existing hardware. Two deliverables are produced within this phase:

**1a — Exact reproduction:** a trace-for-trace replica of the original PCB. No design decisions are introduced. The goal is a board that is electrically and mechanically identical to the original, suitable for component transfer. This is a fabrication exercise, not an engineering one, and serves as a baseline for 1b.

**1b — Structurally improved reproduction:** the same component layout and electrical design as 1a, but with targeted trace-level improvements for durability and repairability. Examples include larger annular rings, copper pour flooding around critical pads, tented vias, and teardrop pad-to-trace transitions. This work is explicitly within Calibre's scope: making the board last longer is as much a part of the project's mission as making it work. A builder could reasonably skip 1a and go straight to 1b once traces are mapped; 1a is retained as a documented baseline for historical accuracy.

The roller PCB (already dissected from Mouse 2) is a candidate for early reproduction work and may be completed ahead of the mainboard.

### Calibre track

- [ ] **Select target revision** — confirm Rev. B as the primary reproduction target (two specimens available; Mouse 3 Rev. A not to be dissected without explicit decision)
- [ ] **Schematic entry** — enter traced mainboard schematic into KiCad from Phase 0 PCB tracing work
- [ ] **1a layout** — reproduce original trace routing in KiCad; match original board dimensions, mounting holes, and component positions exactly
- [ ] **Design rule check** — verify 1a against original board geometry; confirm no unintentional deviations
- [ ] **1b layout** — branch from 1a; introduce structural improvements (annular rings, copper pour, teardrop transitions, tented vias where appropriate); document all deviations from original in commit notes
- [ ] **Roller PCB reproduction** — reproduce roller PCB (Mouse 2 already dissected and scanned); apply 1b-style improvements given the known pad-lift failure mode; treat as a parallel sub-task
- [ ] **Fabrication files** — generate Gerbers, drill files, and BOM for both 1a and 1b; verify against fab house DRC
- [ ] **Fabrication** — send to fab; order components for component transfer test

### Documentation track

- [ ] Document schematic entry process; commit KiCad source to repository
- [ ] Document all 1b deviations from original with rationale
- [ ] Commit roller PCB reproduction files and notes

---

## Phase 2 — Theseus Track: modern drop-in substitution

_Gate: Phase 1 boards fabricated and component transfer verified on at least one unit_

Phase 2 identifies and substitutes modern, currently-sourceable components for original parts that are difficult or impossible to obtain, where substitution can be achieved without schematic changes or with only minor, backwards-compatible modifications. Bespoke components — the laser/sensor assembly and the RF module — are still donor-sourced at this stage and are not replaced.

The goal is a Calibre board that a builder could populate entirely from new stock, minus the bespoke assemblies, and have a functionally equivalent mouse.

### Calibre track

- [ ] **Component availability audit** — identify which original components are currently unavailable or at risk of obsolescence; prioritize substitution candidates
- [ ] **Drop-in substitution** — identify modern equivalents for unavailable passives, discretes, and standard ICs; verify pin and footprint compatibility; update schematic and BOM
- [ ] **Switch substitution** — identify currently-available switches matching original specifications (travel, actuation force, footprint); document as confirmed drop-ins or flag deviations
- [ ] **Battery management substitution** — if original battery management IC is unavailable, identify modern equivalent with compatible pinout or adapt layout minimally
- [ ] **Fabrication and test** — fabricate substitution-populated board; verify electrical equivalence against original

### Documentation track

- [ ] Document all substitutions with original part, replacement part, and compatibility notes
- [ ] Update BOM to reflect modern sourcing
- [ ] Document any remaining bespoke components with sourcing status

---

## Phase 3 — Theseus Track: schematic completion and functional mapping

_Gate: complete schematic of target revision fully traced and verified; all subsystems functionally understood to the level required to begin non-drop-in component substitution_

Phase 3 is the gate between the Theseus and Greenfield tracks. It is not primarily a fabrication phase — it is a knowledge phase. The deliverable is a complete, verified schematic and a functional understanding of every subsystem deep enough that bespoke components (sensor, RF module) could begin to be replaced with non-drop-in modern equivalents.

This gate condition may be met incrementally across Phases 1 and 2; Phase 3 formalizes and verifies completeness. Work in this phase runs concurrently with Phase 2 fabrication and test.

### Calibre track

- [ ] **Schematic verification** — cross-check traced schematic against observed circuit behavior on live hardware; resolve any ambiguities
- [ ] **Sensor subsystem mapping** — fully characterize sensor interface: SPI protocol, SROM loading behavior, register map (cross-referenced against ADNS-6000 datasheet where applicable), optical geometry constraints
- [ ] **RF subsystem mapping** — characterize RF module interface to the extent possible without full protocol reverse engineering; document pinout, signaling, and known register behavior
- [ ] **Power subsystem mapping** — characterize battery management, charging circuit, and power sequencing in full
- [ ] **Gate assessment** — confirm schematic completeness and functional understanding against gate criteria; document any remaining unknowns explicitly

### Documentation track

- [ ] Commit verified schematic to repository
- [ ] Write subsystem mapping documents for sensor, RF, and power systems
- [ ] Document remaining unknowns and open questions; these become research tasks for both tracks

---

> **Track fork — Phase 3 gate**
>
> Once the Phase 3 gate is met, the **Theseus Track** and **Greenfield Track** may proceed in parallel. The Theseus Track continues the incremental replacement strategy, replacing bespoke components one at a time until all original parts have been substituted, then adding new functionality on top. The Greenfield Track (Phases 4–7) designs new internals from scratch and works toward full replication of original MX1000 behavior as a firmware profile.
>
> The Theseus Track does not have a fixed endpoint defined in this roadmap beyond Phase 3; its continuation will be planned based on the state of knowledge at that point.

---

## Phase 4 — Greenfield Track: Calibre first generation design

_Gate: optical geometry confirmed, all physical measurements complete, component shortlist finalized_

Phase 4 produces a functional Calibre PCB that fits the MX1000 shell and provides basic BT HID mouse functionality. The design philosophy is modular from the start: the nRF52840 radio is a daughterboard using an off-the-shelf certified module (nice!nano, Seeed XIAO nRF52840, or equivalent), not integrated into the mainboard. This keeps RF certification out of scope for gen one and allows the radio module to be swapped independently.

### Documentation track

- [ ] Populate `docs/interface-spec/millennium-interface-spec.md` from Phase 0 measurements
- [ ] Complete color comparison photography across all colorways
- [ ] Begin ADNS-6000 SROM version investigation — attempt SROM_ID register read from live hardware; cross-reference Phase 3 sensor mapping findings

### Calibre track

- [ ] **Mainboard schematic** — nRF52840 module interface, PAW3395 sensor, battery management (charging from dock contacts + USB-C), switch matrix, scroll encoder interface, LED driver for battery indicator, USB-C for wired fallback and charging
- [ ] **Daughterboard interface** — define connector spec and signal assignments for RF module (27 MHz, future Phase 6), BT module (gen one), and any future modules; keep backplane-compatible from the start
- [ ] **PCB layout** — fit within MX1000 shell geometry; sensor position must match optical geometry within tolerance; respect battery compartment and mounting point constraints from Phase 0 measurements
- [ ] **Charging contact interface** — design contact pads to mate with C-BN34 dock geometry; maintain Reserve compatibility
- [ ] **Component footprint verification** — verify all footprints against Phase 0 measurements before sending to fab
- [ ] **Design review** — check layout against shell 3D scan; confirm no clearance violations
- [ ] **Fabrication** — send to fab (JLCPCB or equivalent); order components

### Case track

- [ ] Begin parametric shell model in Fusion 360 from 3D scan data and Phase 0 measurements
- [ ] Identify material candidates for shell (ABS for hard shell, TPE for grip panels); source samples
- [ ] Prototype grip panel geometry — test fit against original shell

### Reserve track

- [ ] Begin dock PCB schematic — charging circuit, USB interface to host, contact geometry

### Regulator track

- [ ] Begin Tauri application scaffold
- [ ] Implement HID feature report read/write against nRF52840 test firmware
- [ ] Basic UI: CPI selector, report rate selector, connection status

---

## Phase 5 — Greenfield Track: Calibre bring-up and iteration

_Gate: Calibre PCB fabricated and components in hand_

Phase 5 is bench work. The assembled Calibre board is brought up incrementally — power first, then MCU, then sensor, then wireless, then switches. Each subsystem is verified independently before integrating the next. At the end of Phase 5, Calibre functions as a working wireless mouse inside the MX1000 shell.

### Calibre track

- [ ] **Power bring-up** — verify battery management, charging from dock contacts, voltage rails
- [ ] **MCU bring-up** — flash bootloader and basic firmware; verify USB-C enumeration
- [ ] **Sensor bring-up** — verify PAW3395 SPI communication; confirm tracking on surface; verify optical geometry against Phase 0 predictions
- [ ] **Wireless bring-up** — BT HID enumeration on macOS and Windows; verify all button and scroll events
- [ ] **Switch integration** — verify all button inputs including side buttons and scroll wheel click
- [ ] **LED indicator** — implement incandescent fade behavior; tune timing and brightness curve
- [ ] **Charging indicator** — implement charge state signaling via LEDs
- [ ] **Battery management** — verify charge termination, low battery detection, dock detection
- [ ] **Fit check** — assemble inside MX1000 shell; verify no mechanical interference; confirm charging contacts mate correctly with C-BN34 dock
- [ ] **Iterate** — address any layout or component issues; spin Rev. B if needed

### Documentation track

- [ ] Document Calibre bring-up findings; commit any spec corrections to interface spec
- [ ] Begin firmware architecture documentation

### Case track

- [ ] First prototype shell — 3D print in ABS or equivalent; test fit against Calibre board
- [ ] Evaluate Millennium logo placement and emboss/deboss depth on prototype material
- [ ] Test grip panel material candidates for color and texture match to original

### Reserve track

- [ ] Fabricate Reserve dock PCB prototype
- [ ] Verify charging contact alignment and current delivery to Calibre

### Regulator track

- [ ] Connect Regulator to functional Calibre firmware over HID
- [ ] Implement live CPI adjustment and readback
- [ ] Implement firmware update mechanism

---

## Phase 6 — Greenfield Track: integration and refinement

_Gate: Calibre functional inside MX1000 shell; Reserve dock functional_

Phase 6 integrates all components into a coherent system and begins the refinement work that distinguishes a restoration from a hack. The original MX1000 shell is still in use at this stage — Case is in development but not yet production-ready.

### Calibre track

- [ ] **27 MHz RF daughterboard** — design and bring up the RF module; implement Logitech Fast RF protocol (requires RF protocol reverse engineering or SDR capture; informed by Phase 3 RF subsystem mapping); verify pairing with C-BN34 dock receiver
- [ ] **Firmware profiles** — implement default profile that replicates original MX1000 behavior; begin user-configurable profile support
- [ ] **Power optimization** — characterize battery life under typical use; tune sleep modes and wake thresholds
- [ ] **Reliability testing** — extended use testing; address any latency, dropout, or tracking issues
- [ ] **SROM** — if ADNS-6000 SROM version differences are identified, document their effect on tracking behavior for reference

### Case track

- [ ] **Final geometry** — finalize parametric shell model; incorporate any fit corrections from Phase 5 prototype
- [ ] **Material finalization** — confirm ABS and TPE material selection and color matches; source production-grade material or molding partner
- [ ] **Logo integration** — finalize Millennium logo placement, depth, and method (emboss, deboss, pad print)
- [ ] **Prototype iteration** — print or fabricate refined prototype; fit check with Calibre and Reserve
- [ ] **Color variants** — plan Gunmetal Silver, Midnight Black, and Dark Blue colorways

### Reserve track

- [ ] Finalize Reserve dock design
- [ ] Integrate Millennium logo on dock face
- [ ] Prototype Reserve enclosure; verify fit with mouse and charging alignment

### Regulator track

- [ ] Profile management UI — save, load, switch profiles
- [ ] RF vs. BT connection mode switching
- [ ] Battery level display
- [ ] Firmware update UI
- [ ] macOS and Windows packaging

### Documentation track

- [ ] Write RF protocol documentation from reverse engineering findings
- [ ] Write Calibre firmware architecture document
- [ ] Write Regulator protocol specification (full HID feature report schema)

---

## Phase 7 — Greenfield Track: release preparation

_Gate: full system functional and refined; Case and Reserve in producible form_

Phase 7 prepares Millennium for public release as a usable open source project. The emphasis is on reproducibility — another builder should be able to fabricate a Calibre board, print a Case, and assemble a working system from the repository alone.

### All tracks

- [ ] **Repository audit** — ensure all design files, firmware, schematics, BOMs, and documentation are committed and complete
- [ ] **BOM finalization** — verify all components are currently available; identify second-source options for any single-sourced parts
- [ ] **Assembly documentation** — step-by-step assembly guide with photographs; calibration and bring-up procedure
- [ ] **Compatibility matrix** — document which MX1000 shell variants Calibre is confirmed to fit; note any per-variant differences
- [ ] **License audit** — confirm all third-party components (ZMK or nRF Desktop firmware, KiCad footprints, etc.) are compatible with project licenses
- [ ] **Release** — tag v1.0; publish announcement

---

## Long-term considerations (post-v1.0)

These are explicitly out of scope for the initial release but inform architectural decisions in earlier phases.

- **Electromagnetic scroll wheel** — replaces mechanical encoder; variable detent strength configurable via Regulator; requires position encoder, coil driver, and firmware motor control loop
- **Haptic switches** — replaces mechanical microswitches with LRA actuators and inductive position sensing (TI LDC series); replicates MX1000 click feel in firmware; fully configurable actuation point and feedback intensity via Regulator
- **Calibre Rev. 2** — backplane architecture with swappable modules for radio, scroll wheel, and switch systems; designed for modularity and long-term upgradability
- **27 MHz RF protocol** — full reverse engineering and open implementation; allows pairing with original C-BN34 docks
- **Reserve Rev. 2** — redesigned dock with USB-C host interface; onboard charging IC; potentially wireless charging

---

## Current blockers summary

| Blocker                                            | Blocks                                                              | Resolution                                                      |
| -------------------------------------------------- | ------------------------------------------------------------------- | --------------------------------------------------------------- |
| 3D scanning spray not yet obtained                 | 3D scanning                                                         | Purchase locally                                                |
| SDR hardware not acquired                          | 27 MHz RF capture                                                   | Purchase; defer to Phase 6                                      |
| Physical measurements not yet taken                | Calibre layout, PAW3395 confirmation, Case modeling, Reserve design | Execute Phase 0 measurement work                                |
| PCB tracing not yet complete                       | Phase 1 schematic entry; Phase 3 gate                               | Execute as part of Phase 0 documentation work                   |
| Donor unit availability for component transfer TBD | Phase 1 component transfer test                                     | Determine which specimen is sacrificed for mainboard dissection |
