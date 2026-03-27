# Asset Naming Conventions — Central Firmament

This document defines the naming conventions for all assets in the Central Firmament Unreal Engine 5.7 project. Consistent naming helps the team find and manage assets efficiently.

---

## General Rules

- Use **PascalCase** (e.g., `M_Rock_Granite`, `BP_PlayerCharacter`).
- Always start with the **type prefix** listed below.
- Use underscores (`_`) to separate prefix, base name, and variant.
- Keep names descriptive but concise.
- Avoid spaces and special characters.

---

## Prefix Reference Table

| Asset Type                      | Prefix   | Example                             |
|---------------------------------|----------|-------------------------------------|
| **Blueprint**                   | `BP_`    | `BP_ThirdPersonCharacter`           |
| **Blueprint Interface**         | `BPI_`   | `BPI_Interactable`                  |
| **Animation Blueprint**         | `ABP_`   | `ABP_Unarmed`                       |
| **Animation Montage**           | `AM_`    | `AM_Pistol_Fire`                    |
| **Animation Sequence**          | `MM_`    | `MM_Rifle_Jump_Start`               |
| **Blend Space**                 | `BS_`    | `BS_Idle_Walk_Run`                  |
| **Motion Field (Blend Space)**  | `MBF_`   | `MBF_Pistol_Jog_Fwd`                |
| **Aim Offset**                  | `AO_`    | `AO_Pistol`                         |
| **Material**                    | `M_`     | `M_Terrain_Rock`                    |
| **Material Instance**           | `MI_`    | `MI_Terrain_Rock_Granite`           |
| **Material Function**           | `MF_`    | `MF_ProcGrid`                       |
| **Material Parameter Collection**| `MPC_`  | `MPC_GlobalParams`                  |
| **Texture 2D**                  | `T_`     | `T_Rock_Granite_D` (diffuse)        |
| **Texture Cube**                | `TC_`    | `TC_Sky_HDRI`                       |
| **Static Mesh**                 | `SM_`    | `SM_Rock_01`                        |
| **Skeletal Mesh**               | `SK_`    | `SK_Mannequin`                      |
| **Particle System (Niagara)**   | `NS_`    | `NS_Fire_Small`                     |
| **Sound Wave**                  | `SW_`    | `SW_Footstep_Dirt`                  |
| **Sound Cue**                   | `SC_`    | `SC_Footstep_Dirt`                  |
| **Widget Blueprint**            | `WBP_`   | `WBP_HUD`                           |
| **Data Table**                  | `DT_`    | `DT_WeaponStats`                    |
| **Data Asset**                  | `DA_`    | `DA_CharacterConfig`                |
| **Input Mapping Context**       | `IMC_`   | `IMC_Default`                       |
| **Input Action**                | `IA_`    | `IA_Jump`                           |
| **Level**                       | (none)   | `AI_TestMap`, `Level_Connor`        |
| **Material Instance (Dynamic)** | `MID_`   | `MID_Character_Skin`                |

---

## Texture Suffix Conventions

Append a suffix to the end of texture names to indicate the channel/map type:

| Suffix | Channel/Map      | Example                        |
|--------|-----------------|--------------------------------|
| `_D`   | Diffuse/Albedo   | `T_Rock_Granite_D`             |
| `_N`   | Normal Map       | `T_Rock_Granite_N`             |
| `_R`   | Roughness        | `T_Rock_Granite_R`             |
| `_M`   | Metallic         | `T_Metal_Panel_M`              |
| `_AO`  | Ambient Occlusion| `T_Rock_Granite_AO`            |
| `_E`   | Emissive         | `T_Firmament_Core_E`           |
| `_ORM` | Occlusion/Roughness/Metallic (packed) | `T_Rock_Granite_ORM` |
| `_H`   | Height/Displacement | `T_Rock_Granite_H`          |
| `_MASK`| Mask             | `T_Foliage_Leaf_MASK`              |

---

## Folder Structure

Assets should be organized in the Content Browser under the following folders:

```
Content/
├── AI/
│   └── NPC/                         # NPC Blueprints and AI Controllers
├── Characters/
│   └── Mannequins/
│       ├── Anims/                   # Animations (grouped by weapon type)
│       ├── Materials/               # Character-specific materials
│       ├── Meshes/                  # Skeletal meshes
│       ├── Rigs/                    # Control rigs
│       └── Textures/                # Character textures
├── Input/
│   ├── Actions/                     # Input Actions (IA_)
│   └── Touch/                       # Touch input mappings
├── LevelPrototyping/
│   ├── Interactable/                # Interactive prop assets
│   ├── Materials/                   # Prototype/blockout materials
│   ├── Meshes/                      # Prototype meshes
│   └── Textures/                    # Prototype textures
├── Material/                        # Legacy/shared single-use materials
├── Materials/                       # Shared game materials (new)
│   ├── Environment/                 # Terrain, rock, foliage, water, architecture
│   ├── Characters/                  # Shared skin, fabric, armor materials
│   ├── Effects/                     # VFX, emissive, decal materials
│   └── UI/                          # HUD and UI materials
└── ThirdPerson/
    ├── Blueprints/                  # Third-person template BPs
    └── Lvl_ThirdPerson.umap
```

---

## Examples

### Good Names ✅
- `M_Terrain_Grass` — master terrain grass material
- `MI_Terrain_Grass_Dry` — dry variant material instance
- `T_Rock_Granite_D` — granite diffuse texture
- `SM_Rock_Medium_01` — medium rock static mesh, variant 01
- `BP_NPC_Patrol` — NPC patrol blueprint
- `NS_FX_Explosion_Small` — small explosion Niagara system

### Bad Names ❌
- `Material1` — no prefix, not descriptive
- `rock mat` — spaces not allowed
- `NewBlueprint_Copy` — not descriptive
- `T_texture` — redundant and not descriptive
- `BluePrint_NPC` — wrong case for prefix

---

## Version Numbering

When multiple variants or iterations of the same asset exist, append a two-digit number:

- `SM_Rock_01`, `SM_Rock_02`, `SM_Rock_03`
- `MI_Manny_01`, `MI_Manny_02`

---

## Level Naming

Levels do not use a prefix. Use descriptive names that indicate their purpose:

- `AI_TestMap` — AI testing level
- `Level_Connor` — Connor character sub-level
- `MAIN` — Primary gameplay level
- `Lvl_ThirdPerson` — Third-person prototype level (legacy naming, keep as-is)
