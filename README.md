# ForgeDITA Public

Architecture-first exploration of a modern, standards-driven DITA CCMS.

This repository contains public-facing documents that describe the ideas, principles, and technical direction behind ForgeDITA. It is not the product codebase. It is the thinking behind the product.

## Purpose

ForgeDITA is being built from a simple premise:

A DITA CCMS should preserve the standard, make behavior explicit, and reduce platform-induced complexity.

Most existing systems have evolved through layers of enterprise compromise. The result is often:

* opaque behavior
* difficult administration
* fragile publishing pipelines
* vendor-shaped workflows

This repository exists to document an alternative.

## Contents

### Architecture Brief

A short, focused document outlining the core ForgeDITA model:

* native XML as the system of record
* tenant-scoped semantic registry
* graph-aware services
* BYOE (Bring Your Own Editor)
* immutable, reproducible publishing

Start here:

* [ForgeDITA Architecture Brief](ForgeDITAArchitectureBrief.md)
* [Multi-Tenant Architecture and the Toolchain Registry Model](multiTenant.md)

## What This Is

* A working set of ideas
* A technical position on how DITA systems should behave
* A basis for discussion with experienced practitioners

## What This Is Not

* A marketing site
* A feature list
* A promise of implementation details

The goal is clarity, not hype.

## Status

ForgeDITA is currently in **architecture-first development**.

The product is moving toward MVP. The ideas documented here are intended to be stable enough for technical review, but may evolve as implementation begins.

## Feedback

If you have experience with DITA, structured content systems, or large-scale publishing pipelines, thoughtful feedback is welcome.

Key questions:

* Where does this model break?
* What assumptions are incomplete?
* What would you change before implementation?

## License

(To be determined)

## Related

* Website: <https://forgedita.com>
* Contact: [hello@forgedita.com](mailto:hello@forgedita.com)

Structured content, forged right.
