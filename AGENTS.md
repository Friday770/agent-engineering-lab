# Project Instructions (for AI agents)

## Language policy (HARD RULE)
- Everything written for agents MUST be in English: this file, `CLAUDE.md`, any nested `AGENTS.md`,
  everything under `ai/`, `refs/INDEX.md`, code comments, commit messages, branch/PR descriptions.
- Human-facing documents under `docs/` and `portfolio/` may be Chinese. Do not translate or rewrite them unless asked.
- Replies to the user in chat follow the user's language.

## Goal
Personal repository for learning and building agents, progressing through stages P1-P5.

## Directory conventions
- `docs/`       Human-written notes. Do not edit unless asked.
- `ai/`         Agent plans, specs, prompts, session summaries. English only. NOT tracked by Git (see .gitignore).
                Drafts go in `ai/scratch/`.
- `refs/`       Third-party source, read-only. Only `refs/INDEX.md` is tracked.
- `labs/`       Throwaway practice code.
- `projects/`   Real projects. Must have tests and a README.
- `packages/`   Shared code (created from P3). Changes must be synced across dependent projects.
- `infra/`      Deployment docs/config (created from P3). Never commit real secrets.
- `data/`, `artifacts/`  Local data and run outputs. Not tracked.

## Git workflow (HARD RULE)
- `main` is the reviewed, trusted branch. Never commit or push to `main` directly.
- Claude works only on branch `Claude`; Codex works only on branch `Codex`.
- Changes reach `main` only through a Pull Request reviewed by the user. Never merge a PR yourself.
- Before starting work: `git fetch origin` and rebase/merge latest `main` into your branch.
- Keep commits small, one logical change each. Never force-push `main`.

## Working rules
1. Before changing more than 3 files, write a plan in `ai/plans/NNN-topic.md` and wait for approval.
2. Never read or print `.env` contents.
3. Explain the reason before adding a new dependency.
4. After code changes, run relevant tests and report the result.
5. Milvus / MinIO operations default to the dev environment. Never write to prod.

## Common commands
(Fill in: install, run, test.)
