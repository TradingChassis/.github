# TradingChassis

---

## Purpose

TradingChassis is a trading infrastructure focused on microstructure-driven Strategies. The core architectural goal is a unified conceptual model that makes Backtesting results transferable to Live: Backtesting and Live share the same Runtime semantics, so a Strategy's behavior in simulation aligns with its behavior in production as closely as possible.

TradingChassis is an engineering-focused infrastructure project built around strict Determinism, explicit architectural boundaries, and a strong separation between canonical semantics and their implementation-facing realizations.

---

## Focus Areas

- **Deterministic event-driven Runtime** — all State is a reproducible projection from a canonical Event Stream. No hidden mutable truth.
- **Unified Backtesting and Live semantics** — the same Core governs both Backtesting and Live, aligning simulation behavior with production behavior as closely as possible.
- **Market Microstructure as Primary Market Representation** — all market views are derived from microstructure-level market representation.
- **Structured data platform** — raw market data capture, validation, and canonical promotion with clear Pipeline stages and explicit provenance.
- **Explicit architectural documentation** — architecture decisions, canonical concept definitions, and implementation-facing Stack documents maintained as a first-class engineering artifact.

---

## Repositories

| Repository | Role |
| --- | --- |
| [Core](https://github.com/TradingChassis/core) | The deterministic, event-driven engine: Event processing, State derivation, Strategy execution, Risk validation, Order lifecycle, and Venue interaction. |
| [Core Runtime](https://github.com/TradingChassis/core-runtime) | Deployed environments for the Core for either Backtesting or Live: running the Core against either historical canonical data with a simulated Venue or live feeds with a real Venue. |
| Data (work in progress) | Data Platform for market data recording, validation, normalization, and Canonical Storage infrastructure. |
| [Infrastructure](https://github.com/TradingChassis/infrastructure) | Kubernetes deployment, environment management, and operational tooling. |
| [Infrastructure Secrets](https://github.com/TradingChassis/infrastructure-secrets) | OCI Secrets management and Vault integration for mounting Kubernetes secrets via the Secrets Store CSI driver, including multi-architecture image builds. |
| [Documentation](https://github.com/TradingChassis/docs) | Infrastructure concepts, architecture views, ADRs, implementation-facing Stack documents, and operational model. |

---

## How the Repositories Fit Together

The Data Platform produces canonical datasets from raw market feeds. The Core Runtime consumes those datasets during Backtesting and Live, applying a deterministic event-driven model in both contexts. Research uses the Backtesting environment to evaluate Strategies against historical data. Live applies the same Runtime semantics against real Venues with real-execution consequences.

The Documentation repository is the authoritative reference for how all of this is structured, why it is built the way it is, and what the canonical models mean.

---

## Documentation

The full technical documentation is maintained at:

**[TradingChassis Documentation](https://tradingchassis.github.io/docs/latest/)**

The documentation covers:

- **Architecture** — Structure, logical and physical views, and Architecture Decision Records
- **Concepts** — canonical semantic models: Event, State, Time, Determinism, Order lifecycle, Queue semantics, and invariants
- **Stacks** — implementation-facing descriptions of each Stack (Data Recording, Data Quality, Data Storage, Backtesting, Live, Analysis, Monitoring)
- **Operations** (work in progress) — operational model, monitoring, and recovery context
- **Evolution** — roadmap, milestones and development logs

Concept documents are the authoritative semantic reference. Stack documents are applied implementation views that realize those concepts without redefining them.

---

## Working Principles

**Determinism is non-negotiable.** Given the same Event Stream and Configuration, the Infrastructure must produce identical State at every Event Stream position, across all Runtimes and all domains.

**Events are the only source of State Transitions.** All State evolution is caused by processing canonical Events. No spontaneous updates, timer-driven branches, or out-of-band writes.

**Canonical concepts are separated from implementation.** The Event model, State model, Determinism model, and lifecycle semantics are defined once and applied consistently. Stack documents realize these models — they do not redefine them.

**Architecture is a first-class artifact.** Design decisions are documented as ADRs. Boundaries are explicit. The documentation is maintained with the same discipline as the code.

**Research and Live share a conceptual model.** The architecture is designed to eliminate the divergence between simulation and production — not to minimize it, but to make it structurally impossible by sharing the Core Runtime.

---

## Current Status

This infrastructure is under active development. The documentation repository reflects the current architectural progress, while the code repositories reflect the current implementation progress.

---

## Contributing and Contact

Contributions are welcome. See [CONTRIBUTING.md](https://github.com/TradingChassis/docs/blob/main/CONTRIBUTING.md) in the documentation repository for guidance.

For broader project inquiries, see the organization profile or open a discussion in the relevant repository.
