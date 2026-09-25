# Security model

MapleMCP connects AI clients to real devices. Its security model assumes mistakes, stale state, disconnected clients, hostile/untrusted endpoint output, and ambiguous network failures can occur.

## Enrollment and device identity

A device must be enrolled to an account before it can receive authorized work. Device identity and capability policy are checked independently of the caller's request.

## Capability policy

Devices advertise bounded capability families. An MCP client cannot widen a device's capability policy merely by requesting a tool.

## Execution ownership

Mutable work is associated with controller/session and execution state so unrelated controllers cannot silently take over in-flight work.

## Write lock and emergency stop

Write lock blocks mutation paths. Emergency stop is intended to halt mutable work and prevent new mutations until explicitly cleared.

## Idempotency and uncertainty

Mutation requests use request identity/fingerprints where applicable. Ambiguous results are reconciled rather than blindly retried.

## Process safety

MapleMCP distinguishes bounded input from advanced raw interactive input. Destructive process actions require exact target selection.

## Browser safety

Browser sessions use explicit profiles and session/tab identities. Sensitive capabilities such as cookies, storage export, raw DevTools commands, page JavaScript, and network interception require stronger authorization.

## Human authentication

MFA, passkeys, CAPTCHA, consent, and similar states are human-handoff points. MapleMCP is not intended to bypass authentication controls.

## Untrusted evidence

Text, files, logs, screenshots, browser content, and other endpoint-provided evidence are treated as untrusted data rather than authority instructions.

## Audit

The control plane retains bounded execution/audit metadata needed to establish who requested work, where it was directed, and how it terminated.

For vulnerability reporting, see [../SECURITY.md](../SECURITY.md).
