# Epione

A modern **Next.js + React** web app that brings together a *Feed*, *Events*, *Resources*, *Messaging*, and a personal *Journal* experience—wrapped in a clean UI built with Tailwind.

> This repository contains the frontend for the Epione experience. Some parts of the app run in **demo / mock mode** when a backend is not connected.

---

## What you can do here

- **Feed** (`/home`) – posts, announcements, and polls in one scrollable stream
- **Events** (`/events`) – browse upcoming events and create/edit them
- **Resources** (`/resources`) – explore curated resource buckets
- **Journal** (`/journal`) – write entries, browse by month, and reflect
- **Messaging** (`/messaging`) – real-time chat foundations (WebSocket service + Redux state)
- **Auth pages** (`/login`, `/signup`) – login UI + callback handler

---

## Tech stack

- **Next.js** (Pages Router)
- **React + TypeScript**
- **Redux Toolkit** + **redux-persist** (app state)
- **Tailwind CSS** (styling)
- **Framer Motion** (background/hover animations)
- **Axios** (API requests)

---

## Project structure (quick map)

- `src/pages/` – Next.js routes (Feed, Events, Resources, Journal, Auth, APIs)
- `src/components/` – reusable UI components (Header, forms, feed cards, etc.)
- `src/sections/` – larger feature sections (ex: Events create/edit flows)
- `src/slices/` – Redux slices (`userSlice`, `feedSlice`, `messagingSlice`, `configSlice`)
- `src/config/` – axios config, routes, cookies, constants

---

## Run locally

### 1) Install dependencies

```bash
npm install
```

### 2) Start the dev server

```bash
npm run dev
```

Open: http://localhost:3000

---

## Environment variables

Create a `.env.local` file (optional for demo mode). Common keys used:

- `NEXT_PUBLIC_BACKEND_URL` – backend base URL (defaults to `http://localhost:3000/api`)
- `NEXT_PUBLIC_COOKIE_EXPIRATION_TIME` – cookie expiry in days
- `NEXT_PUBLIC_SOCKET_URL` – websocket URL (if using messaging)
- `NEXT_PUBLIC_GCP_BUCKET` – bucket used for image/resource URLs

---

## Notes (demo mode)

Some pages include mock data so you can see UI without a backend:

- The Feed page (`src/pages/home/index.tsx`) contains demo feed items.
- Events (`src/pages/events/index.tsx`, `src/pages/events/[id].tsx`) include mock events.
- Journal has demo entries & an example API route (`src/pages/api/journal.ts`).

---

## UI details you might notice

- The login background grid animation is powered by **Framer Motion** in:
  - `src/components/common/Background/index.tsx`

---

## Scripts

- `npm run dev` – start development server
- `npm run build` – production build
- `npm run start` – run production server
- `npm run lint` – lint

---

## Contributing

If you're working on this as a team project:

1. Create a feature branch
2. Keep changes small and focused
3. Prefer shared components in `src/components/`
4. Add/adjust types in `src/types/` when introducing new data

---

## License

Add a license if you plan to distribute this project.
