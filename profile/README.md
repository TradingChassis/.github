# TradingChassis

TradingChassis is an applied infrastructure and reliability lab for trading-adjacent systems.

It uses a trading domain to explore SRE, observability, reproducibility, operational workflows, and failure-aware infrastructure design.


<img src="https://img.spacergif.org/spacer.gif" width="1" height="16"/>


<p align="center">
  <img
    src="../assets/tradingchassis-overview.svg"
    alt="TradingChassis overview: applied infrastructure and reliability lab for trading-adjacent systems"
    width="760"
  />
</p>


<img src="https://img.spacergif.org/spacer.gif" width="1" height="16"/>


## Current Direction

<div align="center">

<img src="https://img.shields.io/badge/Reproducible-Run%20Workflows-0F172A?style=for-the-badge" />
<img src="https://img.shields.io/badge/Observable-Metrics%20%2B%20Reports-2563EB?style=for-the-badge" />
<img src="https://img.shields.io/badge/Local--First-Operational%20Tooling-334155?style=for-the-badge" />

<br/>

<img src="https://img.shields.io/badge/Runtime-Safety%20Boundaries-0F766E?style=for-the-badge" />
<img src="https://img.shields.io/badge/Infrastructure-Kubernetes%20%2B%20GitOps-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white" />
<img src="https://img.shields.io/badge/Failure--Aware-System%20Design-7C3AED?style=for-the-badge" />

</div>

<br/>

The current direction is focused on **small, understandable proof-of-skill systems**.

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

<p align="center">
  <img
    src="../assets/active-project-map.svg"
    alt="Active project map: run operations, observability, runtime safety, infrastructure, and documentation"
    width="760"
  />
</p>


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

TradingChassis is intentionally scoped as a portfolio-style engineering lab.

It is not a trading bot, strategy library, alpha research project, or claim of trading performance.

The focus is infrastructure discipline: reproducibility, observability, operational clarity, safety boundaries, and failure-aware workflows.

For technical details, use the individual repository READMEs, documentation, issues, and discussions.

<div align="left">

<img src="https://img.shields.io/badge/Not%20A-Custom%20Trading%20Engine-334155?style=for-the-badge" />
<img src="https://img.shields.io/badge/Not%20A-Production%20Trading%20System-334155?style=for-the-badge" />
<img src="https://img.shields.io/badge/Not%20A-Strategy%20Research%20Platform-334155?style=for-the-badge" />

<br/>

<img src="https://img.shields.io/badge/No-Profitability%20Claim-7F1D1D?style=for-the-badge" />
<img src="https://img.shields.io/badge/No-Alpha%20Claim-7F1D1D?style=for-the-badge" />
<img src="https://img.shields.io/badge/No-Low--Latency%20Claim-7F1D1D?style=for-the-badge" />

</div>

<br/>


<img src="https://img.spacergif.org/spacer.gif" width="1" height="16"/>


## Contributing and Contact

Contributions, feedback, and technical discussion are welcome around infrastructure, reliability engineering, observability, reproducibility, operational workflows, and trading-adjacent systems.

See [CONTRIBUTING.md](https://github.com/TradingChassis/.github/blob/main/CONTRIBUTING.md) for guidance.

For project inquiries, use the relevant repository discussions or issues.
