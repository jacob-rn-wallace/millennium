# Millennium project: development roadmap

This roadmap organizes the Millennium project across four parallel tracks — **Documentation**, **Calibre** (replacement PCB), **Case** (replacement shells), and **Reserve** (dock) — and five sequential phases. Phases represent meaningful capability gates: work within a phase can proceed in any order, but phase boundaries reflect dependencies that must be resolved before the next phase begins. **Regulator** (host configuration software) development is noted within phases but treated as a running parallel track rather than a gated deliverable, since its development is loosely coupled to hardware until functional firmware exists.

The roadmap reflects current project state: Mouse 1 (Gunmetal Silver, Rev. B) and Mouse 3 (Midnight Black, Rev. A) are in hand. Mouse 2 (Dark Blue) is in transit. No Calibre PCB has been designed. No Case geometry exists. Reserve dock design has not begun.

---

## Phase 0 — Physical characterization
*Gate: complete physical documentation of all hardware before any design work is committed*

This phase is the foundation for everything downstream. Decisions made in Calibre, Case, and Reserve are only as good as the measurements they're based on. Phase 0 work should be committed to the repository as it is completed.

**Status: in progress — Mouse 1 and Mouse 3 in hand; Mouse 2 pending**

### Documentation track

- [ ] **External photography** — both units, standardized lighting, all angles; Mouse 1 and Mouse 3 side by side for color comparison; defer three-way comparison until Mouse 2 arrives
- [ ] **Shell measurements** — all external dimensions: length, width, height at multiple points, button surface geometry, grip panel positions, scroll wheel recess, logo placement, foot positions and dimensions
- [ ] **Internal measurements** — PCB dimensions and mounting point positions, battery compartment geometry, charging contact positions and spacing, light pipe geometry, button mechanism travel and actuation positions, scroll wheel encoder dimensions
- [ ] **Mass and inertia** — total mass of both units (with and without battery), center of mass, moment of inertia via trifilar pendulum; document and compare Rev. A and Rev. B
- [ ] **PCB tracing** — trace both Rev. A (Mouse 3) and Rev. B (Mouse 1) mainboards; identify all components, map signal routing for sensor, switches, scroll encoder, battery management, RF module, indicator LEDs; document differences between revisions
- [ ] **Component identification** — identify all ICs and passives on both boards; cross-reference with datasheets; document sensor mount geometry relative to shell window
- [ ] **Charging contact characterization** — voltage and current profile during a full charge cycle on a known-good unit; contact resistance measurement; pin assignments
- [ ] **Battery connector** — pinout, connector family/pitch, dimensions
- [ ] **Scroll wheel encoder** — type (mechanical vs. optical), dimensions, mounting, detent count per revolution
- [ ] **Switch identification** — measure existing switches (travel, actuation force, dimensions, footprint); identify manufacturer and part number where possible
- [ ] **Light pipe experiment** — powered mouse in darkened room; photograph and document LED propagation through light pipes; assess light bleed at boundaries; informs whether Case requires a redesigned light divider
- [ ] **3D scanning** — obtain foot powder spray; scan shell exterior of both units with CR-Scan Ferret SE; export meshes to repository
- [ ] **Dock characterization** — measure C-BN34 dock dimensions; document charging contact geometry and alignment relative to mouse contacts; confirm power input spec
- [ ] **Optical geometry** — measure sensor-to-lens distance, lens-to-surface distance, window geometry; confirm PAW3395 compatibility with MX1000 optical path

### Calibre track

- [ ] Review PAW3395 datasheet against optical geometry measurements — confirm or revisit sensor selection
- [ ] Begin component shortlist: MCU (nRF52840 module), sensor (PAW3395), battery management IC, USB interface IC, haptic driver (DRV2605L or equivalent — future), inductive position sensor (TI LDC series — future)

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

## Phase 1 — Calibre first generation design
*Gate: optical geometry confirmed, all physical measurements complete, component shortlist finalized*

Phase 1 produces a functional Calibre PCB that fits the MX1000 shell and provides basic BT HID mouse functionality. The design philosophy is modular from the start: the nRF52840 radio is a daughterboard using an off-the-shelf certified module (nice!nano, Seeed XIAO nRF52840, or equivalent), not integrated into the mainboard. This keeps RF certification out of scope for gen one and allows the radio module to be swapped independently.

### Documentation track

- [ ] Populate `docs/interface-spec/millennium-interface-spec.md` from Phase 0 measurements
- [ ] Complete three-way color comparison photography once Mouse 2 arrives
- [ ] Document Mouse 2 PCB revision and component inventory; note any differences from Mouse 1 and Mouse 3
- [ ] Begin ADNS-6000 SROM version investigation — attempt SROM_ID register read from live hardware

### Calibre track

- [ ] **Mainboard schematic** — nRF52840 module interface, PAW3395 sensor, battery management (charging from dock contacts + USB-C), switch matrix, scroll encoder interface, LED driver for battery indicator, USB-C for wired fallback and charging
- [ ] **Daughterboard interface** — define connector spec and signal assignments for RF module (27 MHz, future Phase 2), BT module (gen one), and any future modules; keep backplane-compatible from the start
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

## Phase 2 — Calibre bring-up and iteration
*Gate: Calibre PCB fabricated and components in hand*

Phase 2 is bench work. The assembled Calibre board is brought up incrementally — power first, then MCU, then sensor, then wireless, then switches. Each subsystem is verified independently before integrating the next. At the end of Phase 2, Calibre functions as a working wireless mouse inside the MX1000 shell.

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

## Phase 3 — Integration and refinement
*Gate: Calibre functional inside MX1000 shell; Reserve dock functional*

Phase 3 integrates all components into a coherent system and begins the refinement work that distinguishes a restoration from a hack. The original MX1000 shell is still in use at this stage — Case is in development but not yet production-ready.

### Calibre track

- [ ] **27 MHz RF daughterboard** — design and bring up the RF module; implement Logitech Fast RF protocol (requires RF protocol reverse engineering or SDR capture); verify pairing with C-BN34 dock receiver
- [ ] **Firmware profiles** — implement default profile that replicates original MX1000 behavior; begin user-configurable profile support
- [ ] **Power optimization** — characterize battery life under typical use; tune sleep modes and wake thresholds
- [ ] **Reliability testing** — extended use testing; address any latency, dropout, or tracking issues
- [ ] **SROM** — if ADNS-6000 SROM version differences are identified, document their effect on tracking behavior for reference

### Case track

- [ ] **Final geometry** — finalize parametric shell model; incorporate any fit corrections from Phase 2 prototype
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

## Phase 4 — Release preparation
*Gate: full system functional and refined; Case and Reserve in producible form*

Phase 4 prepares Millennium for public release as a usable open source project. The emphasis is on reproducibility — another builder should be able to fabricate a Calibre board, print a Case, and assemble a working system from the repository alone.

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

| Blocker | Blocks | Resolution |
|---------|--------|------------|
| Mouse 2 in transit | Three-way color comparison; Mouse 2 PCB inspection | Wait for customs clearance |
| 3D scanning spray not yet obtained | 3D scanning | Purchase locally |
| SDR hardware not acquired | 27 MHz RF capture | Purchase; defer to Phase 3 |
| Physical measurements not yet taken | Calibre layout, PAW3395 confirmation, Case modeling, Reserve design | Execute Phase 0 measurement work |
