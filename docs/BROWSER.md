# Browser support

MapleMCP supports two complementary browser paths.

## Agent Browser

Agent Browser provides managed browser sessions with explicit session/tab identities and capabilities for:

- session/profile lifecycle
- tab lifecycle and navigation
- semantic snapshots
- screenshots
- clicking, typing, selecting, and key presses
- back/forward/wait
- gated cookie and storage access
- gated DevTools commands and JavaScript evaluation
- gated network interception

Persistent profiles can preserve legitimate user sign-in state. Sensitive capabilities require stronger authorization.

## Browser Companion

Browser Companion is a paired Chromium bridge used for local-browser workflows, including the ChatGPT bridge.

It can queue prompts, inspect generation state, cancel a generation, and continue a named ChatGPT conversation through the paired local browser.

## Human handoff

MFA, passkeys, CAPTCHA, consent, and ambiguous authentication states are human-handoff points. Browser automation should not be used to bypass authentication controls.
