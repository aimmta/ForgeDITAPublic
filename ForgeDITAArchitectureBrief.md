# ForgeDITA Architecture Brief

## A Standards-First Model for Modern DITA CCMS

## 1. Problem

“DITA support” has become a vague and overloaded claim.

In practice, it often means:

* partial XML handling
* constrained authoring models
* platform-shaped workflows
* publishing pipelines that are difficult to reproduce
* content that is technically exportable but operationally trapped

For teams running serious structured content operations, these gaps create real risk:

* **Loss of semantic integrity** when XML is adapted to fit platform assumptions
* **Publishing uncertainty** when outputs cannot be rebuilt deterministically
* **Operational drag** from complex administration and opaque behavior
* **Vendor dependency** that turns migration into a project instead of a capability

The result is a category where the tooling often dictates the workflow, rather than supporting it.

## 2. Core Model

ForgeDITA proposes a different architecture, grounded in a few strict principles.

### 2.1 Native XML as the System of Record

DITA content remains:

* unmodified
* fully exportable
* free of proprietary representation layers

The platform does not reinterpret or reshape the content model to fit internal storage or UI constraints.

### 2.2 Semantic Registry (Tenant-Scoped)

DITA behavior is governed through a declarative semantic layer.

This registry defines:

* specialization handling
* attribute semantics
* subject scheme integration
* processing expectations

Key properties:

* **Tenant-scoped**: no cross-tenant leakage of semantics
* **Explicit**: no hidden or editor-specific behavior
* **Versioned**: changes are tracked and tied to releases

No service is allowed to privately interpret DITA structures outside this registry.

### 2.3 Graph-Aware Core Services

DITA is treated as a graph, not a collection of files.

Core services operate with full awareness of:

* keys and key scopes
* conrefs and reuse chains
* maps and hierarchy
* subject schemes and metadata relationships

This supports:

* accurate impact analysis
* reliable validation
* consistent publishing inputs

### 2.4 Bring Your Own Editor (BYOE)

Editors are treated as clients, not control points.

* Oxygen is a first-class client
* All operations occur through exposed APIs
* No editor-specific behavior defines system semantics

This separates authoring experience from system logic.

### 2.5 Immutable Publishing Model

Publishing is defined as a reproducible system event.

Each release is pinned to:

* content baseline
* semantic registry version
* toolchain bundle (DITA-OT, plugins, configs)
* publishing profile

Outputs are:

* rebuildable
* explainable
* auditable

## 3. Why This Matters

This model is designed to address long-standing failure points in structured content systems.

### 3.1 Auditability

* Every output can be traced to exact inputs and processing rules
* Regulatory and compliance workflows become verifiable

### 3.2 Reproducibility

* Releases are not dependent on mutable environments
* Historical outputs can be rebuilt with confidence

### 3.3 Semantic Integrity

* Specialization and metadata behave consistently
* No hidden transformations or editor-side assumptions

### 3.4 Exit Safety

* Content remains clean and portable
* Toolchain and behavior are explicitly defined

## 4. Open Questions

This model is intentionally direct and may expose trade-offs.

Key areas for validation:

* Does the semantic registry fully capture DITA specialization behavior in practice?
* Are there edge cases where implicit behavior is required for usability?
* What are the performance implications of fully graph-aware services at scale?
* How should validation responsibilities be balanced between client and server?

## 5. Intent

This is not a product pitch.

It is an attempt to define a cleaner operating model for DITA-based content systems.

The goal is simple:

* preserve the standard
* make behavior explicit
* reduce platform-induced complexity
* support real-world publishing discipline

## 6. Request for Feedback

If you have experience with DITA at scale, your perspective would be valuable.

Specifically:

* Where does this model break?
* What assumptions are incomplete?
* What would you change before implementation?

ForgeDITA is currently in architecture-first development toward MVP.
