# Glossary: GitHub and how we work

Plain explanations of the words the FoxieOS docs use for GitHub and for the way the projects work.
You don't need to know any of this before you start; look a word up when you meet it.

Words about Android and phones are in [foxieos's glossary](https://github.com/alopex-org/foxieos/blob/main/docs/GLOSSARY.md).
Words about hardware and radios are in [foxieos-hardware's glossary](https://github.com/alopex-org/foxieos-hardware/blob/main/docs/GLOSSARY.md).

## People and roles

- **Maintainer:** a person who decides for a project and approves changes to it.
  Until the founding meeting on 2026-11-24, the organization's owner is the only, interim maintainer ([governance](GOVERNANCE.md#founding-maintainers)).
- **Member:** someone in the organization's `alopex` team.
  Members suggest changes, review each other's work and take part in every decision.
- **Contributor:** anyone else who suggests a change or reports a problem.
- **Coding agent:** an AI tool, such as Claude Code or Codex, that edits files when a person asks it to.
  The person who uses it is responsible for its work.
  The agent's own rules are in each repository's `AGENTS.md`.
- **Team:** a group of members on GitHub.
  Access to a repository is given to a team, not to one person at a time.

## Where the work lives

- **Organization:** the shared GitHub account that holds all the FoxieOS repositories, [`alopex-org`](https://github.com/alopex-org).
- **Repository (repo):** one project's folder of files, with the full history of every change.
  FoxieOS has `foxieos` (the operating system), `foxieos-hardware` (the device research) and `.github` (shared files like this one).
- **`main`:** the repository's official version.
  Changes reach it only through a pull request.
- **Markdown (`.md`):** the plain-text format these docs are written in.
  GitHub shows it with headings, links and tables.
  Each sentence sits on its own line in the file, so a change shows exactly which sentence changed; the page on GitHub looks the same either way.

## Making a change

- **Clone:** a copy of a repository on your own computer.
- **Fork:** your own copy of a repository on GitHub.
  Until the founding meeting, members put their changes in their fork and suggest them from there.
- **Branch:** a separate line of work inside a repository, so a change can be prepared without touching `main`.
  Each change gets a new branch with a name that says what it does, such as `docs/glossary`.
- **Commit:** one saved step of a change, with a message that says what changed and why.
- **Sign-off:** a line at the end of a commit message, `Signed-off-by: Your Name <address>`.
  With it you state that you wrote the change, or have the right to submit it, under the project's licence.
  This statement is called the Developer Certificate of Origin (DCO).
  `git commit -s` adds the line for you.
- **Noreply address:** the private email address GitHub gives every account, ending in `@users.noreply.github.com`.
  Commits use it so that your personal address never becomes public.
- **Pull request (PR):** a request to bring the changes on a branch into `main`.
  It shows the changes and holds the discussion and the review.
- **Review:** reading someone else's pull request and commenting on it.
  An **approval** is a review that says the change is ready.
- **Merge:** bringing an approved pull request into `main`.
  The FoxieOS repositories merge by **rebasing**: each commit is placed on top of `main` as it was written, so the history stays one straight line.
- **Tag:** a fixed name for one point in the history, used to mark a release.

## Rules the repositories enforce

- **Code owners (`CODEOWNERS`):** a file that names who must approve changes to which files.
  GitHub asks them for a review automatically.
- **Ruleset:** settings that protect `main`, for example that every change needs a pull request and an approval.
  Each repository's `CONTRIBUTING.md` lists its rules.
- **Pre-commit hooks:** small checks that run on your computer every time you commit, once you have run `pre-commit install` in your clone.
  They stop a commit that contains a password or key, a private note file, or no sign-off.
- **gitleaks:** the hook that looks for passwords, keys and other secrets.
- **Workflow (GitHub Actions):** a script that GitHub runs by itself, for example to check every pull request for sign-offs.
- **CI (continuous integration):** checks and builds that run automatically on every change.
- **Dependabot:** a GitHub bot that suggests updates to the tools the repository uses.
- **Two-factor authentication (2FA):** a second step when you sign in, such as a code from an app.
  Every member needs it.

## Tracking the work

- **Issue:** a page on GitHub for one question, problem, task or decision, with its discussion.
- **Issue type:** what kind of issue it is: Decision, Task, Check, Bug or Feature.
- **Label:** a tag on an issue, for example who does the work or what it touches.
- **Milestone:** a group of issues that make up one phase of the roadmap.
- **Roadmap:** the file `docs/ROADMAP.md` in each project, listing the decisions to take and the work in order.
  Its items have short codes:
  - **D1, D2, …:** decisions, questions the maintainers answer;
  - **T1, T2, …:** tasks, pieces of work;
  - **C1, C2, …:** checks, facts to confirm before a task relies on them.

## Reading the docs

- **⚠:** this claim isn't confirmed yet, or sources disagree.
  The text says what would confirm it, usually a check in the roadmap.
- **(unsourced):** this comes from general knowledge and wasn't checked against a source.
- **Planned:** this doesn't exist yet.
- **Sources:** the links at the end of a section, or of a file, that back up what it says.

## Security and licences

- **Private vulnerability reporting:** a GitHub form, under a repository's Security tab, for reporting a security problem so that only the maintainer sees it.
- **Release keys:** the secret files that prove an update really comes from FoxieOS.
  Only the maintainer handles them.
- **Licence:** the terms under which others may use the files.
  The repositories use the Apache License 2.0; the code of conduct uses Creative Commons Attribution-ShareAlike 4.0.
- **Webhook:** a secret address that lets one service post into another, for example GitHub announcing a release on Discord.
- **`*.local.md`:** a private note file that stays on one person's computer.
  Git ignores these files, and nothing from them goes into the repositories.
