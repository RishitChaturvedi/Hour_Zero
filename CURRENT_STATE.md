# Current State

## ## What exists now

- [README.md](http://README.md) and [AGENTS.md](http://AGENTS.md) exist.
- Initial project control files exist.
- Strategy 001 spec exists at research/strategy-specs/strategy_[001.md](http://001.md).
- No backtester implemented.
- No live trading.
- No C++.
- No broker integration.

## What changed last session

- Created Strategy 001: SPY 100-Day Moving Average Trend Filter.
- Pre-committed pass and kill conditions before testing.

## Next task

- Scaffold a minimal Python backtester.

## What changed last session

- Project workflow was locked.
- README.md and AGENTS.md were updated or preserved.
- Initial folder structure was created if missing.

## Current architecture assumptions

- Python comes first.
- Research/backtesting comes before execution.
- No live trading or broker APIs until a strategy survives validation.
- No C++ until the Python research/backtest pipeline proves useful.

## Open questions

- What is Strategy #1?
- What dataset will be used?
- What pass/fail criteria will be used before testing?

## Next task

- Write Strategy #1 spec.

## Known risks

- Overbuilding infrastructure before validating a strategy.
- P-hacking by changing parameters after seeing backtest results.
- Adding too many tools before the basic pipeline works.
- Mistaking a good-looking backtest for real edge.