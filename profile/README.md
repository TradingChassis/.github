# TradingChassis

TradingChassis is an applied infrastructure and reliability lab for trading-adjacent systems.

It uses a trading domain to explore SRE, observability, reproducibility, operational workflows, and failure-aware infrastructure design.

It is not a trading bot, strategy library, alpha research project, or claim of trading performance.


<img src="https://img.spacergif.org/spacer.gif" width="1" height="16"/>


## Current Direction

The current direction is focused on **small, understandable proof-of-skill systems**:

- reproducible run workflows
- artifact-first observability
- local-first operational tooling
- metrics, dashboards, and reports
- runtime safety boundaries
- infrastructure automation
- failure-aware system design

The goal is to demonstrate infrastructure and reliability engineering discipline in a concrete domain, not to build a production trading platform.


<img src="https://img.spacergif.org/spacer.gif" width="1" height="16"/>


## Active Work

| Repository | Status | Role |
| --- | --- | --- |
| [`tradingchassis-ops-lab`](https://github.com/TradingChassis/tradingchassis-ops-lab) | Active / Primary | Local-first operations lab around NautilusTrader for reproducible backtest and paper-run workflows. |
| [`infrastructure`](https://github.com/TradingChassis/infrastructure) | Active / Foundation | Kubernetes, GitOps, observability, environment management, and operational infrastructure. |
| [`infrastructure-secrets`](https://github.com/TradingChassis/infrastructure-secrets) | Supporting | Secret-management integration work for Kubernetes-based infrastructure workflows. |


<img src="https://img.spacergif.org/spacer.gif" width="1" height="16"/>


## Active Project Map

| Area | What it demonstrates |
| --- | --- |
| **Run operations** | Versioned run specs, local workflows, generated artifacts, reports, and operational metadata. |
| **Observability** | Metrics export, local Prometheus/Grafana workflows, and dashboard-oriented inspection. |
| **Runtime safety** | File-based kill switch behavior and explicit operational boundaries. |
| **Infrastructure** | Kubernetes/GitOps foundation for reproducible environments and future deployment paths. |
| **Documentation** | Scope, limitations, run model, quickstarts, demo flows, and archived design history. |


<img src="https://img.spacergif.org/spacer.gif" width="1" height="16"/>


## Archived Work

Earlier repositories explored a custom trading-engine architecture.  
That direction is preserved as historical context, but it is no longer the active implementation path.

| Repository | Status | Notes |
| --- | --- | --- |
| [`core`](https://github.com/TradingChassis/core) | Archived / Legacy | Historical exploration of deterministic event-driven trading decision semantics. |
| [`core-runtime`](https://github.com/TradingChassis/core-runtime) | Archived / Legacy | Historical runtime and orchestration layer for the previous Core architecture. |
| [`docs`](https://github.com/TradingChassis/docs) | Archived / Legacy | Historical documentation archive for architecture, concepts, ADRs, operations, and project evolution. |


<img src="https://img.spacergif.org/spacer.gif" width="1" height="16"/>


## Boundaries

TradingChassis is intentionally scoped as a portfolio-style engineering lab. It is maintained as a personal proof-of-skill project.

It does not aim to be:

- a custom trading engine
- a production trading system
- a live trading system
- a strategy research platform
- a profitability or alpha claim
- a low-latency execution stack

The focus is infrastructure discipline: reproducibility, observability, operational clarity, safety boundaries, and failure-aware workflows.

For technical details, use the individual repository READMEs, documentation, issues, and discussions.

Contributions, feedback, and technical discussion are welcome, especially around trading infrastructure, deterministic systems, market data, research-to-production workflows, observability, reproducibility, and operations.
