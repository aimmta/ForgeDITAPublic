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

This repository will grow into a set of documents that explain the ForgeDITA architecture to experienced DITA and structured-authoring professionals.

The current documents are:

### Architecture Brief

A focused overview of the core ForgeDITA model:

* native XML as the system of record
* tenant-scoped semantic registry
* graph-aware services
* BYOE (Bring Your Own Editor)
* immutable, reproducible publishing

### Multi-Tenant Architecture and Toolchain Model

A deeper look at how ForgeDITA approaches multi-tenancy:

* tenant isolation across all system layers
* toolchain registry as the control point for processing
* versioned, immutable publishing environments
* reproducible releases tied to explicit inputs

Start here:

* [Architecture Brief](ForgeDITAArchitectureBrief.md)
* [Multi-Tenant Architecture and the Toolchain Registry Model](multiTenant.md)

## What This Is

* A working set of ideas
* A technical position on how DITA systems should behave
* A growing body of architectural documentation

## What This Is Not

* A marketing site
* A feature list
* A finalized implementation

The goal is clarity, not hype.

## Status

ForgeDITA is in **architecture-first development**.

The goal is to validate the model before building the full system.

## Feedback

If you work with DITA at scale, your perspective is valuable.

Key questions:

* Where does this model break?
* What assumptions are incomplete?
* What would you change before implementation?

## Contact

[hello@forgedita.com](mailto:hello@forgedita.com)
https://forgedita.com

Structured content, forged right.
