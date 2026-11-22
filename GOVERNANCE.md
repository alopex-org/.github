# Governance

This page says who decides what in the FoxieOS projects, who may change what, and how that will change.
It applies to every repository in the [`alopex-org`](https://github.com/alopex-org) organization, unless a repository's own docs say otherwise.
GitHub words such as pull request, code owner and ruleset are explained in the [glossary](GLOSSARY.md).

## In short

- Right now one person, the organization's owner, acts as the only maintainer, for a short time.
- On Tuesday 2026-11-24 the members meet and choose several maintainers.
- Those maintainers then decide the big questions together.
- Until then, anything the docs call "decided" is only a proposal.

## Founding maintainers

The FoxieOS projects will have several maintainers, not one.

- **The meeting.**
  The members meet on Tuesday 2026-11-24 to choose the maintainers.
  The maintainers then decide the projects' foundations together: what each project is for, whether the hardware project, Alopex, aims to become a product, and how they take decisions among themselves.
- **Until then, one interim maintainer.**
  The organization's owner acts as the only maintainer for now.
  They set up the organization and the repositories' tools, and take no foundational decision alone.
- **Until then, only the interim maintainer's approval merges a change.**
  Each repository's `.github/CODEOWNERS` file names them as the owner of every file, so GitHub needs their approval before a pull request can merge.
  Members still review each other's changes and the maintainer's own.
  The maintainers decide at the meeting who approves changes after that.
- **Until then, members can read but not write.**
  Members have the same read access to every repository as everyone else.
  They put their changes in their own forks and suggest them from there.
  Only the interim maintainer pushes to the organization's repositories, merges, and labels, assigns or closes other people's issues.
  The maintainers decide at the meeting what access members get after that.
- **Earlier decisions are proposals.**
  Everything the repositories mark as decided before the meeting was decided by the interim maintainer alone.
  It counts as a proposal until the maintainers confirm or change it.
- **Recording the result.**
  After the meeting, a pull request records who the maintainers are, updates this page and adds them as code owners.
  Until it merges, "the maintainer" in this page and in the repositories means the interim maintainer.
- **Maintainers' accounts.**
  A maintainer approves pull requests from a GitHub account that is a member of the organization and has two-factor authentication turned on.

## Roles

- **The maintainer** owns the organization; [Founding maintainers](#founding-maintainers) explains how this becomes several people.
  The maintainer:
  - takes the decisions listed in each repository's roadmap;
  - approves changes to the files they own as code owner;
  - handles security and code-of-conduct reports;
  - is the only person who handles release keys and publishes releases.
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
  The maintainer decides, then records the decision and its date in the roadmap, in a pull request that closes the issue.
- **Changes** follow the repository's `CONTRIBUTING.md`.
  Someone other than the author reviews every change, and some areas need a review by a person rather than by a coding agent.
- **Discord** doesn't decide anything by itself.
  An argument or an agreement counts once someone writes it in the issue or pull request it concerns.
- **Disagreements** are argued in the issue or pull request, with sources.
  If they don't settle, the maintainer decides and says why.

## Access

- **Through teams.**
  Members get access to a repository through a team, never one by one.
  Everyone else has read access, the organization's default.
- **`alopex` team.**
  Every member belongs to it.
  Until the founding meeting it has read access to every project repository.
- **Project teams.**
  The `foxieos` and `foxieos-hardware` teams each have write access to their own repository (`foxieos-hardware` to `alopex`), and are kept for roles in that project.
  They stay empty, apart from the maintainer, until the roles are decided and assigned.
- **This `.github` repository** has no team.
  Its files apply to every repository, so only the maintainer changes them, through pull requests.
- **Protected `main`.**
  A ruleset protects each repository's `main` branch.
  Each repository's `CONTRIBUTING.md` lists its rules.
- **Two-factor authentication** is required for every member.
- **The Alopex Discord** belongs to the student organization, and its owner runs it, not the maintainer.
  The code of conduct applies to FoxieOS discussion there, and reports go to the maintainer.
  Who moderates the server under the code of conduct isn't settled yet.
  The server's owner lets GitHub post to chosen channels (the Manage Webhooks permission).
  The maintainer sets up those GitHub connections and keeps their secret addresses out of the repositories, because anyone who has one can post to its channel.

## Continuity

So that the project doesn't depend on one person, more owners will be added.

- The organization has one owner for now.
- The founding meeting decides which maintainers also become owners.
- After that, a further owner is added when a member is ready.
  That member:
  - has contributed to and reviewed the projects;
  - agrees to this page and to the repositories' rules on keys, devices and publishing (in `docs/RELEASING.md` and `AGENTS.md`);
  - is proposed by a maintainer in an issue in this repository, and accepts there.

Owning the organization doesn't give access to release keys.
Release keys stay with the maintainer on the signing computer, as each repository's release docs describe.

## Changing this page

Suggest a change in a pull request to this repository.
The maintainer approves it.
