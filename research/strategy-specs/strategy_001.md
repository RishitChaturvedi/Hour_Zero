# Strategy 001: SPY 100-Day Moving Average Trend Filter

## Status

Draft / Not Tested

## Purpose

This is the first baseline strategy for Hour Zero, the trading research/backtesting repo inside the Day One project.

The goal is not to prove a profitable strategy immediately. The goal is to create a simple, pre-committed strategy spec that can later be used to test the research/backtesting pipeline without p-hacking.

## Hypothesis

SPY may exhibit medium-term trend persistence, where being above its 100-day moving average indicates a higher probability of continued positive returns than being below it.

## Economic Rationale

The strategy is based on trend-following / time-series momentum.

The possible rationale is that investors may react slowly to new information, institutional flows can persist over time, and broad equity indices may trend because of macro and risk-on/risk-off regimes.

This is only a hypothesis and must be tested.

## Instrument / Universe

- Instrument: SPY
- Universe size: 1 ETF
- Asset class: US equity ETF
- Timeframe: Daily bars

## Data Requirements

- Daily OHLCV data for SPY
- Adjusted close prices
- Data must account for dividends and splits
- No missing trading days without explanation
- No future data may be used in signal calculation

## Entry Rule

At the close of each trading day, compute the 100-day simple moving average using only data available up to that day.

Enter long SPY when:

- adjusted close > 100-day simple moving average

## Exit Rule

Exit to cash when:

- adjusted close <= 100-day simple moving average

## Position Sizing

- 100% long SPY when signal is active
- 100% cash when signal is inactive
- No leverage
- No shorting

## Transaction Cost Assumption

Initial baseline:

- 0.05% cost per trade side

Stress test later:

- 0.10% cost per trade side
- 0.20% cost per trade side

## Backtest Rules

- No lookahead bias
- Signal generated using today’s close may only be executed on the next trading day
- Include transaction costs
- Compare against buy-and-hold SPY
- Report total return, annualized return, volatility, Sharpe ratio, max drawdown, number of trades, and exposure percentage

## Pass Condition

The strategy deserves further research only if:

- it performs reasonably after transaction costs
- it reduces max drawdown compared with buy-and-hold
- it does not rely on one or two lucky trades
- it remains directionally reasonable under higher cost assumptions
- its behavior is explainable and not obviously a data artifact

## Kill Condition

Reject or deprioritize the strategy if:

- it underperforms buy-and-hold after costs without reducing drawdown
- performance disappears under slightly higher transaction costs
- results depend heavily on the exact 100-day parameter
- most returns come from one isolated period
- signal timing uses future information
- data quality is questionable

## Notes

This is a baseline strategy for validating the pipeline.

Parameter optimization is not allowed in the first test. Do not test 20, 50, 100, and 200-day moving averages and then pick the best one unless that is logged as a separate experiment.