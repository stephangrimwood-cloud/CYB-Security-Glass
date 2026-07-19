# MISE EN PLACE

Approved CYB production components available throughout the manufacturing chain.

---

# Items

- [x] CYB-001 Security Resin
- [x] CYB-002 Tempered Glass Panel
- [x] CYB-004 Industrial Toolkit

---

# Recipes

- [x] CYB-001 Security Resin Recipe
- [x] CYB-002 Tempered Glass Panel Recipe
- [x] CYB-003 Security Window Recipe (VariantHelper)
- [x] CYB-004 Industrial Toolkit Recipe

---

# Shape Controller

- [x] CYB-003 Security Window Shape Controller

---

# Shape Family

- [x] CYB Security Window Shape Framework
- [x] Hidden Helper Icon Architecture

---

# Materials

- [x] McybSecurityWindow

---

# Localisation

- [x] CYB-001 Security Resin
- [x] CYB-002 Tempered Glass Panel
- [x] CYB-003 Security Window
- [x] CYB-004 Industrial Toolkit
- [x] Helper Shape Localisation

---

# Current Production Status

## Production Ready

### Manufacturing

- CYB-001 Security Resin
- CYB-001 Security Resin Recipe
- CYB-002 Tempered Glass Panel
- CYB-002 Tempered Glass Panel Recipe
- CYB-003 Security Window Recipe (VariantHelper)
- CYB-004 Industrial Toolkit
- CYB-004 Industrial Toolkit Recipe

### Shape Controller System

- CYB-003 Security Window Shape Controller
- CYB Security Window Shape Framework
- Hidden Helper Icon Architecture
- Runtime Shape Generation
- Shape Menu Integration
- VariantHelper Crafting
- Window Shape Library

### Gameplay Systems

- CYB Security Window Durability System
- CYB Security Window Downgrade System
- CYB Security Window Restoration System
- CYB Industrial Toolkit
- CYB Upgrade Restrictions
- McybSecurityWindow Material

### Documentation

- Shape Framework Documentation
- Shape Controller Documentation
- Recipe Documentation
- Material Documentation
- Research Documentation
- Development Reports

---

# Manufacturing Chain

```text
Broken Glass
      │

Glue
Polymers
      │
      ▼

CYB-001 Security Resin
      │
      ▼

CYB-002 Tempered Glass Panel
      │
      ▼

CYB-003 Security Window
(VariantHelper)
      │
      ▼

Select Window Shape
      │
      ▼

Installed CYB Security Window
```

---

# Product Lifecycle

```text
Manufacture
CYB Security Window
      │
      ▼

Select Window Shape
      │
      ▼

Install Window
      │
      ▼

Window Receives Damage
      │
      ▼

Repair Damage
(CYB Security Resin)
      │
      ▼

Glass Shatters
      │
      ▼

Broken Window
      │
      ▼

Repair Frame
(CYB Security Resin)
      │
      ▼

Restore Glass
(CYB Tempered Glass Panel)
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

# Product Philosophy

CYB Security Windows are manufactured architectural building products.

Each product follows a logical engineering lifecycle.

```text
Manufacture
      │
      ▼

Select Shape
      │
      ▼

Install
      │
      ▼

Use
      │
      ▼

Maintain
(CYB Industrial Toolkit)
      │
      ▼

Restore
      │
      ▼

Replace
```

The completed system operates independently of the vanilla building upgrade progression while remaining fully compatible with the vanilla Shape Controller architecture.

---

# CYB Industrial Toolkit

The Industrial Toolkit is the dedicated installation and maintenance tool for the CYB product ecosystem.

Its primary purpose is to:

- Install CYB products
- Maintain CYB products
- Restore damaged CYB products
- Upgrade compatible CYB products

The toolkit utilises the vanilla repair system.

As a consequence, it is capable of repairing any repairable vanilla block. This behaviour is an engine limitation of the vanilla Repair action and is intentionally retained to preserve full XML-only and EAC compatibility.

Upgrade functionality is intentionally restricted to compatible CYB products, ensuring the toolkit remains the dedicated installation and upgrade tool for the CYB ecosystem.

---

# Development Philosophy

Every production component must be:

- Fully functional
- Independently validated
- Production ready before becoming a dependency of another component
- Supported by evidence where engine behaviour influences design

Development followed a strict evidence-based methodology.

Only confirmed in-game behaviour has been accepted into production.

Wherever possible, proven vanilla systems are reused rather than replaced.

Where engine limitations exist, they are documented and incorporated into the overall product design rather than worked around with unsupported solutions.

---

# Project Progress

| Component | Status |
|-----------|--------|
| CYB-001 Security Resin | ✅ Complete |
| CYB-002 Tempered Glass Panel | ✅ Complete |
| CYB-003 Security Window Shape Controller | ✅ Complete |
| CYB-003 Security Window Recipe | ✅ Complete |
| CYB-004 Industrial Toolkit | ✅ Complete |
| CYB-004 Industrial Toolkit Recipe | ✅ Complete |
| CYB Security Window Shape Framework | ✅ Complete |
| Hidden Helper Icon Architecture | ✅ Complete |
| McybSecurityWindow Material | ✅ Complete |
| Runtime Shape Generation | ✅ Complete |
| Shape Menu Integration | ✅ Complete |
| Durability System | ✅ Complete |
| Downgrade System | ✅ Complete |
| Restoration System | ✅ Complete |
| Manufacturing Chain | ✅ Complete |
| Maintenance System | ✅ Complete |
| VariantHelper Crafting | ✅ Complete |
| Upgrade Restrictions | ✅ Complete |
| Localisation | ✅ Complete |
| Gameplay Validation | ✅ Complete |
| XML Cleanup | ⏳ Pending |
| Version 1 Release Package | ⏳ Pending |

---

# Version 1 Status

## Overall Project Status

🟢 **Feature Complete**

The complete manufacturing chain, Shape Controller architecture, Shape Family, helper architecture, material system, maintenance workflow and gameplay systems have been fully implemented, validated and documented.

Version 1 includes:

- Complete manufacturing workflow
- Complete maintenance workflow
- Complete restoration workflow
- Dedicated CYB Industrial Toolkit
- CYB upgrade restrictions
- Vanilla Shape Controller integration
- Hidden helper icon architecture
- VariantHelper crafting
- Runtime shape generation
- Dedicated Shape Family
- Full documentation
- XML-only implementation
- EAC compatibility
- Client and server compatibility

The remaining work before release consists of:

- XML cleanup
- Asset cleanup
- Documentation review
- Final gameplay testing
- Release packaging
- README review
- Release artwork
- Nexus Mods publication
- GitHub publication

CYB-003 and CYB-004 are now considered **Production Ready** and together provide the complete manufacturing, maintenance and restoration foundation for future CYB architectural products.