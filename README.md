# Next.js Dashboard

A financial admin dashboard built as a Next.js practice project — focused on App Router patterns, server-side data fetching, and full-stack CRUD in a realistic UI.

## Stack

- **Next.js** (App Router, Turbopack)
- **TypeScript**
- **Tailwind CSS**
- **PostgreSQL** via `postgres`
- **NextAuth.js** (v5)
- **Zod** for validation

## What this covers

- Route groups, layouts, and nested navigation
- Server Components with async data fetching
- Streaming and loading states
- Search, pagination, and URL-based state
- Server Actions for invoice CRUD
- Auth with credentials and protected routes

## Getting started

```bash
pnpm install
cp .env.example .env.local
```

Set `POSTGRES_URL` and generate an `AUTH_SECRET`:

```bash
openssl rand -base64 32
```

Seed the database, then start the dev server:

```bash
curl http://localhost:3000/seed   # run once after the server is up
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000).

## Scripts

| Command       | Description              |
| ------------- | ------------------------ |
| `pnpm dev`    | Dev server    |
| `pnpm build`  | Production build         |
| `pnpm start`  | Serve production build   |

## Structure

```
app/
├── lib/          # Data access, types, utilities
├── ui/           # Shared and feature components
├── seed/         # Database seeding route
└── query/        # Ad-hoc query route
```
