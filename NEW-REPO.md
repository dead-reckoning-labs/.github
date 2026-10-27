# New repo checklist

Every new repo in `dead-reckoning-labs` starts here. Work top to bottom.

## 1. Create it from the template

- [ ] Create the repo from [`dead-reckoning-labs/repo-template`](https://github.com/dead-reckoning-labs/repo-template) ("Use this template"), private unless there is a reason to be public.
- [ ] Name it in lowercase kebab case. That name is reused for the hosting and database projects below.

## 2. Record the owner

- [ ] Add the repo and its owner to `repo-ownership.md` in the `mantis` repo, in a pull request.
- [ ] Fill in `.github/CODEOWNERS` with the owning team or user.

## 3. About, homepage and topics

- [ ] Set the About description (one line, what it does).
- [ ] Set the homepage to the live URL once there is one.
- [ ] Add topics: the product area (for example `registration`, `marketing`, `internal-tools`) and the main stack (for example `nextjs`, `neon`).

## 4. Hosting and database naming

- [ ] Vercel project named exactly after the repo (`<repo-name>`). A staging project, if needed, is `<repo-name>-staging`.
- [ ] Neon project named exactly after the repo (`<repo-name>`). Preview branches are `preview/<git-branch>`.
- [ ] If the repo name has a dot (for example `example.io`), drop the TLD for Vercel and Neon (`example`).

## 5. Secrets

- [ ] Secrets live in the repo's own vault and in the Vercel project env. Never in git, never in a shared machine `.env`.
- [ ] List every variable name (no values) in `.env.example` and in the README table.
- [ ] Each integration keeps its own keys, OAuth callback and token store in this repo's stack. Do not proxy it through another service.

## 6. Branch protection

- [ ] Nothing to add. The org ruleset "Default branch: PRs only" targets `~ALL` repos, so the new default branch already requires a pull request and blocks force pushes and deletion.

## 7. Fill in the skeletons

- [ ] `README.md`: what it is, live URL, owner, stack, local setup, env var names, tests, deploy, related repos. Delete the "Using this template" note.
- [ ] `AGENTS.md`: real commands, conventions, migrations and money paths. Read [AGENT-RULES.md](AGENT-RULES.md) for the org-wide rules it builds on.
- [ ] `.env.example`: real variable names.

## 8. Confirm automation

- [ ] CI (`ci`) runs green on the first pull request.
- [ ] Dependabot shows npm and github-actions updates under Insights, Dependency graph, Dependabot (after a `package.json` exists).
