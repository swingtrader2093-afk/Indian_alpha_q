# V4 Data Source Policy

| Layer | Preferred | Fallback | Historical caveat |
|---|---|---|---|
| Price/volume | NSE public reports | yfinance | Corporate-action adjustment must be respected |
| Security master | NSE | yfinance | Symbol changes need mapping |
| Corporate actions | NSE | yfinance | Use ex/record dates where available |
| Fundamentals | Point-in-time filings when available | Yahoo/yfinance `.info` | Current `.info` is NOT point-in-time |
| Universe | Point-in-time membership | Current NSE universe | Current universe has survivorship limitation |
| Quant models | Local deterministic calculations | — | Model output is evidence, not prediction certainty |

The app never converts missing data into a fabricated PASS.
