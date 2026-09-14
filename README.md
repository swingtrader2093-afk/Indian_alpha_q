# Indian Alpha Lab V3.6 — Automated Alpha Discovery

This patch adds executable AUTO hypothesis strategies alongside the established strategy set. AUTO strategies are candidate feature-combination hypotheses and are subjected to the same backtest, walk-forward, sensitivity and integrity checks. A promotion engine labels a hypothesis PROMOTED only when robustness gates pass. Promotion is research qualification only, never an order or buy signal.

Includes Darvas Box, VCP, Flat Base, Donchian, High Tight Flag, Base Breakout and existing pattern detectors. Master / Master Watch remain manual-review outputs; R:R, entry, stop and position sizing are intentionally excluded.

Before scaling to the full universe, validate the run on 200 stocks and inspect `strategy_promotion.csv`, `alpha_discovery_diagnostic.csv`, `validation_audit.csv`, and the evidence bundle.


## Universe methodology
The current NSE equity universe is suitable for today's candidate screening but is not survivorship-bias-free historically. The app now reports this separately as `Universe quality = REVIEW — current NSE universe`; it does not classify that known limitation as a computational integrity failure. `Research integrity = PASS` means the experiment completed with required finite metrics; insufficient trade counts remain evidence-quality gates. A future point-in-time historical universe can be added without changing the current-screening workflow.
