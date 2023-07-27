# Notary Project Overview

The Notary Project is a set of specifications and tools intended to provide a cross-industry standard for securing software supply chains by using authentic Container Images and other OCI artifacts. Notation Project specification and tooling provides signing and verification workflows for OCI artifacts, signature portability across OCI compliant registries, and integration with 3rd party key management solutions through a plugin model.

The Notary Project started with an implementation for signing images in container registries and ensuring their integrity before deployment. The initial implementation uses [The Update Framework (TUF)](https://github.com/theupdateframework) and requires registries to host additional server infrastructure for managing signing keys and image metadata. This server infrastructure tightly integrates with the container registry and keeps track of the images pushed to the registry. It has a client component in the form of the `notary` command line interface (CLI) that can be used by developers or CI/CD pipelines to sign and push container images and update the metadata. The CLI wraps the communication to the registry as well as to the key and metadata management server component. The most prominent use of this implementation is in Docker Content Trust (DCT). The server and the client implementation can be found in the [notary](https://github.com/notaryproject/notary) repository under the Notary Project organization.

Container images are portable artifacts that can move between registries. Due to the tight integration between the registry, key, and metadata management server component, portability of signatures and therefore images between registries is limited. Container registry APIs have begun standardizing on the [Open Containers Initiative (OCI)](https://github.com/opencontainers) and with new capabilities are added. To overcome the portability challenges and enable future flexibility and standardization, the Notary Project community decided to concentrate on specifications for helping enhance the software supply chains and provide reference implementations.

The first specification from the Notary Project is the [signature specification](https://github.com/notaryproject/notaryproject/blob/main/specs/signature-specification.md) that specifies how portable signatures wrapped in [COSE](https://github.com/notaryproject/notaryproject/blob/main/specs/signature-envelope-cose.md) or [JWS](https://github.com/notaryproject/notaryproject/blob/main/specs/signature-envelope-jws.md) envelopes can be produced. The specification defines the [signing and verification workflow](https://github.com/notaryproject/notaryproject/blob/main/specs/signing-and-verification-workflow.md) (aka _Notary Project signing and verification_), the [signing scheme](https://github.com/notaryproject/notaryproject/blob/main/specs/signing-scheme.md), the signature format and how to wrap the signature using COSE or JWS envelopes. A signature, also called a _Notary Project signature_, produced according to the Notary Project signature specification can be copied between OCI registries and validated in connected, occasionally connected, and disconnected environments without the need of additional server insfrastructure. The signature specification is available in the [notaryproject](https://github.com/notaryproject/notaryproject/tree/main/specs) repository under the Notary Project.

The [notaryproject](https://github.com/notaryproject/notaryproject/) repository also contains information about the [requirements and scenarios](https://github.com/notaryproject/notaryproject/tree/main/requirements) that the Notary Project supports or plans to support as well as the [reports from security testing and audits](https://github.com/notaryproject/notaryproject/tree/main/security).

A reference implementation to produce and verify Notary Project signatures in Golang is provided in the [`notation-core-go`](https://github.com/notaryproject/notation-core-go) library. A convenience Golang library that interacts with OCI registries and manages the relation between a signed artifact and signatures is provided in the [`notation-go`](https://github.com/notaryproject/notation-go) library. `notation-go` provides an easy way to implement the signing and verification in Golang. The `notation-go` library is also used by the [`notation` CLI](https://github.com/notaryproject/notation) that can be used by developers and CI/CD pipelines to produce portable signatures and store them together with the signed artifacts in OCI-compliant registries. The `notation` CLI implements Notary Project specifications for signing and verification, and can also be used to verify signatures of artifacts stored in OCI-compliant registries.

You can learn more about the Notary Project on the [notaryproject.dev](https://notaryproject.dev) website. 

## Repositories

Here is a list of repositories under the Notary Project organization

| Repository | Description |
| ----- | -----|
| [.github](https://github.com/notaryproject/.github) | This repository contains the Notary Project governance and other common documents that are shared across all repositories under the Notary Project organization. |
| [meeting-notes](https://github.com/notaryproject/meeting-notes) | This repository contains the archived meeting notes. |
| [notary](https://github.com/notaryproject/notary) | This repository contains the source code for the server and the client of the TUF-based implementation circa 2016. |
| [notaryproject](https://github.com/notaryproject/notaryproject) | This repository contains the Notary Project requirements, scenarios,  specifications, and security audits to overcome the challenges from the initial implementation of 2016. |
| [notaryproject.dev](https://github.com/notaryproject/notaryproject.dev) | This repository contains the source code and content for the [Notary Project website](https://notaryproject.dev). | 
| [notation](https://github.com/notaryproject/notation) | This repository contains the source code for the convenient CLI implementation of the new Notary Project signing and verification flow. |
| [notation-go](https://github.com/notaryproject/notation-go) | This repository contains the source code for the convenient Golang library implementation of the Notary signing and verification flow. |
| [notation-core-go](https://github.com/notaryproject/notation-core-go) | This repository contains the source code for the Golang library implementation of the Notary Project signature (hereafter "Notary Project signature")  specification and wrapping (COSE and JWS). |
| [roadmap](https://github.com/notaryproject/roadmap) | This repository is intended for keeping track of development activities in the Notary Project. It may be retired in the future as feature request and milestones are moved to the appropriate repositories. |
| [tuf](https://github.com/notaryproject/tuf) | This repository is intended for prototyping the storage of TUF metadata in OCI-compliant registries. It is not under active development at the moment but there are plans to revive it in the future. |

## Project Status

The Notary Project is in active development. The latest release announcements are published on the [Notary Project blog](https://notaryproject.dev/blog/). The Notary community uses the [project board](https://github.com/orgs/notaryproject/projects/10) for project planning and status tracking. You can also use GitHub milestones to track the progress of each repository:

- [The Notary Project specification milestones](https://github.com/notaryproject/notaryproject/milestones)
- [notation CLI milestones](https://github.com/notaryproject/notation/milestones)
- [notation-go library milestones](https://github.com/notaryproject/notation-go/milestones)
- [notation-core-go library milestones](https://github.com/notaryproject/notation-core-go/milestones)
- [notary milestones](https://github.com/notaryproject/notary/milestones)

You can also check the release pages of each repository for the latest release binaries:

- [The Notary Project specification releases](https://github.com/notaryproject/notaryproject/releases)
- [notation CLI releases](https://github.com/notaryproject/notation/releases)
- [notation-go library releases](https://github.com/notaryproject/notation-go/releases)
- [notation-core-go library releases](https://github.com/notaryproject/notation-core-go/releases)
- [notary releases](https://github.com/notaryproject/notary/releases)

## Security

The Notary Project has had several public security audits:

- [July 31, 2015 by NCC](https://github.com/notaryproject/notary/blob/master/docs/resources/ncc_docker_notary_audit_2015_07_31.pdf) covering `notary` repository.
- [August 7, 2018 by Cure53](https://github.com/notaryproject/notary/blob/master/docs/resources/cure53_tuf_notary_audit_2018_08_07.pdf)) covering TUF and the `notary` repository.
- [Mar 21, 2023 by ADA Logics](https://github.com/notaryproject/notaryproject/blob/main/security/reports/fuzzing/ADA-fuzzing-audit-22-23.pdf) fuzz testing audit covering `notary`, `notation-go`, and `notation-core-go` repositories.
- [Jul 7, 2023 by ADA Logics](https://github.com/notaryproject/notaryproject/blob/main/security/reports/audit/ADA-notation-security-audit-23.pdf) security audit covering `notation`, `notation-go`, and `notation-core-go` repositories.

The Notary Project has a continuous fuzz testing implemented for the following repositories: `notary`, `notation-go`, and `notation-core-go`.

## Community

You can reach the Notary Project community and developers via the following channels:

- Join the [Notary Project Slack channel](https://app.slack.com/client/T08PSQ7BQ/CQUH8U287/) for discussions and to ask questions.
- Follow the [@NotaryProject](https://mobile.twitter.com/NotaryProject) for news about the Notary Project.
- Join the [Notary Project community meetings](https://notaryproject.dev/community/#community-meetings) to stay on top of the latest discussions and development activities.
  - Active meeting notes are captured at the [Notary Project meeting notes](https://hackmd.io/_vrqBGAOSUC_VWvFzWruZw?view)
  - Archived meeting notes are stored in the [meeting-notes repository](https://github.com/notaryproject/meeting-notes)