# CYB-004 Industrial Toolkit Recipe

Production recipe for the CYB Industrial Toolkit.

---

# Recipe

```xml
<!-- ====================================================== -->
<!-- CYB-004 Industrial Toolkit                             -->
<!-- ====================================================== -->

<recipe name="cybIndustrialToolkit"
        count="1"
        craft_area="workbench"
        craft_time="270"
        tags="perkAdvancedEngineering">

    <ingredient name="meleeToolSalvageT3ImpactDriver" count="1"/>
    <ingredient name="cybSecurityResin" count="12"/>
    <ingredient name="resourceDuctTape" count="4"/>
    <ingredient name="resourceForgedIron" count="100"/>
    <ingredient name="resourceMechanicalParts" count="80"/>

</recipe>
```

---

# Recipe Summary

| Property | Value |
|----------|-------|
| Recipe Name | `cybIndustrialToolkit` |
| Output | 1 CYB Industrial Toolkit |
| Crafting Station | Workbench |
| Craft Time | 270 seconds |
| Recipe Tag | `perkAdvancedEngineering` |
| Bulk Crafting | Not included |

---

# Ingredients

| Ingredient | Quantity |
|------------|----------|
| Impact Driver | 1 |
| CYB Security Resin | 12 |
| Duct Tape | 4 |
| Forged Iron | 100 |
| Mechanical Parts | 80 |

---

# Manufacturing Requirements

The CYB Industrial Toolkit is manufactured at a Workbench.

The recipe requires an existing Impact Driver as the mechanical foundation of the toolkit.

Additional industrial materials are then used to reinforce and adapt the tool for CYB maintenance operations.

```text
Impact Driver
      │

CYB Security Resin
Duct Tape
Forged Iron
Mechanical Parts
      │
      ▼

Workbench Manufacturing
      │
      ▼

CYB-004 Industrial Toolkit
```

---

# Design Intent

The Industrial Toolkit is a specialist professional tool rather than an early-game construction item.

The recipe reflects this by requiring:

- A complete Impact Driver
- A substantial quantity of forged metal
- Mechanical components
- Industrial bonding materials
- Access to a Workbench

The existing Impact Driver represents the powered mechanical base of the toolkit.

CYB Security Resin is used as an industrial bonding and protective compound during manufacture.

Forged Iron and Mechanical Parts represent the reinforced housing, drive components and specialist internal mechanisms required for CYB product maintenance.

Duct Tape provides insulation, fastening and protective reinforcement during assembly.

---

# Recipe Progression

The recipe is associated with:

```xml
tags="perkAdvancedEngineering"
```

This integrates the toolkit into the existing Advanced Engineering crafting progression.

The recipe does not introduce a separate custom perk or progression system.

---

# Crafting Behaviour

Confirmed in-game behaviour:

- The recipe appears in the crafting interface.
- The recipe is assigned to the Workbench.
- All required ingredients are displayed.
- The required ingredients are consumed during crafting.
- One CYB Industrial Toolkit is produced.
- The finished toolkit uses its dedicated custom icon.
- The finished toolkit is added to the player inventory after crafting completes.

---

# Production Decisions

## One Tool Per Craft

Each completed recipe produces:

```text
1 CYB Industrial Toolkit
```

Bulk crafting variants are not included.

---

## Impact Driver Requirement

The recipe consumes:

```xml
<ingredient name="meleeToolSalvageT3ImpactDriver" count="1"/>
```

This prevents the Industrial Toolkit from bypassing the acquisition or manufacture of its underlying powered tool.

The Impact Driver is treated as a complete production component rather than a visual reference only.

---

## Dedicated CYB Component

The recipe requires:

```xml
<ingredient name="cybSecurityResin" count="12"/>
```

This connects CYB-004 directly to the established CYB manufacturing chain.

The toolkit therefore depends upon CYB-001 Security Resin rather than being manufactured entirely from vanilla resources.

---

# Validation

| Test | Result |
|------|--------|
| Recipe loads without XML errors | ✅ Passed |
| Recipe appears in crafting interface | ✅ Passed |
| Workbench requirement enforced | ✅ Passed |
| Ingredients displayed correctly | ✅ Passed |
| Ingredients consumed correctly | ✅ Passed |
| Crafting completes successfully | ✅ Passed |
| One toolkit produced | ✅ Passed |
| Custom toolkit icon displayed | ✅ Passed |

---

# Production Status

🟢 **Production Ready**

The CYB-004 Industrial Toolkit recipe has been implemented, tested and confirmed functional.

No further recipe changes are required for Version 1.