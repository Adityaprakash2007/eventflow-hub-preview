# EventFlow Hub

A campus event management & ticketing platform — React + TypeScript (Vite) frontend, Express + Sequelize (MySQL) backend, with Razorpay payment integration.

## Structure

- **`preview.html`** — a standalone, self-contained build of the frontend. Opens directly in any browser, no server or install needed. Uses mock data since there's no live backend attached to this static file.
- **`source/`** — the full, editable project source (frontend + backend). To run it for real:

```bash
cd source
npm install
cp .env.example .env   # then fill in your own DB credentials
npm run dev:all        # runs both the Vite frontend and Express server
```

## Stack

- Frontend: React 18, TypeScript, Vite, shadcn/ui, Tailwind CSS, React Router, React Query, React Hook Form + Zod
- Backend: Express, Sequelize, MySQL
- Testing: Vitest, Testing Library

## Notes

- `.env` is intentionally excluded from this repo — copy `.env.example` and fill in your own local database credentials.
- The Razorpay payment flow currently uses a mock modal (`MockRazorpayModal.tsx`) rather than the live Razorpay SDK.
