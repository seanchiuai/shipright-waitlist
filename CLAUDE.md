# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

ShipRight waitlist landing page - a single-page site with email capture functionality powered by Convex backend.

## Commands

```bash
# Start Convex dev server (syncs functions and watches for changes)
npm run convex:dev

# Deploy Convex functions to production
npm run convex:deploy
```

## Architecture

- **Frontend**: Single `index.html` file with inline CSS/JS, uses Convex browser client via ESM import
- **Backend**: Convex serverless functions in `convex/` directory
  - `schema.ts` - Database schema with `waitlist` table (name, email, phone, location, idea)
  - `waitlist.ts` - Mutations and queries: `add`, `getAll`, `getCount`

## Setup Note

After running `npx convex dev` for the first time, update the `CONVEX_URL` constant in `index.html` with your deployment URL.
