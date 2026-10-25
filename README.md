# MapleMCP

**Secure AI control for your computers, browser, and mobile devices.**

MapleMCP connects authorized AI clients to devices you enroll. It provides a hosted MCP endpoint for files, processes, diagnostics, browser automation, ChatGPT-browser workflows, mobile control, and gated resident-worker capabilities.

This repository is MapleMCP's **public documentation, community, security-reporting, and release home**.

**The MapleMCP product implementation is not open source and is not published in this repository.**

- Product: https://maplemcp.ca
- Downloads: https://maplemcp.ca/downloads
- Hosted MCP endpoint: `https://maplemcp.ca/mcp`
- Beta offered in the download catalog on **2026-10-24**: **0.2.63-beta**, with separate signed sequences for Windows, Linux, and Android
- Tool availability: use current authenticated MCP discovery and effective per-device capability policy; older static tool counts are historical

## What you can find here

- public product and architecture documentation
- security model and vulnerability-reporting instructions
- MCP tool/capability documentation
- installation and release information
- browser and mobile capability documentation
- changelog and provenance
- Issues for bugs and feature requests
- Discussions for questions, ideas, and feedback
- user-facing release artifacts

## What is not published here

MapleMCP's endpoint/runtime implementation, Worker Fabric implementation, browser implementation, hosted control-plane implementation, production infrastructure, deployment configuration, signing operations, private operational runbooks, and internal engineering repository are not published here.

This is deliberate. Users and security researchers should be able to understand what MapleMCP can do, how its trust boundaries work, how to install it, and how to report problems without exposing unrelated private infrastructure or proprietary implementation source.

See [Repository scope](docs/REPOSITORY_SCOPE.md).

## Current capability surface

MapleMCP's tool catalog evolves across endpoint editions, operating systems and server releases. Capabilities include device discovery, files, diagnostics, processes, Agent Browser, Browser Companion and supported Android operations. Advanced and resident-worker functions are gated by account and device policy.

The historical 78-tool figure in earlier public documentation described the 0.2.28–0.2.30 public contract; it is **not** a reliable count for today's live MCP discovery. Inspect the current authenticated tool list and the selected device's effective permissions. See [Tool surface](docs/TOOLS.md) for the historical contract and general capability families.

## Security model

MapleMCP uses layered controls including:

- explicit enrollment and device identity
- device capability policy
- execution ownership for mutable work
- write lock and emergency stop
- mutation idempotency and replay protection
- bounded process/browser sessions
- device-specific authority and revocation
- audit/evidence metadata
- untrusted-endpoint evidence handling
- human handoff for MFA/authentication-sensitive browser states

See [Security model](docs/SECURITY_MODEL.md).

## Install

Use the official downloads page:

https://maplemcp.ca/downloads

Release artifacts are also mirrored under this repository's GitHub Releases when useful.

## Community

- **Bug reports:** GitHub Issues
- **Feature requests:** GitHub Issues
- **Questions and ideas:** GitHub Discussions
- **Security vulnerabilities:** use private vulnerability reporting; **do not open a public issue**
- **Product site:** https://maplemcp.ca

## Provenance

MapleMCP evolved from MapleRemote. The earliest prototype used Desktop Commander 0.2.50 under its MIT license as a local execution dependency. That dependency was later replaced by MapleMCP's native runtime. The historical relationship is documented in [PROVENANCE.md](PROVENANCE.md).

## Repository terms

The documentation and repository material here are not a grant to the private MapleMCP product source. See [LICENSE.md](LICENSE.md) and the live product terms at https://maplemcp.ca/terms.
