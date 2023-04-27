# Contributing Guidelines

Welcome to the notary community. The Notary project accepts contributions via GitHub pull requests. This document outlines the process to help get your contribution accepted.

## Overview of Notary project

The Notary Project aims to provide enterprise-grade solutions and cross-industry standards for securing software supply chain. The following are current repositories, aka sub-projects, under the Notary project umbrella:

| Repository                                                               | Description                                                                                                                                                    |
| ------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [notation](https://github.com/notaryproject/notation)                    | A CLI project to add signatures as standard items in the registry ecosystem, and to build a set of simple tooling for signing and verifying these signatures   |
| [notation-go](https://github.com/notaryproject/notation-go)              | A library project to support sign and verify artifacts and store signatures in the registry                                                                    |
| [notation-core-go](https://github.com/notaryproject/notation-core-go)    | A library project to support Notary signature envelope and format specific implementation                                                                      |
| [notaryproject](https://github.com/notaryproject/notatryproject)         | A project for Notary project requirements and specifications                                                                                                   |
| [notaryproject.dev](https://github.com/notaryproject/notatryproject.dev) | A project for Notary project website                                                                                                                           |
| [.github](https://github.com/notaryproject/.github)                      | A project for notary project governance documents                                                                                                              |
| [meeting-notes](https://github.com/notaryproject/meeting-notes)          | A project for archived meeting notes                                                                                                                           |
| [tuf](https://github.com/notaryproject/tuf)                              | A project to implement the full TUF specification in a registry native way                                                                                     |
| [notary](https://github.com/notaryproject/notatry)                       | The original project, which is an implementation of TUF that runs next to a container registry and adds the ability to sign and verify content in the registry |

## Support Channels

Whether you are a user or contributor, official support channels include:

- Issues for each repository. You can use [Notation issue](https://github.com/notaryproject/notation/issues) if you are not sure about which repository to be involved.
- Slack: [#notary-project](https://app.slack.com/client/T08PSQ7BQ/CQUH8U287/). Join [slack](https://slack.cncf.io/) if it is your first time using Slack.
- [Public community meetings](https://notaryproject.dev/community/#cncf-public-events-calendar)
  - Catch up with [past meetings on YouTube](https://www.youtube.com/@CNCFNotary)

## Reporting Security Issues

> **Warning** If you are reporting a security vulnerability, Please DO NOT file a public issue.

Please refer to [Security Guide](SECURITY.md) on how to report security vulnerabilities.

## Reporting Other Issues

It is a great way to contribute to notary project by reporting issues. Please open an issue on Github and follow the template to fill in required information.

Before opening any issue, please look up the existing issues to avoid submitting a duplication. If you found an issue that describes your problem:

- Please read other user comments first to confirm if they have experienced the same issue. Keep in mind that a given error condition might be indicative of different problems. You may also find a workaround in the comments
- To receive updates on an issue, simply click the 'subscribe' button
- Please only comment if you have new, technical, and relevant information to add to the case.

Issues will be marked with different labels for different purpose, see [Labels](#labels) for details.

### Issue Lifecycle

The issue lifecycle is mainly driven by the maintainers.

1. Issue creation:
   - After an issue is created, it will be labelled `bug` or `enhancement`, and `triage`.
2. Triage: The maintainers will triage the issues. The results of triage could be one of the following:
   - Remove label `triage`, and add the issues to the correct milestone
   - Keep label `triage` to indicate that further triage is required
   - Remove label `triage`, and labelled `wont fix` to indicate this issue is out of the scope of Notary or other reasons.
3. Development:
   - An issue labelled `enhancement` normally require solution proposal and spec updates if needed before implementation
   - An issue that is labeled as `enhancement` or `bug` should be connected to the PR that resolves it
4. Issue closure
   - Close the issue once PRs are merged
   - Close the issue once the author accepts the `wont fix` decision

### Stale issues or PRs

A stale issue or pull request (PR) is one that has not had any activity or updates for 60 days. When an issue or PR becomes stale, it is labelled as `stale`. Normally maintainers will comment on stale issue or PR to prompt participants to take action. Then, if no additional activity occurs after 14 days, this issue or PR will be closed. If an update/comment occur on stale issues or pull requests, the stale label will be removed and the timer will restart.

## Support requests or questions

Please use slack channel for support requests or questions. Issues could be created accordingly if it is a bug or enhancement.

## Contributing Workflow

PR are always welcome, even if they only contain small fixes like typos or a few lines of code. If there will be a significant effort, please document it as an issue and get a discussion going before starting to work on it.

Please submit a PR broken down into small changes bit by bit. A PR consisting of a lot of features and code changes may be hard to review. It is recommended to submit PRs in an incremental fashion.

> **Note** If you split your pull request to small changes, please make sure any of the changes goes to main will not break anything. Otherwise, it cannot be merged until this feature complete.

### Fork and clone

  Fork the repository and clone the code to your local workspace.

### Branch

  Changes should be made on your own fork in a new branch checked out from the `main` branch.

### Develop, Build, and Test

  Write code on the new branch in your fork. Unit test cases should be added to cover the new code. For PR in [notation](https://github.com/notaryproject/notation), end-to-end (e2e) test cases should be added, see [e2e quick start](https://github.com/notaryproject/notation/blob/main/test/e2e/README.md)

### Keep sync with upstream

  Once your branch gets out of sync with the `main` branch, please fetch and rebase from `main` branch.

### Commit

  As Notary project repositories has integrated the [DCO (Developer Certificate of Origin)](https://github.com/apps/dco) check tool, contributors are required to sign off that they adhere to those requirements by adding a `Signed-off-by` line to the commit messages. Git has even provided a `-s` command line option to append that automatically to your commit messages, please use it when you commit your changes.

  Notary project repositories require signed commits, please refer to [commit signatures verification](https://docs.github.com/en/authentication/managing-commit-signature-verification/about-commit-signature-verification) on signing commits.

### Push and Create PR

  When ready for review, push your branch to your fork repository, and [create a new pull request (PR)](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request?tool=webui). Description of a pull request should refer to all the issues that it addresses. Remember to [link the PR to an issue using a keyword](https://docs.github.com/en/issues/tracking-your-work-with-issues/linking-a-pull-request-to-an-issue#linking-a-pull-request-to-an-issue-using-a-keyword) so that the issue can be closed when the PR is merged.

  Once your pull request has been opened it will be assigned to reviewers automatically based on CODEOWNERS. Those reviewers will do a thorough code review, looking for correctness, bugs, opportunities for improvement, documentation and comments, and style.

  Commit changes made in response to review comments to the same branch on your fork.

## Contributing new features

You are heavily encouraged to first discuss what you want to do. You can do so on the slack channel, or by opening an issue that clearly describes the use case you want to fulfill, or the problem you are trying to solve. If this is a new feature, you should then submit a proposal that describes your technical solution and reasoning. It's advisable to address all feedback on this proposal before starting actual work. For new feature requiring changes on Notation CLI flags or commands, the proposal should include the changes on the CLI specification, see [Notation CLI index file](https://github.com/notaryproject/notation/blob/main/specs/notation-cli.md).

After issue and solution proposal are approved by maintainers, you should submit PR based on [Contributing Workflow](#contributing-workflow)

## Documenting

Update the documentation if you are creating or changing features. Good documentation is as important as the code itself.

The main location for the documentation is the [website repository](https://github.com/notaryproject/notaryproject.dev).

Documents are written with Markdown. See [Writing on GitHub](https://docs.github.com/en/get-started/writing-on-github) for more details.

Documentation PRs will follow the same workflow as other PRs.

## Labels

The following tables define all label types used for Notary project. It is split up by category.

### Common

| Label           | Description                                                                 |
| --------------- | --------------------------------------------------------------------------- |
| `bug`           | Marks an issue as a bug or a PR as a bugfix                                 |
| `documentation` | Indicates the issue or PR is a documentation change                         |
| `duplicate`     | Marks an issue or PR already exists                                         |
| `enhancement`   | Marks the issue as a feature request or a PR as a feature implementation    |
| `keep open`     | Denotes that the issue or PR should be kept open past 30 days of inactivity |
| `stale`         | Marks an issue or PR stale                                                  |
| `testing`       | Marks an issue or PR is related to testing                                  |
| `triage`        | Indicates the issue or PR needs triage                                      |
| `UX`            | Marks an issue or PR is related to user experience                          |

### Issue Specific

| Label              | Description                                                              |
| ------------------ | ------------------------------------------------------------------------ |
| `help wanted`      | Marks an issue needs help from the community to solve                    |
| `good first issue` | Marks an issue as a good starter issue for someone new to Notary project |
| `wont fix`         | Marks an issue as discussed and will not be implemented                  |

## Credits

We would like to give credit to the [Helm Community](https://github.com/helm/community) and the [Harbor Community](https://github.com/goharbor/harbor/) for using their contributing guide as references.