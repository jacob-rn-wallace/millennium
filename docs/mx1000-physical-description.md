# MX1000 physical description reference

This document establishes agreed component names and per-colorway visual descriptions for the MX1000 RF mouse (M-RAG97). It exists as a shared reference for the Millennium project to ensure consistency across documentation, design work, and conversation. All descriptions are based on physical inspection of project specimens and primary source imagery unless otherwise noted.

---

## Parts inventory

The following table lists all known discrete plastic parts of the MX1000 case assembly, catalogued from physical inspection of Mouse 3 (P/N 852152-1000, Midnight Black). Part numbers and CAV codes were read directly from markings moulded into each part. Entries marked N/A either bore no marking or the marking was too small to read reliably.

Mould markings (2nd identifiers) were recorded across all seven specimens and are documented separately in `docs/mx1000-mould-markings.md`.

| Part term                  | P/N         | Material         |
|----------------------------|-------------|-----|
| Bottom plate               | 402443-0000 | ABS              |
| Battery cover              | 003107-0000 | ABS              |
| Main body                  | 402442-0000 | ABS (rubberized) |
| Forward/back rockers pivot | 003109-0000 | ABS              |
| Top shell                  | 402444-0000 | ABS              |
| Battery indicator window   | 402449-0000 | ABS              |
| Battery indicator light pipe | N/A       | ABS              |
| Application switch button  | N/A         | ABS              |
| Scroll wheel               | N/A         | ABS (rubberized) |
| Scroll wheel cage          | N/A         | ABS              |
| Scroll wheel pivot clip    | N/A         | ABS              |
| Scroll wheel surround      | N/A         | ABS              |
| Cruise control rockers     | N/A         | ABS              |
| Forward/back rockers       | N/A         | ABS              |
| Connect/Reset button       | N/A         | ABS              |
| Power switch               | N/A         | ABS              |

Parts marked N/A either bore no part number marking or the marking area was too small to read reliably.

---

## Agreed component names

The following names are used consistently throughout project documentation. Where Logitech used a different name internally or in marketing, it is noted. Part numbers reference the inventory above.

### Top shell (402444-0000) — viewed from above

The top shell is a discrete ABS part screwed to the main body. It is the primary color surface of the mouse. The left button and right button are integral features of the top shell — moulded as part of the same piece, not separate parts.

**Top shell** — the large curved hard plastic surface covering the upper body of the mouse, from the front button edge to the rear.

**Left button** — the primary click surface, left side. An integral feature of the top shell.

**Right button** — the primary click surface, right side. An integral feature of the top shell.

**Scroll wheel assembly** — the scroll wheel zone in the center of the top shell. Comprises two mechanically independent sub-assemblies: the tilting scroll wheel mechanism below, and the scroll wheel surround with captured cruise control rockers above.

The tilting scroll wheel mechanism:

- **Scroll wheel** — the rubberized ABS wheel itself, used for vertical scrolling and middle-click
- **Scroll wheel cage** — the ABS structure that retains the scroll wheel and forms the body of the tilting mechanism. The cage rests on two contact points on the bottom plate: a fulcrum protrusion toward the rear (user side), and a loose retaining protrusion toward the front. The cage can rock laterally on the rear fulcrum; the front protrusion limits travel without constraining it tightly. Tilting left or right actuates one of the two side scroll switches on the roller PCB
- **Scroll wheel pivot clip** — the ABS clip screwed down onto the rear fulcrum protrusion of the bottom plate. Retains the scroll wheel cage on the fulcrum while allowing the lateral rocking motion

The surround assembly:

- **Scroll wheel surround** — the moulded ABS frame surrounding the scroll wheel opening. Sits proud of the top shell surface with filleted edges that blend the transition. Screwed into the main body from above, with screws passing through the top shell; this holds the top shell captive as a secondary retention. The cruise control rockers are captured within the surround — inseparable from it, but independently articulating. **This is the key colorway-distinguishing element** — see per-colorway descriptions below
- **Cruise control rockers** — the two elongated rocker buttons fore and aft of the scroll wheel, used for line-by-line incremental scrolling. Their pivot is moulded into the surround such that they cannot be removed without damaging the surround, but tilt independently of it. Each rocker has an arm that passes down through the scroll wheel opening into the body, positioned just above the corresponding fore or aft switch on the roller PCB. The arms have no physical connection to the scroll wheel cage or PCB — actuation is by proximity only. Silver/chrome on all known colorways

**Battery indicator** — the charge level indicator on the left side of the top shell, visible from above. Logitech called this the "4-level battery indicator." Comprises two discrete parts:

- **Battery indicator window** (402449-0000) — the ABS lens/window piece visible from the outside; four apertures
- **Battery indicator light pipe** — the internal ABS pipe that guides LED light to the window

**Logitech logo** — printed on the right side of the top shell; an integral feature of the top shell surface

---

### Main body (402442-0000)

The main body is a single rubberized ABS part comprising most of the structural mass of the mouse. What might appear to be a separate rubber grip panel on the left side and a separate hard plastic panel on the right are both surface zones of this one part. The rubberized finish gives the grip zones their texture; the part is not a TPE overmold.

**Left grip zone** — the rubberized surface on the left (thumb) side of the main body

**Right side** — the smooth surface on the right side of the main body; houses no buttons on the standard M-RAG97

**Thumb groove** — the pronounced concave recess on the left side of the main body where the thumb rests naturally

**Forward/back rockers** — a single pivoting ABS piece on the left side of the main body, above the thumb groove. Pressing the upper portion actuates the forward function; pressing the lower portion actuates the back function. (The forward/upper and back/lower convention maps to the standard browser navigation direction but is ultimately a firmware convention, not a physical one.) A cutout in the center of the piece accommodates the application switch button.

