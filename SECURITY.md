# Security Policy

## Reporting a vulnerability

This repo is the **landing page** for [Claudeway](https://github.com/JordanNewell/claudeway) — a static HTML site with no server-side code, no database, and no user accounts. The attack surface is minimal.

That said, if you find something exploitable (XSS via the interactive verifier's input handling, supply-chain risk in the CDN dependencies, etc.) please report it:

1. Open a **private security advisory** on the SDK repo: https://github.com/JordanNewell/claudeway/security/advisories/new
2. Or email `security@jordannewell.com` (GPG-encrypt if sensitive — key published on the site)

Please **do not open a public issue** for security-relevant findings.

## Response SLA

- **Acknowledgement:** within 72 hours.
- **Initial assessment + triage:** within 7 days.
- **Fix or mitigation:** target 30 days for low/medium, 7 days for high/critical.

These are targets, not contractual guarantees. Claudeway is maintained by one person; sustained-burst attention is realistic, 24/7 on-call is not.

## Scope

**In scope:**
- The static HTML / CSS / inline JavaScript in this repo.
- The interactive receipt verifier's client-side logic.
- CDN dependencies (`@noble/curves`, `@noble/hashes`, Google Fonts).

**Out of scope** (filed against [JordanNewell/claudeway](https://github.com/JordanNewell/claudeway) instead):
- The Claudeway Python SDK.
- The cryptographic receipt format.
- The Ed25519 / ML-DSA-65 signature backends.
- The MCP server.

## Acknowledgements

Reporter credit is offered for accepted vulnerabilities. Coordinated disclosure follows [GitHub's CNA workflow](https://docs.github.com/en/code-security/security-advisories) — public disclosure happens after a fix ships, on a date we both agree on.
