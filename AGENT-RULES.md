# Agent rules for every dead-reckoning-labs repo

These rules apply to every coding agent (Claude, Copilot, and any other assistant or bot) in every repo in this org. A repo's own `AGENTS.md` adds repo-specific commands and conventions on top; when they conflict, the stricter rule wins.

## Before you start

- Read the repo's `AGENTS.md` first, then its `README.md`.
- Work only in repos you are assigned to change. Reading other repos for context is fine.

## Branches and merges

- Work on a feature branch and open a pull request. Never commit or push to `main` or `master`.
- Never merge a pull request without the repo owner's explicit OK.
- Keep pull requests small. The body has `## What`, `## Why` and `## Test plan`, and says whether the change is customer-visible and whether it touches a money path.

## Writing

- **No em dashes.** Not in code, comments, copy, docs, commit messages or PR text. Use commas, colons or periods.
- **No color bars.** Never put a thin colored accent stripe on any edge of a card, panel, callout, quote, modal, slide or graphic. Brand color goes on buttons, progress, chips and imagery instead.

## Databases and migrations

- Migrations are additive and idempotent: `CREATE TABLE IF NOT EXISTS`, `ADD COLUMN IF NOT EXISTS`, `CREATE INDEX IF NOT EXISTS`.
- Never drop, truncate or rewrite data without a backup or a database branch first, and the owner's OK.
- Test migrations against a preview branch, not production.

## Money paths

- Payments, payouts, refunds, pricing, fees, tax, and auth or sign-in are money paths.
- Flag any change that touches one in the pull request. It never merges without the owner's explicit OK, even when checks are green.

## Secrets

- Never commit secrets, tokens, keys or real `.env` files. Variable names go in `.env.example`; values live in the repo's own vault and hosting env.
- If a secret is ever committed, stop and tell the owner so it can be rotated. Do not just delete it in a later commit.

## Build first-party

- Build each integration inside the repo that owns its data, with that repo's own secrets, callback, token store and scheduled jobs.
- Do not route production features through another repo's service or a personal machine as a shortcut.

## External actions

- Sending email or messages, posting publicly, deploying to production, and deleting external data all need the owner's OK first. Stage them (draft, dry run, draft PR) and ask.
