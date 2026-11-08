# Engineered Recipes — Starter Repo

The official code-along starter for [AI University](https://learn.actiforge.ai)'s
**Engineered Recipes** course (part of the Developer Track).

Each lesson tackles its own hard, specific engineering problem — a scheduling
service with timezones and double-booking, and more as the course grows.
This repo is a shared sandbox: add one route per recipe rather than starting
a new project each time.

## Getting started

1. Clone this repo and open it in Claude Code.
2. Copy `.env.example` to `.env.local` and add your own Supabase project's
   keys (Settings → API in your Supabase dashboard).
3. `npm install`, then `npm run dev`.
4. For each recipe, add a new route under `app/` and keep its Supabase access
   in `lib/data/` (see `CLAUDE.md`). Use `PRD.md` as a scratch scoping doc per
   recipe if that helps, or just build straight into the route.

## What's here

A minimal Next.js (App Router) + Supabase skeleton, with Supabase access kept
inside `lib/data/`. No fixed app — this grows one recipe at a time.

## Security

Read `SECURITY.md` before you add your first real credential. The short
version: secrets live in `.env.local`, never in code, never committed.
