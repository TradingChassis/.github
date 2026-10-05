# TradingChassis

TradingChassis is an applied engineering portfolio focused on **infrastructure and operational discipline**.

Trading is used as a demanding technical domain to demonstrate practical and architectural infrastructure engineering skills.

It is **not** a trading bot, alpha research platform, or claim of financial performance.

## Repository Map

```text
TradingChassis
│
├── Trading System Architecture
│
│   core
│   └── deterministic domain and decision logic
│        │
│        ▼
│   core-runtime
│   └── execution and runtime environment
│        │
│        ▼
│   infrastructure
│   └── deployment and operations
│        │
│        └── oci-secrets-store-csi-driver-provider
│            └── Kubernetes ↔ OCI Vault secrets integration
│
│   docs
│   └── architecture, concepts, and design decisions
│
└── tradingchassis-ops-lab
    └── standalone operations and reliability lab
        built around NautilusTrader
```

These repositories represent different layers of one larger **System Architecture**.

`core` contains deterministic trading-domain logic. `core-runtime` provides an environment in which that logic can be executed. `infrastructure` provides Kubernetes, GitOps, observability, storage, and cloud platform around those workloads. The OCI Secrets Store CSI provider supports that infrastructure by integrating Kubernetes workloads with OCI Vault.

`docs` preserves architecture, terminology, concepts, ADRs, and design decisions behind that system.

The custom trading-engine direction represented by `core`, `core-runtime`, and the archived documentation is retained as **architectural exploration and engineering evidence**, rather than active implementation direction.

## Operations Lab

[`tradingchassis-ops-lab`](https://github.com/TradingChassis/tradingchassis-ops-lab) is intentionally separate from custom trading-engine architecture.

It is a local-first operations and reliability lab built around **NautilusTrader**, focusing on reproducible workflows, artifacts, observability, reconciliation, failure handling, and operational controls rather than strategy performance.

## Repositories

| Repository | Role |
| --- | --- |
| [`tradingchassis-ops-lab`](https://github.com/TradingChassis/tradingchassis-ops-lab) | Standalone operations and reliability lab around NautilusTrader |
| [`infrastructure`](https://github.com/TradingChassis/infrastructure) | OCI, Kubernetes, GitOps, observability, storage, and infrastructure |
| [`oci-secrets-store-csi-driver-provider`](https://github.com/TradingChassis/oci-secrets-store-csi-driver-provider) | Kubernetes integration for retrieving secrets from OCI Vault |
| [`core`](https://github.com/TradingChassis/core) | Deterministic event-driven trading-domain and decision semantics |
| [`core-runtime`](https://github.com/TradingChassis/core-runtime) | Runtime and orchestration layer around Core |
| [`docs`](https://github.com/TradingChassis/docs) | Architecture, concepts, ADRs, operations, and project evolution |
| [`infrastructure-secrets`](https://github.com/TradingChassis/infrastructure-secrets) | Predecessor of the current OCI Secrets Store CSI provider fork, retained for historical context |
