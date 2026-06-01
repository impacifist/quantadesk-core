# Publication Checklist

Use this checklist before making the public QuantaDesk repository visible.

## Repository Creation

- Create a new public repository with no private Git history.
- Copy only the sanitized public files into the new repository.
- Do not push the private development repository or any rewritten branch until
  the resulting history has been inspected.
- Confirm the open-source license before announcing the project. This starter
  package currently uses Apache-2.0.

## Content Boundary

- No production strategy source files.
- No private strategy YAML, TOML, JSON, or generated parameter files.
- No proprietary research notes, rankings, private market files, or operational
  candidates.
- No market archive, journal, fill, order, account, runtime, backup, or report
  files from a real operator environment.
- No exchange API keys, webhook secrets, passphrases, tokens, or credentials.
- No screenshots containing real balances, account identifiers, symbols,
  strategy IDs, order IDs, or performance numbers.

## Suggested First Release

- Static project page.
- Public roadmap.
- Usage overview.
- Security and public/private boundary document.
- License.
- Issue templates for bug reports and feature requests.
- GitHub Actions public-safety scan.

## Final Local Checks

Run keyword scans before publishing:

```powershell
rg -n -i "api[_-]?key|secret|passphrase|token|password|private key" .
rg -n -i -f path\to\private-publish-denylist.txt .
```

Keep the private publish denylist outside the public repository. It should
contain project-specific strategy names, private command names, candidate IDs,
market-list filenames, and other terms that should never appear in public copy.

Inspect the rendered page at desktop and mobile widths. Confirm that no image,
copy, command, path, or document exposes private strategy material.
