# Materials Specification — Central Firmament

This document defines the materials to be created in Unreal Engine 5.7 for the Central Firmament game project. All materials should be placed in the `Content/Materials/` folder hierarchy.

---

## Naming Conventions

| Asset Type               | Prefix | Example                        |
|--------------------------|--------|-------------------------------|
| Material                 | `M_`   | `M_Rock_Granite`               |
| Material Instance        | `MI_`  | `MI_Rock_Granite_Dark`         |
| Material Function        | `MF_`  | `MF_BlendLayers`               |
| Material Parameter Collection | `MPC_` | `MPC_GlobalParams`        |

---

## Environment Materials (`Content/Materials/Environment/`)

These materials are used on terrain, architectural surfaces, and natural features in the game world.

### Terrain

| Asset Name               | Type              | Description                              | Notes                                    |
|--------------------------|-------------------|------------------------------------------|------------------------------------------|
| `M_Terrain_Grass`        | Master Material   | Grass ground cover                       | Supports wind displacement, PBR          |
| `MI_Terrain_Grass_Dry`   | Material Instance | Dried/dead grass variant                 | Derived from `M_Terrain_Grass`           |
| `MI_Terrain_Grass_Lush`  | Material Instance | Lush green variant                       | Derived from `M_Terrain_Grass`           |
| `M_Terrain_Dirt`         | Master Material   | Bare dirt/soil                           | PBR, supports wetness parameter          |
| `MI_Terrain_Dirt_Wet`    | Material Instance | Wet mud variant                          | Derived from `M_Terrain_Dirt`            |
| `M_Terrain_Rock`         | Master Material   | Rock/stone surfaces                      | PBR, supports multiple rock types        |
| `MI_Terrain_Rock_Granite`| Material Instance | Granite variant                          | Derived from `M_Terrain_Rock`            |
| `MI_Terrain_Rock_Slate`  | Material Instance | Slate/dark rock variant                  | Derived from `M_Terrain_Rock`            |

### Architecture / Built World

| Asset Name               | Type              | Description                              | Notes                                    |
|--------------------------|-------------------|------------------------------------------|------------------------------------------|
| `M_Concrete`             | Master Material   | Smooth and rough concrete                | PBR, supports cracks/damage              |
| `MI_Concrete_Smooth`     | Material Instance | Smooth poured concrete                   | Derived from `M_Concrete`               |
| `MI_Concrete_Rough`      | Material Instance | Rough/worn concrete                      | Derived from `M_Concrete`               |
| `M_Metal_Panel`          | Master Material   | Metal panel/sheet surfaces               | PBR, supports rust and patina            |
| `MI_Metal_Panel_Clean`   | Material Instance | Clean polished metal                     | Derived from `M_Metal_Panel`            |
| `MI_Metal_Panel_Rusted`  | Material Instance | Rusted worn metal                        | Derived from `M_Metal_Panel`            |
| `M_Wood_Plank`           | Master Material   | Wooden plank surfaces                    | PBR, supports grain direction            |
| `MI_Wood_Plank_Oak`      | Material Instance | Oak wood variant                         | Derived from `M_Wood_Plank`             |
| `MI_Wood_Plank_Pine`     | Material Instance | Pine wood variant                        | Derived from `M_Wood_Plank`             |
| `M_Glass`                | Master Material   | Glass/window surfaces                    | Translucent, supports reflections        |
| `MI_Glass_Clear`         | Material Instance | Clear glass                              | Derived from `M_Glass`                  |
| `MI_Glass_Frosted`       | Material Instance | Frosted/opaque glass                     | Derived from `M_Glass`                  |

### Foliage

| Asset Name               | Type              | Description                              | Notes                                    |
|--------------------------|-------------------|------------------------------------------|------------------------------------------|
| `M_Foliage_Tree_Leaf`    | Master Material   | Tree leaf material                       | Two-sided, supports wind, subsurface     |
| `MI_Foliage_Leaf_Green`  | Material Instance | Green summer leaves                      | Derived from `M_Foliage_Tree_Leaf`       |
| `MI_Foliage_Leaf_Yellow` | Material Instance | Yellow autumn leaves                     | Derived from `M_Foliage_Tree_Leaf`       |
| `M_Foliage_Bush`         | Master Material   | Bush/shrub foliage                       | Two-sided, subsurface scattering         |

### Water

| Asset Name               | Type              | Description                              | Notes                                    |
|--------------------------|-------------------|------------------------------------------|------------------------------------------|
| `M_Water_Ocean`          | Master Material   | Ocean/large water body surface           | Translucent, animated normals            |
| `M_Water_River`          | Master Material   | Flowing river/stream                     | Translucent, directional flow            |

---

## Character Materials (`Content/Materials/Characters/`)

Shared materials used for player characters and NPC characters not covered by existing mannequin materials.

