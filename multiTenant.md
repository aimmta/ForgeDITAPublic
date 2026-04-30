# ForgeDITA Whitepaper

## Multi-Tenant Architecture and the Toolchain Registry Model

## 1. Problem

Multi-tenancy in CCMS platforms is often treated as a deployment concern rather than an architectural principle.

In many systems, “multi-tenant” means:

* shared infrastructure with partial logical separation
* configuration overlays that vary by customer
* environment-level isolation without semantic isolation

This creates predictable problems:

* publishing behavior varies across environments
* toolchains drift over time
* tenant-specific rules leak into shared logic
* reproducibility becomes difficult or impossible

For DITA-based systems, the problem is more acute.

DITA processing is not just storage and retrieval. It includes:

* specialization handling
* key resolution
* subject scheme interpretation
* validation rules
* publishing transformations

If these behaviors are not fully isolated per tenant, the platform cannot guarantee consistency.

## 2. ForgeDITA Position

Multi-tenancy must extend beyond infrastructure.

It must include:

* content
* semantics
* processing
* publishing

Every layer of the system must be tenant-scoped and explicitly defined.

ForgeDITA approaches this through a combination of strict boundaries and a central concept: the toolchain registry.

## 3. The Toolchain Registry

The toolchain registry is the authoritative definition of how content is processed for a given tenant.

It defines:

* DITA-OT version
* plugin set
* catalog resolution
* specialization shells and constraints
* Schematron and validation rules
* transformation parameters
* publishing profiles

Each registry entry represents a complete, versioned toolchain.

Key properties:

### 3.1 Tenant-Scoped

Each tenant has its own registry.

* No shared global defaults
* No hidden inheritance
* No cross-tenant mutation

### 3.2 Versioned

Toolchains are immutable once published.

* Changes produce new versions
* Previous versions remain available
* Releases can reference exact toolchain states

### 3.3 Explicit

All processing behavior is declared.

* No implicit platform assumptions
* No editor-defined semantics
* No hidden configuration layers

## 4. Multi-Tenancy from Sub-Basement to Top-Floor

ForgeDITA enforces tenant isolation at every layer of the system.

### 4.1 Storage Layer

* Content stored per tenant
* No shared content pools
* Clean export always available

### 4.2 Semantic Layer

* Tenant-scoped semantic registry
* Defines specialization behavior and metadata interpretation
* No service may invent private semantics

### 4.3 Graph Layer

* Keys, conrefs, maps, and relationships resolved within tenant boundaries
* Graph operations are deterministic and reproducible

### 4.4 Validation Layer

* Validation rules tied to tenant semantics and toolchain
* Client and server validation aligned but independent

### 4.5 Toolchain Layer

* Toolchain registry defines all processing inputs
* DITA-OT and plugins versioned and pinned
* No shared mutable environments

### 4.6 Publishing Layer

* Publishing is a reproducible event
* Each output references:

  * content baseline
  * semantic registry version
  * toolchain version
  * publishing profile

### 4.7 API Layer

* All services are tenant-aware by design
* No global endpoints with hidden tenant logic
* Behavior is consistent across all clients

## 5. Why the Toolchain Registry Matters

The registry is the control point that makes multi-tenancy real.

Without it:

* toolchains drift
* environments diverge
* publishing becomes unreliable
* debugging becomes guesswork

With it:

### 5.1 Reproducibility

Any release can be rebuilt from:

* content
* semantic registry
* toolchain definition

### 5.2 Isolation

Tenant behavior is fully contained.

* No accidental cross-impact
* No shared configuration surprises

### 5.3 Transparency

Processing is inspectable.

* Inputs are known
* transformations are defined
* outputs are explainable

### 5.4 Portability

Toolchains can be exported and reused.

* migration becomes feasible
* environments can be recreated

## 6. Comparison with Typical Approaches

Typical CCMS platforms:

* rely on shared environments
* accumulate configuration over time
* mix tenant behavior with platform logic
* treat publishing as an operational side effect

ForgeDITA:

* isolates tenants completely
* defines processing declaratively
* pins toolchains to releases
* treats publishing as a deterministic system function

## 7. Trade-offs

This model introduces constraints.

* requires explicit configuration
* reduces reliance on implicit defaults
* demands discipline in versioning

However, these constraints are intentional.

They replace hidden complexity with visible structure.

## 8. Open Questions

* How should toolchain promotion workflows be managed across environments?
* What governance is required for semantic registry evolution?
* How can performance be maintained with fully isolated graph operations?
* What developer experience is required to keep the system usable?

## 9. Conclusion

Multi-tenancy is not a hosting feature.

It is an architectural commitment.

For DITA systems, that commitment must include:

* semantics
* processing
* publishing

The toolchain registry provides the mechanism to enforce that commitment.

ForgeDITA’s position is direct:

If the system cannot guarantee tenant isolation and reproducible publishing, it is not truly multi-tenant.

## 10. Request for Feedback

This model is intended for practitioners who work with structured content at scale.

Questions:

* Where does this model break in real-world use?
* What assumptions are incomplete?
* What would you change before implementation?

ForgeDITA is in architecture-first development toward MVP.
Structured content, forged right.
