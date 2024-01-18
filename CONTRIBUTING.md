# Contributing Guidelines

This document offers an overview of the process for users to contribute by either opening a pull request or reporting an issue. For more more information about the Notary Project, please refer to the [Notary Project Overview](https://github.com/notaryproject/.github/blob/main/README.md).

## Reporting a Security Issue

> [!Warning]
> If you are reporting a security vulnerability, Please DO NOT open a public issue.

Please refer to [Security Guide](SECURITY.md) on how to report security vulnerabilities.

## Reporting an Issue

Reporting an issue is a great way to contribute. Please open an issue on Github with required information.

Prior to opening a new issue, we kindly request that you check the existing issues to prevent duplicate submissions. In the event that you come across an issue that aligns with your problem please do following:

- Carefully review the issue description and comments to validate that your issue aligns with a similar problem. It's important to note that a specific error could potentially be associated with various issues. Additionally, you might discover a potential solution or workaround in the comments section
- To receive notifications regarding an issue, just click the 'subscribe' button
- Please only comment if you have new, technical, and relevant information to add to the case.

Issues will be marked with different labels for different purpose, see [Labels](#labels) for details.

### Issue Lifecycle

The issue lifecycle is mainly driven by the maintainers.

1. Issue creation:
   - After an issue is created, it will be labelled `bug` or `enhancement`, and `triage`.
2. Triage: The maintainers will triage the issues weekly. The results of triage will be one of the following:
   - Remove label `triage`, and add the issues to the correct milestone.
   - Remove the `triage` label and apply the `need information` label to indicate that this issue requires additional information. Once this issue has been clarified with the necessary details, it can then be assigned to the appropriate milestone or labeled as `wont fix`.
   - Remove the `triage` label and assign the `wont fix` label to signify that this issue falls outside the scope of the Notary Project or for other relevant reasons.
3. Development:
   - An issue labelled `enhancement` normally require solution proposal and spec updates if needed before implementation
   - An issue that is labeled as `enhancement` or `bug` should be connected to the PR that resolves it
4. Issue closure: According to the [guidance](https://docs.github.com/en/issues/tracking-your-work-with-issues/closing-an-issue), there are two reasons for closing an issue: `Close as completed` (default reason) and `Close as not planned`. 
   - Use `Close as completed` if the issue is fixed, resolved, or done. 
   - Use `Close as not planned` if the author accepts the wont fix decision, or if the issue cannot be reproduced, duplicated, or is stale.

### Stale issues or PRs

A stale issue is one that remains inactive or without updates for a period of 60 days. A stale pull request (PR) is one that remains inactive or without updates for a period of 45 days. When an issue or PR becomes stale, it is labelled as `stale`. Normally maintainers will comment on stale issue or PR to prompt participants to take action. If there is no activity for additional 30 days, this issue or PR will be closed. If an update/comment occur on stale issues or pull requests, the stale label will be removed and the timer will restart.

## Milestones

The Notary Project uses [milestones](https://docs.github.com/en/issues/using-labels-and-milestones-to-track-work/about-milestones) to track progress on groups of issues or pull requests in a repository. The following table defines the milestones that used by the Notary Project.

| Milestone           | Description                                                                                                                       |
| ------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| `in discussion`     | This milestone includes issues or PRs that require discussion before they can be added to the correct milestone.                  |
| `backlog`           | This milestone includes issues or PRs that are valuable but are not currently planned for release.                                |
| `<Release Version>` | This milestone includes issues or PRs that are planned for a specific release. The format is `vX.Y.Z`, For example, `v1.1.0`, `v1.2.0`. See [Release Versioning](https://github.com/notaryproject/notation/blob/v1.0.1/RELEASE_MANAGEMENT.md#release-versioning) for details. |

## Support requests or questions

Please use slack channel for support requests or questions. Issues could be created accordingly if it is a bug or enhancement.

## Contributing Workflow

PRs are always welcome, even if they only contain small fixes like typos or a few lines of code. If there will be a significant effort, please document it as an issue and get a discussion going before starting to work on it.-

Please submit a PR broken down into small changes bit by bit. A PR consisting of a lot of features and code changes may be hard to review. It is recommended to submit PRs in an incremental fashion.

> **Note** If you split your pull request to small changes, please make sure any of the changes goes to main will not break anything. Otherwise, it cannot be merged until this feature complete.

### Fork and clone

  Fork the repository and clone the code to your local workspace.

### Branch

Changes should be made on your own fork in a new branch checked out from the `main` branch.

### Develop, Build, and Test

Write code on the new branch in your fork. You can try to build the notation project locally by following the [Building guide](https://github.com/notaryproject/notation/blob/main/building.md)

Unit test cases should be added to cover the new code. For PR in [notation](https://github.com/notaryproject/notation), end-to-end (e2e) test cases should be added, see [e2e quick start](https://github.com/notaryproject/notation/blob/main/test/e2e/README.md)

### Keep sync with upstream

Once your branch gets out of sync with the `main` branch, please fetch and rebase from `main` branch.

### Commit

You should follow [conventional commits](https://www.conventionalcommits.org/en/v1.0.0/) to write commit message. As the Notary Project repositories enforces the [DCO (Developer Certificate of Origin)](https://github.com/apps/dco) on Pull Requests, contributors are required to sign off that they adhere to those requirements by adding a `Signed-off-by` line to the commit messages. Git has even provided a `-s` command line option to append that automatically to your commit messages, please use it when you commit your changes. 

The Notary Project repositories require signed commits, please refer to [SSH commit signature verification](https://docs.github.com/en/authentication/managing-commit-signature-verification/about-commit-signature-verification#ssh-commit-signature-verification) on signing commits using SSH as it is easy to set up. You can find other methods to sign commits in the document [commit signature verification](https://docs.github.com/en/authentication/managing-commit-signature-verification/about-commit-signature-verification). Git has provided a `-S` flag to create a signed commit.

An example of `git commit` command:

```shell
git commit -s -S -m <commit_message>
```

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

The following tables define all label types used for the Notary Project. It is split up by category.

### Common

| Label           | Description                                                                 |
| --------------- | --------------------------------------------------------------------------- |
| `bug`           | Marks an issue as a bug or a PR as a bugfix                                 |
| `documentation` | Indicates the issue or PR is a documentation change                         |
| `duplicate`     | Marks an issue or PR already exists                                         |
| `enhancement`   | Marks the issue as a feature request or a PR as a feature implementation    |
| `stale`         | Marks an issue or PR stale                                                  |
| `testing`       | Marks an issue or PR is related to testing                                  |
| `ux`            | Marks an issue or PR is related to user experience                          |

### Issue Specific

| Label              | Description                                                                  |
| ------------------ | ---------------------------------------------------------------------------- |
| `help wanted`      | Marks an issue needs help from the community to solve                        |
| `good first issue` | Marks an issue as a good starter issue for someone new to the Notary Project |
| `need information` | Indicates the issue need further information                                 |
| `triage`           | Indicates the issue needs triage                                             |
| `wont fix`         | Marks an issue as discussed and will not be implemented                      |

## Credits

We would like to give credit to the [Helm Community](https://github.com/helm/community) and the [Harbor Community](https://github.com/goharbor/harbor/) for using their contributing guide as references.
