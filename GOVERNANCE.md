# Governance

Who decides what in the FoxieOS projects, and how that changes.
It applies to every repository in the [`alopex-org`](https://github.com/alopex-org) organization, unless a repository's own docs say otherwise.

## Founding maintainers

The FoxieOS projects will have several maintainers, not one.

- The members meet on Tuesday 2026-11-24 to choose the maintainers.
  The maintainers then decide the projects' foundations together: what each project is for, whether the hardware project aims at a product, and how they take decisions among themselves.
- Until then, the organization's owner acts as the only, interim maintainer.
  The interim maintainer sets up the organization and the repositories' tooling, and takes no foundational decision alone.
- Until then, only the interim maintainer's approval lets a pull request merge: each repository's `.github/CODEOWNERS` makes them a code owner of every file.
  Members still review each other's changes and the maintainer's own; the maintainers decide at the meeting who approves changes after that.
- Until then, members have read access to every repository, like everyone else.
  They push branches to their own forks, and only the interim maintainer pushes to the organization's repositories, merges, and labels, assigns or closes other people's issues.
  The maintainers decide at the meeting what access members get after that.
- Everything the repositories mark as decided before the meeting was decided by the interim maintainer alone.
  It counts as a proposal until the maintainers confirm or change it.
- After the meeting, a pull request records who the maintainers are, updates this document, and adds them as code owners.
  Until it merges, "the maintainer" in this document and in the repositories means the interim maintainer.
- A maintainer approves pull requests from a GitHub account that is a member of the organization, with two-factor authentication on.

## Roles

- **The maintainer** owns the organization; [Founding maintainers](#founding-maintainers) explains how this becomes several maintainers.
  The maintainer takes the decisions in each repository's roadmap, approves changes to code-owned paths, handles security and code-of-conduct reports, and is the only person who handles release keys and publishes releases.
- **Members** belong to the `alopex` team, which covers every FoxieOS project.
  They open pull requests, review each other's changes and take part in the discussion of every decision.
- **Contributors** are everyone else.
  They open issues, and pull requests from their own forks.
- **Coding agents** work under a person's direction and follow the repository's `AGENTS.md`.
  The person who directs an agent signs off its commits and is responsible for them.

## How decisions are made

- **Roadmap decisions** (D1, D2, …) each have a section in the repository's `docs/ROADMAP.md` and an issue of type Decision.
  Anyone can comment on the issue.
  The maintainer decides, then records the decision and its date in the roadmap through a pull request that closes the issue.
- **Changes** follow the repository's `CONTRIBUTING.md`: every change is reviewed by someone other than its author, and some areas need a person's review.
- **Discussion on Discord** doesn't decide anything by itself.
  An argument or an agreement counts once someone writes it in the issue or pull request concerned.
- **Disagreements** are argued in the issue or pull request, with sources.
  If they don't settle, the maintainer decides and says why.

## Access

- Members get access to a repository through a team, never one by one; the organization's base permission is read.
- The `alopex` team has read access to every project repository until the founding meeting, and every member belongs to it.
- The `foxieos` and `foxieos-hardware` teams each have write access to their own repository, and are reserved for roles in that project.
  They stay empty, apart from the maintainer, until the roles are decided and assigned.
- This `.github` repository has no team: its files apply to every repository, so only the maintainer changes them, through pull requests.
- A ruleset protects each repository's `main` branch.
  Each repository's `CONTRIBUTING.md` lists its rules.
- Two-factor authentication is required for every member.
- The Alopex Discord belongs to the student organization, and its owner runs it, not the maintainer.
  The code of conduct applies to FoxieOS discussion there, and reports go to the maintainer; who moderates the server under it is not settled yet.
  The server's owner grants Manage Webhooks on the channels GitHub posts to.
  The maintainer sets the GitHub webhooks and the repositories' Discord webhook secrets, which are never committed, since anyone with a webhook URL can post to its channel.

## Continuity

The organization has one owner for now.
The founding meeting decides which maintainers become owners too.
After it, a further owner is added when a member is ready.
That member:

- has contributed to and reviewed the projects;
- agrees to this document and to the key rules in the repositories' `AGENTS.md` and `docs/RELEASING.md`;
- is proposed by a maintainer in an issue in this repository, and accepts there.

Owning the organization doesn't give access to release keys.
Release keys stay with the maintainer on the signing host, as each repository's release docs describe.

## Changing this document

Propose a change in a pull request to this repository.
The maintainer approves it.
