# Governance

Who decides what in the FoxieOS projects, and how that changes.
It applies to every repository in the [`alopex-org`](https://github.com/alopex-org) organization, unless a repository's own docs say otherwise.

## Roles

- **The maintainer** owns the organization.
  The maintainer takes the decisions in each repository's roadmap, approves changes to code-owned paths, handles security and code-of-conduct reports, and is the only person who handles release keys and publishes releases.
- **Members** belong to the `alopex` team, which covers every FoxieOS project.
  They push branches to the project repositories, open pull requests, review each other's changes and take part in the discussion of every decision.
- **Contributors** are everyone else.
  They open issues, and pull requests from their own forks.
- **Coding agents** work under a person's direction and follow the repository's `AGENTS.md`.
  The person who directs an agent signs off its commits and is responsible for them.

## How decisions are made

- **Roadmap decisions** (D1, D2, …) each have a section in the repository's `docs/ROADMAP.md` and an issue of type Decision.
  Anyone can comment on the issue.
  The maintainer decides, then records the decision and its date in the roadmap through a pull request that closes the issue.
- **Changes** follow the repository's `CONTRIBUTING.md`: every change is reviewed by someone other than its author, and some areas need a person's review.
- **Disagreements** are argued in the issue or pull request, with sources.
  If they don't settle, the maintainer decides and says why.

## Access

- Members get access to a repository through a team, never one by one; the organization's base permission is read.
- The `alopex` team has write access to every project repository, and every member belongs to it.
- The `foxieos` and `foxieos-hardware` teams each have write access to their own repository, and are reserved for roles in that project.
  They stay empty, apart from the maintainer, until the roles are decided and assigned.
- This `.github` repository has no team: its files apply to every repository, so only the maintainer changes them, through pull requests.
- A ruleset protects each repository's `main` branch.
  Each repository's `CONTRIBUTING.md` lists its rules.
- Two-factor authentication is required for every member.

## Continuity

The organization has one owner.
The maintainer adds a second owner when they judge a member ready.
That member:

- has contributed to and reviewed the projects;
- agrees to this document and to the key rules in the repositories' `AGENTS.md` and `docs/RELEASING.md`;
- is proposed by the maintainer in an issue in this repository, and accepts there.

Owning the organization doesn't give access to release keys.
Release keys stay with the maintainer on the signing host, as each repository's release docs describe.

## Changing this document

Propose a change in a pull request to this repository.
The maintainer approves it.
