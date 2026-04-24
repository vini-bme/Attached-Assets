# Workspace

## Overview

pnpm workspace monorepo using TypeScript. Each package manages its own dependencies.

## Stack

- **Monorepo tool**: pnpm workspaces
- **Node.js version**: 24
- **Package manager**: pnpm
- **TypeScript version**: 5.9
- **API framework**: Express 5
- **Database**: PostgreSQL + Drizzle ORM
- **Validation**: Zod (`zod/v4`), `drizzle-zod`
- **API codegen**: Orval (from OpenAPI spec)
- **Build**: esbuild (CJS bundle)

## Key Commands

- `pnpm run typecheck` — full typecheck across all packages
- `pnpm run build` — typecheck + build all packages
- `pnpm --filter @workspace/api-spec run codegen` — regenerate API hooks and Zod schemas from OpenAPI spec
- `pnpm --filter @workspace/db run push` — push DB schema changes (dev only)
- `pnpm --filter @workspace/api-server run dev` — run API server locally

See the `pnpm-workspace` skill for workspace structure, TypeScript setup, and package details.

## Artifacts

- **`api-server`** — Express 5 API. Exposes `POST /api/ai/insight` (Gemini-powered structural analysis) and `GET /api/healthz`.
- **`fleximap`** — React + Vite web app at path `/`. Protein flexibility & allosteric target mapping suite.
  - **Analytics page (`/`)**: PDB upload (or built-in 1CRN crambin demo), client-side Gaussian Network Model dynamics, 3Dmol viewer color-coded by per-residue fluctuation, recharts profile, sortable/filterable residue table with CSV export, and AI structural insight.
  - **Docking page (`/docking`)**: ligand sequence input, before/after metrics (binding affinity, RMSD shift, targetability), 3D stabilization map highlighting damped hinge residues in teal, and AI mechanism-of-action explainer.
  - **Pocket Profiler page (`/pocket`)**: top-15 most-flexible residues with biochemical properties, polarity composition bar, and AI pharmacophore generator.
  - **Protein Compare page (`/compare`)**: two independent upload slots, side-by-side 3D viewers, normalized overlaid flexibility profile chart, and a "conserved hinges" table showing aligned positions where both proteins fall in the top 25% flexibility percentile, plus an AI cross-protein interpretation.
  - Built with `3dmol`, `ml-matrix` (eigendecomposition for GNM), `recharts`, `wouter`, `papaparse`, plus the standard shadcn/ui kit.
- **`mockup-sandbox`** — design playground (template default).

## Integrations

- **Replit Gemini AI** — wired through `lib/integrations-gemini-ai`. Requires `AI_INTEGRATIONS_GEMINI_BASE_URL` and `AI_INTEGRATIONS_GEMINI_API_KEY` env vars (set via the integrations panel).
