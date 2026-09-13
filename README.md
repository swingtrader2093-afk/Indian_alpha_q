# Indian Alpha Lab V3.6

V3.6 is the systematic research platform built on the validated V2.8 engine. Its purpose is simple: reduce the NSE universe to a small, explainable set of stocks worth manual chart review.

## Master pipeline
- Current NSE equity universe / manual tickers
- Fast broad screen
- Deep historical testing across 8 swing strategies
- Walk-forward validation and parameter sensitivity
- Current SAME-strategy signal check
- Current classical chart-pattern scan
- Volume confirmation
- Relative strength (RS60)
- Market-regime context
- Fundamental/quality context for deep-confirmation candidates
- Portfolio-correlation / sector diagnostics for Master candidates
- Forward Master-signal ledger for paper/live evaluation
- Evidence drill-down and complete ZIP evidence bundle

## Strict Master rule
A row reaches **MASTER** only when:
1. The same strategy is historically `PROMISING` after integrity, walk-forward and robustness checks.
2. That same strategy is active on the latest available bar.
3. A current chart pattern is detected for the ticker.
4. Pattern volume confirmation is `PASS`.

There is **no risk/reward gate** in V3.6. Entry, stop, position sizing and R:R remain a separate manual decision layer so the Master shortlist is not over-filtered.

Market regime, RS60, fundamentals, portfolio correlation and sector context are displayed as supporting information and do not silently remove Master candidates.

## Research lab
Markov, HMM, GARCH-style volatility, Student-t Monte Carlo, the 8 strategies, walk-forward validation, sensitivity, costs/slippage, research memory, NSE screening, parallel pattern scanning and evidence generation are retained from V2.8.

V3.6 also includes a small alpha-discovery diagnostic. It is deliberately research-only: it does not create or promote new live signals automatically, which helps limit data-mining/overfitting risk.

## Forward validation
Qualifying Master signals are appended to `research_memory/master_signal_ledger.csv`. This is the bridge from historical research to real forward evidence. The system does not execute orders.

## Important limitations
- The current NSE universe is not survivorship-bias-free historically.
- Yahoo Finance data availability and corporate-action history can vary.
- Fundamental fields may be unavailable for some securities; missing fundamentals never block a Master candidate.
- Pattern detection is heuristic structural recognition, not proof of a textbook pattern.
- Research scores and model outputs are not probabilities of profit.
- V3.6 is research-only and does not guarantee profitability.
