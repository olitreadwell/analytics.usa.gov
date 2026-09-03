# 18F/analytics.usa.gov context
> refreshed 2026-09-03 | upstream default: develop @ af6435c

## Identity & policies
- upstream: 18F/analytics.usa.gov (US federal public-web-traffic dashboard; JavaScript + Jekyll + React/d3). English-first (yes — all docs/UI/issue conversation in US English).
- Default branch: `develop` (promotion flow develop -> staging -> master).
- CLA/DCO: none (CONTRIBUTING = public domain CC0 note only; org 18F/.github CONTRIBUTING is welcome + conduct, no CLA/DCO/signup).
- AI-assisted PR policy: unstated (bans_ai=false, ai_disclosure_required=false from passport).
- signed commits required: no.
- PR template: `.github/PULL_REQUEST_TEMPLATE.md` (## Summary / ## Impacted Areas of the Site / ## Optional Screenshots / "This pull request changes..." / "This pull request is ready to merge when..." checklists).
- external tracker: GitHub.
- Repo does not ban trivial/drive-by PRs (bans_trivial=false; CONTRIBUTING only asks for CC0 waiver agreement).

## Conventions (verified from merged PRs)
- branch naming: plain kebab-case descriptive names, no type prefix dominant (e.g. `remove-pa11y-dependency`, `upgrade-puppeteer`, `rename-fns-to-fna`, `update-csp-for-source-map`). Use `<kebab-description>` (occasionally `feature/...`, `fix/...`).
- commit style: plain imperative; CI gates = `npm run lint:js`, `npm run lint:styles`, `npm test` (jest), `npm audit signatures`, axe + pa11y accessibility jobs.
- Outside PRs merge via review by another developer; template gates require tests passing + peer review + documentation.

## Maintainer picture
- Maintainers responsive; Tim Lowden historically system owner; DAP team (digital-analytics-program) active through 2026 via dependabot + accessibility/GA4 work. Recent merges frequent (dependabot + feature PRs). Outside/cold PRs accepted (README, GA4 copy, accessibility passes landed).

## Issue-area health
- Active areas: GA4 data front-end, accessibility (axe/pa11y), dependency bumps (npm/bundler), CI/deploy (GitHub Actions replacing CircleCI). Avoid inventing work in these; they are well-maintained.

## Gap ledger (dedupe — READ FIRST, never re-pick)
- `2026-09-03` self-found — trivial-fix pass: doc typos in README.md + docs/maintenance.md (12 typos) + 1 verified dead link (TerserWebpackPlugin URL 404 -> webpack-contrib GitHub repo). outcome: pr-opened. Lesson: pure typo/README/docs doc cleanup for a small clean PR.

## Mined gaps (discovered, not yet attempted)
- `2026-09-03` docs/maintenance.md + docs/procedures.md still reference CircleCI + Gemnasium + handbook.18f.gov — stale service refs; removing/rewriting changes content so left untouched (not a clean trivial fix). status: proposed
