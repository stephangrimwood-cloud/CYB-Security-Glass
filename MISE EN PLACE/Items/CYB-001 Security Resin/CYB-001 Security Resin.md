# CYB-001 – CYB Security Resin

## Status

🟢 Production Ready

---

## Purpose

A specialist industrial bonding compound used in the manufacture, installation and repair of CYB construction products.

---

## Product Specification

**Internal Name**

cybSecurityResin

**Display Name**

CYB Security Resin

**Category**

Building Materials

**Product Icon**

Custom CYB Security Resin

**Stack Size**

500

**Lootable**

No

Manufactured only.

**Sell Value**

20 *(Not sellable to traders.)*

**Repair Item**

No

**Used For**

- CYB Security Window
- Future CYB Construction Products

---

## Manufacturing

### Crafting Stations

- Chemistry Station *(preferred manufacturing method)*
- Campfire *(available for early-game production)*

### Manufacturing Philosophy

CYB Security Resin is intentionally available from both the Campfire and Chemistry Station.

The Campfire provides a slower early-game manufacturing option, while the Chemistry Station rewards player progression through significantly faster production.

Both workstations manufacture the same product; only production efficiency differs.

### Approved Craft Times

| Workstation | Craft Time |
|--------------|-----------:|
| Chemistry Station | **30 seconds** |
| Campfire | **1 minute 40 seconds** |

---

## Development Checklist

### Design

- [x] Product concept
- [x] Product specification
- [x] Manufacturing philosophy

### Assets

- [x] Item XML
- [x] Localisation
- [x] Custom product icon

### Manufacturing

- [x] Chemistry Station recipe
- [x] Campfire recipe
- [x] In-game recipe testing
- [x] Recipe balancing

### Integration

- [x] Intended for CYB Security Window
- [x] Final gameplay testing

### Approval

- [x] Approved for Production

---

## Validation

### Recipe Testing

**Status**

✅ PASS

The recipe functions correctly in both supported workstations.

### Final Craft Times

| Workstation | XML `craft_time` | In-Game Time |
|--------------|-----------------:|-------------:|
| Chemistry Station | 6 | 30 seconds |
| Campfire | 40 | 1 minute 40 seconds |

### Validation Results

- Recipes appear correctly in both workstations.
- Crafting completes successfully.
- Item output is correct.
- Custom CYB product icon loads correctly.
- Item appears correctly in the Creative Menu, inventory and trader interface.
- Item is correctly prevented from being sold to traders.
- No XML or loading errors encountered.
- Workstation craft times are affected by internal workstation modifiers rather than the raw `craft_time` value.

### Design Outcome

The intended manufacturing progression has been achieved.

- Campfire production provides an accessible early-game option.
- Chemistry Station production rewards player progression through significantly faster manufacturing.
- CYB Security Resin establishes the visual identity for future CYB products through its custom branded icon.

---

## Notes

CYB Security Resin is an intermediate manufacturing component.

It cannot be looted and is manufactured exclusively by the player.

The item is intentionally prevented from being sold to traders, preserving its role within the CYB manufacturing chain.

### Development Lessons

During development the following was confirmed:

- Localisation failures were caused by CSV formatting rather than XML definitions.
- Custom item icons for **7 Days to Die v3.0** are successfully loaded from:

```text
UIAtlases/
└── ItemIconAtlas/
    └── cybSecurityResin.png