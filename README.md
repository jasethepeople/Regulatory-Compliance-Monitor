# Regulatory-Compliance-Monitor

A Replit workspace export containing a generic pnpm monorepo scaffold — no project-specific application code.

## Features

- Express 5 API server skeleton with a single `/healthz` route and Zod-validated response
- OpenAPI spec with Orval codegen into React hooks (`api-client-react`) and Zod schemas (`api-zod`)
- Drizzle ORM Postgres schema package (empty schema index)
- `mockup-sandbox` React + shadcn preview harness for UI mockups
- Workspace tooling: esbuild bundling, shared tsconfig, typecheck/build scripts

## Tech stack

- TypeScript 5.9, Node.js 24, pnpm workspaces
- Express 5, Drizzle ORM, Zod v4, Orval

## Getting started

```bash
pnpm run typecheck              # typecheck all libs
pnpm run build                  # typecheck + build all packages
pnpm --filter @workspace/api-server run dev   # API server (port 5000)
```

Requires `DATABASE_URL` (Postgres). Commands come from `replit.md` in the repo.

## Project structure

```
├── artifacts/api-server/    # Express app (health route only)
├── artifacts/mockup-sandbox/ # React/shadcn mockup preview app
├── lib/api-spec/            # OpenAPI YAML + Orval config
├── lib/api-client-react/    # generated React API hooks
├── lib/api-zod/             # generated Zod schemas
├── lib/db/                  # Drizzle config (empty schema)
└── scripts/                 # build/merge tooling
```

## Status

**Stub / project scaffold.** The workspace template files (`replit.md`) were never populated. This tree is byte-identical to the `One-Person-Empire-OS` repo apart from metadata — it is the unmodified Replit starter, with nothing specific to regulatory compliance in it. Original workspace: https://replit.com/@serenebuilding/Regulatory-Compliance-Monitor
