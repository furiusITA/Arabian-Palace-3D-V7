# Central Keep v02 — Combined Structure & Import Guide

This revision corrects the first prototype's missing architectural connections. It is a single global 89×89 central keep represented by four non-overlapping VOXORA quadrants.

## Module offsets and counts

| Quadrant | File | Global X | Global Z | Offset (X,Y,Z) | Blocks |
|---|---|---|---|---|---:|
| NW | central_keep_v02_nw.json | -44…-1 | -44…-1 | (-44,0,-44) | 28385 |
| NE | central_keep_v02_ne.json | 0…44 | -44…-1 | (0,0,-44) | 28896 |
| SW | central_keep_v02_sw.json | -44…-1 | 0…44 | (-44,0,0) | 28944 |
| SE | central_keep_v02_se.json | 0…44 | 0…44 | (0,0,0) | 29462 |

Each quadrant uses local coordinates 0…44 horizontally. Add its listed offset to recover global palace coordinates.

## What changed from v01

- The dome has a broad, thick lower shoulder and a fuller bulbous profile. It rises from a pronounced collar rather than appearing as a thin shell starting abruptly.
- The circular drum now extends down to the main floor and is structurally tied into the building, instead of beginning only above the roof.
- The roof terrace fills the space between the drum and the outer parapet, so the dome is no longer an isolated object inside a large open square.
- The exterior walls now have regular pilasters, string courses, stepped buttresses, recessed window rhythm, and a more articulated cornice.
- The north and south walls have real 11-wide, 16-high passage openings through all three wall layers, framed by monumental portal piers and stepped crowns.
- The four corner turrets have complete stepped crimson roofs and finials.
- The entire global geometry is enforced to be exactly four-way symmetrical at the block/material level.

## Geometry validation performed

- 115,727 unique occupied global block coordinates.
- 0 symmetry failures across X=0 and Z=0.
- 0 blocks obstructing the two portal passage volumes (expected 0).
- Four quadrant coordinate ranges are disjoint.
- Every block entry uses numeric state 0; no air placeholders are exported.
- Vertical range Y=0…91, within the VOXORA 96-block height limit.
- The geometry is checked as one combined global coordinate map before export.

This is still a design prototype. Import and visual inspection in VOXORA remain necessary before acceptance. Inspect the combined whole, not each quadrant as if it were a separate building.

## Import and combined inspection

1. Import all four quadrant files into separate VOXORA tabs/projects.
2. Use the offsets above as the exact global placement coordinates.
3. Inspect the portal openings across the NW/NE and SW/SE seams.
4. Inspect the dome and drum in the combined central view; each quadrant only contains a quarter of those forms.
5. Send screenshots of the four quadrants and the combined view if VOXORA offers a merge/assembly workflow. If it does not, we will use aligned inspection windows and the global-coordinate manifest; do not hand-assemble by guessing.

## Next review checklist

- Lower dome shoulder visible and connected to the drum.
- Roof terrace closes the former gap around the dome.
- North/south gateway is genuinely open through the wall.
- Wall buttresses and pilasters read as deliberate architecture, not random decoration.
- Corner turret roofs and crowns are complete.
- No unintended collisions or seam gaps.
