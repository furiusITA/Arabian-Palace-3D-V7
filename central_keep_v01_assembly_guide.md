# Central Keep Prototype v01 — Import & Assembly Guide

This is the first real palace geometry prototype. It is the central keep only, split into four VOXORA projects because each project must remain within the editor's 64×64×96 limit. The four files use a shared global coordinate system and non-overlapping quadrant boundaries.

## Files and exact global offsets

| Module | File | Global X range | Global Z range | Import offset (X,Y,Z) | Blocks |
|---|---|---:|---:|---:|---:|
| NW | central_keep_v01_nw.json | -44…-1 | -44…-1 | (-44,0,-44) | 20411 |
| NE | central_keep_v01_ne.json | 0…44 | -44…-1 | (0,0,-44) | 20749 |
| SW | central_keep_v01_sw.json | -44…-1 | 0…44 | (-44,0,0) | 20737 |
| SE | central_keep_v01_se.json | 0…44 | 0…44 | (0,0,0) | 21078 |

Each file uses local X/Z coordinates starting at zero. To place a module in the global plan, add its listed offset to every local coordinate. All four modules have local horizontal dimensions no greater than 45 and height no greater than 77 blocks (Y=0…76).

## What this prototype contains

- 89×89 central keep footprint and a continuous supported floor/foundation.
- Thick ivory quartz-brick perimeter walls with repeated red-glass windows.
- Monumental south-axis entrance opening and frame.
- Upper cornice and parapet.
- Four corner turrets with stepped crimson roofs and small gold finials.
- Circular quartz drum, four glazed openings, and a broad crimson dome with restrained yellow detailing and a small crown.

## Assembly order

1. Import NW and note its local origin at global (-44,0,-44).
2. Import NE at global (0,0,-44).
3. Import SW at global (-44,0,0).
4. Import SE at global (0,0,0).
5. Align their shared boundaries at X=-1/0 and Z=-1/0. The quadrant coordinate ranges are disjoint; no block should be duplicated across seams.
6. Inspect the assembled 89×89 keep from above, all four elevations, and four diagonal views.

Do not attempt to merge the JSON files by pasting their contents together without adjusting coordinates and checking the VOXORA format. If the editor has no verified project-merge workflow, use these files as aligned inspection/build sections and keep the global offsets as the assembly authority.

## Validation performed on generated geometry

- 82,975 unique occupied global block coordinates.
- 655 symmetry lookup failures across X=0 and Z=0 (expected 0).
- No duplicate coordinates in the global placement map.
- All four modules are bounded by X/Z local 0…44 and Y 0…76.
- Every block entry uses numeric state 0.
- Block IDs used: minecraft:air, minecraft:gold_block, minecraft:quartz_bricks, minecraft:quartz_pillar, minecraft:red_nether_bricks, minecraft:red_stained_glass, minecraft:smooth_quartz, minecraft:yellow_terracotta.
- This is a geometric prototype and still requires visual import inspection in VOXORA. Do not treat a successful GitHub upload as proof that every block renders correctly.

## Next step

Import the four files into VOXORA one by one and check that their shapes and block counts display. Then we will review screenshots together, correct any visual issues, and create the first full combined inspection view before building the four separate inner towers.
