# Arabian Palace — Project Ledger

This is the continuity record and source of truth for the Arabian Palace project.
Update this file whenever a module is created, revised, validated, positioned, or assembled.
A new chat must resume from this ledger and the linked master plan, not from guesses or memory alone.

## Canonical design document

- Master plan: [palace_master_plan_v01.md](palace_master_plan_v01.md)
- Overall planning envelope: 241 × 241 blocks, global X/Z coordinates -120…+120.
- Origin: centre of central keep; symmetry planes X=0 and Z=0.
- Main keep planning footprint: 89 × 89.
- Four inner towers: centres (0,-72), (72,0), (0,72), (-72,0), planned footprint 27 × 27 each.
- Eight perimeter towers: centres (±96,±40) and (±40,±96), planned footprint 21 × 21 each.
- Great dome target peak: approximately Y=108–116; validate silhouette before finalizing.
- Style: ivory/quartz, deep crimson dome/roofs, restrained gold/yellow, muted bronze/copper.
- Target game for actual building: Minecraft Bedrock on PS5. VOXORA Java project is for design/inspection; check block compatibility before recommending manual placement.

## Non-negotiable workflow rules

1. The palace is always designed and reviewed as one complete global-coordinate composition.
2. Every module must have a unique module ID, filename, purpose, global origin/offset, local bounds, vertical range, and neighbour/connection list.
3. Never create a module in isolation without checking the master plan and its adjacent modules.
4. After every module, update this ledger with its version, block count, bounds, material list, validation status, and GitHub link.
5. Keep a coordinate-level placement manifest for every accepted module. Use it to test duplicate coordinates, intersections, missing joins, and symmetry.
6. Before declaring a group complete, assemble a combined inspection model or equivalent global-coordinate preview. If the full model exceeds VOXORA limits, create overlapping inspection windows/sections; do not shrink or distort the design.
7. Inspect the whole silhouette from top, all four sides, and oblique views. Check that roofs, crowns, galleries, foundations, and transitions are present.
8. Do not ask the user to solve module placement or alignment. Provide a numbered assembly sequence with exact offsets and orientation, and guide each step.
9. Do not overwrite or delete earlier project files. New revisions receive new filenames/versions unless the user explicitly approves replacement.
10. A module is not marked accepted merely because GitHub upload succeeded. It must also import correctly and pass geometry checks.

## Current module register

| ID | Module | Status | Notes |
|---|---|---|---|
| REF-ASHEN | Ashen Spire test | Reference only | Imported successfully; format reference, not palace geometry |
| OLD-KEEP-01 | Central keep V01 | Historical / do not assume accepted | Earlier sandstone prototype |
| OLD-KEEP-02 | Central keep V02 | Historical / do not assume accepted | Earlier 61×61 prototype; not the new master-scale keep |
| OLD-KEEP-03 | Central keep V03 | Rejected | Invalid/unreliable block state field; do not use |
| OLD-KEEP-04 | Central keep V04 | Unverified / do not assemble | Upload recorded, but content fetch returned empty; 40,209 placements claimed, 61×61 footprint, height 76 |
| KEEP-PROTOTYPE-01 | New central keep prototype | Not started | Must follow master plan; prototype scale/silhouette, not compressed to 64×64 |
| INNER-TOWER-01 | Inner tower master | Not started | One complete full-size tower, including roof, balconies and crown; mirror only after validation |
| GALLERY-* | Gallery links | Not started | Exact endpoints and widths to be coordinated with keep and towers |
| OUTER-TOWER-* | Eight perimeter towers | Not started | Eight placements on the outer ring |
| WING-* | Wings / pavilions | Not started | Build from mirrored, globally coordinated pairs |
| ENTRANCE-01 | Main entrance | Not started | Centred on south axis |
| GARDEN-* | Gardens / courtyards | Not started | Last phase, after architecture and circulation are fixed |

## Accepted project format

Known working VOXORA JSON structure:
- format: `voxora-project`
- version: `1`
- app: `VOXORA Studio`
- game: `minecraft`
- mcVersion: `1.21.11`
- blocks: arrays `[x,y,z,"minecraft:block_id",0]`
- Use numeric state `0` in the final field, as in the verified Ashen Spire project.
- Validate actual block identifiers and Bedrock compatibility separately.
- VOXORA projects must respect the editor's per-project 64×64×96 limits. The palace itself is not limited to those dimensions.

## Assembly and collision protocol

For every accepted module:
- Record its global placement transform: translation (X,Y,Z), rotation, and mirror state.
- Convert every occupied block to global coordinates.
- Check for duplicate occupied coordinates between modules. Any overlap must be explicitly designed and documented; otherwise it is a defect.
- Check intended connections: gallery-to-keep, gallery-to-tower, wall-to-tower, stairs/doors and roof transitions.
- Check unintended gaps, floating blocks, unsupported spans, buried entrances, blocked circulation, and inconsistent floor heights.
- Generate an overall plan/top-down view and sectional/elevation inspections.
- Where a single VOXORA file cannot contain the whole palace, create coordinated inspection windows that show the same global coordinates and deliberately include enough neighbouring geometry to inspect seams.
- Give the user an exact assembly guide with module filenames, offsets, orientations, and order. Walk through it one step at a time.

## New-chat continuation instruction

When continuing in a new conversation, the user can provide this repository link:
https://github.com/furiusITA/Arabian-Palace-3D-V7

Resume by reading this ledger and the master plan. Then inspect the latest module files and continue from the first item marked Not started or In progress. Do not restart the design, silently change coordinates, or treat historical/rejected modules as accepted.

## Current checkpoint — 2026-11-20

- Master architectural plan v01 created and verified in GitHub.
- Overall layout and coordinate system established.
- Central keep prototype v01 created as four VOXORA quadrant files: `central_keep_v01_nw.json`, `central_keep_v01_ne.json`, `central_keep_v01_sw.json`, `central_keep_v01_se.json` (historical; superseded by v02).
- Each quadrant contains 21,017 placements; combined global map contains 82,762 unique occupied coordinates and has 0 symmetry lookup failures across X=0 and Z=0.
- Assembly guide: `central_keep_v01_assembly_guide.md` (historical; superseded by v02).
- GitHub upload and content retrieval succeeded. VOXORA import and visual inspection by the user are still pending; do not mark the prototype visually accepted yet.
- Central keep prototype v02 created as four replacement quadrants: `central_keep_v02_nw.json`, `central_keep_v02_ne.json`, `central_keep_v02_sw.json`, `central_keep_v02_se.json`.
- v02 geometry contains 115,727 unique occupied global block coordinates; 0 symmetry failures; 0 blocks obstructing the north/south gate passages. The dome shoulder and drum are expanded, roof terrace connected, facade pilasters/buttresses/string courses added, and north/south portal openings cut through all wall layers.
- v02 assembly guide: `central_keep_v02_assembly_guide.md`.
- GitHub file creation succeeded for all four v02 files. The fetch service returned empty content for these large JSON files, so post-upload content retrieval could not be completed; treat GitHub upload as successful but not independently re-read. VOXORA visual inspection remains pending.
- Next action: user imports v02 quadrants and shares views; review dome transition, portals, facade rhythm, corner turrets and seams before moving to inner towers.
