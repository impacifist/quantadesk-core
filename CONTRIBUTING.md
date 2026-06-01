# Contributing

Thanks for considering a contribution to QuantaDesk.

This public project is intentionally focused on the open-source core: local
operator workflow, backtest plumbing, reporting, safety boundaries, deployment
readiness, and private strategy extension points.

## Good Contributions

- Documentation improvements.
- UI polish for the public project page.
- Safer setup and publishing guidance.
- Demo data and toy strategy examples that do not imply real edge.
- Tests for public infrastructure and safety boundaries.
- Bug reports with sanitized logs and reproduction steps.

## Please Do Not Submit

- Production strategy implementations.
- Parameter sets, ranking files, or generated candidates.
- Real market lists, fills, orders, balances, or account screenshots.
- Exchange credentials, webhook secrets, passphrases, or tokens.
- Proprietary research notes or private operator state.

## Pull Request Checklist

- Keep the change scoped.
- Avoid committing generated runtime data.
- Run sensitive-term scans before opening the PR.
- Explain safety implications when touching risk, execution, auth, or reporting
  boundaries.
- Use sanitized examples for logs, screenshots, and fixtures.

## Financial Safety

QuantaDesk is research and operations software. Contributions must not present demo
behavior as a profit promise, financial advice, or approval to trade real funds.
