<p align="center">
  <a href="#the-capital-system">THE CAPITAL SYSTEM</a> ·
  <a href="#data-moat">DATA MOAT</a> ·
  <a href="#research-engine">RESEARCH ENGINE</a> ·
  <a href="#deployment-gate">DEPLOYMENT GATE</a> ·
  <a href="#operating-leverage">OPERATING LEVERAGE</a>
</p>

<h1 align="center">codeshark94</h1>

<p align="center">
  <strong>From market data to controlled capital deployment.</strong><br>
  Building the layers that make an economic edge harder to fake and easier to operate.
</p>

<p align="center">
  <code>truth</code> → <code>edge</code> → <code>gate</code> → <code>leverage</code>
</p>

## The capital system

The strongest work here is not a collection of unrelated demos. It is one compounding loop:

<table>
  <tr>
    <td width="25%"><strong>01 / TRUTH</strong><br>remove survivorship and data-quality traps</td>
    <td width="25%"><strong>02 / EDGE</strong><br>turn questions into replayable candidates</td>
    <td width="25%"><strong>03 / GATE</strong><br>make execution earn authority</td>
    <td width="25%"><strong>04 / LEVERAGE</strong><br>repeat the loop locally</td>
  </tr>
</table>

## Data moat

### 01 / [FONA](https://github.com/codeshark94/FONA) — fix the question before optimizing the answer

Most backtests fail upstream. A universe built only from today's surviving tickers, unclassified instruments, or unfiltered corporate actions can manufacture an edge that never existed.

FONA — Finance Open Network Archive — builds a local, auditable DuckDB layer for that problem. It combines SEC-led delisting discovery, recoverable historical bars, security classification, liquidity metrics, price-quality flags, and a lifecycle-adjusted tradable universe.

<table>
  <tr>
    <td width="25%"><strong>24.06M</strong><br>daily price rows</td>
    <td width="25%"><strong>11.85K</strong><br>priced symbols</td>
    <td width="25%"><strong>12.88M</strong><br>lifecycle-adjusted memberships</td>
    <td width="25%"><strong>1,793</strong><br>delisting outcomes</td>
  </tr>
</table>

<p align="center"><sub>Read-only query against the current local DuckDB snapshot · price history through 2026-06-18 · 4,237 trading dates.</sub></p>

**Economic mechanism:** prevent false positives before they reach the model. One trustworthy data layer can reduce wasted research capital across every downstream strategy, while preserving the evidence needed to challenge a result.

## Research engine

### 02 / [SpectraGrid](https://github.com/codeshark94/SpectraGrid) — spend compute on candidates that can survive scrutiny

SpectraGrid takes a market question and carries it through deterministic strategy generation, point-in-time backtesting, archive context, correlation-aware portfolio selection, and contract-backed handoff. The dashboard keeps the path visible as **Operations → Alpha → Archive → Source**.

<p align="center">
  <img src="assets/spectragrid-alpha.png" alt="SpectraGrid Alpha dashboard showing portfolio selection, strategy counts, and an equity curve" width="100%">
</p>

<p align="center"><sub>Fresh local Alpha Lab capture · 2026-09-03 · 4/4 deployable combinations · 15,581 current strategies · alpha-v29 policy.</sub></p>

**Economic mechanism:** turn research time into reusable, cost-aware portfolio candidates instead of one-off charts. The screen is an archived backtest state; a separate forward paper run remains a separate evidence stream.

## Deployment gate

### 03 / [MARF](https://github.com/codeshark94/MARF) — make capital earn the right to move

MARF is the control plane between research evidence and execution. Account state, pre-trade risk, execution authority, market-session evidence, and orderbook capture remain separate gates. Paper is the default surface; live writes stay blocked until the protocol explicitly allows them.

<p align="center">
  <img src="assets/marf-safety.png" alt="MARF Safety workspace showing Paper risk and readiness gates" width="100%">
</p>

<p align="center"><sub>Safety surface: risk, readiness, and authority remain visible in Paper scope.</sub></p>

<p align="center">
  <img src="assets/marf-routers.png" alt="MARF Router workspace showing model, mode, order record, and orderbook replay evidence" width="100%">
</p>

<p align="center"><sub>Router replay: 5 models · 3 fixed modes · 1,595,643 orderbook snapshots; partial coverage remains explicit.</sub></p>

**Economic mechanism:** reduce the cost of operational mistakes while making execution quality measurable. MARF is valuable because it makes uncertainty visible before capital crosses a write boundary.

## Operating leverage

### 04 / [Codeshark](https://github.com/codeshark94/codeshark) — make the loop repeatable on a private machine

Codeshark is the local operating layer around Codex: project routing, persistent context, task execution, verification, and result delivery. It keeps sensitive work on the Mac while turning a finished task into a repeatable unit with a concrete project, a minimal change, fresh evidence, and a clear handoff.

**Economic mechanism:** operator leverage. The same control plane can carry data engineering, research, validation, and deployment work without turning private project state into a hosted dependency.

## What the stack protects

| Layer | Boundary |
| --- | --- |
| Data | survivorship-reduced universe ≠ a claim that every provider is complete |
| Research | backtest archive ≠ forward paper run ≠ live performance |
| Execution | replay diagnostics ≠ broker fills; acknowledgement ≠ acceptance |
| Operations | a ready-looking interface ≠ verified downstream behavior |

<p align="center"><sub>Selected visuals are fresh local captures from the actual project surfaces. Metrics are dated snapshots; they are not promises of realized returns or revenue.</sub></p>
