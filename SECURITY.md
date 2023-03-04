# Notation Security Process and Policy
This document provides the details on the Notation security policy and details the process surrounding security handling including a how to report a security vulnerability for anything within the Notary Project organization. 

* [Reporting a Vulnerability](#reporting-a-vulnerability)
    * [When To Send a Report](#when-to-send-a-report)
    * [When Not To Send a Report](#when-not-to-send-a-report)
    * [Security Vulnerability Response](#security-vulnerability-response)
    * [Public Disclosure](#public-disclosure)
* [Security Team Membership](#security-team-membership)
    * [Responsibilities](#responsibilities)
    * [Membership](#membership)
* [Patch And Release Team](#patch-and-release-team)
    * [Supported Versions](#supported-version)
* [Credits](#credits)

## Reporting a Vulnerability

We're extremely grateful for security researchers and users who report vulnerabilities to the Notation community. All reports are thouroughly investigated by a set of Notation maintainers.

To make a report plese use the GitHub Security Vulnerability Disclosure process for each one of the Notation repositories. Here are the links to report vulnerabilities for each repository:

- [Notation CLI Vulnerability Report](https://github.com/notaryproject/notation/security/advisories/new)
- [Notation-Go Library Vulnerability Report](https://github.com/notaryproject/notation-go/security/advisories/new)
- [Notation-Core-Go Library Vulnerability Report](https://github.com/notaryproject/notation-go/security/advisories/new)
- [Notation Spcecification Vulnerability Report](https://github.com/notaryproject/notaryproject/security/advisories/new)

### When To Send a Report
You think you have found a vulnerability in any of the Notation sub-projects or a dependency of the Notation sub-projects. 

### What To Include In a Report
The more details are included in the report, the easier will be for the maintainers to understand the vulnerability and provide mitigations. Our vulnerability disclosure template requires the following information:
- Short summary of the problem
    This should be a single sentence that clearly summarize the vulnerability.
- Detailed description of the vulnerability
    Provide all possible details about the vulnerability. Versions of binaries, pointing to incriminated source code, environment details etc. are essential to understand the vulnerability and its impact.
- Proof of Concept (PoC) steps
    Detailed steps to reproduce the vulnerabilitt. This should include CLI commands, specific configuration details, library calls, etc.
- Impact
    Describe the impact of the vulnerability and who the impacted audience is.
    
Feel free to include anything else that you deem relevant for better understanding of the vulnerability.

### When Not To Send a Report
- If a vulnerability has been found in an application that uses Notation or the Notation binaries. Instead, contact the maintaners of the respective application.
- For guidance on securing Notation, please see the [documentation](https://notaryproject.dev/docs/) or ask on the [Slack channel](https://cloud-native.slack.com/archives/CQUH8U287).
- You are looking for help applying security updates.

### Security Vulnerability Response
Each report will be reviewed and receipt acknowledged within 3 business days. This will set off the security review process detailed below.

Any vulnerability information shared with the security team stays within the Notary Project and will not be shared with others unless it is necessary to fix the issue. Information is shared only on a need to know basis.

We ask that vulnerability reporter(s) act in good faith by not disclosing the issue to others. And we strive to act in good faith by acting swiftly, and by justly crediting the vulnerability reporter(s) in writing.

As the security issue moves through triage, identification, and release the reporter of the security vulnerability will be notified. Additional questions about the vulnerability may also be asked of the reporter.

### Public Disclosure
A public disclosure of security vulnerabilities is released alongside release updates or details that fix the vulnerability. We try to fully disclose vulnerabilities once a mitigation strategy is available. Our goal is to perform a release and public disclosure quickly and in a timetable that works well for users. For example, a release may be ready on a Friday but for the sake of users may be delayed to a Monday.

CVEs will be assigned to vulnerabilities. Due to the process and time it takes to obtain a CVE ID, disclosures will happen first. Once the disclosure is public the process will begin to obtain a CVE ID. Once the ID has been assigned the disclosure will be updated.

If the vulnerability reporter would like their name and details shared as part of the disclosure process we are happy to. We will ask permission and for the way the reporter would like to be identified. We appreciate vulnerability reports and would like to credit reporters if they would like the credit.

Vulnerability disclosures are published in the Security Advisories sections in each repository. The disclosures will contain an overview, details about the vulnerability, a fix for the vulnerability that will typically be an update, and optionally a workaround if one is available.

Disclosures will be published on the same day as a release fixing the vulnerability after the release is published.

Here are the links to security advisories for each repository:

- [Notation CLI Security Advisories](https://github.com/notaryproject/notation/security/advisories)
- [Notation-Go Library Security Advisories](https://github.com/notaryproject/notation-go/security/advisories)
- [Notation-Core-Go Library Security Advisories](https://github.com/notaryproject/notation-go/security/advisories)
- [Notation Spcecification Security Advisories](https://github.com/notaryproject/notaryproject/security/advisories)

## Security Team Membership
The security team is made up of a subset of the Notation project maintainers who are willing and able to respond to vulnerability reports.

### Responsibilities
- Members MUST be active project maintainers on active (non-deprecated) Notation projects as defined in the governance
- Members SHOULD engage in each reported vulnerability, at a minimum to make sure it is being handled
- Members MUST keep the vulnerability details private and only share on a need to know basis

### Membership
New members are required to be active maintainers of Notation projects who are willing to perform the responsibilities outlined above. The security team is a subset of the maintainers. Members can step down at any time and may join at any time.

From time to time, Notation projects are deprecated. If at any time a security team member is found to be no longer be an active maintainer on active Notation projects, this individual will be removed from the security team.

## Patch and Release Team
When a vulnerability comes in and is acknowledged, a team - including maintainers of the Notation project affected - will be assembled to patch the vulnerability, release an update, and publish the vulnerability disclosure. This may expand beyond the security team as needed but will stay within the pool of Notation project maintainers.

## Credits
We would like to give credit to the [Helm Community](https://github.com/helm/community) for using their security process and policy as an example.