# honojs/hono context
> refreshed 2026-09-03 | upstream default: main @ e2740d5a

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
- test command: `bun run test`; format/lint: `bun run format:fix && bun run lint:fix`
- package manager: Bun (`bun install --frozen-lockfile`)

## Maintainer picture
- Yusuke Wada (@yusukebe) founder; active maintainer team; fast external merges (108 external merges/60d)

## Issue-area health
- (trivial pass) hunting typos, dead links, stale command references, wrong doc lines

## Gap ledger (dedupe — READ FIRST, never re-pick)
- 2026-08-26 test-coverage sweep — outcome skipped (no-genuine-fix-this-cycle) — no clean verifiable bug; all real issues had open PRs or maintainer-declined resolutions

## Mined gaps (discovered, not yet attempted)
- (this run) trivial/minor-fix pass per config trivial_fix_rules
