# Contribution Guidelines

Thank you for your time and your contribution.

These guidelines apply to all [FUTO](https://github.com/futo-org) repositories. A repository can add rules or change these rules in its own `CONTRIBUTING.md`. If the two guides disagree, follow the guide in the repository.

These are mostly guidelines, not rules. Use your best judgment. To propose a change to these guidelines, open a pull request.

If you follow these guidelines, you show respect for the time of the maintainers. When the maintainers reply to your issue, review your changes and help you finish your pull request, they respect your time in return.

## AI Usage Policy

You can use AI tools to contribute to [FUTO](https://github.com/futo-org) repositories.

> [!IMPORTANT]
> If you use AI tools for any part of a contribution, disclose it in the pull request or issue.

Say which tools you used and how much they did, for example documentation only or most of the code. If AI writes your replies to review comments, disclose that too. You do not need to disclose autocomplete of single words or short phrases.

Example disclosures:

> Claude Code wrote most of this pull request. I reviewed and tested every change.

> I used ChatGPT to understand the codebase, but I wrote the change myself.

Disclosure tells reviewers how closely to review a contribution. It is also a courtesy to the people who review your work. Maintainers can close a contribution with undisclosed AI use, and repeated cases can get your account banned from contributing.

Individual repositories can publish their own AI policies, for example in an `AGENTS.md` file. If a repository has its own AI policy, follow that policy.

## Before Getting Started

Read the [code of conduct](./CODE_OF_CONDUCT.md).

Ask questions in the [FUTO community chat](https://chat.futo.org/). Use issues only for bugs, feature requests and documentation problems.

## Different contributions

You can contribute in these ways:

- Write tutorials.
- Improve the documentation.
- Report bugs and request features.
- Write code for the project.

If you find a bug in the source code or a mistake in the documentation, [submit an issue](#submitting-an-issue).

If you find a security vulnerability, report it as the [security policy](./SECURITY.md) describes. Do not submit an issue unless a maintainer asks you to.

If you want to improve the documentation, tell others about your work, so that two people do not do the same work. Open a new issue, or comment on a related issue.

### Missing a Feature?

To request a new feature, [submit an issue](#submitting-an-issue). If you want to build a new feature yourself, the size of the change decides the next steps.

For a major feature, first open an issue that describes your proposal. We discuss the proposal in the issue. The discussion helps us coordinate work, prevents duplicate work and helps you make a change that we can accept. A new documentation topic, or a large rewrite of a topic, counts as a major feature.

For a small feature, you can submit a pull request directly.

## Submission Guidelines

### Submitting an Issue

Before you submit an issue, search the issue tracker. An issue for your problem can already exist, and its discussion can show a workaround.

Before we fix a bug, we must reproduce it and make sure that it is real. For this reason, you must give a minimal reproduction of the bug. A minimal reproduction is the smallest setup that shows the bug. It gives us the information that we need, without more questions to you.

With a minimal reproduction, we can quickly make sure that the problem is a bug and not an error in your code. We can also make sure that we fix the correct problem.

A minimal reproduction saves time for the maintainers, so they can fix more bugs. Developers often find the problem in their own code while they prepare a minimal reproduction. It can be hard to take the necessary code out of a large codebase. But we must isolate the problem before we can fix it.

We cannot examine or fix a bug without a minimal reproduction. If an issue does not have enough information to reproduce the bug, and you do not reply, we close the issue.

Keep what you observed separate from what you inferred. Mark anything that you did not test yourself.

To submit an issue, select one of the issue templates and fill it in.

### Naming a Pull Request (PR)

The title of your pull request (PR) must follow the [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) style. The title shows the type of work in the PR. The release workflow also reads the title to increase the correct part of the version number, as [Semantic Versioning](https://semver.org/spec/v2.0.0.html) specifies.

Use this format for the title:

`<type>[(optional scope)][!]: <description>`

The `<type>` is one of these [conventional commit types](https://github.com/commitizen/conventional-commit-types):

- `feat:` a new feature
- `fix:` a bug fix
- `docs:` changes to the documentation only
- `style:` changes that do not affect the meaning of the code, for example white space, formatting or missing semicolons
- `refactor:` a code change that does not fix a bug or add a feature
- `perf:` a code change that improves performance
- `test:` new tests or corrections to existing tests
- `build:` changes to the build system or to external dependencies
- `ci:` changes to the CI configuration files and scripts
- `chore:` other changes that do not change source or test files
- `revert:` a revert of an earlier commit

If the change is not backward compatible, add an exclamation mark `!` after the type. Add it only to `feat` or `fix`.

> [!NOTE]
> We enforce conventional commits only for the title of your pull request, not for each commit message.

Examples:

- `feat: add option for custom log level`

  This pull request adds a new configuration option.

- `fix!: rename deprecated config key`

  This pull request fixes a bug. The `!` after the type shows that the change is not backward compatible.

> [!TIP]
> If your pull request has only one commit, GitHub uses the message of that commit as the default title. If that message uses the conventional commit style, the title is already correct.

### Submitting a Pull Request

Before you submit your pull request, do these steps:

1. Search the repository for an open or closed PR that is related to your change. This prevents duplicate work.

1. Make sure that an issue describes the problem that you fix, or the design of the feature that you add. If we agree on the design first, we are ready to accept your work.

1. Fork the repository.

1. Create a new git branch for your change:

   ```shell
   git checkout -b feature/my-fix-branch main
   ```

1. Make your change.

1. If your change needs tests, add them.

1. Make sure that all tests pass.

1. Review every line of your change. Be ready to explain any of it. You are responsible for the change, whatever tools you used.

1. Commit your changes with a descriptive commit message:

   ```shell
   git commit -s -m 'Awesome commit message'
   ```

   The optional `-a` flag makes `git commit` add and remove the changed files automatically.

1. Push your branch to your fork on GitHub:

   ```shell
   git push origin feature/my-fix-branch
   ```

1. On GitHub, open a pull request from the branch on your fork to the `main` branch of the upstream repository. The upstream repository is the repository that you forked.

1. After we merge your pull request, delete your branch. You can also delete your fork.

### Reviewing a Pull Request

Anyone can review pull requests, and we encourage contributors to review the work of others. But only maintainers can approve a pull request. A pull request often needs approvals from several maintainers before it can merge.

## Your First Contribution

If you do not know where to start, look for issues with the "good first issue" or "help wanted" label. A "good first issue" needs only a few lines of code and one or two tests. A "help wanted" issue needs more work than a "good first issue".

The free series [How to Contribute to an Open Source Project on GitHub](https://app.egghead.io/playlists/how-to-contribute-to-an-open-source-project-on-github) shows how to open your first pull request. If you prefer written tutorials, read <https://github.blog/developer-skills/github/beginners-guide-to-github-creating-a-pull-request/> and <https://www.firsttimersonly.com/>.

Then you are ready to make your changes. If you need help, ask for it. Everyone is a beginner at first.

If a maintainer asks you to rebase your PR, a lot of code changed since you started. To rebase is to move your commits on top of the latest target branch. Rebase your branch, so that your PR is easier to merge.
