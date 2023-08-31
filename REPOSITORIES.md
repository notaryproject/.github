## Repositories

This document describes the lifecycle of repositories under the [Notary Project](https://github.com/notaryproject/) organization.

Anyone can submit proposals regarding repositories' lifecycle by opening a GitHub issue in the
[notaryproject/.github](https://github.com/notaryproject/.github) repository. The [Notary Project governance maintainers](MAINTAINERS) will take into account the community feedback and decide on the proposal.

### Create a new sub-project

A new sub-project can be created as a repository and contributed to the Notary Project organization by opening a GitHub issue to request [Notary Project governance maintainers](MAINTAINERS) to vote in the
[notaryproject/.github](https://github.com/notaryproject/.github) repository. A new sub-project can be created after having a supermajority of approval from Notary Project governance maintainers.

If the decision is to add the proposed project, then one of the Notary Project GitHub organization admins will assist the issue opener in creating a repository or transferring an existing repository to the Notary Project organization. Upon creation, the repository must be reviewed to make sure it follows [Notary Governance](GOVERNANCE.md). 

### Lifecycle change 

A repository can be archived if no activity like Pull Requests for a year. The sub-project maintainers of a given repository can propose changing its status by opening a GitHub issue in the [notaryproject/.github](https://github.com/notaryproject/.github) repository. The [Notary Project governance maintainers](MAINTAINERS) will take into account the community feedback and decide on the proposal. The project status should be stated in the README of the repository.

#### Archiviation

Repositories showing little to no activity during the time span of a year can be proposed for Archiviation by opening a GitHub [issue](https://github.com/notaryproject/.github/issues). Once the proposal issue has a super-majority of approval from Notary Project governance maintainers, they can be archived. [Archived repositories](https://docs.github.com/en/repositories/archiving-a-github-repository/archiving-repositories) will remain inside the Notary Project GitHub organization but will be read-only and will not be maintained. As such, `CODEOWNERS` files contained in archived repositories are not valid.

In some cases, a repository is archived to reserve its name for future use.

#### Unarchiviation

Archived repositories can be proposed for unarchiviation by opening a GitHub issue in the [notaryproject/.github](https://github.com/notaryproject/.github) repository. Once the proposal issue has a supermajority of approval from Notary Project governance maintainers, the archived repository can be changed to active. In general, the same rules as for new repositories apply. 

## Credits

Parts of the content are borrowed from [falcosecurity/evolution](https://github.com/falcosecurity/evolution/blob/main/REPOSITORIES.md).