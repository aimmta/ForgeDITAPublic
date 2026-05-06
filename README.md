# ForgeDITA Public

Architecture-first exploration of maintainable, standards-first DITA infrastructure.

This repository contains public-facing documents describing the architectural direction, operating principles, and technical assumptions behind ForgeDITA.

This is not the product codebase.

It is the thinking behind the product.

---

## Why This Repository Exists

Many structured content environments slowly become operationally difficult to live with.

Experienced practitioners recognize the pattern:

- publishing behavior drifts
- customization accumulates
- semantics become fragmented
- workflows expand around platform limitations
- operational workarounds become institutionalized
- and tribal knowledge becomes necessary just to maintain stability

Teams adapt.

They build processes around the system.

Eventually the operational overhead surrounding documentation becomes larger than the documentation changes themselves.

ForgeDITA exists because too many organizations quietly accept this trajectory as inevitable.

This repository documents an alternative architectural approach.

---

## Core Position

ForgeDITA is built around a direct premise:

## Documentation infrastructure should remain understandable and maintainable over time

The platform is intentionally designed around:

- standards integrity
- explicit semantics
- reproducible publishing
- graph-aware processing
- operational clarity
- and long-term maintainability

The goal is not to accumulate more enterprise complexity.

The goal is to reduce operational fragility before it becomes normalized.

---

## Contents

This repository contains architecture-focused documents intended for experienced DITA and structured-authoring practitioners.

Current documents include:

## Architecture Brief

A high-level overview of the ForgeDITA operating model:

- native XML as system of record
- tenant-scoped semantic registry
- graph-aware services
- Bring Your Own Editor architecture
- immutable publishing model
- operational maintainability principles

## Multi-Tenant Architecture and Toolchain Registry Model

A deeper exploration of:

- tenant isolation
- explicit processing environments
- toolchain versioning
- reproducible publishing
- semantic isolation
- graph-aware multi-tenancy
- and operational reproducibility

---

## Start Here

[Architecture Brief](ForgeDITAArchitectureBrief.md)
[Multi-Tenant Architecture and the Toolchain Registry Model](multiTenant.md)

---

## What This Repository Is

- a working architectural model
- a technical position on maintainable DITA infrastructure
- a set of explicit assumptions and trade-offs
- an attempt to make system behavior understandable

---

## What This Repository Is Not

- a marketing site
- a feature checklist
- a finalized implementation
- a generic SaaS positioning exercise

The goal is clarity.

Not hype.

---

## Why Architecture-First

ForgeDITA is intentionally being developed architecture-first.

The goal is to validate:

- operational assumptions
- semantic models
- reproducibility constraints
- governance requirements
- and architectural trade-offs

before large-scale implementation.

The architecture matters because operational fragility is usually easier to prevent than to remove later.

---

## Feedback

If you operate DITA systems at scale, your perspective would be valuable.

Particularly:

- Where does this model fail operationally?
- Which assumptions become unrealistic in practice?
- What hidden complexity risks remain?
- Which trade-offs would organizations reject?
- What long-term maintenance problems are still unsolved?

---

## Contact

<hello@forgedita.com>
<https://forgedita.com>

Structured content infrastructure designed for long-term maintainability.
