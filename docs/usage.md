# Usage

The public QuantaDesk release should be used as a local research and operator
workstation scaffold.

## Local Preview

The current project page is static:

```text
open index.html
```

or serve the folder with any static file server.

## Intended Product Flow

1. Start the local workstation.
2. Confirm that credentials and private modules are stored outside Git.
3. Check data coverage and warnings.
4. Run demo backtests or private strategy backtests locally.
5. Review run cards, drawdown, fees, ledgers, and warning notes.
6. Observe paper-mode behavior before any operational promotion.
7. Keep live controls blocked until readiness gates pass.
8. Export reports for audit and review.

## Strategy Plug-In Shape

The public core should eventually support a private strategy package loaded from
local configuration. A private module can implement the strategy interface while
the public repository only documents the contract and ships safe examples.

Example shape:

```text
quantadesk-core/
  src/quantadesk/
    strategy_api.py

quantadesk-private-strategies/
  my_private_package/
    strategies/
      private_strategy.py
```

## Operator Safety

- Keep real credentials in `.env` or a secret manager, never in Git.
- Use paper mode until data quality, reporting, and risk controls are verified.
- Treat a backtest as evidence to investigate, not permission to trade.
- Keep all private research and candidate files outside the public repository.
