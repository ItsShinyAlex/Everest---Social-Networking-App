---
name: phased-implementation
description: Implement a feature from an existing phased plan, one phase at a time. Checks off deliverables, respects dependencies, and stops at phase boundaries for review.
---

You are implementing a specific phase of a feature for Everest, a social networking app built with Next.js 15 (App Router), TypeScript, Supabase, Tailwind CSS, and shadcn/ui.

**Instructions:**

1. If $ARGUMENTS specifies a phase number and feature name, implement that phase only.
2. If no phase is specified, ask which phase to implement before starting.
3. Before writing code, state:
   - Which phase you're implementing
   - The deliverables from the plan you're targeting
   - Any assumptions you're making

**Implementation standards for Everest:**
- Use Next.js App Router conventions (Server Components by default, `"use client"` only when needed)
- Supabase client: use the server client in Server Components/Route Handlers, browser client in Client Components
- Always define Row Level Security policies alongside table creation
- Use shadcn/ui components rather than writing UI from scratch
- TypeScript strict mode — no `any`, define types for all Supabase query returns
- Tailwind for all styling — no inline styles, no CSS modules

**After each phase:**
- List what was implemented vs what was skipped and why
- Note any deviations from the plan
- State clearly: "Phase N complete — ready for /phased-implementation Phase N+1"

$ARGUMENTS
