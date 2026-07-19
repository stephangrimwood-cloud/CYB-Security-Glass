# CYB-002 – CYB Tempered Glass Panel

## Status

🟢 Complete / Signed Off

---

## Purpose

A reinforced tempered glass panel manufactured using an industrial Forge.

The CYB Tempered Glass Panel is the primary glazing component used in the manufacture of CYB Security Windows and represents the first stage of the CYB glass production chain.

---

## Product Specification

**Internal Name**

cybTemperedGlassPanel

**Display Name**

CYB Tempered Glass Panel

**Category**

Resources

**Inventory Icon**

Custom CYB Tempered Glass Panel (CYB branded)

**Stack Size**

500

**Weight**

8

**Intrinsic Value**

120

Represents the intrinsic manufacturing value of the component.

CYB products are intentionally not purchasable by vanilla traders.

**Lootable**

No

Manufactured only.

**Repair Item**

No

**Placeable**

No

The Tempered Glass Panel is an intermediate manufacturing component and is not intended to be placed directly into the world.

**Used For**

- CYB Security Window

---

## Manufacturing

### Crafting Station

- Forge *(Requires Crucible)*

### Manufacturing Philosophy

The recipe is intentionally based upon the vanilla Bulletproof Glass manufacturing process.

Rather than replacing Bulletproof Glass, the CYB Tempered Glass Panel provides a more efficient manufacturing path for players investing in the complete CYB production chain.

Only the raw material quantities have been reduced.

Manufacturing progression, workstation requirements, output quantity and overall gameplay remain intentionally consistent with vanilla.

### Design Decisions

- CYB Security Resin is **not** used within the Forge recipe.
- The Forge is responsible only for manufacturing the Tempered Glass Panel.
- CYB Security Resin is reserved for final assembly at the Workbench.
- Intermediate CYB manufacturing components are not sellable to traders.

---

## Approved Recipe (v1.0)

Based directly on the vanilla Bulletproof Glass recipe.

| Material | Vanilla | CYB |
|-----------|--------:|----:|
| Glass | 112 | 100 |
| Stone | 10 | 8 |
| Lead | 40 | 35 |
| Iron | 20 | 16 |
| Clay | 20 | 16 |

### Output

- **1 × CYB Tempered Glass Panel**

### Manufacturing Requirements

- Forge
- Crucible
- Advanced Engineering

---

## Validation Results

### Confirmed In-Game

- ✅ Item appears correctly in the Creative Menu.
- ✅ Localisation displays correctly.
- ✅ Custom CYB inventory icon displays correctly.
- ✅ Custom icon displays correctly within the Forge.
- ✅ Forge recipe appears correctly.
- ✅ Recipe correctly requires a Crucible.
- ✅ Recipe crafts successfully.
- ✅ Correct item is produced.
- ✅ Item is intentionally non-placeable.
- ✅ Item cannot be sold to traders.
- ✅ Trader correctly displays **No Sell Price**.
- ✅ Scrap recovery returns Broken Glass fragments only.
- ✅ No XML or loading errors encountered during testing.

### Additional Observations

Testing confirmed the following:

- Forge component tier affects manufacturing speed.
- `SellableToTrader` successfully prevents trader exploitation while preserving intrinsic item value.
- `EconomicValue` and trader sale eligibility operate independently.
- Scrapping the panel returns Broken Glass fragments only, matching the intended manufacturing philosophy.

### Forge Performance

| Forge Components | Craft Time |
|------------------|-----------:|
| T1 Anvil + T1 Bellows | ~1m 08s |
| T6 Anvil + T6 Bellows | ~26s |

Forge tool tier appears to influence manufacturing speed in Version 3.0 and will continue to be monitored during future balancing.

---

## Development Checklist

### Design

- [x] Product concept
- [x] Product specification
- [x] Manufacturing philosophy
- [x] Recipe design

### Assets

- [x] Item XML
- [x] Recipe XML
- [x] Localisation
- [x] Custom CYB inventory icon

### Manufacturing

- [x] Forge recipe implemented
- [x] In-game recipe testing
- [x] Recipe validation
- [x] Manufacturing balance review

### Integration

- [ ] Used by CYB Security Window
- [ ] Final gameplay balancing

### Approval

- [x] Approved for Mise en Place
- [x] Component complete
- [x] Signed off

---

## Notes

This product replaces the previously proposed **CYB Laminated Glass**.

Following review of the vanilla workstation progression, the intermediate product was renamed **CYB Tempered Glass Panel**.

This more accurately reflects the Forge's role within the manufacturing chain and reserves CYB Security Resin for final assembly of the completed CYB Security Window.

Weight, intrinsic value, stack size and trader behaviour have all been balanced against the approved CYB manufacturing philosophy.

Final gameplay balancing will occur after the complete CYB Security Window production chain has been implemented and tested.

---

## Project Standards Established

Development of CYB-002 established the following standards for future CYB manufactured components:

- Intermediate manufacturing components are categorised as **Resources**.
- Intermediate manufacturing components are not sellable to vanilla traders.
- Vanilla mechanics are preferred wherever they satisfy the intended gameplay.
- Inventory icons use lightly modified vanilla artwork with consistent CYB branding.
- Placeholder world meshes remain vanilla unless a gameplay benefit exists.
- Every implementation decision is documented and validated through in-game testing.

---

## Manufacturing Chain

```text
Raw Materials
(Glass • Stone • Lead • Iron • Clay)
          │
          ▼

Forge
(Requires Crucible)

          │
          ▼

CYB Tempered Glass Panel

          │
          ▼

Workbench

Concrete Mix
CYB Tempered Glass Panel
CYB Security Resin
Mechanical Parts

          │
          ▼

CYB Security Window
```