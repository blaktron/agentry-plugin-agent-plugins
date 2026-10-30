# Agentry (Agent Plugins package)

Agentry brings QuickAgents into your agent host. Search a registry, read a QuickAgent's capability contract, scan findings and signature, install it, and run it in Agentry's sandboxed runner with a preview you approve first. Build your own QuickAgent, validate it, get an AI Review and test it before you publish. The plugin drives the Agentry CLI on your computer; the CLI keeps your sign-in and enforces each QuickAgent's contract.

This package is an [Agent Plugins 1.0.0](https://agent-plugins.org/specification)
package: `plugin.json`, the `agentry` skill and the bundled Agentry MCP server
0.6.999 in `mcp.json`. It installs in every host that loads that format.

## Install

GitHub Copilot CLI:

```sh
copilot plugin install blaktron/agentry-plugin-agent-plugins
```

Hermes Agent:

```sh
hermes plugins install blaktron/agentry-plugin-agent-plugins --enable
```

Hermes asks before every Agentry call that is not read-only, because the
package marks the server untrusted.

Kiro: open the Powers panel, choose Add Custom Power, then Import power from
GitHub, and give it https://github.com/blaktron/agentry-plugin-agent-plugins.

Qwen Code, Devin CLI, Mistral Vibe and OpenHands load this package too; see
each host's documentation for its plugin directory.

## Requirements

- The Agentry CLI 0.6.63 or newer on `PATH`. Install it from https://secureagentry.net/download.
- Node 20 or newer on `PATH`.
- Docker, for runs on this computer.

Signing in stays in your terminal (`agentry login`); the plugin never sees
your token. Documentation: https://docs.secureagentry.net/agentry/mcp/. Privacy: https://secureagentry.net/privacy.
