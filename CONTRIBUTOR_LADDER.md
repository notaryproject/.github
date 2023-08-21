# Contributor Ladder Template

- [Contributor Ladder Template](#contributor-ladder-template)
  - [Contributor Ladder](#contributor-ladder)
    - [Contributor](#contributor)
    - [Organization Member](#organization-member)
    - [Org Maintainer](#org-maintainer)
  - [Subproject Maintainer](#subproject-maintainer)
  - [Inactivity](#inactivity)
  - [Involuntary Removal or Demotion](#involuntary-removal-or-demotion)
  - [Stepping Down/Emeritus Process](#stepping-downemeritus-process)
  - [Contact](#contact)
  - [Reference](#reference)

## Contributor Ladder

Hello! We are excited that you want to learn more about our project contributor ladder! This contributor ladder outlines the different contributor roles within the project, along with the responsibilities and privileges that come with them. Community members generally start at the first levels of the "ladder" and advance up it as their involvement in the project grows.  Our project members are happy to help you advance along the contributor ladder.

Each of the contributor roles below is organized into lists of three types of things. "Responsibilities" are things that a contributor is expected to do. "Requirements" are qualifications a person needs to meet to be in that role, and "Privileges" are things contributors on that level are entitled to.

### Contributor

Description: A Contributor contributes directly to the project and adds value to it. Contributions need not be code. People at the Contributor level may be new contributors, or they may only contribute occasionally.

- Responsibilities include:
  - Follow the CNCF CoC
  - Follow the project contributing guide
- Requirements (one or several of the below):
  - Report and sometimes resolve issues
  - Occasionally submit PRs
  - Contribute to the documentation
  - Show up at meetings, takes notes
  - Answer questions from other community members
  - Submit feedback on issues and PRs
  - Test releases and patches and submit reviews
  - Run or helps run events
  - Promote the project in public
  - Help run the project infrastructure
- Privileges:
  - Invitations to contributor events
  - Eligible to become an Organization Member

### Organization Member

Description: An Organization Member is an established contributor who regularly participates in the project. Organization Members have privileges in both project repositories and elections, and as such are expected to act in the interests of the whole project.

An Organization Member must meet the responsibilities and has the requirements of a Contributor, plus:

- Responsibilities include:
  - Continues to contribute regularly, as demonstrated by having at least [TODO: Number] [TODO: Metric] a year, as demonstrated by [TODO: contributor metrics source]. <!-- Example: "as demonstrated by having at least 50 GitHub contributions per year, as shown by Devstats"-->
- Requirements:
  - Must have successful contributions to the project, including at least one of the following:
    - [TODO: Number] accepted PRs,
    - Reviewed [TODO: Number] PRs,
    - Resolved and closed [TODO: Number] Issues,
    - Become responsible for a key project management area,
    - Or some equivalent combination or contribution
  - Must have been contributing for at least [TODO: Number] months
  - Must be actively contributing to at least one project area
  - Must have two sponsors who are also Organization Members, at least one of whom does not work for the same employer
  - Must enabling 2FA on their GitHub account

- Privileges:
  - May be assigned Issues and Reviews
  - May give commands to CI/CD automation
  - Entitled to vote in elections
  - Can be added to Notary Project teams
  - Can recommend other contributors to become Org Members

The process for a Contributor to become an Organization Member is as follows:

1. The member contributor is nominated by a sponsor, by opening an issue in the appropriate repository.
2. The second sponsor from a different employer seconds the nomination in the issue.
3. The nomination is reviewed publicly in a community meeting. All members vote for the nomination. A majority is required in order to approve the nomination.
4. Publicly announce the result in the issue, and in the [slack channel](https://app.slack.com/client/T08PSQ7BQ/CQUH8U287/).

### Org Maintainer

Description: Org Maintainers are very established contributors who are responsible for the entire project. As such, they have the ability to approve PRs against any area of the project, and are expected to participate in making decisions about the strategy and priorities of the project.

A Maintainer must meet the responsibilities and requirements of a Organization Member, plus:

- Responsibilities include:
  - Reviewing at least [TODO: Number] PRs per year, especially PRs that involve multiple parts of the project
  - Mentoring new members
  - Writing refactoring PRs
  - Participating in CNCF maintainer activities
  - Determining strategy and policy for the project
  - Participating in, and leading, community meetings
- Requirements
  - Experience as a org member for at least [TODO: Number] months
  - Demonstrates a broad knowledge of the project across multiple areas
  - Is able to exercise judgment for the good of the project, independent of their employer, friends, or team
  - Mentors other contributors
  - Can commit to spending at least [TODO: Number] hours per month working on the project
- Additional privileges:
  - Approve PRs to any area of the project
  - Represent the project in public as a Maintainer
  - Communicate with the CNCF on behalf of the project
  - Have a vote in Maintainer decision-making meetings

Process of becoming a maintainer:

1. Any current Maintainer may nominate a current Organization Member to become a new Maintainer, by opening a PR against the root of the [TODO: main repository name] adding the nominee as an Approver in the OWNERS file.
2. The nominee will add a comment to the PR testifying that they agree to all requirements of becoming a Maintainer.
3. A majority of the current Maintainers must then approve the PR.

## Subproject Maintainer

Description: Subproject Maintainers wwn a distinct subproject or repository of the main project. Responsible for everything there.

A Subproject Maintainer must meet the responsibilities and requirements of a Organization Member, plus:

- Responsibilities include:
  - Reviewing at least [TODO: Number] PRs per year of the subproject
  - Writing refactoring PRs
  - Determining strategy and policy for the subproject
  - Participating in, and leading, community meetings
- Requirements
  - Experience as a Org member for at least [TODO: Number] months
  - Demonstrates a broad knowledge of the subproject
  - Is able to exercise judgment for the good of the subproject, independent of their employer, friends, or team
  - Mentors other contributors
  - Can commit to spending at least [TODO: Number] hours per month working on the subproject
- Additional privileges:
  - Approve PRs of the subproject
  - Represent the subproject in public as a Maintainer
  - Communicate with the CNCF on behalf of the subproject
  - Have a vote in Maintainer decision-making meetings

Process of becoming a subproject Maintainer:

1. Any current Maintainer or subproject Maintainer may nominate a current Organization Member to become a new subproject Maintainer, by opening a PR against the root of the subproject adding the nominee as an Approver in the OWNERS file.
2. The nominee will add a comment to the PR testifying that they agree to all requirements of becoming a subproject Maintainer.
3. At least one of the current org maintainers, and a majority of the current subproject maintainers must then approve the PR.

## Inactivity

It is important for contributors to be and stay active to set an example and show commitment to the project. Inactivity is harmful to the project as it may lead to unexpected delays, contributor attrition, and a lost of trust in the project.

- Inactivity is measured by:
  - Periods of no contributions for longer than [TODO: Number] months
  - Periods of no communication for longer than [TODO: Number] months
- Consequences of being inactive include:
  - Involuntary removal or demotion
  - Being asked to move to Emeritus status

## Involuntary Removal or Demotion

Involuntary removal/demotion of a contributor happens when responsibilities and requirements aren't being met. This may include repeated patterns of inactivity, extended period of inactivity, a period of failing to meet the requirements of your role, and/or a violation of the Code of Conduct. This process is important because it protects the community and its deliverables while also opens up opportunities for new contributors to step in.

Involuntary removal or demotion is handled through a vote by a majority of the current Maintainers.

## Stepping Down/Emeritus Process

If and when contributors' commitment levels change, contributors can consider stepping down (moving down the contributor ladder) vs moving to emeritus status (completely stepping away from the project).

Contact the Maintainers about changing to Emeritus status, or reducing your contributor level.

## Contact

- For inquiries, please reach out to [Notary Project Governance Maintainers](mailto:)

## Reference

- [Contributor Ladder Template](https://github.com/cncf/project-template/blob/main/CONTRIBUTOR_LADDER.md)
