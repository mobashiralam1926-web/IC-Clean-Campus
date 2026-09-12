 Clean Campus 🌿

A modern, mobile-responsive campus cleanliness platform built with **Next.js 14** and **Tailwind CSS**.

## Features

- 🎓 **Student Dashboard** — points, rank, recent reports & activity
- 🗺️ **Find a Bin** — interactive Leaflet map with bin status (ok / almost-full / full)
- 📸 **Report Garbage** — form with photo upload, category, urgency & success flow
- 🏆 **Leaderboard** — podium, ranked list, points breakdown
- 🛡️ **Admin Dashboard** — manage reports, filter, update statuses, view users

## Getting Started

```bash
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000).

## Demo Accounts

| Role    | Email                 | Password   |
|---------|-----------------------|------------|
| Student | aisha@campus.edu      | student123 |
| Admin   | admin@campus.edu      | admin123   |

## Tech Stack

- **Next.js 14** (App Router, TypeScript)
- **Tailwind CSS v3** with custom green theme
- **Leaflet.js + react-leaflet** for interactive maps
- **Lucide React** icons
- **Mock data** in `lib/mockData.ts` — ready to swap with Firebase

## Deploying to Vercel

```bash
npm install -g vercel
vercel
```

## Adding Firebase (Next Steps)

1. `npm install firebase`
2. Create `lib/firebase.ts` with your Firebase config
3. Replace mock auth in `app/login/page.tsx` with `signInWithEmailAndPassword`
4. Replace mock data in `lib/mockData.ts` with Firestore queries
5. Add `firebase.storage` for photo uploads in the report form

## Project Structure

```
clean-campus/
├── app/
│   ├── layout.tsx
│   ├── page.tsx            # → /login
│   ├── login/page.tsx
│   ├── dashboard/page.tsx
│   ├── map/page.tsx
│   ├── report/page.tsx
│   ├── leaderboard/page.tsx
│   └── admin/page.tsx
├── components/
│   ├── Navbar.tsx
│   ├── StatCard.tsx
│   └── MapComponent.tsx
└── lib/
    └── mockData.ts
```
