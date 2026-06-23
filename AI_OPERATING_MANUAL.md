# AI Operating Manual

## Roles

ChatGPT is used for:

* strategy research
* statistical validation
* backtest methodology
* architecture reasoning
* reviewing results
* identifying risks and failure modes

Claude Code is used for:

* repo implementation
* refactoring
* writing tests
* keeping code consistent with docs
* updating CURRENT_STATE.md after changes

Gemini is used only for rare external adversarial review.

The human is the final decision-maker.

## Rules

* GitHub/docs are the source of truth.
* Do not rely on chat history as source of truth.
* No live trading or broker execution code until a strategy survives validation.
* No C++ until the Python research/backtest pipeline proves useful.
* Every strategy needs a pre-written pass condition and kill condition.
* Every code change must update tests or explain why no test is needed.
* Every major decision gets an ADR.
* Do not optimize a strategy before the first clean baseline test.
* Do not change strategy rules after seeing results unless the change is logged as a new experiment.
