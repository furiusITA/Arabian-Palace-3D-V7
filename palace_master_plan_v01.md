# Arabian Palace — Master Architectural Plan v01

Status: master layout and coordination plan; not yet a finished block model.

## 1. Design decision

The palace is designed at its proper architectural scale first. VOXORA's 64×64×96 project limit is treated as a module limit only, never as a limit on the palace itself.

- Overall planning envelope: **241 × 241 blocks** (coordinates -120…+120 on X and Z).
- Main footprint: a symmetrical octagonal composition within that envelope.
- Primary symmetry: X=0 and Z=0; all major placements are mirrored across both axes.
- Vertical ambition: the central dome may rise above 96 blocks. Tall structures will be split into vertically aligned VOXORA sections if needed.
- Style: ivory/quartz architecture, deep crimson dome and selected roofs, restrained gold/yellow highlights, muted bronze/copper accents.
- All geometry must be buildable with ordinary Minecraft blocks, supported, non-intersecting, and checked for symmetry.

The 241-block envelope is a deliberate increase from 201: it gives the central keep, four inner towers, galleries, perimeter towers and courtyards room to breathe. It is a planning envelope, not a requirement to fill every block.

## 2. Coordinate system

- Origin (0,0,0): centre of the main keep at ground level.
- X: west/east; Z: north/south; positive Z is south.
- Y: vertical, with Y=0 as the principal finished ground datum.
- Coordinates below refer to structure centres unless a range is explicitly stated.
- Every coordinate and footprint is mirrored about X=0 and Z=0.

## 3. Primary composition

| Element | Planning position / footprint | Design intent |
|---|---:|---|
| Central keep | 89×89; X/Z -44…+44 | Monumental square central hall and drum supporting the great dome |
| Great dome | centred at (0,0); target diameter about 53 | Deep crimson, broad shoulder, complete crown and finial |
| Four inner towers | centres (0,-72), (72,0), (0,72), (-72,0); each 27×27 | Large independent towers with full roofs, balconies and crowns; not squeezed against the dome |
| Gallery links | connect keep to each inner tower; target clear width 11–13 | Covered, legible connections with open courtyard space between |
| Eight perimeter towers | centres (±96,±40) and (±40,±96); each 21×21 | Eight evenly mirrored outer defensive/ceremonial towers |
| Outer octagonal boundary | vertices (0,-120), (85,-85), (120,0), (85,85), (0,120), (-85,85), (-120,0), (-85,-85) | Defines the principal palace precinct and wall/garden composition |
| Main entrance | centred on south axis (X=0, positive Z) | Monumental approach aligned with the keep and dome |
| Side pavilions | paired east/west and north/south compositions, set between tower groups | Smaller secondary masses; their exact footprints follow the verified circulation plan |

### Tower separation check

The central keep ends at X/Z ±44. Each inner tower is 27×27 and is centred 72 blocks from the origin on a cardinal axis. On its principal axis, the clear gap from the keep to the tower is approximately 14 blocks. This gives room for a proper gallery connection and visible courtyard separation. Tower heights and crowns will be designed independently of the keep's dome.

The eight perimeter towers form a second, distinct ring. They must not be confused with or substituted for the four inner towers.

## 4. Height hierarchy (targets, subject to silhouette testing)

- Main ground datum: Y=0.
- Main occupied floors: establish a consistent floor module during the central-keep prototype.
- Inner tower roofs/crowns: complete architectural tops, with their own visible silhouette below the dome's dominant peak.
- Great dome: target peak approximately Y=108–116, subject to a proportion test. If it exceeds VOXORA's 96-block vertical limit, model it in vertically aligned sections.
- Perimeter towers: clearly lower than the four inner towers, but still substantial and fully roofed.
- No floating bases, unsupported overhangs, missing caps, or decorative pieces that disappear at module boundaries.

## 5. Material language

**Primary:** smooth quartz, quartz bricks, quartz pillars, calcite.

**Crimson:** red stained glass where glazing is intended; red nether bricks or other tested deep-red vanilla blocks for opaque roof/dome structure. The final red combination will be checked in VOXORA before large-scale use.

**Accents:** yellow terracotta and carefully limited gold blocks. Use copper-family blocks only where their actual hue and oxidation state suit the palette. Gold is a highlight, not a dominant surface.

No material is approved solely because its Java name exists: each chosen block must be checked for Bedrock availability and appearance.

## 6. VOXORA module strategy

Each project stays within 64×64×96. The complete palace remains on the global coordinate grid above.

1. Build and inspect the central keep as several adjacent 64×64 planning windows if needed; do not shrink the keep to fit one file.
2. Build each inner tower as its own module, with its complete roof and crown. A tower can be inspected independently and positioned using its stated global centre.
3. Build the four gallery links as separate modules with overlap/connection details documented at their ends.
4. Build mirrored north/south and east/west wings as paired modules. Use VOXORA mirror tools only after the source half is validated.
5. Build the eight perimeter towers as independent modules.
6. Assemble the master layout by global coordinates. Do not assume separate JSON files automatically merge; verify any merge workflow before relying on it.

For a module with local origin (0,0,0), its global placement is recorded as an explicit X/Y/Z offset. Shared seams must use a single agreed boundary convention so that blocks are neither duplicated nor omitted.

## 7. Validation gates

A module is not accepted until it passes:

- JSON parses and imports in VOXORA.
- All block entries use the verified numeric state field.
- Every block coordinate is unique within the module.
- Bounds stay within the intended module dimensions.
- All block IDs are valid vanilla blocks.
- Symmetry is checked numerically, not just by eye.
- Foundations touch the intended ground; no unsupported floating sections.
- No unintended intersections with neighbouring modules.
- Roofs, crowns, balconies and top details are present in the exported/imported result.
- A material/count summary is recorded.

## 8. Build order

**Phase A — Central keep prototype:** establish the main hall, drum, dome profile and the correct scale relationship. Preserve the quartz palette. The prototype is a design test, not the entire palace.

**Phase B — Four inner towers:** design one complete tower at full intended scale, validate its top and proportions, then mirror/rotate it to the other three positions.

**Phase C — Galleries and courtyards:** connect the core and inner towers without closing off the open spaces.

**Phase D — Perimeter ring:** add the eight outer towers, perimeter walls, pavilions and entrance.

**Phase E — Gardens and final detailing:** add the formal approach, water features, planted courtyards and restrained ornament.

## 9. Current next deliverable

The next model should be a **central-keep scale and silhouette prototype**, not another compressed whole-palace attempt. It will establish the dome's diameter, drum height, roof profile, and the keep's relationship to the four inner towers. After that, the inner tower will be modelled separately at full size with its entire top visible.
