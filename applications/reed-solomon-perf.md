# Performance Improvments for Reed Solomon Erasure Coding

- **Team Name:** konifay
- **Payment Address:** 1st63Adu7W4cB268CvKHfMwq5rJQkzTitBnWsvGrAx83iiT

## Project Overview :page_facing_up:

### Overview

Improve reed solomon erasure coding used in polkadot to reduce the static overhead the current implementation has regardless of the number of shards required.

### Project Details

- introduce SIMD instructions to the current implementation to improve performance for 1000+ validators
- implement a different algorithm that reduces the static table computation overhead for up to 1000 validators

The project is only concerned with the performance aspects of reed solomon erasure coding, nothing more, nothing less.

The API used by polkadot will not change, the side effects of breaking changes of internal behavior is not part of this work package.

### Ecosystem Fit

- Reed solomon erasure coding is used in the current polkadot implementation, let's make it better, to scale polkadot further
- Short term scalability, reducing CPU load and leaving more for network package processing

## Team :busts_in_silhouette:

### Team members

- @drahnr

### Contact

- **Contact Name:** Bernhard Schuster
- **Contact Email:** w3f-ppp@konifay.io
- **Website:** https://konifay.io

### Legal Structure

- **Registered Address:** 91186 Kühedorf, Heidenbergstr. 20
- **Registered Legal Entity:** konifay (Inhaber Bernhard Schuster)

### Team's experience

I am a former parity employee, and did the initial implementation of the reed solomon erasure coding,
as well as performance measurments and the now decomissioned infrastructure automation for automated perf
around it.

### Team Code Repos

- <https://github.com/drahnr>

### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/in/bernhardschuster

## Development Roadmap :nut_and_bolt:

1. do performance measurements baseline
2. setup decommissioned CI infra again
3. add SIMD to the current implementation
4. implement a alternate version
5. measure and tune the alternate
6. determine a threshold, where which one is more performant
7. implement a dynamic switch over

All code implemented will be `rust` 🦀

### Overview

- **Total Estimated Duration:** 3 months
- **Full-Time Equivalent (FTE):** 4 FTE
- **Total Costs:** 32,680 EUR

Note that this is a discounted rate and shall not be assumed for further enquiries, since I actually would like to get this done.

### Milestone 1 - Improve current

- **Estimated duration:** 1 month
- **FTE:**  1
- **Costs:** 10,560 EUR

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 / MIT |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and an outline |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. |
| 1. | SIMD perf | Implement SIMD |
| 2. | Measurement CI | Recover the measurement CI infra |

### Milestone 2 — Implement an alternate algorithm

- **Estimated Duration:** 2 months
- **FTE:**  2.66
- **Costs:** 22,120 EUR

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 / MIT |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and an outline |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. |
| 0e. | Article | We will publish an **article** that explains the approach (what was done/achieved as part of the grant). (Content, language and medium should reflect your target audience described above.) |
| 1. | Alternative Algorithm | Implement Gao Mateer Algorithm |
| 2. | Perf | Tune the algorithm for performance |
| 3. | Compare | Find the threshold where one or the other is better |

## Future Plans

No plans, unless further optimization is required to bridge to a full zk-based approach.

## Additional Information :heavy_plus_sign:

As stated, I did the initial impl. and I do have sufficient experience both with the theoretical background and the concrete implementation to get it done.
