# allternit-sdk — Agent Guide

> SDK monorepo: AI runtime, universal plugin SDK, and 12 card plugins.

## Quick Start

```bash
# There is no root install. Work inside the subdirectories:
cd plugin-sdk && npm install && npm run build
cd ../sdk              # build dist/ with `bun sdk/js/script/build.ts` from the platform repo
cd ../plugins/emailcomposercard-plugin && npm install && npm run build
```

## Key Commands

| Directory | Build | Test | Notes |
|-----------|-------|------|-------|
| `sdk/` | `bun sdk/js/script/build.ts` (run from platform repo) | — | `dist/` is build output, untracked |
| `plugin-sdk/` | `npm run build` (tsc) | `npm run test` (vitest) | Self-contained package |
| `plugins/*/` | `npm run build` (tsc) | — | Run `allternit-plugin validate` after build |

## Directory Map

| Path | Purpose |
|------|---------|
| `sdk/` | `@allternit/sdk` — AI runtime, harness, providers, ACP, client |
| `plugin-sdk/` | `@allternit/plugin-sdk` — Universal plugin runtime + CLI |
| `plugins/` | 12 card plugins (e.g., `marketresearchcard-plugin`) |

## Conventions

- **plugin-sdk** and **plugins** use plain `npm` (Node >= 18).
- **sdk** builds with Bun from the platform monorepo context.
- Plugins depend on `@allternit/plugin-sdk` and compile to `dist/` (CommonJS).

## Warnings

- Do not run `npm install` at the repo root — there is no root `package.json`.
- If you change `plugin-sdk/src/`, rebuild it before rebuilding any plugins that depend on it.
- Publishing is manual via `plugin-sdk/publish-all.sh`.

## Related Repos

- [`allternit-platform`](https://github.com/Gizziio/allternit-platform) — Core platform (needed to regenerate SDK from OpenAPI)
- [`gizzi-code`](https://github.com/Gizziio/gizzi-code) — AI assistant CLI
- [`allternit-docs`](https://github.com/Gizziio/allternit-docs) — Platform documentation
