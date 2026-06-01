# Security Policy

## Reporting A Security Issue

Please report security issues privately. Do not open a public issue containing
credentials, account state, private logs, or exploit details.

Until a dedicated security email is published, use a private repository contact
or maintainer channel.

## Sensitive Data

Never include the following in public issues, pull requests, screenshots, or
attachments:

- API keys, secrets, passphrases, tokens, passwords, or private keys.
- Real account balances, fills, orders, positions, journals, or runtime state.
- Private strategy source code, parameter files, rankings, or candidate files.
- Proprietary research notes or private market lists.

## Live Execution Boundary

Public code and examples should keep live execution fail-closed by default.
Automated review or model-assisted workflows must not place orders, increase
risk, disable safety gates, or edit live runtime settings.

## Supported Versions

The public release is pre-1.0. Security expectations may change as the
repository is separated from the private development codebase.
