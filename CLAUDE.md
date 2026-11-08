# CLAUDE.md — Engineered Recipes Starter

> Starter repo for AI University's **Engineered Recipes** course. Each lesson
> is its own hard, specific problem — add a route per recipe as you go rather
> than renaming the whole project.

## What this is
A shared Next.js + Supabase sandbox for the course's recipes (scheduling &
concurrency, and others as the course adds them).

## Stack
- Language: TypeScript
- Framework: Next.js (App Router) + React
- Datastore: Supabase (Postgres)
- Package manager: npm

## Run & test
- Install: `npm install`
- Dev: `npm run dev`
- Typecheck: `npm run typecheck`
- Lint: `npm run lint`

## House convention: keep Supabase calls in lib/data/
Only `lib/data/*` should import from `@supabase/ssr` or `@supabase/supabase-js`.
Routes and components call into `lib/data/` — they never run a query directly.

## Coding style
- ES modules / async-await, 2-space indent, descriptive names
- Comment WHY, not WHAT — skip obvious comments

## How to work here
- Read existing code before changing anything
- Each recipe is a focused, self-contained problem — don't let one recipe's
  code leak into another's route
- Run `npm run typecheck` after changes before saying done
- If a request seems wrong, ask before proceeding

## Security
- Secrets go in `.env.local` only — see SECURITY.md
- `.env.local` is gitignored; never commit it
- `SUPABASE_SERVICE_ROLE_KEY` is server-only — never import `lib/data/supabase-server.ts` from a Client Component

## Project-specific notes
[Add a line per recipe here as you build it: what it is, where it lives]
