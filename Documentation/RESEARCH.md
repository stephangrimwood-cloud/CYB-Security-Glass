---

### Shape Controller Crafting

#### Objective

Determine how vanilla Shape Controllers are crafted.

Early production recipes attempted to craft the Shape Controller directly.

Example:

```xml
<recipe name="cybSecurityWindowShapes">
```

Result:

❌ Failed

The engine reported:

```
No item/block with name 'cybSecurityWindowShapes' existing
```

---

### Investigation

Comparison against vanilla recipes revealed an important implementation detail.

Vanilla Shape Controllers are **not** crafted directly.

Example:

```
woodShapes
```

Recipe:

```xml
<recipe name="woodShapes:VariantHelper">
```

The Shape Controller automatically generates a helper object used for crafting and inventory handling.

The same behaviour applies to custom Shape Controllers.

Production implementation:

```xml
<recipe name="cybSecurityWindowShapes:VariantHelper">
```

---

### Confirmed Behaviour

Shape Controller

```
cybSecurityWindowShapes
```

↓

Automatically generates

```
cybSecurityWindowShapes:VariantHelper
```

↓

Recipe crafts

```
VariantHelper
```

↓

Player selects desired shape

↓

Runtime block generated

---

### Result

The VariantHelper system is part of the standard vanilla Shape Controller architecture.

Custom Shape Controllers must craft the generated VariantHelper rather than the Shape Controller itself.

This behaviour exactly mirrors the vanilla implementation.

Status:

**PASS**

---

CYB-003 Research
================

Objective
---------
Custom icon for VariantHelper.

Engine Flow
-----------
...

Confirmed
---------
✔ CreateMaterialHelper creates VariantHelper.
✔ CreateProperties copies CustomIcon.
✔ ItemClassBlock copies Block.CustomIcon.
✔ GetIconName uses ItemClass.CustomIcon.

Outstanding
-----------
VariantHelper Block.CustomIcon is null.

Next Investigation
------------------
Determine where _shapeNames is built and where
VariantHelper Block.CustomIcon is lost.