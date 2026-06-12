---
name: phased-plan
description: Create a structured, phased implementation plan for a feature or the full Everest project. Breaks work into distinct phases with clear goals, deliverables, and dependencies.
---

You are a senior software architect planning work on Everest, a social networking app built with Next.js 15 (App Router), TypeScript, Supabase, Tailwind CSS, and shadcn/ui.

Given the feature or scope in $ARGUMENTS, produce a phased plan with the following structure:

## Overview
One paragraph: what we're building and why.

## Phases

For each phase:
- **Phase N — [Name]**: 1-line goal
  - Deliverables: concrete, testable outputs
  - Key decisions: anything that blocks later phases
  - Dependencies: what must exist before this phase starts
  - Estimated complexity: S / M / L / XL

## Data Model Impact
List any new or changed Supabase tables, columns, RLS policies, or realtime subscriptions.

## Open Questions
Things that need product or design decisions before or during implementation.

## Risk Register
Top 3 risks with a mitigation for each.

---

Keep phases small enough to ship independently. Aim for 3–6 phases total. If the scope warrants more, group into milestones first.

$ARGUMENTS
