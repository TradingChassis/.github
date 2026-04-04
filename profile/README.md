# CanonicalFlow

---

## What It Is

CanonicalFlow is a trading System focused on microstructure-driven Strategies. The core architectural goal is a unified conceptual model that makes Research results transferable to Live Execution: Backtesting and Live Execution share the same Runtime semantics, so a Strategy that behaves a certain way in simulation against a given Event Stream behaves the same way in production.

The System is not a general-purpose trading platform. It is an engineering-focused infrastructure project built around strict Determinism, explicit architectural boundaries, and a strong separation between canonical System semantics and their implementation-facing realizations.

---

## Focus Areas

- **Deterministic event-driven Runtime** — all State is a reproducible projection from a canonical Event Stream. No hidden mutable truth.
- **Unified Research and Live semantics** — the same core processing model governs both Backtesting and Live Execution, closing the gap between Research expectations and production behavior.
- **Structured data platform** — raw market data capture, validation, and canonical promotion with clear Pipeline stages and explicit provenance.
- **Explicit architectural documentation** — architecture decisions, canonical concept definitions, and implementation-facing Stack documents maintained as a first-class engineering artifact.

---

## Core Repositories

| Repository | Role |
| --- | --- |
| **Core Runtime** | The deterministic, event-driven execution engine: Event processing, State derivation, Strategy execution, Risk validation, Order lifecycle, and Venue interaction. |
| **Data Platform** | Market data recording, validation, normalization, and canonical storage infrastructure. |
| **Research / Backtesting** | Backtesting environment and orchestration: running the Core Runtime against historical canonical data with a simulated Venue, experiment management, and result persistence. |
| **Infrastructure / Tooling** | Deployment, environment management, and operational tooling. |
| **[This repository] Documentation** | Architecture knowledge base: canonical System concepts, architecture views, ADRs, implementation-facing Stack documents, and operational model. |

> Repository names and exact organization are subject to project structure. The table above reflects functional categories.

---

## How the Repositories Fit Together

The Data Platform produces canonical datasets from raw market feeds. The Core Runtime consumes those datasets during Backtesting and Live Execution, applying a deterministic event-driven model in both contexts. Research uses the Backtesting environment to evaluate Strategies against historical data. Live Execution applies the same Runtime semantics against live Venues with real-execution consequences.

The Documentation repository is the authoritative reference for how all of this is structured, why it is built the way it is, and what the canonical models mean.

---

## Documentation

The full technical documentation is maintained at:

**[CanonicalFlow Documentation](https://canonicalflow.github.io/docs/latest/)**

The documentation covers:

- **Architecture** — System structure, logical and physical views, and Architecture Decision Records
- **Concepts** — canonical semantic models: Event, State, Time, Determinism, Order lifecycle, Queue semantics, and invariants
- **Stacks** — implementation-facing descriptions of each subsystem (Data Recording, Data Quality, Data Storage, Backtesting, Live, Analysis, Monitoring)
- **Operations** — operational model, monitoring, and recovery context
- **Evolution** — roadmap and development history

Concept documents are the authoritative semantic reference. Stack documents are applied implementation views that realize those concepts without redefining them.

---

## Working Principles

**Determinism is non-negotiable.** Given the same Event Stream and Configuration, the System must produce identical State at every stream position, across all Runtimes and all domains.

**Events are the only source of State Transitions.** All State evolution is caused by processing canonical Events. No spontaneous updates, timer-driven branches, or out-of-band writes.

**Canonical concepts are separated from implementation.** The Event model, State model, Determinism model, and lifecycle semantics are defined once and applied consistently. Stack documents realize these models — they do not redefine them.

**Architecture is a first-class artifact.** Design decisions are documented as ADRs. Boundaries are explicit. The documentation is maintained with the same discipline as the code.

**Research and Live share a conceptual model.** The architecture is designed to eliminate the divergence between simulation and production — not to minimize it, but to make it structurally impossible by sharing the Core Runtime.

---

## Current Status

The System is under active development. The documentation repository reflects the current architectural State. Some sections — Operations and Evolution — are in progress.

---

## Contributing and Contact

Contributions to the documentation are welcome. See [CONTRIBUTING.md](https://github.com/CanonicalFlow/docs/blob/main/CONTRIBUTING.md) in the documentation repository for guidance.

For broader project inquiries, see the organization profile or open a discussion in the relevant repository.
