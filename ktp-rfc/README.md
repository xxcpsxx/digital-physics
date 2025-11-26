# Kinetic Trust Protocol (KTP) - RFC Series

**Status**: Draft Specification - NMCITRA  
**Version**: 0.1  
**Date**: November 2025

This repository contains draft specifications developed by the New Mexico
Cyber Intelligence & Threat Response Alliance (NMCITRA). These documents
have not been submitted to the IETF and do not represent Internet Standards
or consensus of any standards body.

> *"We cannot command Nature except by obeying her."* — Francis Bacon

## Overview

The Kinetic Trust Protocol (KTP) is a framework for dynamic, physics-based authorization of autonomous agents. It replaces static permission models with environmental constraints that adapt in real-time to system conditions.

**The Core Insight**: Instead of asking "Does this agent have permission?", KTP asks "Can this environment safely support this action?"

## The Problem

Traditional authorization systems suffer from three fatal assumptions:

1. **The Passport Fallacy**: Possession of a credential equals proof of identity
2. **The Static Fallacy**: Permissions verified at time T remain valid at T+1
3. **The Vacuum Fallacy**: Digital systems operate independent of physical reality

In the age of autonomous agents operating at machine-speed, all three assumptions fail catastrophically.

## The Solution: Digital Physics

KTP introduces a physics-based model where:

- **Trust is Mass**: Earned through survival, not assigned by fiat
- **Risk is Friction**: Environmental stress that constrains movement
- **Authorization is Motion**: The result of mass overcoming friction
- **Identity is Trajectory**: A vector of movement, not a static credential

## The Zeroth Law

The foundational constraint of all KTP systems:

```
A ≤ E

Where:
  A = Autonomy (intrinsic risk of the requested action)
  E = Environment stability (current Trust Score)
```

This is not a policy. It is a physical constraint enforced by cryptography.

## RFC Series

This repository contains the complete RFC specification for KTP:

| RFC | Title | Status | Description |
|-----|-------|--------|-------------|
| [Constitution](constitution.txt) | Constitution of Digital Physics | Draft | Preamble and 10 Articles defining the governing framework |
| [KTP-CORE](rfcs/ktp-core.txt) | Core Protocol | Draft | Trust Score, Context Tensor, Trust Proof, Silent Veto |
| [KTP-IDENTITY](rfcs/ktp-identity.txt) | Vector Identity | Draft | Trajectory Chains, Proof of Resilience, Sponsorship, Identity Proofing (NIST 800-63) |
| [KTP-SENSORS](rfcs/ktp-sensors.txt) | Context Tensor Sensors | Draft | Sensor specs, Risk Domains, normalization, domain profiles |
| [KTP-ENFORCE](rfcs/ktp-enforce.txt) | Enforcement Layer | Draft | PEPs, Trust Tiers, Adaptive Dormancy, Mass Ceiling |
| [KTP-AUDIT](rfcs/ktp-audit.txt) | Flight Recorder | Draft | Decision Geometry, immutable logging, forensics |
| [KTP-ZONES](rfcs/ktp-zones.txt) | Blue Zone Discovery | Draft | Zone types, discovery, ingress/egress |
| [KTP-FEDERATION](rfcs/ktp-federation.txt) | Trust Federation | Draft | Inter-zone trust, cross-attestation, governance |
| [KTP-CELESTIAL](rfcs/ktp-celestial.txt) | Celestial Wayfinding | Draft | Interplanetary trust, light-cone model, Polynesian navigation philosophy |
| [KTP-MIGRATION](rfcs/ktp-migration.txt) | Migration Guide | Draft | Adoption pathways, legacy integration, staged deployment |
| [KTP-HUMAN](rfcs/ktp-human.txt) | Human Integration | Draft | Humans as agents, collaboration, system ethics (draft) |
| [KTP-CONFORMANCE](rfcs/ktp-conformance.txt) | Conformance Requirements | Draft | Levels, testing, certification, interoperability |
| [KTP-PROBLEMS](rfcs/ktp-problems.txt) | Open Problems | Draft | Known limitations, anticipated critiques, call for collaboration |

## Quick Start

### The Trust Equation

```
E(trust) = E(base) × (1 - R)

Where:
  E(base)  = Agent's intrinsic capability (0-100)
  R        = Risk factor from Context Tensor (0-1)
  E(trust) = What the environment allows (0-100)
```

### The Context Tensor

Seven dimensions of environmental reality:

| Dimension | Symbol | Physics Equivalent | Measures | Sensors |
|-----------|--------|-------------------|----------|---------|
| Mass | M | Density/Mass | Physical density | CO2, LIDAR, RF noise, device count |
| Momentum | P | Kinetic Energy | Data flow velocity | TPS, link saturation, packet velocity |
| Heat | H | Entropy/Temperature | Adversarial pressure | WAF blocks, anomaly rates, CPU temps |
| Time | T | Temporal Phase | Moment criticality | Event countdown, maintenance windows |
| Inertia | I | Inertial Mass | Blast radius | Topology centrality, dependency depth |
| Observer | O | Frame of Reference | Who is watching | VIP presence, regulatory jurisdiction |
| **Soul** | **S** | **Cosmological Constant** | **Sovereignty constraints** | **TK Labels, OCAP/CARE, Sacred Land geofences** |

