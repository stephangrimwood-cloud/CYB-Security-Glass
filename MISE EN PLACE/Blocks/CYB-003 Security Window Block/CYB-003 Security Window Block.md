# CYB-003 – Security Windows

## Status

🟢 **Production Ready**

---

# Objective

Develop a production-ready CYB Security Window system using the vanilla Shape Controller architecture while integrating seamlessly with the CYB manufacturing chain.

The completed framework provides logical installation, durability, maintenance and restoration behaviour while preserving full compatibility with vanilla game systems.

Rather than replacing existing defensive blocks, CYB Security Windows are designed to expand architectural building options through a realistic manufacturing and maintenance workflow.

---

# Design Philosophy

CYB Security Windows follow a simple engineering philosophy:

> **Keep It Simple.**

Development followed a strict evidence-based methodology.

Every experiment consisted of:

1. One XML change.
2. One in-game test.
3. One confirmed result.
4. Documentation before continuing.

Only validated behaviour has been retained.

Wherever possible, existing vanilla systems have been reused rather than replaced.

---

# Production Overview

The completed framework provides:

- Dedicated Shape Controller
- Custom CYB Shape Family
- Independent durability balancing
- Two-stage destruction system
- Glass-to-frame downgrade
- Tempered glass restoration
- Manufacturing-based gameplay
- Vanilla-compatible Shape Menu integration
- Hidden helper icon architecture

---

# Shape Controller

Version 1 uses a dedicated Shape Controller.

```text
cybSecurityWindowShapes
```

The controller provides shared:

- Material behaviour
- Repair behaviour
- Sound behaviour
- Harvest behaviour
- Shape variant selection

Individual window models and gameplay behaviour are defined within:

```text
shapes.xml
```

The vanilla Shape Controller automatically generates every runtime block.

Crafting follows the standard vanilla Shape Controller architecture by targeting the automatically generated VariantHelper rather than the controller itself.

```text
cybSecurityWindowShapes
        │
        ▼
cybSecurityWindowShapes:VariantHelper
```

This mirrors the vanilla implementation used by helper blocks such as:

```text
woodShapes:VariantHelper
```

---

# Helper Architecture

The production Shape Controller uses a hidden internal helper shape to provide the VariantHelper icon.

```text
cybWindowIconDummy
```

This internal shape:

- Supplies the helper block icon.
- Is hidden from the Shape Menu.
- Is never visible to players.
- Does not affect the available window selections.

This allows the helper block to maintain its own dedicated CYB icon while every visible window shape retains its own individual shape icon.

This behaviour is achieved using the vanilla Shape property:

```xml
<property name="ShapeMenu" value="false"/>
```

No Harmony patches or custom code are required.

---

# Development Summary

The original prototype helper block:

```text
cybTestShapes
```

was used throughout development to validate every gameplay mechanic before migrating into the production Shape Controller.

Testing confirmed:

- Shape selection
- Placement
- Rotation
- Painting
- Collision
- Durability
- Downgrade
- Upgrade
- Repair
- Restoration
- Harvest behaviour
- Visual presentation

Once validated, the prototype helper architecture was retired in favour of the dedicated production Shape Controller.

---

# Durability System

## Base Material

All production windows derive their durability from:

```text
McybSecurityWindow
```

Base material durability:

```xml
MaxDamage="3000"
```

The Shape Menu displays the material durability.

Players never experience this value directly.

---

## Full Window

MaterialHitpointMultiplier

```text
0.5
```

Effective durability:

```text
1500 HP
```

When exhausted:

```text
Glass shatters
```

↓

```text
Broken Window
```

---

## Broken Window

MaterialHitpointMultiplier

```text
0.333
```

Effective durability:

```text
999 HP
```

Combined player-facing durability:

```text
2499 HP
```

Each runtime window calculates durability independently using its configured MaterialHitpointMultiplier.

---

# Maintenance Workflow

The complete maintenance system has been validated.

```text
Manufacture Window
        │
        ▼
Install Window
        │
        ▼
Window Receives Damage
        │
        ▼
Glass Shatters
        │
        ▼
Broken Window
        │
        ▼
Restore Using
CYB Tempered Glass Panel
        │
        ▼
Full Window Restored
```

