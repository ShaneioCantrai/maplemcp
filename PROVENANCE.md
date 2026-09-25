# MapleMCP provenance

MapleMCP's engineering lineage is intentionally documented.

## Desktop Commander

The earliest MapleRemote Windows-agent prototype used `@wonderwhy-er/desktop-commander` 0.2.50 under its MIT license as a local MCP execution component. That dependency helped validate the remote-device architecture quickly.

MapleRemote's broker, enrollment, remote transport, identity model, OAuth/control plane, update control, and later MapleMCP product architecture were separate systems.

The Desktop Commander execution dependency was subsequently replaced by MapleMCP's native file, process, search, policy, and local-engine implementation. The 0.2.9-beta release line announced that Desktop Commander was no longer bundled or used by the Windows runtime.

Current MapleMCP releases do **not** depend on Desktop Commander at runtime.

## Compatibility

During the native-engine replacement, MapleMCP intentionally retained compatible MCP concepts and tool names where doing so reduced migration cost. Interface compatibility does not mean the implementations share source.

## Current source policy

MapleMCP's implementation repository is private. This public repository exists for documentation, releases, security reporting, Issues, Discussions, and public product metadata.

Publishing provenance is still important even when implementation source is proprietary: MapleMCP does not present its current runtime as if the early dependency never existed.
