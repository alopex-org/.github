# Maintainer guide

This page is for the maintainers of the projects in the [`alopex-org`](https://github.com/alopex-org) organization.
It says how to do the everyday work: reviewing and merging pull requests, looking after issues, recording decisions and changing who the maintainers are.
It adds no rules of its own.
The rules are in [GOVERNANCE.md](GOVERNANCE.md) and in each repository's `CONTRIBUTING.md`, and this page links to them; where they disagree, they win.
GitHub words such as pull request, code owner and ruleset are explained in the [glossary](GLOSSARY.md).
Members have their own [member guide](MEMBERS.md).

## In short

- You approve and merge pull requests, and you look after issues, in `foxieos` and `alopex`.
- Only maintainers approve pull requests, and never their own; ask another maintainer to approve yours.
- A person, not a coding agent, reads every change to the roadmap, the design and the other sensitive areas each `CONTRIBUTING.md` lists.
- Everyday pull requests stay open for two days before they merge; foundational ones, such as roadmap decisions, for seven days and with a majority of the maintainers.
- Pull requests merge by rebasing, once the DCO check passes and every comment thread is resolved.
- When the maintainers disagree, they talk it through, then vote, and the members vote if the maintainers can't decide.
- A decision counts once it is written in its issue and in the roadmap, not when it is agreed on Discord.
- Some tasks need more access than you have, so the organization's owner does them for now ([What only the owner can do](#what-only-the-owner-can-do-for-now)).

## Your access

The maintainers are listed in [GOVERNANCE.md](GOVERNANCE.md#maintainers).
You have write access to the project repositories through their teams: `foxieos` for [foxieos](https://github.com/alopex-org/foxieos) and `alopex-hardware` for [alopex](https://github.com/alopex-org/alopex).
With it you can:

- approve pull requests, as a code owner of every file;
- merge pull requests;
- set labels, issue types and milestones, assign issues, and close or reopen them;
- re-run the automatic checks on a pull request.

Keep two-factor authentication turned on for your GitHub account; the organization requires it.

### What only the owner can do, for now

These need more access on GitHub than the project teams give, so the organization's owner does them alone until the maintainers decide how to share them ([GOVERNANCE.md](GOVERNANCE.md#what-the-owner-covers-for-now)):

- reading security and code-of-conduct reports sent through GitHub's private reporting form;
- approving pull requests to this `.github` repository;
- creating tags and releases, overriding the rules on `main`, and managing repository secrets, teams and organization settings.

The owner uses these powers to carry out what the maintainers decide, and overrides the rules on `main` only in the cases [GOVERNANCE.md](GOVERNANCE.md#the-organizations-owner) lists.

If a task needs one of these, ask the owner in the issue or pull request.

## Before your first review

- Clone the repositories and run `pre-commit install` in each clone, as their `CONTRIBUTING.md` says.
- Set your commit address to your GitHub noreply address with `git config --local user.email`.
- Read each repository's `CONTRIBUTING.md`, especially its "Review" section, and its `AGENTS.md`, which coding agents follow.

## Reviewing a pull request

GitHub asks the maintainers for a review on every pull request, because `.github/CODEOWNERS` names them as owners of every file.
For an everyday change, one maintainer's approval is enough to merge, from a maintainer other than the author.
A foundational change, such as a roadmap decision, needs a majority of the maintainers ([GOVERNANCE.md](GOVERNANCE.md#how-changes-are-approved)).

Check these before you approve:

1. **The DCO check passes.**
   Every commit needs a `Signed-off-by:` line from its author, except commits from bots such as Dependabot.
   If one is missing, point the author to "Forgot the sign-off?" in `CONTRIBUTING.md`.
2. **The change is in the right place.**
   One logical change per commit, and a subject line written as `scope: description`.
   Docs change in the same commit as what they describe.
3. **A person reads the sensitive areas.**
   Each `CONTRIBUTING.md` lists them under "Review"; in both repositories they include `docs/ROADMAP.md` and `docs/DESIGN.md`.
   You may use a coding agent to help you review other docs, but you answer for that review as for your own.
4. **Decisions stay with the maintainers.**
   A pull request must not mark an open roadmap decision as decided, unless it records a decision taken as described in [Recording a decision](#recording-a-decision).
5. **Facts have sources.**
   A new claim links its source, or is marked ⚠ (not confirmed) or "(unsourced)", as "Writing docs" in `CONTRIBUTING.md` asks.
6. **Nothing private or secret.**
   No keys, passwords or tokens, and no machine names, addresses, local folder paths or personal details.
   If a secret reached GitHub, deleting it isn't enough: the owner of the secret cancels or replaces it.
7. **The pull request says what was checked.**
   It lists the commands run and the sources checked, with what passed, what failed and what was skipped.
8. **Matching changes are linked.**
   If the change needs a matching change in the other repository, both pull requests link each other.
   FoxieOS depends on Alopex, not the other way round, so a change in `foxieos` never asks `alopex` to adapt.

Then choose:

- **Approve** when the change is ready.
- **Request changes** when something must change first, and say what.
  If you still disagree after the author has answered, your review is an objection: the pull request doesn't merge until you approve it or the disagreement is settled ([Disagreements](#disagreements)).
- **Comment** for questions and suggestions that don't block the merge.

Only maintainers approve pull requests, so members' reviews don't count toward merging; answer their comments before merging, as `CONTRIBUTING.md` asks.

**Your own pull requests** need another maintainer's approval; never approve or merge your own without one.
In this `.github` repository GitHub counts only the owner's approval for now, so the other maintainers approve the owner's own pull requests here by writing "Approved" in a review or a comment ([What only the owner can do](#what-only-the-owner-can-do-for-now)).

**Never dismiss another maintainer's review** that asks for changes, although GitHub lets you.
Only the maintainer who wrote it withdraws it, unless [Disagreements](#disagreements) has settled the question; then link the result when you dismiss it.

## Disagreements

When maintainers disagree about a pull request or a decision, follow [Settling a disagreement](GOVERNANCE.md#settling-a-disagreement):

1. Talk it through in the pull request or issue, with sources, for up to seven days.
2. If that doesn't settle it, call a vote of the maintainers in a comment: everyone writes "for" or "against" within seven days, and the majority of the votes given decides.
3. If the vote is tied or fewer than two maintainers vote, call a vote of the whole `alopex` team, with a link to the question; it decides by majority if at least half the team votes.

If you call a vote, count it and write the result in the same place.
If nothing is decided, nothing changes: the pull request closes, or the decision stays open.

## Merging

A pull request can merge when:

- a maintainer other than the author has approved it, or a majority of the maintainers for a foundational change;
- it has been open for at least two days, or seven days with its issue linked for a foundational change; GitHub doesn't check this, so you do ([GOVERNANCE.md](GOVERNANCE.md#how-changes-are-approved));
- no maintainer's objection is still open;
- no new commits were pushed after that approval, since a push cancels earlier approvals;
- the DCO check has passed;
- every review comment thread is resolved.

A fix to a typo, a broken link or a failing check, or to a security problem that can't wait, may merge without the wait; say why in the pull request.
If a maintainer objects to a change that merged early, reverse it in a new pull request, and let the change come back as an ordinary one.

Merge with **Rebase and merge**, the only method the repositories allow.
Each commit then lands on `main` as written, so check that the commit messages are ready before you merge.
If GitHub says the branch can't be rebased, ask the author to run `git rebase main` and push again.

## Looking after issues

Every decision (D), task (T) and check (C) in a repository's `docs/ROADMAP.md` has an issue, and each roadmap phase is a milestone.

- **New issues:** set the issue type (Decision, Task, Check, Bug or Feature), the labels and, for roadmap work, the milestone.
- **Labels** say who does the work (`who:`), what it touches (`area:`) and what it waits for (`blocked`, `upstream`, `needs: person review`).
  The list lives in the repository's `.github/labels.sh`.
  To change it, change that file in a pull request; once it has merged, run `.github/labels.sh` with the [GitHub CLI](https://cli.github.com/) to update GitHub.
- **Security or code-of-conduct problems posted in public:** don't discuss the details there.
  Point the author to the repository's `SECURITY.md` or to the [code of conduct](CODE_OF_CONDUCT.md#reporting-an-issue), which explain how to report privately.
- **Roadmap changes:** when a roadmap item changes, the change goes into `docs/ROADMAP.md` in a pull request that links its issue.
  A new roadmap item gets a new issue as well.
- **Closing:** a task or check closes when the pull request that finishes it merges; mention the issue in the pull request so it closes by itself.

## Recording a decision

The maintainers take the decisions listed in each repository's roadmap ([GOVERNANCE.md](GOVERNANCE.md#how-decisions-are-made)).

A roadmap decision is a foundational change ([GOVERNANCE.md](GOVERNANCE.md#foundational-changes)).

1. The discussion happens in the decision's issue, where anyone can comment.
   Post a link to the issue on the Alopex Discord, so the members know about it.
   Arguments made on Discord count once someone writes them there.
2. A pull request records the proposed decision and its date in `docs/ROADMAP.md`, and in `docs/DESIGN.md` if it changes the design, and links the issue.
   A person reviews it, because it changes the roadmap.
3. It merges after seven days, once a majority of the maintainers approve it; an author who is a maintainer counts.
   If two members who aren't maintainers object in the issue, with reasons, the members vote instead.
   If the maintainers disagree, follow [Disagreements](#disagreements).
   Write each vote in the issue or pull request, so the record stays with the decision.
4. Merging the pull request closes the decision's issue.

## Adding or removing a maintainer

Adding or removing a maintainer is a foundational change, decided in an issue in this repository like a roadmap decision ([GOVERNANCE.md](GOVERNANCE.md#maintainers)).
Once the change is decided:

1. Open a pull request here that updates the table in [GOVERNANCE.md](GOVERNANCE.md#maintainers) and this repository's `.github/CODEOWNERS`.
2. Open a matching pull request in `foxieos` and in `alopex` that updates their `.github/CODEOWNERS`, and link all three.
3. The organization's owner adds the person to, or removes them from, the `foxieos` and `alopex-hardware` teams.
   A new maintainer must be a member of the organization with two-factor authentication turned on.

## Releases and keys

Nothing has been released yet.
Only the maintainers handle release keys, on the signing computer, and only the organization's owner can create the tag that publishes a release.
The steps are in each project's release docs, such as [foxieos's RELEASING.md](https://github.com/alopex-org/foxieos/blob/main/docs/RELEASING.md).
Never put a release key, or anything copied from one, in a repository, an issue or a chat.

## Not settled yet

- How the tasks in [What only the owner can do](#what-only-the-owner-can-do-for-now) are shared among the maintainers, for example through a team for the maintainers or another owner.
- Who moderates the Alopex Discord under the code of conduct.
- A contact address for security reports (FoxieOS roadmap decision D8, the security contact).

## Changing this page

Suggest a change in a pull request to this repository.
When a rule changes in `GOVERNANCE.md` or a `CONTRIBUTING.md`, update this page in step.