If the supporting frame is destroyed:

```text
Broken Window
        │
        ▼
Destroyed
        │
        ▼
Recover Broken Glass
        │
        ▼
Manufacture Replacement Window
```

---

# Window Behaviour

## Full Window

- Metal impact sounds
- Vanilla glass shatter effects
- Downgrades to Broken Window
- Preserves paint
- Preserves appearance

---

## Broken Window

- Damaged frame remains visible
- Fully interactive
- Restored using:

```text
CYB Tempered Glass Panel
```

One panel restores one complete window.

---

# Manufacturing Chain

```text
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

Each manufactured component exists to produce the next, creating a logical industrial production chain.

---

# Product Philosophy

CYB Security Windows are manufactured architectural products.

They are:

- Manufactured
- Installed
- Maintained
- Restored
- Eventually replaced

They operate independently from the standard vanilla upgrade progression.

```text
Wood
 ↓
Cobblestone
 ↓
Concrete
 ↓
Steel
```

Instead, they represent a premium standalone construction system.

---

# Material Philosophy

## CYB Security Resin

Manufacturing material.

Used exclusively during production.

Not required for field maintenance.

---

## CYB Tempered Glass Panel

Manufactured glazing component.

Used for:

- Window maintenance
- Glass replacement
- Window restoration

It is the primary maintenance component carried by the player.

---

# Material System

Production windows use the custom material:

```text
McybSecurityWindow
```

This material provides:

- Metal impact sounds
- Base durability
- Structural stability
- Vanilla-compatible behaviour
- Independent balancing

Visual presentation continues to utilise vanilla window assets, preserving:

- Charcoal window frames
- Broken glass appearance
- Glass shatter effects
- Vanilla painting behaviour

---

# Shape Family

The completed Shape Family provides:

- Dedicated Shape Controller
- Shared gameplay behaviour
- Shared durability balancing
- Shared maintenance workflow
- Shared restoration workflow
- Expandable window library

Additional CYB window designs can now be added simply by creating new entries within the `CYBWindows` Shape Family.

---

# Balance Philosophy

CYB Security Windows are intended to improve architectural building rather than increase combat strength.

Design goals:

- Stronger than standard glass
- Suitable for decorative home bases
- Suitable for premium architectural builds
- Suitable for carefully planned horde bases
- Weaker than Bulletproof Glass
- Weaker than reinforced concrete or steel

The objective is improved building freedom rather than power creep.

---

# Technical Validation

The completed system has been validated for:

- Shape Controller integration
- Shape Menu integration
- Hidden helper icon architecture
- Shape selection
- Placement
- Rotation
- Painting
- Collision
- Runtime durability generation
- Downgrade
- Upgrade
- Restoration
- Harvesting
- Repair
- Material behaviour
- Nailgun compatibility
- VariantHelper crafting

All systems operate entirely through the vanilla Shape Controller, Shape Menu and repair pipeline.

No Harmony patches or custom DLLs are required.

---

# Current Outcome

CYB Security Windows have successfully evolved from an experimental prototype into a complete production-ready architectural glazing framework.

The completed system now provides:

- Dedicated Shape Controller
- Custom Shape Family
- Hidden helper icon architecture
- Complete manufacturing chain
- Consistent durability across every approved shape
- Standardised maintenance workflow
- Standardised restoration workflow
- Vanilla architectural appearance
- Distinct CYB gameplay identity

---

# Future Development

Possible future expansion includes:

- Decorative stained glass products
- Additional architectural window collections
- Custom CYB window models
- Premium glazing systems
- Additional CYB construction products

These are future enhancements and are not required for Version 1.

---

# Version 1 Completion

CYB-003 has successfully progressed from an experimental prototype into a complete production-ready Shape Controller framework.

Version 1 demonstrates that complex architectural construction products can be implemented entirely through the vanilla Shape Controller, Shape Menu and repair systems while remaining:

- Fully XML-driven
- EAC compatible
- Client/server compatible
- Harmony free
- Easily expandable

The completed architecture now serves as the foundation for every future CYB Security Window released as part of the CYB Security Glass project.