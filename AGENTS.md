# Agent Behavior Guidelines

These guidelines apply to any AI agent operating in this repository.

## Scope And Roles
- Agents may: read the repo, run code, create branches, generate code/tests/docs, open PRs, and perform first-pass code review.
- Agents must not: merge to `main`, modify secrets or infrastructure, or access production logs without explicit permission.
- Humans must: approve merges, decide on architecture/design, handle sensitive data, and manage production changes.

## Work Principles
- Use existing patterns, folder structure, and naming conventions.
- Ask before assuming when requirements or design decisions are unclear.
- Keep PRs small and reviewable; split into multiple PRs if needed.
- Prefer tests first: draft tests before implementing features and ensure they fail prior to the fix.
- Update docs and diagrams in the same PR as the code change; use Mermaid for diagrams.
- If a command fails (tests/lint/build), fix and rerun. Note persistent errors in the PR.

## Quality Gates (Definition Of Done)
- CI passes: linting, type checks, and unit/integration tests.
- PR includes:
  - Clear description (what/why).
  - Test evidence (console output or coverage).
  - Screenshots and preview link for UI changes.
  - Rollback note if deployment scripts are touched.
- Human approval required: at least one engineer reviews and merges.
- Deployment is live and smoke-tested (navigation, forms, broken links).

## Security And Data
- Never modify secrets or environment variables.
- Do not access production data or logs unless explicitly instructed.
- Do not invent facts for public copy; mark AI-written copy as draft unless verified.

## Project Context (Pilot)
This repo targets a 5-page marketing site with Next.js + Vercel. Key routes include:
- `/` (Home)
- `/projects` and `/projects/[slug]`
- `/about`, `/about/book`, `/about/entrepreneurship`
- `/contact`, `/terms`, `/privacy`
- Footer links to LinkedIn and YouTube

Temporary lead capture should use a simple form and a minimal API endpoint.
