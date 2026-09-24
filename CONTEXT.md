# honojs/hono context
> refreshed 2026-09-24 | upstream default: main @ 8dcd52b9

## Identity & policies
- upstream: honojs/hono, default branch main, primary language TypeScript, English-first (yes)
- CLA/DCO: none
- AI-assisted PR policy: allowed but must not waste maintainer time; maintainer may close PR and block account (docs/CONTRIBUTING.md "AI Usage Policy")
- signed commits required: no
- PR template: .github/pull_request_template.md (checklist: add tests, run tests, format/lint, TSDoc/JSDoc)
- external tracker: github

## Conventions (verified from merged PRs)
- branch naming: `fix/<kebab-description>` (dominant), also `perf/...`
- commit style: Conventional Commits `type(scope): subject (#PR)`
- package manager: pnpm (migrated from Bun, PR #5433, 2026-09-24; lockfile `pnpm-lock.yaml`, `pnpm install`)
- test command: `pnpm run test` (tsc -p tsconfig.spec.json + vitest); format: `pnpm run format` (oxfmt, replaced prettier PR #5435); lint: `pnpm run lint`
- CI: vitest projects for node/workerd/fastly/lambda/lambda-edge; 11 pre-existing logger/color env-dependent failures on clean main (color.test.ts, helper/dev, middleware/logger) — known, not introduced by our runs

## Maintainer picture
- Yusuke Wada (@yusukebe) founder; active maintainer team; fast external merges (108 external merges/60d); all fresh issues get claimed by open PRs within days

## Issue-area health
- Router semantics family kept being contested/decided by maintainers (LinearRouter/PatternRouter/TrieRouter param-segment and strict-slash disagreements) — avoid, they are either claimed or still under maintainer decision
- Feature/enhancement issues are long-lived discussion threads, not pick targets

## Gap ledger (dedupe — READ FIRST, never re-pick)
- 2026-08-26 test-coverage sweep
- 2026-09-03 trivial/minor-fix pass (loop-trivial) — outcome pr-opened (PR #4) — 4 genuine typo fixes in test comments/descriptions (cookie 'ignore'->'ignored', 'thi'->'this'; jsx 'rended'->'rendered' x2); fork CI substantive checks green, only Coverage fails on missing CODECOV_TOKEN (fork artifact) — outcome skipped (no-genuine-fix-this-cycle) — no clean verifiable bug; all real issues had open PRs or maintainer-declined resolutions
- 2026-09-09 trivial/minor-fix pass — skipped (no-genuine-fix-this-cycle) — codespell + misspelling regex + duplicate-word + ~165 URL checks clean; upstream already fixed remaining typos; PR #4 covered the rest
- 2026-09-09 (2nd, loop-trivial) — skipped (no-genuine-fix-this-cycle) — re-verified same upstream HEAD clean; no new fixes; fewer than 3 genuine fixes -> skip
- 2026-09-24 repo-audit cycle — outcome skipped (no-genuine-fix-this-cycle) — no maintainer-engaged open issue survived (all fresh issues #5345/#5406/#5422/#5369/#5370 claimed by open PRs #5367/#5348, #5410, #5423, #5404, #5318; #5432/#5431 triage, unengaged). repo-audit matrix: clean-code (no TODOs; middleware/util impls clean), security (`pnpm audit --prod` no vulns), deps (no known vulns), tests/CI (green except 11 known env logger/color failures), docs (prior sweeps clean). No novel, verifiable, uncontested bug or gap found. Honest skip per loop_policy — no PR opened.
## Mined gaps (discovered, not yet attempted)
- (this run) repo-audit cycle — no verifiable gap survived dedupe + filters; all self-found candidates (router semantics, jsx-renderer streaming headers, method-override body re-read) either claimed, contested, or intentional
