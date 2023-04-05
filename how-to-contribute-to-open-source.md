# How to contribute to open source projects

- [Contributions on behalf of Syngenta](#contributions-on-behalf-of-syngenta)
  - [How to communicate that you contribute on behalf of Syngenta](#how-to-communicate-that-you-contribute-on-behalf-of-syngenta)
- [Private contributions](#private-contributions)
- [Using forks in your code](#using-forks-in-your-code)
- [Contributing to a project on GitHub](#contributing-to-a-project-on-github)

## Contributions on behalf of Syngenta

This document describes rules and recommendations for contributing to open-source projects **on behalf of Syngenta company** — done during your working hours or related to your work on Syngenta projects.

Contributions done on behalf of Syngenta represent the company. You should be reasonable and take responsibility for your actions and consequences. Do your best job when contributing to open-source projects; respect the community and rules.

### How to communicate that you contribute on behalf of Syngenta

Making open-source contributions, you should communicate that you are doing it on behalf of Syngenta.

Each open-source projects have its way of listing contributors. Please, respect the way of listing contributors specific to each project.

Some general guidelines:

- Use your `@syngenta.com` email in your commit messages.
- _Optionally:_ Specify yourself as a contributor with the "username (Syngenta)" string in the project's changelog.
- _Optionally:_ Some projects keep the list of contributors in a separate file or README. Specify yourself and Syngenta as contributors in a way appropriate and used for the project.

## Private contributions

Your private contributions to open-source done on your own (in your own time and not related to Syngenta) are not subject to the rules described in this document.

You are responsible to ensure that you do not use any confidential information belonging to Syngenta, or that is known due to your work at Syngenta; and that you do not use/publish any code or other work created for Syngenta (which becomes part of Syngenta’s property).

## Using forks in your code

Avoid using forked code and try to contribute your change upstream.

It's typical for forks to fall far behind the upstream repository and such dependencies become a source of pain:

- Rebasing the branch may become non-trivial, and it'd become hard to bring such dependency up to date.
- Some other libraries in your project might depend on the original version, creating a [diamond dependency problem](https://en.wikipedia.org/wiki/Dependency_hell).

There may be good reasons to create a fork:

- To fix a security issue not being fixed upstream fast enough if it's affecting our customers or us.
- Any other reasons? Talk to your peers and use your best judgment.

If you decide to create a fork, make sure you open an issue that:

- Describes the reason for the fork to exist.
- Links to the MR(s) where the fork was introduced as a dependency.
- Links to any relevant issues in the upstream project. If the issue was not reported already, make sure you report it in the project's issue tracker. This is important because if the project's maintainers don't know about it they will not fix it.
- Links to any opened PRs to fix the issue upstream.
- Describes the remediation work needed to start using the upstream code again.
- If it's not just changes in the forked code, but also some modifications in your code to use the fork, consider putting a TODO and a link to this issue next to that code in a comment.

## Contributing to a project on GitHub

If your GitHub account's primary email is not your `@syngenta.com` email, you can add it as an additional address. No need to create a separate account.

1. Fork the repository you want to contribute to into your account.
2. Follow the usual [pull request flow](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request-from-a-fork).
3. Respect the recommendations described in [Contributions on behalf of Syngenta](#contributions-on-behalf-of-syngenta).

## Contributor License Agreements

Some open-source projects require that contributors agree to a "Contributor License Agreement" (CLA) before contributing.

These CLAs are legally binding and may enforce some terms or conditions inappropriate for Syngenta.

Before contributing to any project with a CLA, you must obtain permission from the OSPO team (we will check legal issues).