**The Soul Veto**: Unlike the first six dimensions (which contribute weighted values to the Risk Factor), Soul acts as a **binary veto**. If sovereignty constraints are violated (S = 1), the action is forbidden regardless of Trust Score. This represents immutable laws—ethical, legal, and spiritual constraints that exist outside the operational domain.

### Trust Tiers

| Tier | E(trust) | Capabilities |
|------|----------|--------------|
| God Mode | ≥ 95 | Create, destroy, mutate infrastructure |
| Operator Mode | ≥ 85 | Restart services, read configs |
| Analyst Mode | ≥ 70 | Query data, read-only access |
| Observer Mode | < 70 | Emit logs only |

## Blue Zones

Blue Zones are network segments where Digital Physics is enforced—safe harbors on the internet where humans and agents can operate with cryptographic trust guarantees.

```
┌─────────────────────────────────────────────────┐
│                   BLUE ZONE                      │
│  ┌───────────────────────────────────────────┐  │
│  │           Trust Oracle Mesh                │  │
│  │   [Oracle 1] ←→ [Oracle 2] ←→ [Oracle 3]  │  │
│  └───────────────────────────────────────────┘  │
│                      ↓                          │
│  ┌───────────────────────────────────────────┐  │
│  │         Context Tensor Sensors             │  │
│  │   [M] [P] [H] [T] [I] [O] [S]             │  │
│  └───────────────────────────────────────────┘  │
│                      ↓                          │
│  ┌───────────────────────────────────────────┐  │
│  │      Policy Enforcement Points             │  │
│  │   [API GW] [Service Mesh] [IAM] [DB]      │  │
│  └───────────────────────────────────────────┘  │
│                      ↓                          │
│  ┌───────────────────────────────────────────┐  │
│  │          Agent Population                  │  │
│  │   [Tethered] [Divergent] [Persistent]     │  │
│  └───────────────────────────────────────────┘  │
└─────────────────────────────────────────────────┘
                       ↕
              [ZONE GATEWAY]
                       ↕
┌─────────────────────────────────────────────────┐
│              WILD INTERNET                       │
│   (Static credentials, binary permissions)      │
└─────────────────────────────────────────────────┘
```

## Repository Structure

```
ktp-rfc/
├── README.md                 # This file
├── constitution.txt          # The Constitution of Digital Physics
├── rfcs/                     # RFC specifications
│   ├── ktp-core.txt
│   ├── ktp-identity.txt
│   ├── ktp-sensors.txt
│   ├── ktp-enforce.txt
│   ├── ktp-audit.txt
│   ├── ktp-zones.txt
│   ├── ktp-federation.txt
│   ├── ktp-celestial.txt
│   ├── ktp-migration.txt
│   ├── ktp-human.txt
│   └── ktp-conformance.txt
├── schemas/                  # JSON schemas
│   ├── trust-proof.json
│   ├── context-tensor.json
│   ├── soul-constraint.json
│   └── sensor-config.json
└── (future)
    ├── examples/             # Implementation examples
    ├── docs/                 # Additional documentation
    └── reference/            # Reference implementations
```

## Contributing

This specification is in active development. Contributions welcome:

1. **RFC Review**: Submit issues for clarifications or improvements
2. **Implementation**: Reference implementations in any language
3. **Sensor Profiles**: Domain-specific Context Tensor configurations
4. **Blue Zone Pilots**: Real-world deployment experiences

## Philosophy

> *"Freedom is the recognition of necessity."* — Baruch Spinoza

KTP is built on the insight that true autonomy requires constraint. An agent is not free because it can do anything—it is free because it acts within the bounds of what the environment can safely support.

We are not building a prison for AI. We are building physics for the digital world.

## Authors

Chris Perkins  
New Mexico Cyber Intelligence & Threat Response Alliance (NMCITRA)  
Email: cperkins@nmcitra.org

## License

This specification is released under the Apache License, Version 2.0.

## References

### Foundational Articles

1. "The Missing Law of Motion" - Part I
2. "The Ghost in the Machine" - Part II
3. "Sailing by Starlight" - Part III
4. "Proof of Physics" - Part IV
5. "The Tether" - Part V
6. "The Constitution of Digital Physics" - Part VI

### Related Standards

- RFC 7519 - JSON Web Token (JWT)
- RFC 8693 - OAuth 2.0 Token Exchange
- RFC 9396 - OAuth 2.0 Rich Authorization Requests

---

*"We are moving from a world governed by policies (written by humans, enforced by humans, violated by humans) to a world governed by physics (defined by humans, enforced by mathematics, violated by no one)."*
