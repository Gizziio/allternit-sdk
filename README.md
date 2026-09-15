# Allternit SDK

> **Allternit SDK Monorepo**
> AI runtime, universal plugin SDK, and 12 ready-to-use card plugins for the Allternit platform.
[![License: Apache 2.0](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

## Packages

| Package | Description | NPM |
|---------|-------------|-----|
| `@allternit/sdk` | AI runtime, harness, providers, ACP, and OpenAPI-generated client | [npm](https://www.npmjs.com/package/@allternit/sdk) |
| `@allternit/plugin-sdk` | Universal plugin runtime + 6 adapters + CLI | [npm](https://www.npmjs.com/package/@allternit/plugin-sdk) |
| `@allternit/*-plugin` | 12 card plugins (market research, code review, image gen, etc.) | [search](https://www.npmjs.com/search?q=%40allternit%20plugin) |

## Directory Layout

```
sdk/           ← AI runtime SDK (harness, providers, ACP, client)
plugin-sdk/    ← Universal plugin SDK + adapters + CLI
plugins/       ← 12 card plugins
```

## Quick Start

```bash
# Install the SDK
npm install @allternit/sdk

# Install the plugin SDK
npm install @allternit/plugin-sdk

# Install a plugin globally
npm install -g @allternit/marketresearchcard-plugin
```

## Related Repositories

- [`allternit-platform`](https://github.com/Gizziio/allternit-platform) — Core platform monorepo
- [`gizzi-code`](https://github.com/Gizziio/gizzi-code) — Workspace-aware AI assistant CLI
- [`allternit-docs`](https://github.com/Gizziio/allternit-docs) — Platform documentation

## License

Licensed under the [Apache License, Version 2.0](LICENSE). Copyright 2026 Allternit LLC.
Allternit, Gizzi, and A:// are trademarks of Allternit LLC (see [NOTICE](NOTICE)).
