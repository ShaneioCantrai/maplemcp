# Changelog

MapleMCP is currently in beta.

## 0.2.30-beta — 2026-09-25

- hardened downloadable runtime artifacts so MapleMCP no longer ships a convenient readable implementation source tree
- minified desktop/server runtime JavaScript after compilation
- reduced the updater to a minified bundled entrypoint plus runtime dependencies/trust metadata
- shipped Browser Companion 0.1.7 as a minified runtime-only package
- rejected MapleMCP-owned TypeScript/TSX/source-map files from release runtime trees
- rebuilt and timestamp-signed the Windows installer from the exact accepted hardened artifacts
- independently extracted the signed installer and reverified its embedded agent/updater hashes and hardened contents

## 0.2.29-beta — 2026-09-25

- completed the new Windows installer lifecycle and recovery path
- hardened fresh install, repair, upgrade, canary promotion, uninstall persistence, and failure rollback behavior

## 0.2.28-beta — 2026-09-24

- shipped the resident Worker Fabric canary behind explicit gates
- kept normal public MCP discovery at 78 tools
- continued the MapleMCP public-domain migration while preserving compatibility identifiers
- published refreshed Windows and Linux beta artifacts
- verified a live ChatGPT-controller → MapleMCP → resident worker canary path
- verified Worker → Agent Browser canary handoff
- preserved durable worker state across restart

## 0.2.27-beta — 2026-09-24

- made `maplemcp.ca` the public product origin for new enrollment/public-facing flows
- preserved existing MapleRemote compatibility paths for enrolled agents/runtime identifiers

## 0.2.26-beta — 2026-09-23/24

- expanded the public MCP contract to 78 tools
- added broad Agent Browser and ChatGPT-browser coverage
- added desktop diagnostics including hashing, sizing, resources, networking, DNS, TCP probing, and process trees

## 0.2.9-beta

- replaced the historical Desktop Commander-backed Windows execution runtime with MapleMCP's native engine

For current binaries and release-specific notes, see GitHub Releases and https://maplemcp.ca/downloads.
