# Performance Improvments for Reed Solomon Erasure Coding

- **Team Name:** konifay
- **Payment Address:** 1st63Adu7W4cB268CvKHfMwq5rJQkzTitBnWsvGrAx83iiT

## Project Overview :page_facing_up:

### Overview

Refactor the codebase and add architecture level documentation, plus continued maintenance of the CI system, code review, merging PRs, and answer questions on a capacity limited basis.

### Project Details

- remove non-idiomatic constructs that make it hard to understand, particularly the `include!` based generation and conditional lookup table generation
- continue maintaining the crate for 12months, including answering questions, reviewing PRs and cutting releases in a semver compliant fashion.

The project is only concerned with the cleanup of the codebase and mainting it for the given time and helping users to understand the code via a matrix channel, nothing more, nothing less.

### Ecosystem Fit

- Reed solomon erasure coding is used in the current polkadot implementation, let's make it accessible by non-mathematicians and rust magicians.
- Maintainence for a critical part of the current polkadot implementation.

## Team :busts_in_silhouette:

### Team members

- @drahnr

### Contact

- **Contact Name:** Bernhard Schuster
- **Contact Email:** <w3f-ppp@konifay.io>
- **Website:** <https://konifay.io>

### Legal Structure

- **Registered Address:** 91186 Kühedorf, Heidenbergstr. 20
- **Registered Legal Entity:** konifay (Inhaber Bernhard Schuster)

### Team's experience

I am a former parity employee, and did the initial implementation of the reed solomon erasure coding,
as well as performance measurments and the now re-comissioned infrastructure automation for automated perf and CI.

### Team Code Repos

- <https://github.com/drahnr>

### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/in/bernhardschuster

## Development Roadmap :nut_and_bolt:

1. introduce semver compliance checks as part of a release CI pipeline
2. refactor the codebase to avoid `include!`-file based pseudo generic code generation and type extension
3. extract the table generation into a primitives crate to reach decoupling
4. answer questions around the implementation, architecture up to a total of 3h per month
5. maintain dependency updates, and do releases in a semver compliant fashion as needed

All code implemented will be `rust` 🦀

### Overview

- **Total Estimated Duration:** 27 months
- **Full-Time Equivalent (FTE):** 0.28 FTE
- **Total Costs:** 108,120

Note that this is a discounted rate and shall not be assumed for further enquiries, since I actually would like to see this crate flourish.

Note that this includes a long term commitment over 2 years of maintenence.

All calculations include a 20% margin for dot price volatility.

### Milestone 1 — Integrate semver-checks release process

- **Estimated Duration:** 3 months
- **FTE:**  0.5
- **Costs:** 31,800 EUR

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 / MIT |
| **0b.** | Documentation | We will be provided as part of the commit messages and the release change logs | 1. | PR review | Give reasonable and actionable
| 1. | CI release pipeline | Implement a semver compliant release process, includign changelog generation and publishing of the crate hirarchy |
| 2. | Documentation | Document the release process extensively |
| 3. | Refactor Codebase | Split into more crates, avoid antipatterns while maintaining research accessability. |
| 4. | Explain Session | Do code explanation sessions, up to 3h per month, async via matrix |

### Milestone 2 - Maintain crate and review PR 2024

- **Total Estimated Duration:** 12 months
- **Full-Time Equivalent (FTE):** 0.25 FTE
- **Total Costs:** 38,160 EUR

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 / MIT |
| **0b.** | Documentation | We will be provided as part of the commit messages and the release change logs | 1. | PR review | Give reasonable and actionable feedback, maintaining code quality and integrity of the crate |
| 2. | Releases | Do semver compliant releases on demand |
| 3. | Maintenence | Continue maintenence of the existing CI release pipeline |
| 4. | Explain Session | Do code explanation sessions, up to 3h per month, async via matrix |

### Milestone 3 - Maintain crate and review PR 2025

- **Total Estimated Duration:** 12 months
- **Full-Time Equivalent (FTE):** 0.25 FTE
- **Total Costs:** 38,160 EUR

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 / MIT |
| **0b.** | Documentation | We will provide both **** of the code and an outline |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. |
| 1. | PR review | Give reasonable and actionable feedback, maintaining code quality and integrity of the crate |
| 2. | Releases | Do semver compliant releases on demand |
| 3. | Maintenence | Continue maintenence of the existing CI release pipeline |
| 4. | Explain Session | Do code explanation sessions, up to 3h per month, async via matrix |

## Future Plans

Continue maintenence until the polkadot implementation moved on to a zk based approach and that is deployed on the polkadot network.

## Additional Information :heavy_plus_sign:

As stated, I did the initial impl. and I do have sufficient experience both with the theoretical background and the concrete implementation to get it done.