| Asset Name               | Type              | Description                              | Notes                                    |
|--------------------------|-------------------|------------------------------------------|------------------------------------------|
| `M_Character_Skin`       | Master Material   | Human skin base material                 | Subsurface scattering, PBR               |
| `MI_Skin_Light`          | Material Instance | Light skin tone                          | Derived from `M_Character_Skin`          |
| `MI_Skin_Medium`         | Material Instance | Medium skin tone                         | Derived from `M_Character_Skin`          |
| `MI_Skin_Dark`           | Material Instance | Dark skin tone                           | Derived from `M_Character_Skin`          |
| `M_Character_Fabric`     | Master Material   | Clothing/fabric master material          | PBR, supports color tint parameter       |
| `MI_Fabric_Default`      | Material Instance | Default neutral clothing                 | Derived from `M_Character_Fabric`        |
| `M_Character_Armor`      | Master Material   | Hard armor/equipment surfaces            | PBR, metallic, supports damage           |
| `MI_Armor_Default`       | Material Instance | Default armor finish                     | Derived from `M_Character_Armor`         |
| `M_NPC_Default`          | Master Material   | Generic NPC material                     | Simple PBR, performance-optimized        |
| `MI_NPC_Hostile`         | Material Instance | Red-tinted hostile NPC variant           | Derived from `M_NPC_Default`             |
| `MI_NPC_Neutral`         | Material Instance | Neutral NPC variant                      | Derived from `M_NPC_Default`             |
| `MI_NPC_Friendly`        | Material Instance | Green-tinted friendly NPC variant        | Derived from `M_NPC_Default`             |

---

## Effects Materials (`Content/Materials/Effects/`)

Materials for visual effects, particle systems, and special emissive/glow effects.

| Asset Name               | Type              | Description                              | Notes                                    |
|--------------------------|-------------------|------------------------------------------|------------------------------------------|
| `M_FX_Emissive`          | Master Material   | Generic emissive glow material           | Additive blend, emissive intensity param |
| `MI_FX_Glow_Blue`        | Material Instance | Blue energy glow                         | Derived from `M_FX_Emissive`            |
| `MI_FX_Glow_Red`         | Material Instance | Red danger/energy glow                   | Derived from `M_FX_Emissive`            |
| `MI_FX_Glow_White`       | Material Instance | White/neutral glow                       | Derived from `M_FX_Emissive`            |
| `M_FX_Fire`              | Master Material   | Fire/flame effect material               | Additive, particle-ready                 |
| `M_FX_Smoke`             | Master Material   | Smoke effect material                    | Translucent, particle-ready              |
| `M_FX_Decal_Blood`       | Master Material   | Blood splatter decal                     | DBuffer decal type                       |
| `M_FX_Decal_Scorch`      | Master Material   | Scorch/burn mark decal                   | DBuffer decal type                       |
| `M_FX_Firmament`         | Master Material   | Central Firmament energy effect          | Emissive, animated UVs for the core VFX  |
| `MI_FX_Firmament_Core`   | Material Instance | Core Firmament glow variant              | Derived from `M_FX_Firmament`           |

---

## UI Materials (`Content/Materials/UI/`)

Materials used for HUD and UI elements.

| Asset Name               | Type              | Description                              | Notes                                    |
|--------------------------|-------------------|------------------------------------------|------------------------------------------|
| `M_UI_Base`              | Master Material   | Generic UI element material              | Unlit, supports opacity mask             |
| `MI_UI_Healthbar`        | Material Instance | Health bar fill material                 | Derived from `M_UI_Base`                |
| `MI_UI_StaminaBar`       | Material Instance | Stamina bar fill material                | Derived from `M_UI_Base`                |
| `M_UI_Glow`              | Master Material   | UI glow/pulse effect                     | Unlit, additive, animated               |

---

## Material Parameter Collections (`Content/Materials/`)

Global parameter collections for runtime material control.

| Asset Name                | Description                                           |
|---------------------------|-------------------------------------------------------|
| `MPC_GlobalParams`        | Global wind speed, time-of-day, and weather values    |
| `MPC_PostProcess`         | Post-process material parameters (vignette, contrast) |

---

## Existing Materials (Reference)

The following materials already exist in the project and should be used as a reference or starting point:

| Location                                                    | Asset                        | Purpose                    |
|-------------------------------------------------------------|------------------------------|----------------------------|
| `Content/Material/Cubes.uasset`                             | `Cubes`                      | Basic cube surface material |
| `Content/LevelPrototyping/Materials/M_PrototypeGrid.uasset` | `M_PrototypeGrid`            | Prototype grid material     |
| `Content/LevelPrototyping/Materials/M_FlatCol.uasset`       | `M_FlatCol`                  | Flat color material         |
| `Content/LevelPrototyping/Materials/MF_ProcGrid.uasset`     | `MF_ProcGrid`                | Procedural grid function    |
| `Content/LevelPrototyping/Materials/MI_DefaultColorway.uasset` | `MI_DefaultColorway`      | Default colorway instance   |
| `Content/LevelPrototyping/Materials/MI_PrototypeGrid_Gray.uasset` | `MI_PrototypeGrid_Gray` | Gray grid variant           |
| `Content/Characters/Mannequins/Materials/M_Mannequin.uasset`| `M_Mannequin`                | Mannequin base material     |
| `Content/Characters/Mannequins/Materials/Manny/MI_Manny_01_New.uasset` | `MI_Manny_01_New` | Manny variant 1           |
| `Content/Characters/Mannequins/Materials/Quinn/MI_Quinn_01.uasset` | `MI_Quinn_01`        | Quinn variant 1             |

---

## Creation Workflow

1. Open `AI_Test.uproject` in Unreal Engine 5.7.
2. Navigate to the target folder in the Content Browser (e.g., `Content/Materials/Environment`).
3. Right-click → **Create Basic Asset** → **Material** to create a new master material.
4. Name the material using the prefix conventions above.
5. For material instances, right-click the master material → **Create Material Instance**.
6. Set up parameters in the master material to enable variation in instances.
7. Save all assets with **Ctrl+Shift+S**.

Refer to [AssetNamingConventions.md](AssetNamingConventions.md) for full naming rules.
