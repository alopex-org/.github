# Instructions for coding agents

This file is for AI coding agents working in this repository.
It holds the organization's profile and shared community files ([README.md](README.md)), which apply to every FoxieOS repository.

If an `AGENTS.local.md` file exists next to this one, read it too.
Files named `*.local.md` are git-ignored and hold notes for one contributor's setup.
Never copy anything from them into a commit, pull request or issue.

## Rules

1. **Follow [foxieos's AGENTS.md](https://github.com/alopex-org/foxieos/blob/main/AGENTS.md)** for branches, commits, sign-off, review and how to write the docs.
2. **Every change here affects every repository.**
   Keep a change to the files the repositories inherit (`CODE_OF_CONDUCT.md`, `GOVERNANCE.md`, `SUPPORT.md`) in step with the repositories' own docs, and propose the matching pull requests there.
3. **Nothing outward-facing without the maintainer.**
   That includes pushing to any remote, changing organization settings and posting anything.
4. **Keep private details out of the repository.**
   Describe machines by their role, never by name, address, hardware inventory or local path.

## Commands

- Checks: the pre-commit hooks in `.pre-commit-config.yaml` (gitleaks, blocks on key files and `*.local.md` notes, and a DCO sign-off on the commit message), once `pre-commit install` has been run in the clone.
  On pull requests, the DCO workflow checks the sign-off again.
