# Current State

## What exists now

* README.md and AGENTS.md exist.
* Initial project control files are being created.
* No strategy implemented.
* No backtester implemented.
* No live trading.
* No C++.
* No broker integration.

## What changed last session

* Project workflow was locked.
* README.md and AGENTS.md were updated or preserved.
* Initial folder structure was created if missing.

## Current architecture assumptions

* Python comes first.
* Research/backtesting comes before execution.
* No live trading or broker APIs until a strategy survives validation.
* No C++ until the Python research/backtest pipeline proves useful.

## Open questions

* What is Strategy #1?
* What dataset will be used?
* What pass/fail criteria will be used before testing?

## Next task

* Write Strategy #1 spec.

## Known risks

* Overbuilding infrastructure before validating a strategy.
* P-hacking by changing parameters after seeing backtest results.
* Adding too many tools before the basic pipeline works.
* Mistaking a good-looking backtest for real edge.
