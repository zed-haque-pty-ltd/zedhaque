# AI-Native Marketing Site Pilot

This repository contains a 5-page marketing site pilot built with Next.js and deployed on Vercel. The goal is to ship a production-ready site in one week while validating an AI-native engineering workflow.

## Project Scope
- Pages: Home, Projects (landing + detail), About (index + Book + Entrepreneurship), Contact, Terms, Privacy
- Footer links: LinkedIn and YouTube
- Temporary lead capture: simple form + minimal API endpoint

## Routes
- `/` Home
- `/projects` Projects landing
- `/projects/[slug]` Project details
- `/about` About index
- `/about/book` Book
- `/about/entrepreneurship` Entrepreneurship
- `/contact` Contact
- `/terms` Terms
- `/privacy` Privacy

## Getting Started
1. Install dependencies:
```bash
npm install
```
2. Run the dev server:
```bash
npm run dev
```
3. Open `http://localhost:3000`.

## Scripts
- `npm run dev` Start local dev server
- `npm run build` Build for production
- `npm run start` Run production build
- `npm run lint` Lint the codebase

## Structure
- `app/` App Router pages and layouts
- `public/` Static assets

## Lead Capture
Temporary lead capture should use a minimal API endpoint (e.g., `/api/lead`) and store submissions via email or CSV. Post-pilot, this can be replaced with a CRM integration (e.g., HubSpot).

## Workflow And Quality
All contributors (human and AI) should follow the rules in `AGENTS.md`, including:
- Small, reviewable PRs
- Tests before implementation
- Docs and diagrams updated in the same PR
- Human approval for merges

## Deployment
Vercel preview deployments are expected on every PR; production deploys on merge to `main`.
