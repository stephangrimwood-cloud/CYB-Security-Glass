# CYB-002 – CYB Tempered Glass Panel Recipe

## Status

🟢 Complete / Signed Off

---

## Purpose

Defines the Forge manufacturing recipe for the CYB Tempered Glass Panel.

The recipe represents the first stage of the CYB Security Window manufacturing chain and is intentionally based upon the vanilla Bulletproof Glass production process.

---

## Manufacturing

### Workstation

- Forge *(Requires Crucible)*

### Manufacturing Philosophy

The recipe closely follows the vanilla Bulletproof Glass manufacturing process to maintain familiarity, progression and gameplay balance.

Only the raw material quantities have been reduced to reward players investing in the complete CYB manufacturing chain.

Workstation requirements, perk progression, output quantity and Forge behaviour remain intentionally consistent with vanilla.

---

## Approved Recipe (v1.0)

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

## Validation

### Recipe Testing

**Status**

✅ Complete

### Confirmed In-Game

- ✅ Recipe appears correctly in the Forge.
- ✅ Recipe requires a Crucible.
- ✅ Recipe crafts successfully.
- ✅ Correct item is produced.
- ✅ Correct localisation is displayed.
- ✅ Custom CYB inventory icon displays correctly.
- ✅ Crafted item is intentionally non-placeable.
- ✅ No XML or loading errors encountered during testing.

---

## Observations

### Forge Tool Quality (Version 3.0)

Testing confirmed that Forge tool tier affects manufacturing speed.

| Forge Components | Craft Time |
|------------------|-----------:|
| T1 Anvil + T1 Bellows | ~1m 08s |
| T6 Anvil + T6 Bellows | ~26s |

This appears to be a Version 3.0 gameplay mechanic replacing the previous binary Forge workstation bonus system.

Further investigation may be undertaken during future balancing to determine the exact scaling behaviour.

---

## Development Checklist

### Design

- [x] Recipe philosophy
- [x] Recipe balancing

### Implementation

- [x] Forge recipe XML
- [x] In-game recipe testing
- [x] Recipe validation

### Approval

- [x] Approved for Mise en Place
- [x] Recipe complete
- [x] Signed off

---

## Notes

The Forge is responsible only for manufacturing the CYB Tempered Glass Panel.

CYB Security Resin is intentionally excluded from the Forge recipe and reserved for final assembly of the completed CYB Security Window at the Workbench.

The Tempered Glass Panel is an intermediate manufacturing component and is not intended to be placed directly into the world.

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