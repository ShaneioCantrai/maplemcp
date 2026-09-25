# Public architecture

At a high level:

```text
MCP client
   |
   | authenticated MCP
   v
Hosted MapleMCP control plane
   |
   | authenticated device relay
   v
Enrolled MapleMCP endpoint
   |
   +-- files / search
   +-- managed processes
   +-- system diagnostics
   +-- Agent Browser
   +-- Browser Companion / ChatGPT bridge
   +-- resident Worker Fabric canary

Mobile devices enroll as a separate device class.
```

## Capability enforcement

A tool existing in the global MCP schema does not automatically grant a device permission to execute it.

Each enrolled device advertises capability policy. Mutable work is additionally constrained by execution ownership and account/device policy.

## Browser paths

MapleMCP has two browser concepts:

- **Agent Browser** — managed browser sessions with explicit profiles, tabs, snapshots, screenshots, DOM-level actions, and gated advanced capabilities.
- **Browser Companion** — a paired Chromium bridge for workflows such as sending/continuing ChatGPT conversations in the user's local browser.

MFA, passkeys, CAPTCHA, consent, and ambiguous authentication states are human-handoff points.

## Worker Fabric

0.2.28 includes a resident Worker Fabric canary. Worker tasks are durable and re-enter the same capability/authority paths as explicit MCP calls. Worker controls remain feature-gated and are not included in normal 78-tool discovery.
