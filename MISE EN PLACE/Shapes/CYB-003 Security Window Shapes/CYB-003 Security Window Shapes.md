# CYB-003 – Security Window Shapes

## Status

🟢 **Production Ready**

---

# Objective

Develop a complete library of CYB Security Window shapes that:

- Integrate seamlessly with the vanilla Shape Menu.
- Operate through the vanilla Shape Controller system.
- Preserve the vanilla architectural appearance.
- Utilise the proven CYB durability framework.
- Support the CYB downgrade and restoration workflow.
- Remain completely isolated from vanilla assets.
- Provide a consistent gameplay experience across every approved window shape.

---

# Design Philosophy

The CYB Security Window project follows a simple engineering philosophy.

> **Keep It Simple.**

Development followed a strict evidence-based methodology.

Every experiment consisted of:

1. One XML change.
2. Launch the game.
3. Observe the result.
4. Document the outcome.

Only confirmed behaviour was carried forward into production.

Wherever possible, the framework reuses existing vanilla systems rather than replacing them.

---

# Development History

## Experiment 001 — Custom Shape Creation

### Goal

Determine whether a completely custom shape could be created and loaded by the game.

### Result

✅ Success

A custom shape successfully loaded using only:

- A unique shape name.
- A valid model reference.

### Conclusion

The game requires surprisingly few properties for a custom shape to exist.

---

## Experiment 002 — Custom Shape Icon

### Goal

Determine whether a custom icon could be assigned to a shape.

### Result

✅ Success

The custom icon displayed correctly.

### Conclusion

Shape icons operate independently of the vanilla window definitions.

---

## Experiment 003 — Shape Categories

### Goal

Determine whether `ShapeCategories` controls placement within the Shape Menu.

### Result

✅ Success

The custom shape appeared in the correct Shape Menu category.

### Conclusion

`ShapeCategories` is required for proper organisation within the Shape Menu.

---

## Experiment 004 — Shape Menu Visibility

### Goal

Determine why the custom shape failed to appear within the Shape Menu.

### XML Added

```xml
<property name="Path" value="solid"/>
```

### Result

✅ Major Breakthrough

The shape:

- Appeared within the Shape Menu.
- Displayed correctly.
- Could be selected.
- Produced no XML errors.

### Conclusion

`Path="solid"` is the minimum requirement for a custom architectural window shape to appear within the Shape Menu.

This became the foundation of every subsequent CYB window.

---

## Experiment 005 — Placement Validation

### Goal

Validate in-game placement.

### Result

✅ Success

The custom window:

- Places correctly.
- Rotates correctly.
- Uses proper collision.
- Renders correctly.
- Produces no XML errors.

---

## Experiment 006 — Downgrade & Restoration

### Goal

Validate downgrade and restoration behaviour.

### Result

✅ Success

Damage sequence:

```text
Full Window
      │
      ▼
Broken Window
      │
      ▼
Destroyed
```

Restoration sequence:

```text
Broken Window
      │
      ▼
CYB Tempered Glass Panel
      │
      ▼
Full Window
```

### Conclusion

The complete CYB durability and restoration workflow was successfully validated.

---

## Experiment 007 — Vanilla Visual Restoration

### Goal

Restore the complete vanilla visual presentation while retaining the custom CYB gameplay systems.

### Imported Vanilla Properties

- UseGlobalUV
- ShapeAltTexture
- DowngradeFX
- CopyPaintOnDowngrade

### Result

✅ Success

The completed framework preserves:

- Vanilla charcoal frames.
- Vanilla broken glass.
- Vanilla glass shatter effects.
- Vanilla painting behaviour.

while maintaining the custom CYB durability framework.

### Conclusion

Rather than replacing vanilla behaviour, the CYB framework intentionally extends it.

---

## Experiment 008 — Shape Controller Migration

### Goal

Replace the prototype helper architecture with the vanilla Shape Controller system.

### Result

✅ Major Architectural Breakthrough

The dedicated Shape Controller successfully:

- Generated all runtime window variants.
- Integrated with the vanilla Shape Menu.
- Preserved repair behaviour.
- Preserved durability behaviour.
- Preserved upgrade behaviour.
- Eliminated the requirement for the prototype helper block.

### Conclusion

The project now utilises a dedicated Shape Controller and Shape Family architecture equivalent to the vanilla building system.

---

## Experiment 009 — Runtime Durability

### Goal

Validate the runtime durability calculation used by the Shape Controller.

### Result

✅ Success

Runtime durability is calculated using:

```text
Material MaxDamage
        ×
MaterialHitpointMultiplier
```

The Shape Menu displays the material's base durability while each generated window receives its own calculated runtime durability.

### Conclusion

The durability system operates exactly as intended by the vanilla Shape Controller architecture.

