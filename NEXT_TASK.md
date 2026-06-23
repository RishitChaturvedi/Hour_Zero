# Next Task

## Objective

Scaffold a minimal Python backtesting framework for Strategy 001.

## Context

Strategy 001 has been specified in:

research/strategy-specs/strategy_[001.md](http://001.md)

The next goal is to build only the basic research/backtesting plumbing needed to test this strategy later. Do not optimize the strategy. Do not add live trading.

## Requirements

Create a minimal Python structure that supports:

- loading daily OHLCV CSV data

- using adjusted close prices

- computing a 100-day simple moving average signal

- applying next-day execution logic

- applying transaction costs

- calculating an equity curve

- comparing against buy-and-hold

- reporting:

  - total return

  - annualized return

  - annualized volatility

  - Sharpe ratio

  - max drawdown

  - number of trades

  - exposure percentage

## Non-goals

- No live trading.

- No broker API.

- No C++.

- No dashboard.

- No parameter optimization.

- No multiple strategies.

- No machine learning.

- No intraday data.

## Tests required

Add tests for:

- moving average calculation

- signal generation

- transaction cost application

- max drawdown calculation

- basic equity curve calculation

## Definition of done

A minimal backtester exists and can run Strategy 001 on a CSV file later.

CURRENT_[STATE.md](http://STATE.md) is updated after implementation.