# Central Firmament

An Unreal Engine 5.7 third-person action game featuring AI-driven NPCs, dynamic environments, and interactive gameplay.

## Project Overview

Central Firmament is a third-person action game built on Unreal Engine 5.7. The game features:
- AI-driven NPC characters with custom controllers
- Third-person character movement and combat
- Interactable level elements (doors, jump pads, targets)
- Multiple character sub-levels: Connor, Dakota, Joaquin, and VAL

## Repository Structure

```
Central_Firmament/
├── Config/                          # Engine and game configuration
│   ├── DefaultEditor.ini
│   ├── DefaultEngine.ini
│   ├── DefaultGame.ini
│   └── DefaultInput.ini
├── Content/                         # All game assets
│   ├── AI/                          # AI behavior assets
│   │   └── NPC/                     # NPC blueprints and controllers
│   ├── Characters/                  # Character assets
│   │   └── Mannequins/
│   │       ├── Anims/               # Character animations (unarmed, pistol, rifle)
│   │       ├── Materials/           # Character materials (Manny, Quinn)
│   │       ├── Meshes/              # Skeletal meshes
│   │       ├── Rigs/                # Rigging data
│   │       └── Textures/            # Character textures
│   ├── Input/                       # Input mapping contexts and actions
│   ├── LevelPrototyping/            # Prototype assets for level design
│   │   ├── Interactable/            # Interactive props (doors, jump pads, targets)
│   │   ├── Materials/               # Prototype grid and flat-color materials
│   │   ├── Meshes/                  # Prototype meshes
│   │   └── Textures/                # Prototype textures
│   ├── Materials/                   # Shared game materials (see Materials section)
│   │   ├── Environment/             # Terrain, rock, foliage, water materials
│   │   ├── Characters/              # Shared character and skin materials
│   │   ├── Effects/                 # VFX and emissive materials
│   │   └── UI/                      # UI and HUD materials
│   ├── ThirdPerson/                 # Third-person template blueprints
│   └── *.umap                       # Level maps
└── Docs/                            # Project documentation
    ├── Materials.md                 # Material specifications and guidelines
    └── AssetNamingConventions.md    # Asset naming rules
```

## Getting Started

1. Install Unreal Engine 5.7 from the [Epic Games Launcher](https://www.epicgames.com/store/download).
2. Clone this repository.
3. Open `AI_Test.uproject` with Unreal Engine 5.7.
4. The editor will open with the `AI_TestMap` level.

## Team

| Member     | Area of Responsibility         |
|------------|-------------------------------|
| Connor     | Character sub-level            |
| Dakota     | Character sub-level            |
| Joaquin    | Character sub-level            |
| VAL        | Character sub-level            |
| JFVGMU2027 | Materials and Assets           |
| djustus1224| Whitebox Level Design          |
| ilyval04   | Map and Landscape              |

## Key Maps

| Map                     | Description                        |
|-------------------------|------------------------------------|
| `AI_TestMap.umap`       | Main AI testing level              |
| `MAIN.umap`             | Primary gameplay level             |
| `BIGMAIN.umap`          | Expanded main level                |
| `Level_Connor.umap`     | Connor character sub-level         |
| `Level_Dakota.umap`     | Dakota character sub-level         |
| `Level_Joaquin.umap`    | Joaquin character sub-level        |
| `Level_VAL.umap`        | VAL character sub-level            |
| `ThirdPerson/Lvl_ThirdPerson.umap` | Third-person prototype level |

## Asset Guidelines

Refer to [Docs/AssetNamingConventions.md](Docs/AssetNamingConventions.md) for the full naming convention guide.

Refer to [Docs/Materials.md](Docs/Materials.md) for the full material specification.
