# alopex-org/.github

This repository holds the files that every repository in the organization shares: the organization's public profile, the code of conduct, the governance rules and where to get help.

GitHub shows `profile/README.md` on the [organization's page](https://github.com/alopex-org).
When a repository in the organization has no code of conduct, governance or support file of its own, GitHub shows the one from here instead ([GitHub Docs][default-files]).

## Files

- [GOVERNANCE.md](GOVERNANCE.md): who decides what, who can change what, and how that changes after the founding meeting.
- [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md): how we treat each other, and how to report a problem privately.
- [SUPPORT.md](SUPPORT.md): where to ask a question or report something.
- [GLOSSARY.md](GLOSSARY.md): plain explanations of the GitHub words the docs use, such as branch, pull request and sign-off.
- [profile/README.md](profile/README.md): the short introduction on the organization's page.

Each project repository keeps its own `CONTRIBUTING.md`, `SECURITY.md`, issue forms and pull-request template, because those differ between projects.
A repository's own file always wins over the shared one.

## Suggesting a change

A change here affects every repository in the organization, so the maintainer reviews each one ([.github/CODEOWNERS](.github/CODEOWNERS)).
The rules for changes are the same as in [foxieos's CONTRIBUTING.md](https://github.com/alopex-org/foxieos/blob/main/CONTRIBUTING.md): a new branch for each change, a signed-off commit with a short `scope: description` subject, and one sentence per line.
Run `pre-commit install` in your clone first, so the checks run before each commit.
AI coding agents also follow [AGENTS.md](AGENTS.md).

## License

The files are under the Apache License 2.0 ([LICENSE](LICENSE)), except `CODE_OF_CONDUCT.md`.
`CODE_OF_CONDUCT.md` is adapted from the [Contributor Covenant][covenant] 3.0, and stays under its Creative Commons Attribution-ShareAlike 4.0 licence, as its attribution section says.

Raspberry Pi is a trademark of Raspberry Pi Ltd.
The projects are not affiliated with Raspberry Pi Ltd or the Meshtastic project.

[default-files]: https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file
[covenant]: https://www.contributor-covenant.org/version/3/0/
