# Member guide

This page is for the members of the [`alopex-org`](https://github.com/alopex-org) organization: everyone in its `alopex` team.
It says how to take part: getting set up, suggesting changes, reviewing other people's work and joining in the decisions.
It adds no rules of its own.
The rules are in [GOVERNANCE.md](GOVERNANCE.md) and in each repository's `CONTRIBUTING.md`, and this page links to them; where they disagree, they win.
GitHub words such as fork, pull request and review are explained in the [glossary](GLOSSARY.md).
The maintainers have their own [maintainer guide](MAINTAINING.md).

## In short

- You can read every repository, like everyone else, and you make your changes in your own fork.
- You suggest changes through pull requests, and a maintainer merges them.
- You review each other's pull requests, and the maintainers' own; your comments are answered before a pull request merges.
- You take part in every decision by commenting in its issue, and you vote when a disagreement reaches the members.
- Discord is for talking; anything that should be kept goes in an issue or a pull request.

## What members do

As the founding meeting decided ([GOVERNANCE.md](GOVERNANCE.md#the-founding-meeting)):

- **You can:** open issues and pull requests, review and comment on any pull request, comment on every decision, and vote when a question reaches the members.
- **You can't:** push to the organization's repositories, merge, or set labels, issue types and milestones on other people's issues.
  Suggest a label or milestone in a comment, and a maintainer sets it.
- **Your approval** of a pull request doesn't count toward merging, because only maintainers approve pull requests; GitHub still records it, and the maintainers read it.

## Getting set up

1. **Your GitHub account.**
   Accept the invitation to the organization, and turn on two-factor authentication; the organization requires it.
2. **Your commit address.**
   Commit with your GitHub noreply address, which ends in `@users.noreply.github.com`, so that your personal address never becomes public.
   Set it in each clone with `git config --local user.email`.
3. **Your forks.**
   Fork the repository you want to work on, [foxieos](https://github.com/alopex-org/foxieos) or [alopex](https://github.com/alopex-org/alopex), and clone your fork.
4. **The checks.**
   Install [pre-commit](https://pre-commit.com/#install), then run `pre-commit install` in each clone.
   It stops a commit that contains a secret or a private note, or that has no sign-off.
5. **Read the repository's `CONTRIBUTING.md`.**
   It holds the rules for branches, commits, sign-offs, reviews and writing the docs.

## Suggesting a change

The steps are in each repository's `CONTRIBUTING.md`, under "In short".
In brief:

1. Pick something from the repository's `docs/ROADMAP.md` or its issues, or open an issue about what you want to change.
   Decisions marked open there are the maintainers' to make, so ask before building on one.
2. Make a new branch in your fork for the change.
3. Commit with a sign-off (`git commit -s`).
4. Open a pull request, and say what you changed, why, and what you checked.
5. Answer the review comments, until a maintainer approves and merges it.
   Pull requests stay open for at least two days before they merge, so that others can read them.

If you use an AI coding agent, you are responsible for its work as for your own, and you sign off its commits with your own name.

## Reviewing

Reviewing each other's work is one of the main things members do.

- Open a pull request, read the changes under "Files changed", and comment on the lines you have a question about.
- Choose **Comment** for questions and suggestions, **Request changes** when something must change first, or **Approve** when you think it is ready.
- If you object to a change, say why; a maintainer answers your objection in the pull request before it merges.
- Check what each `CONTRIBUTING.md` asks of a change: a sign-off on every commit, a source for every fact, nothing private or secret, and a list of what was checked.
- Some areas, such as the roadmap and the design, need a person to read every change.
  Each `CONTRIBUTING.md` lists them under "Review".

## Decisions

The maintainers take the decisions listed in each repository's roadmap ([GOVERNANCE.md](GOVERNANCE.md#how-decisions-are-made)).

- Every decision has an issue of type Decision; anyone can comment there.
  A link to it is posted on the Alopex Discord, and it stays open for at least seven days.
- Give your argument, with sources, in the issue.
  An argument made on Discord counts once someone writes it in the issue.
- **Sending a question to the members.**
  If you and at least one other member who isn't a maintainer object to a roadmap decision or another foundational change in its issue, within its seven days and with reasons, the question goes to a vote of the members ([GOVERNANCE.md](GOVERNANCE.md#foundational-changes)).
- **When the maintainers disagree,** they talk it through and then vote; if their vote is tied, or too few of them vote, the members vote ([GOVERNANCE.md](GOVERNANCE.md#settling-a-disagreement)).
- **Voting.**
  A maintainer calls the vote in the pull request or issue.
  Write "for" or "against" in a comment there within seven days; a vote on Discord doesn't count.
  The majority of the votes given decides, if at least half the team votes; otherwise nothing changes.
  You can ask once for seven more days, for example during exams.

## Talking and reporting

- **The Alopex Discord** is for conversation and quick questions ([SUPPORT.md](SUPPORT.md)).
  It has no public invite for now; a member can invite someone new.
- **A security problem** goes through the repository's `SECURITY.md`, never a public issue or Discord.
- **A code-of-conduct problem** goes through the [code of conduct](CODE_OF_CONDUCT.md#reporting-an-issue), including for something that happened on Discord.

## Changing this page

Suggest a change in a pull request to this repository.
When a rule changes in `GOVERNANCE.md` or a `CONTRIBUTING.md`, update this page in step.
