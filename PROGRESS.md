# Everest — Progress Tracker

## Concept

Achievement-focused social network. Users share personal and professional goals, milestones, projects, and challenges — from full planned journeys with phases to single "I did this" posts. Content is strictly achievement-oriented; no generic status updates. Privacy controls determine who can see what (friends, colleagues, fans, or public).

---

## Done

### Project Setup
- [x] Chose tech stack: Next.js 16 (App Router) + TypeScript + Supabase + Tailwind v4 + shadcn/ui + TanStack Query
- [x] Bootstrapped Next.js 16 project with TypeScript, Tailwind CSS v4, ESLint, App Router, `src/` layout
- [x] GitHub repo created and connected: https://github.com/ItsShinyAlex/Everest---Social-Networking-App
- [x] `CLAUDE.md` with stack conventions for AI-assisted development
- [x] `AGENTS.md` with Next.js-specific agent rules

### Claude Code Skills (`.claude/commands/`)
- [x] `/grill-me` — challenges assumptions before building a feature
- [x] `/phased-plan` — creates a phased implementation plan for any feature
- [x] `/phased-implementation` — implements one phase at a time with clear stop points

### Stack Integration
- [x] **Supabase SSR clients** wired up:
  - `src/lib/supabase/client.ts` — browser client (use in `"use client"` components)
  - `src/lib/supabase/server.ts` — server client (use in Server Components + Route Handlers)
  - `src/lib/supabase/middleware.ts` — session refresh logic
  - `src/middleware.ts` — runs session refresh on every request
- [x] **TanStack Query** provider (`src/providers/query-provider.tsx`) wired into root layout
- [x] **shadcn/ui** initialized (Tailwind v4 compatible), first component `Button` added
- [x] `.env.local.example` template for Supabase credentials
- [x] App metadata updated to Everest branding

---

## Pending — Immediate (before first feature)

- [ ] **Supabase project creation** — go to supabase.com, create free project, copy URL + anon key into `.env.local`
- [ ] **Verify dev server runs** — `npm run dev` should open localhost:3000 without errors

---

## Pending — Core Features (suggested order)

### 1. Auth
- [ ] Sign up / log in (Supabase Auth — email+password + Google OAuth)
- [ ] User profile (display name, avatar, bio)
- [ ] Protected routes (redirect unauthenticated users)

### 2. Achievements (core content type)
- [ ] Data model: `achievements` table (title, description, type, status, visibility, user_id)
- [ ] Achievement types: goal (with phases/milestones), single post, challenge
- [ ] Create/edit/delete achievement
- [ ] Visibility controls: public / followers / connections only / private

### 3. Feed
- [ ] Home feed (achievements from people you follow)
- [ ] Profile feed (all public achievements for a user)
- [ ] Explore / discover page

### 4. Social Graph
- [ ] Follow system (asymmetric, like Twitter)
- [ ] Connection system (mutual, like LinkedIn) — for colleagues
- [ ] Privacy model tied to follow/connection status

### 5. Engagement
- [ ] Reactions (celebrate, support, inspire)
- [ ] Comments
- [ ] Share / reshare an achievement

### 6. Notifications
- [ ] Real-time notifications (Supabase Realtime) for reactions, comments, follows

### 7. Media
- [ ] Image uploads for achievements (Supabase Storage)
- [ ] Progress photos for milestone-based goals

### 8. Mobile
- [ ] Responsive design (Tailwind)
- [ ] PWA manifest (installable on mobile)
- [ ] Consider React Native / Expo app later for native mobile

---

## Stack Reference

| Layer | Choice |
|---|---|
| Framework | Next.js 16 (App Router) + TypeScript |
| Database | Supabase (PostgreSQL + Realtime + Auth + Storage) |
| Styling | Tailwind CSS v4 + shadcn/ui |
| Data fetching | TanStack Query (client) + Server Components (server) |
| Deployment | Vercel (free tier) |
| Repo | GitHub — ItsShinyAlex/Everest---Social-Networking-App |

---

## How to Work on This

```bash
npm run dev        # Dev server at localhost:3000
npm run build      # Production build check
npm run lint       # ESLint
```

**Before starting a feature:**
```
/grill-me <feature name>          # Challenge assumptions
/phased-plan <feature name>       # Build the plan
/phased-implementation Phase 1    # Implement one phase at a time
```
