# Roadmap

QuantaDesk's public roadmap is about making a safer local research workstation,
not publishing private strategy logic.

## Phase 0: Clean Public Foundation

- Publish a clean-history repository.
- Keep the public surface free of private strategy material.
- Add a project page, public roadmap, and security-boundary documentation.
- Add CI checks that fail if known private paths or sensitive keywords appear.

## Phase 1: Local Operator Console

- Provide a simple local WebUI for setup, status, paper mode, reports, and
  emergency controls.
- Keep advanced research tools available, but separate them from the beginner
  operator flow.
- Make safety state obvious: stopped, paper-only, blocked, warning, or ready for
  operator review.

## Phase 2: Backtest And Report Kit

- Include sample data and toy strategy examples that demonstrate the interface
  without revealing proprietary edge.
- Export run cards, ledgers, equity curves, drawdown charts, and plain-language
  summaries.
- Make result artifacts reproducible and easy to audit.

## Phase 3: Private Strategy Plug-Ins

- Define a stable strategy interface.
- Document how operators can load private strategy packages locally.
- Keep private modules outside the public repository by default.
- Provide example plug-ins that are educational rather than production-grade.

## Phase 4: Deployment Readiness

- Add self-host templates for private deployments.
- Provide health checks, backup guidance, restore drills, and log rotation.
- Harden authentication and role boundaries before any remote exposure.
- Keep live controls fail-closed until readiness checks and operator approval
  pass.

## Phase 5: Model-Assisted Review

- Use models for summaries, risk notes, evidence review, and quarantine
  recommendations.
- Keep model output advisory only.
- Prevent model workflows from placing orders, increasing risk, editing live
  settings, or bypassing deterministic controls.
