# Collaborative Whiteboard (Miro Clone)

A real-time collaborative whiteboard built with Next.js, Convex, and Liveblocks.

## Tech Stack

- Next.js (App Router)
- Convex (backend and database)
- Liveblocks (real-time collaboration)
- Clerk (authentication)
- Tailwind CSS and shadcn/ui
- TypeScript

## Features

- Real-time collaborative canvas
- Drawing tools: rectangles, ellipses, freehand paths, sticky notes, text
- Live cursors and participant presence
- Layer selection, movement, and deletion
- Dashboard with favorites, organization boards, and search
- Create, rename, and delete boards
- Color picker for stroke and fill

## Getting Started

### Prerequisites

- Node.js 18+
- Accounts on Convex, Liveblocks, and Clerk

### Setup

1. Clone the repository and install dependencies:

```bash
git clone [<your-repo-url>](https://github.com/shwetamadhale/collaborative-whiteboard.git)
cd collaborative-whiteboard
npm install
```

2. Copy `.env.example` to `.env.local` and fill in the required keys:

```bash
cp .env.example .env.local
```

Required variables:

| Variable | Description |
| --- | --- |
| `CONVEX_DEPLOYMENT` | Convex deployment name |
| `NEXT_PUBLIC_CONVEX_URL` | Convex deployment URL |
| `NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY` | Clerk publishable key |
| `CLERK_SECRET_KEY` | Clerk secret key |
| `LIVEBLOCKS_SECRET_KEY` | Liveblocks secret key |
| `NEXT_PUBLIC_LIVEBLOCKS_PUBLIC_KEY` | Liveblocks public key |

3. Start Convex in a separate terminal:

```bash
npx convex dev
```

4. Start the dev server:

```bash
npm run dev
```

Open http://localhost:3000.

## Scripts

| Command | Description |
| --- | --- |
| `npm run dev` | Start the dev server |
| `npm run build` | Build for production |
| `npm run start` | Start the production server |
| `npm run lint` | Run ESLint |

## Project Structure

```
app/                  Dashboard, API routes, and board canvas
components/           Shared UI components
convex/               Schema, queries, mutations, auth config
hooks/                Custom React hooks
lib/                  Utilities
providers/            Convex and modal providers
store/                Zustand stores
types/                TypeScript types
```

