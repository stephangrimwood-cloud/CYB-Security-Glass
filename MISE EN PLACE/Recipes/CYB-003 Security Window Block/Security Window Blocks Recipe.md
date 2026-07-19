# CYB-003 – Security Window Recipe

## Status

🟢 Production Ready

---

# Overview

The CYB Security Window is the final manufactured product within the Version 1 CYB Security Glass production chain.

Unlike conventional blocks, the Security Window is produced using the vanilla Shape Controller system.

The crafted item is the automatically generated **VariantHelper**, allowing full integration with the vanilla Shape Menu.

---

# Production Recipe

```xml
<recipe name="cybSecurityWindowShapes:VariantHelper"
        count="1"
        craft_area="workbench"
        craft_time="40"
        tags="perkAdvancedEngineering">

    <ingredient name="resourceForgedIron" count="10" />
    <ingredient name="cybTemperedGlassPanel" count="2" />
    <ingredient name="cybSecurityResin" count="1" />
    <ingredient name="resourceMechanicalParts" count="4" />

</recipe>
```

---

# Manufacturing Requirements

| Component | Quantity | Purpose |
|-----------|---------:|---------|
| Forged Iron | 10 | Structural frame |
| CYB Tempered Glass Panel | 2 | Security glazing |
| CYB Security Resin | 1 | Industrial bonding |
| Mechanical Parts | 4 | Window hardware |

---

# Production Location

Workbench

---

# Craft Time

```
40 seconds
```

The longer production time reflects the specialist nature of the product while remaining practical for normal gameplay.

---

# Product Output

```
1 × CYB Security Window
```

The player receives a single Shape Controller helper item capable of placing every approved CYB Security Window shape.

---

# VariantHelper Architecture

The most significant discovery during development was the way vanilla Shape Controllers are crafted.

The Shape Controller itself is **not** the crafted item.

```
cybSecurityWindowShapes
```

Instead, the recipe targets the automatically generated helper object:

```
cybSecurityWindowShapes:VariantHelper
```

This mirrors the vanilla implementation used throughout the game.

Example:

```
woodShapes
        │
        ▼
woodShapes:VariantHelper
```

The VariantHelper stores the selected shape variant while integrating seamlessly with the vanilla Shape Menu.

---

# Manufacturing Chain

```
Broken Glass
      │

Glue
Polymers
      │
      ▼

CYB Security Resin
      │
      ▼

CYB Tempered Glass Panel
      │
      ▼

CYB Security Window
```

Each manufactured product exists to produce the next, creating a logical industrial workflow.

---

# Gameplay Philosophy

The Security Window is intended to feel like a manufactured architectural product rather than an upgraded building block.

Players:

- Manufacture the product.
- Install the product.
- Maintain the product.
- Restore damaged glazing.
- Replace destroyed units.

This approach preserves the vanilla upgrade progression while introducing a dedicated construction product.

---

# Technical Validation

The production recipe has been validated for:

- Correct VariantHelper generation.
- Workbench crafting.
- Correct inventory item.
- Shape Menu integration.
- Placement.
- Rotation.
- Shape selection.
- Durability.
- Repair workflow.
- Restoration workflow.

No Harmony patches or custom DLLs are required.

---

# Production Status

The CYB Security Window recipe is now fully production-ready and mirrors the vanilla Shape Controller crafting architecture used throughout 7 Days to Die.