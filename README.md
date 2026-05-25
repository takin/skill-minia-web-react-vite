# Web React Vite Dashboard Skill

OpenCode skill for building, reviewing, and maintaining authenticated SaaS dashboard projects that use React, Vite, Bun, TanStack libraries, Shadcn UI, generated OpenAPI clients, and static Nginx deployment.

The full implementation standard lives in [`SKILL.md`](./SKILL.md).

## Use This Skill For

- React + Vite dashboard setup and review.
- TanStack Router, Query, Form, and Table conventions.
- Shadcn UI component usage, theming, and initialization rules.
- Generated OpenAPI client boundaries.
- Static dashboard deployment through Docker Compose and Nginx.
- Dashboard CI, testing, linting, formatting, and build gates.

## Core Standards

- Runtime and package manager: Bun.
- Build tool: Vite.
- UI framework: React 19+ with React Compiler enabled.
- Routing: TanStack Router.
- Server state: TanStack Query.
- Forms: TanStack Form + Zod.
- Tables: TanStack Table.
- Styling: Tailwind CSS v4+ and Shadcn UI.
- Deployment: static `dist/` served by Nginx in Docker Compose.

## Key Boundaries

- Do not add SSR, server functions, API routes, or database access to dashboard projects.
- Backend APIs own authentication, authorization, validation, persistence, and business rules.
- Route guards are UX only, not an authorization boundary.
- Generated API code belongs under `src/lib/api/generated/` and should not be hand-edited.
- Production dashboard runtime serves static files only. Do not run Vite, Bun, Node, or a custom app server in production.

## Related Skills

When available, load these alongside this skill before implementing dashboard code:

- `typescript-best-practices`
- `shadcn`
- `react-state-management`

## Installation

Place this repository where OpenCode discovers skills, or copy `SKILL.md` into your configured skill directory.

## Repository Contents

- `SKILL.md`: The complete dashboard engineering standard and workflow.
- `README.md`: Overview and quick reference.
