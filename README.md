# Indian Alpha Lab V4 — Institutional Research Engine

## Purpose
V4 is a research-grade opportunity discovery tool for Indian equities. Its job is to reduce the NSE universe to a small set of stocks worth manual chart/research time. It is not an order-execution system and does not claim to predict prices.

## Included research stack
- 8 established swing strategies
- 6 executable AUTO feature-combination hypotheses
- Markov chains
- Hidden Markov Model (where `hmmlearn` is available)
- GARCH-style volatility regime
- Student-t Monte Carlo
- XGBoost / LSTM research components retained from the V3 engine where dependencies are available
- walk-forward validation
- sensitivity testing
- cross-stock AUTO promotion
- classical pattern scanner including Darvas, Donchian, VCP, bases, flags/pennants, triangles, wedges, H&S and double tops/bottoms
- relative strength, volume and market/sector context
- fundamentals as contextual evidence
- Master shortlist and forward signal ledger
- evidence drilldown and downloadable research bundle

## Data policy
The V4 architecture explicitly separates data provenance from research logic.

- NSE public reports are the preferred source for market/security/corporate-action data when available.
- Yahoo Finance/yfinance is retained as a practical fallback and for the current fundamental snapshot.
- Current NSE universe screening is clearly labelled `CURRENT_NSE` and `Universe quality = REVIEW` because it is not a point-in-time survivorship-bias-free historical universe.
- That universe limitation is NOT a computational integrity failure.
- Missing or unavailable data is labelled unknown/review rather than fabricated.

NSE publicly exposes equity reports including Common Bhavcopy/UDiFF, security master, delivery positions and adjusted 52-week reports. NSE also provides corporate-action reports with record/ex dates.

## Institutional-grade boundary
This package implements an institutional-style research architecture and audit discipline, but it does not claim to possess a paid institutional point-in-time vendor dataset. A true point-in-time universe/fundamental-vintage dataset can be plugged into the declared schemas later without redesigning the quant engine.

## Run
1. Upload the ZIP to Streamlit Community Cloud.
2. Run 200 stocks first for a smoke/validation run.
3. Review the COMPLETE EVIDENCE BUNDLE.
4. Then scale to the full NSE universe.
5. Treat Master as a research shortlist; perform manual chart, liquidity, event and risk review before any trade.

## Important
- No risk/reward filter is used in Master by design.
- No model is a buy signal by itself.
- Promotion requires cross-stock robustness and final validation.
- Research results do not guarantee future profitability.
