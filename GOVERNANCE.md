# Governance

This page says who decides what in the FoxieOS projects, who may change what, and what the founding meeting decided.
It applies to every repository in the [`alopex-org`](https://github.com/alopex-org) organization, unless a repository's own docs say otherwise.
GitHub words such as pull request, code owner and ruleset are explained in the [glossary](GLOSSARY.md).

## In short

- The members held their founding meeting on 2026-11-24.
- The projects have three maintainers ([Maintainers](#maintainers)).
  The organization's owner is one of them, with the same say as the others.
- **Everyday changes** need one approval from a maintainer who didn't write them, and stay open for two days first so that others can see them ([Everyday changes](#everyday-changes)).
- **Foundational changes**, such as roadmap decisions, this page and who the maintainers are, stay open for seven days and need a majority of the maintainers; two members together can send one to a vote of the members ([Foundational changes](#foundational-changes)).
- **A maintainer's objection** stops a change until it is settled: first by talking, then by a vote of the maintainers, then by a vote of the members ([Settling a disagreement](#settling-a-disagreement)).
- If nothing is decided, nothing changes.
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
  Changed on 2026-11-26 so that the organization's owner decided who settled a disagreement.
  Changed again, back toward the meeting's rule: the maintainers vote, and the members vote if the maintainers can't decide, each within a set time ([Settling a disagreement](#settling-a-disagreement)).
- **Merging.**
  One maintainer's approval lets a pull request merge.
  Since 2026-11-26, only a maintainer other than the pull request's author can give that approval.
  Changes also wait a set time before merging, and foundational changes need a majority of the maintainers ([How changes are approved](#how-changes-are-approved)).
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
Adding or removing a maintainer is a [foundational change](#foundational-changes).
Anyone in the organization can propose a person in an issue in this repository, and the person accepts there.
The pull request that makes the change also updates every `.github/CODEOWNERS` file.
How the maintainers do their everyday work is in the [maintainer guide](MAINTAINING.md).

### What the owner covers for now

The other maintainers have write access to the project repositories, through the `foxieos` and `alopex-hardware` teams ([Access](#access)).
There they approve and merge pull requests and look after issues.
Some maintainer tasks need more access on GitHub than that, so for now the organization's owner does them alone:

- **Security and code-of-conduct reports.**
  Both arrive through GitHub's private reporting form, and only the organization's owner sees what is sent there.
- **This `.github` repository.**
  No team gives the maintainers write access here, so GitHub counts only the organization's owner's approval.
  The other maintainers approve the owner's own pull requests here by writing "Approved" in a review or a comment.
  The owner then merges with the override ([The organization's owner](#the-organizations-owner)), and the approvals stay on the pull request as the record.
  A maintainer's objection here is a review that asks for changes, as anywhere else, and stops the merge in the same way, even though GitHub doesn't enforce it.
- **Tags and releases, overriding the rules on `main`, and repository secrets.**
  These need GitHub's admin role, which only the organization's owner has.

This stays so until the maintainers decide how to share these tasks, for example with a team for the maintainers or another owner ([Continuity](#continuity)).

## Roles

- **The maintainers** are listed under [Maintainers](#maintainers).
  The maintainers:
  - take the decisions listed in each repository's roadmap;
  - approve changes to the files they own as code owners, but never their own pull requests;
  - handle security and code-of-conduct reports;
  - are the only people who handle release keys and publish releases.

  For now the organization's owner does some of these alone ([What the owner covers for now](#what-the-owner-covers-for-now)).
- **The organization's owner** is one of the maintainers, with the same say as the others ([The organization's owner](#the-organizations-owner)).
- **Members** belong to the `alopex` team, which covers every project in the organization.
  They open pull requests, review each other's changes, take part in the discussion of every decision and vote when a question reaches them.
  How they do this is in the [member guide](MEMBERS.md).
- **Contributors** are everyone else.
  They open issues, and open pull requests from their own forks.
  Their pull requests follow the same rules as members'.
- **Coding agents** are AI tools that a person directs.
  The person who directs an agent signs off its commits and is responsible for them, as for their own work.
  A pull request written by an agent counts as that person's pull request.
  The agent follows the repository's `AGENTS.md`.

## How changes are approved

Every change reaches `main` through a pull request, as each repository's `CONTRIBUTING.md` describes.
The same rules apply whoever wrote the change: a contributor, a member, a maintainer or the organization's owner.
"The author" means everyone who wrote commits in the pull request.

### Everyday changes

Most changes are everyday changes: docs, research notes, fixes, scripts and anything else that isn't a [foundational change](#foundational-changes).

- **One approval.**
  A maintainer who isn't an author of the pull request approves it.
- **Two days open.**
  The pull request stays open for at least two days (48 hours) before it merges, so that the other maintainers and the members can read it.
  GitHub doesn't enforce this wait; the maintainer who merges keeps to it.
- **What may merge sooner.**
  A fix to a typo, a broken link or a failing check may merge as soon as it is approved.
  So may a fix to a security problem that can't wait.
  The pull request says why it didn't wait.
- **Undoing an early merge.**
  If a maintainer objects to a change that merged before its wait was over, any maintainer undoes it with a pull request that reverses it, and the change comes back as an ordinary pull request.
  The reversing pull request needs no wait.

### Foundational changes

Foundational changes shape the projects or the organization, so everyone gets time to take part.
They are:

- taking a roadmap decision (D1, D2, …);
- changing a project's purpose, scope or commercial direction;
- changing this page, the [code of conduct](CODE_OF_CONDUCT.md) or a licence;
- adding or removing a maintainer or an owner, or changing who has access to what.

A foundational change:

1. **Has an issue.**
   A roadmap decision uses its issue of type Decision; any other foundational change gets an issue in this repository.
   Someone posts a link to the issue on the Alopex Discord, so the members know about it.
2. **Stays open for seven days.**
   The pull request links the issue and stays open for at least seven days, for comments, before it merges.
3. **Needs a majority of all the maintainers.**
   An author who is a maintainer counts toward it.
   With three maintainers that means two, so an author who is a maintainer needs one more maintainer's approval, and anyone else needs two.
4. **Can be sent to the members.**
   If at least two members who aren't maintainers object in the issue within the seven days, and say why, the question goes straight to a [vote of the members](#settling-a-disagreement).

### Objections

- **A maintainer objects** with a review that asks for changes and says why.
  GitHub then stops the pull request from merging until that maintainer approves it.
  A review that only asks for small fixes is not an objection; it ends when the author makes them.
  It becomes one if the author and the reviewer still disagree after the author has answered.
- **Only the maintainer who objected withdraws an objection**, by approving or by dismissing their own review.
  GitHub lets any maintainer dismiss a review; they don't, except to carry out the result of [Settling a disagreement](#settling-a-disagreement), and they link that result when they do.
- **A member objects** with a review that asks for changes, or with a comment.
  GitHub doesn't count members' reviews, so a maintainer answers the objection in the pull request before it merges.
  For a foundational change, two members' objections send it to a vote of the members, as above.

## Settling a disagreement

The same steps settle every disagreement: over a pull request, a roadmap decision, or anything else in the projects.
Each step has a deadline, so that a question never waits on one person.
A step ends early once everyone in it has said their view.

1. **Talk it through** in the pull request or issue, with sources, for up to seven days.
   The author may change the proposal, and the objector may withdraw.
2. **The maintainers vote.**
   Once the talking hasn't settled it, any maintainer calls the vote in a comment.
   Every maintainer, the author and the objector included, writes "for" or "against" in a comment within seven days.
   The majority of the votes given decides.
   With three maintainers, the one who wasn't involved yet usually decides.
   If the vote is tied, or fewer than two maintainers vote, the question goes to the members.
3. **The members vote.**
   The maintainer who called the first vote calls this one, with a link to the question.
   Everyone in the `alopex` team, the maintainers included, writes "for" or "against" in a comment within seven days.
   The majority of the votes given decides, if at least half of the team voted.

**If nothing is decided, nothing changes.**
Until the question is settled the change doesn't merge.
If the members' vote is tied or too few vote, the pull request closes and the roadmap decision stays open.

**Votes are written down.**
Votes count only as comments in the pull request or issue; a vote on Discord doesn't count.
The person who called the vote counts it and writes the result in the same place.
The result settles that proposal; a new proposal that changes it in substance can be made later.

**More time.**
Anyone taking part can ask once, in the pull request or issue, for seven more days in a step, for example during exams.

## How decisions are made

- **Roadmap decisions** have short codes (D1, D2, …).
  Each one has a section in the repository's `docs/ROADMAP.md` and an issue of type Decision.
  Anyone can comment on the issue.
  The maintainers decide together, as a [foundational change](#foundational-changes).
  The decision and its date go into the roadmap, in a pull request that closes the issue.
- **Changes** follow [How changes are approved](#how-changes-are-approved) and the repository's `CONTRIBUTING.md`.
  Someone other than the author reviews every change, and some areas need a review by a person rather than by a coding agent.
  Only a maintainer approves a pull request, and never their own.
- **Discord** doesn't decide anything by itself.
  An argument or an agreement counts once someone writes it in the issue or pull request it concerns.
- **Disagreements** are argued in the issue or pull request, with sources, and settled as [Settling a disagreement](#settling-a-disagreement) describes.

## The organization's owner

- **The owner is one of the maintainers**, with one vote and the same say as the others.
- **The owner's admin powers carry out decisions; they don't take them.**
  The owner manages teams, settings, tags and secrets as the maintainers decide.
- **The owner overrides the rules on `main` only:**
  - to merge a pull request in this `.github` repository that the other maintainers approved in writing ([What the owner covers for now](#what-the-owner-covers-for-now));
  - in an emergency: `main` is broken, or a security problem can't wait.
    The owner says so in the pull request, or in an issue within a day, and the other maintainers can then object as for any change.
- **Never to merge their own change** without another maintainer's approval.
- Every override is recorded in the ruleset's history.

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
  Its files apply to every repository, so only the maintainers change them, through pull requests ([What the owner covers for now](#what-the-owner-covers-for-now)).
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
- A further owner is added when a member is ready, as a [foundational change](#foundational-changes).
  That member:
  - has contributed to and reviewed the projects;
  - agrees to this page and to the repositories' rules on keys, devices and publishing (in `docs/RELEASING.md` and `AGENTS.md`);
  - is proposed in an issue in this repository, and accepts there.

Owning the organization doesn't give access to release keys.
Release keys stay with the maintainers on the signing computer, as each repository's release docs describe.

## Growing

These rules are written for a few maintainers and a small team, and they keep working as the number of maintainers grows: the votes count a majority, whoever takes part.
When the team grows enough that one vote of all the maintainers becomes slow, the maintainers can propose giving each project its own maintainers, as a foundational change.

## Changing this page

Changing this page is a [foundational change](#foundational-changes).
Suggest it in a pull request to this repository, with an issue for the discussion.
