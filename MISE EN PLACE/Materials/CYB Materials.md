# CYB Materials

## Status

🟢 Production Ready

---

# Objective

Develop custom CYB material definitions that provide independent control over durability, sounds and physical behaviour while remaining fully compatible with the vanilla engine.

Rather than modifying vanilla materials directly, CYB materials selectively reuse proven vanilla behaviour while applying CYB-specific balancing where required.

This approach provides complete independence from future vanilla balancing changes.

---

# Design Philosophy

The CYB Material System follows a simple engineering philosophy.

> Keep It Simple.

Materials are designed to:

- Reuse proven vanilla behaviour.
- Support the vanilla Shape Controller system.
- Remain isolated from vanilla material definitions.
- Provide consistent gameplay across every CYB product.

Every material is validated through practical in-game testing before being approved for production use.

---

# Current Material

## McybSecurityWindow

### Purpose

Custom material developed specifically for the CYB Security Window system.

Designed to provide:

- Metal impact behaviour.
- Shared Shape Controller durability.
- Vanilla-compatible physical properties.
- Consistent structural behaviour.
- Independence from future vanilla balancing.

---

# Material Definition

```xml
<material id="McybSecurityWindow">
    <property name="damage_category" value="metal"/>
    <property name="surface_category" value="metal"/>
    <property name="forge_category" value="iron"/>
    <property name="Hardness" type="float" value="1"/>
    <property name="stepsound" value="metal"/>
    <property name="stability_glue" value="300"/>
    <property name="Mass" type="int" value="20"/>
    <property name="explosionresistance" value="0.5"/>
    <property name="MaxDamage" value="3000"/>
    <property name="Experience" value="2"/>
</material>
```

---

# Durability System

The material provides the base durability for the complete CYB Security Window Shape Family.

```
Material MaxDamage

3000
```

The vanilla Shape Controller calculates runtime durability using:

```
Material MaxDamage
        ×
MaterialHitpointMultiplier
```

Resulting runtime durability:

| Window State | MaterialHitpointMultiplier | Effective HP |
|--------------|---------------------------:|-------------:|
| Full Window | 0.5 | 1500 HP |
| Broken Window | 0.333 | 999 HP |

The Shape Menu displays the material durability (3000).

Players interact only with the calculated runtime durability of each generated window.

---

# Validated Behaviour

Confirmed in-game:

- ✅ Metal impact sounds.
- ✅ Metal placement sounds.
- ✅ Glass shatter effects retained.
- ✅ Compatible with Shape Controller architecture.
- ✅ Compatible with custom downgrade workflow.
- ✅ Compatible with custom upgrade workflow.
- ✅ Compatible with CYB Security Resin repairs.
- ✅ Compatible with CYB Tempered Glass Panel restoration.
- ✅ Runtime durability generated correctly.
- ✅ Shape Menu integration validated.

---

# Physical Properties

The material provides:

- Metal damage category.
- Metal surface category.
- Iron forge category.
- Standard hardness.
- Metal footstep sounds.
- Structural stability.
- Moderate explosion resistance.
- Shared durability source.
- Experience rewards.

These values are intentionally conservative and designed to complement the existing vanilla balance rather than replace it.

---

# Current Usage

| Product | Material |
|----------|----------|
| CYB-003 Security Window Shape Family | `McybSecurityWindow` |

---

# Design Philosophy

The CYB Material System is based upon proven vanilla behaviour rather than replacing it.

Vanilla materials are investigated, understood and selectively adapted to meet the design goals of each CYB product.

This provides:

- Independent balancing.
- Consistent gameplay.
- Vanilla compatibility.
- Easier long-term maintenance.
- Reusable material definitions.
- Scalable architecture for future CYB products.

---

# Future Expansion

The CYB Material System is intended to support future products throughout the CYB ecosystem.

Potential future materials include:

- `McybBlastDoor`
- `McybSecurityShutter`
- `McybCompositeWall`
- Additional specialist materials as required.

Each future material will follow the same development methodology established during CYB-003.

---

# Lessons Learned

Development confirmed several important principles.

- Build from proven vanilla behaviour.
- Validate every property through testing.
- Separate materials from gameplay logic.
- Allow the Shape Controller to calculate runtime durability.
- Keep material definitions reusable.
- Extend vanilla systems rather than replacing them.

The investigation into Shape Controller durability confirmed that the material acts as the shared durability source for every generated runtime shape.

---

# Current Outcome

The CYB Material System has successfully progressed from research and experimentation into a production-ready reusable framework.

The completed material system now provides:

- Shared durability balancing.
- Shared physical behaviour.
- Shared audio behaviour.
- Complete Shape Controller compatibility.
- Independent balancing from vanilla materials.
- A scalable foundation for future CYB construction products.

---

# Version 1 Completion

The CYB Material System has successfully established the first reusable CYB material framework.

`McybSecurityWindow` now serves as the production foundation for the complete CYB Security Window Shape Family while demonstrating the methodology that will be used for all future CYB material development.