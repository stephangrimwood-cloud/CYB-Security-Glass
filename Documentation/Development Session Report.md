# Development History — Version 1

**Project:** CYB Security Glass

**Status:** 🟢 Feature Complete / Release Preparation

---

# Purpose

This document records the major development milestones achieved during Version 1 of the CYB Security Glass project.

Rather than documenting every individual experiment, it summarises the confirmed architectural decisions, technical discoveries and production systems that now form the foundation of the project.

---

# Project Vision

Version 1 began with a simple objective:

Create a security window system that integrates naturally with the vanilla game while remaining lightweight, maintainable and fully XML-driven.

From the outset the project adopted several guiding principles:

- XML-first development
- Reuse vanilla systems wherever possible
- Test one change at a time
- Validate every discovery in-game
- Keep solutions simple before pursuing complexity

These principles remained unchanged throughout development.

---

# Manufacturing Chain

The complete manufacturing pipeline was successfully established.

## CYB-001 — Security Resin

Completed:

- Custom item
- Chemistry Station recipe
- Campfire recipe
- Custom icon
- Localisation
- In-game validation

Status:

**🟢 Production Ready**

---

## CYB-002 — Tempered Glass Panel

Completed:

- Custom item
- Forge recipe
- Custom icon
- Localisation
- Manufacturing balance
- In-game validation

Status:

**🟢 Production Ready**

---

## CYB-003 — Security Windows

Version 1 successfully transitioned from prototype helper blocks into a fully validated Shape Controller architecture.

Completed:

- Dedicated Shape Controller
- Custom Shape Family
- Runtime Shape Controller generation
- Complete architectural window library
- Shared material framework
- Standardised durability
- Downgrade workflow
- Repair workflow
- Restoration workflow
- Harvest behaviour
- Shape Menu integration
- Production recipe

Status:

**🟢 Production Ready**

---

## CYB-004 — Industrial Toolkit

A dedicated maintenance tool was developed to support the complete CYB repair workflow.

Completed:

- Custom toolkit item
- Workbench recipe
- Custom icon
- Localisation
- Repair amount configuration
- Repair sounds
- Upgrade sounds
- Held model
- Durability
- CYB repair validation
- CYB restoration validation

Status:

**🟢 Production Ready**

---

# Major Technical Discoveries

Throughout development several important vanilla systems were successfully reverse engineered.

## Shape Controller

Confirmed:

- VariantHelper architecture
- Runtime block generation
- Shared gameplay behaviour
- Shared material inheritance

---

## Hidden Helper Architecture

Confirmed:

```xml
<property name="ShapeMenu" value="false"/>
```

allows internal helper shapes to remain hidden while still supplying the VariantHelper icon.

This discovery enabled a dedicated CYB icon without exposing unnecessary player-facing shapes.

---

## Shape Menu Requirements

Confirmed:

```xml
<property name="Path" value="solid"/>
```

is required for custom architectural window shapes to appear correctly within the Shape Menu.

---

## Runtime Durability

Testing confirmed that runtime durability is calculated using:

```text
Material MaxDamage
        ×
MaterialHitpointMultiplier
```

Production values:

| Window State | Multiplier | Runtime HP |
|--------------|-----------:|-----------:|
| Full Window | 0.500 | 1500 |
| Broken Window | 0.333 | 999 |

---

## Material Framework

The custom material:

```text
McybSecurityWindow
```

provides:

- Shared durability
- Metal impact sounds
- Metal placement sounds
- Structural stability
- Independent balancing

The material now serves as the durability foundation for every production CYB Security Window.

---

# Completed Gameplay Systems

Version 1 now provides:

- Complete manufacturing chain
- Shape Controller architecture
- Shape Family framework
- Runtime durability generation
- Standardised repair system
- Standardised restoration system
- Downgrade behaviour
- Harvest behaviour
- Painting compatibility
- Vanilla architectural presentation
- Dedicated maintenance toolkit

---

# Project Milestones

Major milestones achieved during Version 1 include:

- Manufacturing chain established
- Security Resin completed
- Tempered Glass Panel completed
- Prototype helper architecture retired
- Dedicated Shape Controller implemented
- Shape Family completed
- Runtime durability understood
- Hidden helper icon architecture implemented
- Complete production window library validated
- Industrial Toolkit completed
- Documentation framework established

---

# Lessons Learned

Version 1 reinforced several important engineering principles.

- Start with the simplest solution.
- Build upon confirmed vanilla behaviour.
- Test one XML change at a time.
- Document discoveries as they occur.
- Prefer reuse over reinvention.
- Keep systems modular.
- Allow the vanilla engine to perform the heavy lifting wherever possible.

Many of the project's largest breakthroughs resulted from understanding existing vanilla behaviour rather than introducing new mechanics.

---

# Version 1 Outcome

Version 1 successfully evolved from an experimental concept into a complete production-ready framework.

The completed project now delivers:

- CYB-001 Security Resin
- CYB-002 Tempered Glass Panel
- CYB-003 Security Window Shape Controller
- Complete architectural window library
- Hidden helper icon architecture
- VariantHelper manufacturing
- Shared material framework
- Standardised durability
- Repair and restoration systems
- CYB-004 Industrial Toolkit
- Complete XML-only implementation

The resulting architecture provides a stable and expandable foundation for future CYB construction products while remaining fully compatible with the vanilla game.

---

# Looking Forward

Future development will build upon the Version 1 framework rather than replacing it.

Potential areas for expansion include:

- Additional architectural window collections
- Decorative glazing systems
- Premium security windows
- Custom CYB models
- Additional construction products
- Future CYB architectural projects

The Version 1 foundation is considered complete and ready for release.