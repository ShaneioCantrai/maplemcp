# Security Policy

MapleMCP controls real devices. Security reports are treated as product-safety reports, not ordinary bug reports.

## Report a vulnerability privately

**Do not open a public GitHub issue for a suspected vulnerability.**

Use GitHub private vulnerability reporting:

https://github.com/ShaneioCantrai/maplemcp/security/advisories/new

Include the affected version/component, reproduction steps, expected impact, and safely redacted evidence.

Never include passwords, tokens, cookies, private keys, enrollment credentials, personal data, or unrelated infrastructure details in a public Issue or Discussion.

## Safe testing

Only test MapleMCP against systems and accounts you own or are explicitly authorized to test.

Do not use testing to access another user's devices, credentials, sessions, or data.

## Security model

MapleMCP uses device enrollment, capability policy, execution ownership, write lock, emergency stop, idempotency/replay protection, revocation, bounded process/browser sessions, human authentication handoff, and audit metadata.

See [docs/SECURITY_MODEL.md](docs/SECURITY_MODEL.md).

## Coordinated disclosure

We prefer coordinated disclosure. Credible reports will be triaged privately. Researcher credit can be provided when requested and appropriate.
