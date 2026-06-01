# QuantaDesk

![QuantaDesk project page hero](assets/hero-workstation.png)

QuantaDesk is a local-first trading research and operator workstation. It is
designed around a simple rule: experiments should become operational only after
data checks, backtests, paper evidence, risk review, and human approval agree.

This public repository is the sanitized open-source surface for the project. It
focuses on the workstation, evidence pipeline, reporting, safety boundaries, and
extension points. Private strategy implementations, parameter sets, proprietary
research, private market lists, operational candidates, credentials, journals,
and operator state are intentionally excluded.

## Project Page

Open the static project page:

```text
index.html
```

No build step is required. The page can be served directly by GitHub Pages.

## What This Public Version Covers

- Local operator workflow and WebUI direction.
- Backtest and reporting infrastructure.
- Run-card, audit, and evidence-first product language.
- Risk gate and fail-closed live-control philosophy.
- Documentation for the public/private strategy boundary.
- Roadmap for a clean open-source core.

## What This Public Version Does Not Include

- Production strategies or parameter files.
- Proprietary research notes or rankings.
- Private market lists or operational candidates.
- Exchange credentials, runtime journals, or operator state.
- Backtest result bundles that reveal selection logic.

## Repository Map

```text
.
├── index.html
├── styles.css
├── assets/
│   └── hero-workstation.png
├── docs/
│   ├── roadmap.md
│   ├── security-boundary.md
│   ├── publishing.md
│   └── usage.md
├── .github/
│   ├── ISSUE_TEMPLATE/
│   └── workflows/
├── LICENSE
└── PUBLICATION_CHECKLIST.md
```

## Publishing Notes

Publish this as a clean-history repository. Do not convert the private
development repository to public, because private strategy material may exist in
its Git history.

This starter package uses Apache-2.0 for the public surface. If you prefer a
different license, change `LICENSE` before the first public push.

See [docs/publishing.md](docs/publishing.md) for the clean-repository publishing
flow.

## Disclaimer

QuantaDesk is research and operations software. It is not financial advice, a
profit guarantee, or permission to trade real funds. Live trading should remain
blocked unless the operator has verified data quality, paper evidence, risk
controls, credentials, deployment security, and personal risk acceptance.
