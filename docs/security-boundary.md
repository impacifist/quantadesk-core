# Security And Public Boundary

QuantaDesk is designed for local-first research and operations. The public project
must never require publishing private strategy logic or operator state.

## Public By Default

These areas are appropriate for the public open-source core:

- local WebUI shell and operator workflow,
- backtest and reporting infrastructure,
- risk gate patterns and fail-closed controls,
- audit logs and run-card formats,
- deployment-readiness checklists,
- toy strategies and demo data,
- documentation for extension points.

## Private By Default

These areas should stay outside the public repository:

- production strategy implementations,
- strategy parameters and generated candidate files,
- proprietary research notes and rankings,
- private market lists and operational candidates,
- market archives, journals, fills, orders, account snapshots, and reports,
- exchange credentials, webhook secrets, passphrases, and tokens,
- screenshots or videos that show real operator state.

## Recommended Repository Split

Use two repositories:

```text
quantadesk-core/                 public, clean history
quantadesk-private-strategies/   private, operator-owned
```

The public core should expose interfaces. The private repository should provide
operator-specific strategy modules and local configuration.

## Live Trading Boundary

Live execution should be blocked unless all required safety checks pass. Model
or agent workflows may summarize, warn, veto, quarantine, or reduce risk, but
they must not place orders, increase risk, disable gates, or edit live runtime
settings.

## Publishing Rule

Do not make the private development repository public. Create a clean public
repository instead, because deleting files from the current working tree does
not remove them from Git history.