---

## Experiment 010 — Hidden Helper Icon Source

### Goal

Provide the Shape Controller helper block with a dedicated CYB icon without displaying an additional selectable shape.

### Result

✅ Major Breakthrough

A hidden internal helper shape successfully:

- Supplies the VariantHelper icon.
- Remains hidden from the Shape Menu.
- Does not appear in the player-facing shape list.
- Preserves all visible production window shapes.

### XML Discovery

```xml
<property name="ShapeMenu" value="false"/>
```

### Conclusion

The vanilla `ShapeMenu` property allows internal helper shapes to remain hidden while still participating in the Shape Controller architecture.

This enables a dedicated helper icon without affecting the player experience.

---

# Production Shape Standard

Every approved CYB Security Window follows the same engineering standard.

## Full Window

- Appears within the Windows Shape Menu.
- Uses a vanilla architectural model.
- Uses the appropriate vanilla window icon.
- Preserves the vanilla visual appearance.
- `MaterialHitpointMultiplier = 0.5`
- Downgrades to its Broken variant.
- Uses vanilla glass shatter effects.

---

## Broken Window

- Hidden from the Shape Menu.
- `MaterialHitpointMultiplier = 0.333`
- Displays the damaged frame.
- Uses vanilla frame textures.
- Restored using:

```text
CYB Tempered Glass Panel
```

One panel restores one complete window.

---

# Shape Controller Integration

All approved CYB windows are generated through:

```text
cybSecurityWindowShapes
```

The Shape Controller provides shared:

- Material
- Repair behaviour
- Sounds
- Harvest behaviour
- Shape Menu integration
- Gameplay behaviour

Individual shapes define only their own geometry and unique visual properties.

---

# Helper Architecture

The Shape Controller uses a hidden internal helper shape:

```text
cybWindowIconDummy
```

This internal shape:

- Supplies the VariantHelper icon.
- Remains hidden from the Shape Menu.
- Is never selectable by the player.
- Has no gameplay purpose beyond supporting the helper architecture.

This allows the helper block to maintain its own dedicated CYB icon while every visible production shape retains its own individual window icon.

---

# Production Shape Collection

Current implementation includes:

- Store Windows
- Industrial Windows
- Circular Windows
- Arch Windows
- Plate Windows
- Ramp Windows
- Wedge Windows
- Corner Windows
- Triangle Windows
- Additional architectural window variants

All approved shapes utilise the same CYB durability framework.

---

# Current Production Framework

Every production window now provides:

- Consistent durability
- Consistent downgrade behaviour
- Consistent repair behaviour
- Consistent restoration workflow
- Consistent visual presentation
- Consistent player experience

The framework has been validated across the complete production shape library.

---

# Confirmed Requirements

A production-ready CYB window requires:

- Unique shape name
- Valid model reference
- `Path="solid"`
- `CustomIcon`
- `ShapeCategories`
- `MaterialHitpointMultiplier`
- `DowngradeBlock` (where applicable)
- `UpgradeBlock` (broken variants)
- Standardised durability values
- Standardised upgrade behaviour

---

# Lessons Learned

The project reinforced several important engineering principles.

- Keep It Simple.
- Test one XML change at a time.
- Never assume vanilla behaviour.
- Build from confirmed working XML.
- Document discoveries immediately.
- Expand only from proven foundations.
- Reuse vanilla systems wherever possible.

The most significant technical discoveries were:

```xml
<property name="Path" value="solid"/>
```

and

```xml
<property name="ShapeMenu" value="false"/>
```

Together with the Shape Controller architecture, these discoveries provide a scalable foundation for every future CYB window.

---

# Current Outcome

The CYB Security Window Shape Framework is production ready.

The framework provides:

- Complete vanilla architectural appearance.
- Standardised durability across all approved shapes.
- Glass-to-frame downgrade behaviour.
- Tempered Glass Panel restoration.
- Unified repair workflow.
- Unified Shape Menu integration.
- Dedicated Shape Controller architecture.
- Hidden helper icon architecture.
- Production-ready foundation for future CYB window expansion.

---

# Future Development

Possible future expansion includes:

- Decorative stained glass collections.
- Additional architectural window styles.
- Custom CYB window models.
- Premium glazing systems.
- Additional CYB construction products.

These are considered future enhancements and are not required for Version 1.

---

# Version 1 Completion

The CYB Security Window Shape Framework has successfully progressed from research and experimentation into a fully validated production Shape Controller system.

The completed framework demonstrates that advanced architectural window systems can be implemented entirely through vanilla XML while remaining:

- Fully XML-driven
- EAC compatible
- Client/server compatible
- Harmony free
- Easily expandable

The completed architecture now serves as the technical foundation for every future CYB Security Window released as part of the CYB Security Glass project.