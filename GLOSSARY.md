# Glossary: GitHub and how we work

Plain explanations of the words the FoxieOS docs use for GitHub and for the way the projects work.
You don't need to know any of this before you start; look a word up when you meet it.

Words about operating systems and the cyber-deck's software are in [foxieos's glossary](https://github.com/alopex-org/foxieos/blob/main/docs/GLOSSARY.md).
Words about the cyber-deck's hardware are in [Alopex's glossary](https://github.com/alopex-org/alopex/blob/main/docs/GLOSSARY.md).

## People and roles

- **Alopex:** two things share this name.
  The Alopex student organization runs the projects, the `alopex` team on GitHub and the Alopex Discord.
  Alopex is also the name of the hardware project, whose repository is `alopex` (called `foxieos-hardware` until 2026-11-23).

- **Maintainer:** a person who decides for a project and approves changes to it.
  Only maintainers approve pull requests, never their own ([governance](GOVERNANCE.md#how-changes-are-approved)); the [maintainer guide](MAINTAINING.md) says how they do their everyday work.
- **Owner:** an account that controls the whole GitHub organization: its settings, teams, tags and secrets.
  The organization's owner is also a maintainer, with the same say as the others ([governance](GOVERNANCE.md#the-organizations-owner)).
- **Member:** someone in the organization's `alopex` team.
  Members suggest changes, review each other's work and take part in every decision ([member guide](MEMBERS.md)).
- **Contributor:** anyone else who suggests a change or reports a problem.
- **Coding agent:** an AI tool, such as Claude Code or Codex, that edits files when a person asks it to.
  The person who uses it is responsible for its work.
  The agent's own rules are in each repository's `AGENTS.md`.
- **Team:** a group of members on GitHub.
  Access to a repository is given to a team, not to one person at a time.

## Where the work lives

- **Organization:** the shared GitHub account that holds all the projects' repositories, [`alopex-org`](https://github.com/alopex-org).
- **Repository (repo):** one project's folder of files, with the full history of every change.
  The organization has `foxieos` (the operating system), `alopex` (Alopex, the hardware project) and `.github` (shared files like this one).
- **`main`:** the repository's official version.
  Changes reach it only through a pull request.
- **Markdown (`.md`):** the plain-text format these docs are written in.
  GitHub shows it with headings, links and tables.
  Each sentence sits on its own line in the file, so a change shows exactly which sentence changed; the page on GitHub looks the same either way.

## Making a change

- **Clone:** a copy of a repository on your own computer.
- **Fork:** your own copy of a repository on GitHub.
  Members put their changes in their fork and suggest them from there.
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
  An **approval** is a review that says the change is ready; only a maintainer other than the author can give one that counts.
- **Merge:** bringing an approved pull request into `main`.
  The repositories merge by **rebasing**: each commit is placed on top of `main` as it was written, so the history stays one straight line.
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

## Deciding

- **Everyday change:** any change that isn't foundational.
  It needs one maintainer's approval and stays open for two days before it merges.
- **Foundational change:** a change that shapes the projects or the organization, such as a roadmap decision, the governance page or who the maintainers are.
  It stays open for seven days and needs a majority of the maintainers ([governance](GOVERNANCE.md#foundational-changes)).
- **Objection:** a review that asks for changes and still stands after the author has answered.
  A maintainer's objection stops the pull request from merging until the disagreement is settled.
- **Majority of the votes given:** more "for" than "against" among the people who voted; people who didn't vote aren't counted.
- **Revert:** a new change that undoes an earlier one.

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

- **Private vulnerability reporting:** a GitHub form, under a repository's Security tab, for reporting a security problem so that only the organization's owner sees it.
- **Release keys:** the secret files that prove an update really comes from FoxieOS.
  Only the maintainers handle them.
- **Licence:** the terms under which others may use the files.
  The repositories use the Apache License 2.0; the code of conduct uses Creative Commons Attribution-ShareAlike 4.0.
- **Webhook:** a secret address that lets one service post into another, for example GitHub announcing a release on Discord.
- **`*.local.md`:** a private note file that stays on one person's computer.
  Git ignores these files, and nothing from them goes into the repositories.
