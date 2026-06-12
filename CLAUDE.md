@AGENTS.md

# Everest — Social Networking App

Achievement-focused social network. Users share personal and professional goals, milestones, projects, and challenges. Content is strictly achievement-oriented (no generic status updates).

## Stack

- **Framework**: Next.js 16 (App Router) + TypeScript — strict mode
- **Database**: Supabase (PostgreSQL + realtime + auth + storage)
- **Styling**: Tailwind CSS v4 + shadcn/ui
- **Data fetching**: TanStack Query (client), Server Components (server)
- **Deployment**: Vercel

## Project Structure

```
src/
  app/          # Next.js App Router pages and layouts
  components/   # Shared UI components (shadcn/ui extensions and custom)
  lib/          # Utilities, Supabase clients, helpers
  hooks/        # Custom React hooks
  types/        # Shared TypeScript types
```

## Key Conventions

- Server Components by default — add `"use client"` only when needed (event handlers, hooks, browser APIs)
- Supabase: `lib/supabase/server.ts` for Server Components/Route Handlers, `lib/supabase/client.ts` for Client Components
- Every Supabase table must have Row Level Security (RLS) policies defined alongside it
- No `any` types — define explicit types for all Supabase query returns
- Tailwind for all styling — no inline styles, no CSS modules
- Use shadcn/ui components before writing custom UI from scratch

## Custom Skills

- `/grill-me [feature]` — Challenge assumptions about a feature before building it
- `/phased-plan [feature]` — Create a phased implementation plan
- `/phased-implementation [phase N of feature]` — Implement one phase at a time

## Dev Commands

```bash
npm run dev      # Start dev server (localhost:3000)
npm run build    # Production build
npm run lint     # ESLint
```