**Forward/back rockers pivot** (003109-0000) — the ABS bracket that holds the forward/back rockers in place and provides the pivot axis

**Application switch button** — a small discrete ABS button that sits in the cutout of the forward/back rockers on the left side of the mouse

**Connect/Reset button** — small recessed ABS button on the underside; black on M-RAG97, red on M-RBA97 Bluetooth variant

**Power switch** — ABS slider on the underside

---

### Bottom plate (402443-0000)

The bottom plate is a discrete ABS part forming the underside of the mouse. It has two protrusions on its inner face that interface with the scroll wheel cage: a rear fulcrum (user side) onto which the scroll wheel pivot clip is screwed, and a front retaining protrusion that loosely locates the front of the cage.

**Foot pads** — PTFE (Teflon) glide pads; the original MX1000 shipped with four

**Laser window** — the optical aperture for the ADNS-6000 laser sensor

**Hardware label** — contains part number (P/N), model number (M/N), serial number (S/N), regulatory marks, and power specifications

---

### Battery cover (003107-0000)

A discrete ABS part. The Li-ion battery is internal and not user-accessible in the conventional sense; the battery cover provides access to the battery compartment.

---

### Dock (C-BN34)

**Charging contacts** — two metal contact pads on the underside-front of the mouse that mate with corresponding contacts on the dock cradle

**Dock cradle** — the curved rest that holds the mouse upright during charging

**Connect button** — tactile button on the front face of the dock used for RF pairing/re-sync

---

## Per-colorway visual descriptions

### Gunmetal Silver (P/N 852152-0000 / -0100 / -0200 / -0300)

**Top shell finish:** Matte metallic. The color has a strong blue-grey cast that varies significantly with lighting — appearing as grey, blue-grey, or greenish-grey depending on the light source and angle. This explains the inconsistency in how sources describe it: "gunmetal," "gunmetal bluish," "Blue/Black," "2-Tone," "green." All refer to the same finish.

**Scroll wheel surround:** Silver/chrome, matching the cruise control rockers. The surround and rockers together form one continuous silver zone in the center of the top shell.

**Left grip zone:** Rubberized ABS surface of the main body; reads as black rubber

**Right side:** Smooth ABS surface of the main body, same color family as the top shell

**Cruise control rockers:** Silver/chrome

**Battery indicator LEDs:** Green

**Logitech logo:** Silver/metallic print

---

### Onyx Black "Midnight" (P/N 852152-1000)

**Top shell finish:** Glossy. A deep, near-black finish with no metallic flake — the same surface character as a glossy black automotive finish or consumer electronics of that era. Confirmed by physical inspection of Mouse 3 and consistent across all promotional imagery.

**Scroll wheel surround:** Black, matching the main body surface and top shell. The silver cruise control rockers are visible as discrete elements within the black surround — they do not blend into the surround the way they do on the Gunmetal Silver variant.

**Left grip zone:** Rubberized ABS surface of the main body; reads as black rubber

**Right side:** Smooth ABS surface of the main body, same glossy black as the top shell

**Cruise control rockers:** Silver/chrome (same as Gunmetal Silver)

**Battery indicator LEDs:** Green (same as Gunmetal Silver)

**Logitech logo:** Silver/metallic print (same as Gunmetal Silver)

---

### Dark Blue / MX 3100 bundle variant (P/N 852376-0000)

**Top shell finish:** Matte metallic, identical in character to the Gunmetal Silver finish. Confirmed by physical inspection of Mouse 2.

**Top shell color:** A distinctly darker, more saturated blue than the Gunmetal Silver's blue-grey cast. Reads as very dark blue or near-black under some lighting conditions.

**Scroll wheel surround:** Silver/chrome — identical to the Gunmetal Silver variant. The entire scroll wheel zone (surround and cruise control rockers) reads as one continuous silver assembly, same as Gunmetal Silver.

**Left grip zone:** Rubberized ABS surface of the main body — assumed identical to Gunmetal Silver by inspection.

**Cruise control rockers:** Silver/chrome (same as all variants).

**Battery indicator LEDs:** Green (assumed same as other variants, unconfirmed).

**Logitech logo:** Silver/metallic print (assumed same as other variants, unconfirmed).

The Dark Blue variant is effectively **identical to the Gunmetal Silver in every respect except the top shell color**. The scroll wheel surround, grip zones, and all other elements match the Gunmetal Silver configuration.

---

## Key visual differentiators between colorways

| Feature | Gunmetal Silver | Midnight Black | Dark Blue |
|---------|----------------|----------------|-----------|
| Top shell finish | Matte metallic | Glossy | Matte metallic |
| Top shell color | Blue-grey (light-dependent) | Near-black | Dark saturated blue |
| Scroll wheel surround | Silver/chrome | Black | Silver/chrome |
| Scroll wheel zone reading | Unified silver element | Silver rockers on black surround | Unified silver element |

---

## Notes on color photography

The Gunmetal Silver finish is notoriously difficult to photograph consistently. The metallic flake in the finish reflects different wavelengths depending on angle and light source, causing the color to read as anything from warm grey to distinctly blue-grey to slightly greenish. This is intrinsic to the finish and not a defect or batch variation. Any two photographs of the same Gunmetal Silver unit taken under different lighting can appear to show different colors.

The Midnight Black finish is more consistent in photography due to its glossy, non-metallic character. It reads as deep black or very dark charcoal across most lighting conditions, with the gloss visible as highlights and reflections rather than as color variation.
