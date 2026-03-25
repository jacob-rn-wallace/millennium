# Contributing to Millennium

Contributions of any kind are welcome — measurements, photographs, firmware,
PCB design, CAD work, casting experience, documentation, and sourcing research
are all equally valuable at this stage of the project.

Please open an issue or discussion before proposing major architectural changes
so that design intent can be preserved.

---

## Code of Conduct

Millennium is a technical project and this is a technical space. Contributions
are evaluated on their merits. Discussion should remain focused on the work.

The short version: be direct, be honest, and be respectful. Criticism of ideas
is welcome and expected. Personal attacks, harassment, and dismissiveness are
not.

If you have a concern about conduct, open a private discussion with the
maintainer.

---

## What the project needs right now

The most urgent contributions are physical characterization of the MX1000
itself. If you have a unit and are willing to open it:

- Internal photography (high resolution, all angles, both PCBs)
- Dimensional measurements (calipers) of shell geometry, PCB, and charging
  contacts
- Charging contact voltage and current measurement from the original cradle
- RF traffic capture of the 27MHz wireless link (see RF section below)

If you do not have a unit but have relevant skills, the areas of greatest need
are listed in the README.

---

## How to contribute

**For measurements, photographs, and physical documentation:**
Open a GitHub issue with your findings, or submit a pull request placing files
in the appropriate directory. Either approach is welcome. If submitting a pull
request, follow the file naming and directory conventions below.

**For firmware:**
Open a discussion before beginning significant work so that implementation
decisions can be agreed on in advance. Submit changes as a pull request against
the  `main`  branch.

**For hardware design (PCB, mechanical):**
Open a discussion before beginning significant work. Submit KiCad files and
Fusion 360 exports as a pull request. Native format files (`.kicad_pcb`,
`.f3d`) are preferred over exports alone.

**For documentation:**
Submit a pull request directly. No prior discussion needed for documentation
fixes or additions.

---

## File naming and directory conventions

Files should be named descriptively and in lowercase with hyphens, not spaces
or underscores — for example  `top-shell-exterior-left.jpg`  rather than
`Top Shell Exterior Left.jpg`  or  `top_shell_exterior_left.jpg`.

Place files in the directory that matches their type:
```
electrical/bom/          — component identification and sourcing
electrical/datasheets/   — component datasheets and protocol specifications
electrical/photos/       — high resolution PCB photography
electrical/rf/           — RF capture files and protocol documentation
electrical/schematics/   — traced schematics in KiCad or PDF
firmware/calibre/        — Calibre PCB firmware
firmware/reserve/        — Reserve dock firmware
manufacturing/assembly/  — reassembly documentation
manufacturing/casting/   — mold-making and casting instructions
manufacturing/materials/ — material specifications and suppliers
mechanical/drawings/     — dimensioned drawings and measurement records
mechanical/fusion/       — Fusion 360 native files
mechanical/scans/        — raw scan data
mechanical/stl/          — print-ready STL and 3MF files
sourcing/batteries/      — battery replacement sourcing
sourcing/secondary/      — secondary market and donor unit guidance
sourcing/switches/       — Omron switch equivalents and sourcing
```

---

## Measurements

When submitting physical measurements, include:

- The tool used (caliper model, multimeter model, SDR hardware)
- The unit's condition and approximate age if known
- Whether the unit is an early or late production MX1000 (if distinguishable)
- Any relevant context — surface condition, modification history, etc.

Measurements submitted as markdown tables in a GitHub issue are perfectly
acceptable. They do not need to be formatted as CAD files to be useful.

---

## RF capture

Capturing the 27MHz wireless protocol requires an SDR receiver capable of
operating at 27MHz. An RTL-SDR with an appropriate antenna is sufficient.

If you are attempting RF capture:

- Record raw IQ samples at a sample rate of at least 1 MSPS
- Capture during normal mouse operation — movement, clicks, and scroll events
- Capture a power cycle to observe the pairing/presence handshake
- Note the SDR hardware, software, and sample rate used

RF capture files can be large — share via a link in a GitHub issue rather than
attaching directly to the repository.

---

## Versioning

Calibre (PCB) and Reserve (dock) revisions follow the M1K### designation
scheme defined in the interface specification. Do not assign revision numbers
to your own contributions — revision numbers are assigned by the maintainer
when a design is formally adopted.

---

## License

By contributing to Millennium you agree that your contributions will be
licensed under the same terms as the component they belong to:

- Hardware designs: CERN-OHL-S-2.0
- Firmware: GPL-3.0
- Documentation: CC BY 4.0