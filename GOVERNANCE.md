# Governance

This page says who decides what in the FoxieOS projects, who may change what, and what the founding meeting decided.
It applies to every repository in the [`alopex-org`](https://github.com/alopex-org) organization, unless a repository's own docs say otherwise.
GitHub words such as pull request, code owner and ruleset are explained in the [glossary](GLOSSARY.md).

## In short

- The members held their founding meeting on 2026-11-24.
- For now the project has one maintainer, the organization's owner; a second maintainer is to be appointed soon.
- The maintainers decide by majority vote; if a vote is tied, the members decide by majority vote.
- One maintainer's approval lets a pull request merge.
- Members keep read access and work from their own forks.

## The founding meeting

<!-- Keeps links to this section's earlier title, "Founding maintainers", working. -->
<a id="founding-maintainers"></a>

The members met on 2026-11-24 to choose the maintainers and confirm the projects' foundations.
This section records what the meeting decided.

- **Maintainers.**
  The organization's owner is the only maintainer for now.
  A second maintainer is to be appointed soon; a pull request then adds them to this page and as a code owner.
- **How the maintainers decide.**
  By majority vote.
  If a vote is tied, the members decide by majority vote.
- **Merging.**
  One maintainer's approval lets a pull request merge.
  Each repository's `.github/CODEOWNERS` file names the maintainers as owners of every file, so GitHub needs a maintainer's approval before a pull request can merge.
  Members still review each other's changes and the maintainers' own.
- **Members' access.**
  Members keep read access to every repository, like everyone else.
  They put their changes in their own forks and suggest them from there.
  Only maintainers push to the organization's repositories, merge, and label, assign or close other people's issues.
- **Owners.**
  The organization keeps one owner, the maintainer, for now ([Continuity](#continuity)).
- **The projects' foundations.**
  The meeting confirmed:
  - the move from an Android phone to a user-serviceable, portable cyber-deck with LoRa and Wi-Fi, pocket-sized if possible, for both projects;
  - that the cyber-deck runs a Linux distribution, for now; which one is FoxieOS's open decision D10;
  - that Alopex, the hardware project, builds a prototype first, then a product (Alopex decision D5);
  - hosting on GitHub, Alopex as a project separate from FoxieOS, and the built-in LoRa radio;
  - the way the repositories work: sign-offs, rebase-only merges, protected `main`, code owners and an issue for every roadmap item.
- **What stays a proposal.**
  Everything else that the repositories marked as decided or proposed before the meeting was written by one maintainer alone, and stays a proposal until the maintainers decide it through its roadmap item.
- **Maintainers' accounts.**
  A maintainer approves pull requests from a GitHub account that is a member of the organization and has two-factor authentication turned on.

## Roles

- **The maintainers** are chosen by the members ([The founding meeting](#the-founding-meeting)); for now there is one, who also owns the organization.
  The maintainers:
  - take the decisions listed in each repository's roadmap;
  - approve changes to the files they own as code owners;
  - handle security and code-of-conduct reports;
  - are the only people who handle release keys and publish releases.
- **Members** belong to the `alopex` team, which covers every project in the organization.
  They open pull requests, review each other's changes and take part in the discussion of every decision.
- **Contributors** are everyone else.
  They open issues, and open pull requests from their own forks.
- **Coding agents** are AI tools that a person directs.
  The person who directs an agent signs off its commits and is responsible for them, as for their own work.
  The agent follows the repository's `AGENTS.md`.

## How decisions are made

- **Roadmap decisions** have short codes (D1, D2, …).
  Each one has a section in the repository's `docs/ROADMAP.md` and an issue of type Decision.
  Anyone can comment on the issue.
  The maintainers decide by majority vote, and the members break a tie by majority vote.
  The decision and its date go into the roadmap, in a pull request that closes the issue.
- **Changes** follow the repository's `CONTRIBUTING.md`.
  Someone other than the author reviews every change, and some areas need a review by a person rather than by a coding agent.
- **Discord** doesn't decide anything by itself.
  An argument or an agreement counts once someone writes it in the issue or pull request it concerns.
- **Disagreements** are argued in the issue or pull request, with sources.
  If they don't settle, the maintainers decide by vote and say why.

## Access

- **Through teams.**
  Members get access to a repository through a team, never one by one.
  Everyone else has read access, the organization's default.
- **`alopex` team.**
  Every member belongs to it.
  It has read access to every project repository, as the founding meeting decided.
- **Project teams.**
  The `foxieos` and `foxieos-hardware` teams each have write access to their own repository (`foxieos-hardware` to `alopex`), and are kept for roles in that project.
  They stay empty, apart from the maintainers, until the roles are decided and assigned.
- **This `.github` repository** has no team.
  Its files apply to every repository, so only the maintainers change them, through pull requests.
- **Protected `main`.**
  A ruleset protects each repository's `main` branch.
  Each repository's `CONTRIBUTING.md` lists its rules.
- **Two-factor authentication** is required for every member.
- **The Alopex Discord** belongs to the student organization, and its owner runs it, not the maintainers.
  The code of conduct applies to FoxieOS discussion there, and reports go to the maintainers.
  Who moderates the server under the code of conduct isn't settled yet.
  The server's owner lets GitHub post to chosen channels (the Manage Webhooks permission).
  The maintainers set up those GitHub connections and keeps their secret addresses out of the repositories, because anyone who has one can post to its channel.

## Continuity

So that the project doesn't depend on one person, more owners will be added.

- The organization has one owner for now.
- The founding meeting kept it that way for now.
- A further owner is added when a member is ready.
  That member:
  - has contributed to and reviewed the projects;
  - agrees to this page and to the repositories' rules on keys, devices and publishing (in `docs/RELEASING.md` and `AGENTS.md`);
  - is proposed by a maintainer in an issue in this repository, and accepts there.

Owning the organization doesn't give access to release keys.
Release keys stay with the maintainers on the signing computer, as each repository's release docs describe.

## Changing this page

Suggest a change in a pull request to this repository.
A maintainer approves it.
