# Governance

This page says who decides what in the FoxieOS projects, who may change what, and what the founding meeting decided.
It applies to every repository in the [`alopex-org`](https://github.com/alopex-org) organization, unless a repository's own docs say otherwise.
GitHub words such as pull request, code owner and ruleset are explained in the [glossary](GLOSSARY.md).

## In short

- The members held their founding meeting on 2026-11-24.
- The projects have three maintainers: the organization's owner, who was the only one after the meeting, and two more appointed by them on 2026-11-26 ([Maintainers](#maintainers)).
- The maintainers decide by majority vote; if a vote is tied, the members decide by majority vote.
- One maintainer's approval lets a pull request merge.
- Members keep read access and work from their own forks.

## The founding meeting

<!-- Keeps links to this section's earlier title, "Founding maintainers", working. -->
<a id="founding-maintainers"></a>

The members met on 2026-11-24 to choose the maintainers and confirm the projects' foundations.
This section records what the meeting decided.

- **Maintainers.**
  The meeting kept the organization's owner as the only maintainer for now.
  The meeting said a second maintainer would be appointed soon; the organization's owner appointed two on 2026-11-26 ([Maintainers](#maintainers)).
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
  The organization keeps one owner, @alevromitis, for now ([Continuity](#continuity)).
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

## Maintainers

The maintainers of every project in the organization, with the GitHub accounts they work from:

| Maintainer | Since | How |
|---|---|---|
| [@alevromitis](https://github.com/alevromitis) | 2026-11-24 | Chosen by the members at the founding meeting; also the organization's owner |
| [@evansyrsiris](https://github.com/evansyrsiris) | 2026-11-26 | Appointed by @alevromitis, as the founding meeting foresaw |
| [@Leandros64](https://github.com/Leandros64) | 2026-11-26 | Appointed by @alevromitis, as the founding meeting foresaw |

Each repository's `.github/CODEOWNERS` lists the same accounts.
A change to this list is made in a pull request that also updates those files.
How the maintainers do their everyday work is in the [maintainer guide](MAINTAINING.md).

### What the owner covers for now

The other maintainers have write access to the project repositories, through the `foxieos` and `alopex-hardware` teams ([Access](#access)).
There they approve and merge pull requests and look after issues.
Some maintainer tasks need more access on GitHub than that, so for now the organization's owner does them alone:

- **Security and code-of-conduct reports.**
  Both arrive through GitHub's private reporting form, and only the organization's owner sees what is sent there.
- **This `.github` repository.**
  No team gives the maintainers write access here, so only the organization's owner approves its pull requests.
- **Tags and releases, overriding the rules on `main`, and repository secrets.**
  These need GitHub's admin role, which only the organization's owner has.

This stays so until the maintainers decide how to share these tasks, for example with a team for the maintainers or another owner ([Continuity](#continuity)).

## Roles

- **The maintainers** are listed under [Maintainers](#maintainers); one of them also owns the organization.
  The maintainers:
  - take the decisions listed in each repository's roadmap;
  - approve changes to the files they own as code owners;
  - handle security and code-of-conduct reports;
  - are the only people who handle release keys and publish releases.

  For now the organization's owner does some of these alone ([What the owner covers for now](#what-the-owner-covers-for-now)).
- **Members** belong to the `alopex` team, which covers every project in the organization.
  They open pull requests, review each other's changes and take part in the discussion of every decision.
  How they do this is in the [member guide](MEMBERS.md).
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
  The `foxieos` and `alopex-hardware` teams each have write access to their own repository (`alopex-hardware` to `alopex`), and are kept for roles in that project.
  They hold only the maintainers until the roles are decided and assigned.
- **This `.github` repository** has no team.
  Its files apply to every repository, so only the maintainers change them, through pull requests; for now only the organization's owner approves them ([What the owner covers for now](#what-the-owner-covers-for-now)).
- **Protected `main`.**
  A ruleset protects each repository's `main` branch.
  Each repository's `CONTRIBUTING.md` lists its rules.
- **Two-factor authentication** is required for every member.
- **The Alopex Discord** belongs to the student organization, and its owner runs it, not the maintainers.
  The code of conduct applies to FoxieOS discussion there, and reports go to the maintainers.
  Who moderates the server under the code of conduct isn't settled yet.
  The server's owner lets GitHub post to chosen channels (the Manage Webhooks permission).
  The organization's owner sets up those GitHub connections and keeps their secret addresses out of the repositories, because anyone who has one can post to its channel.

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
