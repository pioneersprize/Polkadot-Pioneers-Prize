# Performance Improvments for Reed Solomon Erasure Coding

> Don't remove any of the mandatory parts presented in bold letters or as headlines (except for the title)! Lines starting with a `>` (such as this one) should be removed. 
>
> See the [Process](https://github.com/pioneersprize/Guidelines#7-process) on how to submit a proposal.
- **Team Name:** konifay
- **Payment Address:** 1st63Adu7W4cB268CvKHfMwq5rJQkzTitBnWsvGrAx83iiT

> :exclamation: *The combination of your GitHub account submitting the application and the payment address above will be your unique identifier during the program. Please keep them safe.*
## Project Overview :page_facing_up:

### Overview

Please provide the following:

- If the name of your project is not descriptive, a tagline (one sentence summary).
- A brief description of your project.
- An indication of how your project relates to / integrates into Polkadot.
- An indication of why your team is interested in creating this project.

Improve reed solomon erasure coding used in polkadot to reduce the static overhead the current implementation.



### Project Details

We expect the teams to already have a solid idea about your project's expected final state. Therefore, we ask the teams to submit (where relevant):

* introduce SMID instructions to the current implementation to improve performance for 1000+ validators
* implement a different algorithm that reduces the static table computation overhead for up to 1000 validators

The project is only concerned with the performance aspects of reed solomon erasure coding, nothing more, nothing less.

The API used by polkadot will not change, the side effects of breaking changes of internal behavior is not part of this.

### Ecosystem Fit

- Where and how does your project fit into the ecosystem? It's already there, let's make it better to scale polkadot
- What need(s) does your project meet? Polkadot short term scalability, reducing CPU use

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

- https://github.com/drahnr


### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/in/bernhardschuster

## Development Roadmap :nut_and_bolt:

1. do performance measurements baseline
2. setup decommissioned CI infra again
3. add SMID to the current implementation
4. implement a alternate version
5. measure and tune the alternate
6. determine a threshold, where which one is more performant
7. implement a dynamic switch over

> :exclamation: If any of your deliverables is based on somebody else's work, make sure you work and publish _under the terms of the license_ of the respective project and that you **highlight this fact in your milestone documentation** and in the source code if applicable! 

### Overview

- **Total Estimated Duration:** 3 months
- **Full-Time Equivalent (FTE):** 4 FTE
- **Total Costs:** 26,400 EUR

Note that this is a discounted rate and shall not be assumed for further enquiries, since I actually would like to get this done.

### Milestone 1 - Improve current

- **Estimated duration:** 1 month
- **FTE:**  2
- **Costs:** 13,200 EUR

> :exclamation: **The default deliverables 0a-0d below are mandatory for all milestones**, and deliverable 0e at least for the last one. 

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 / MIT |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and an outline |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. |
| 0e. | Article | We will publish an **article** that explains the gains and measurements (what was done/achieved as part of the grant). (Content, language and medium should reflect your target audience described above.) |
| 1. | SMID perf | Implement SMID |
| 2. | Measurement CI | Recover the measurement CI infra |


### Milestone 2 — Implement an alternate algorithm

- **Estimated Duration:** 2 month
- **FTE:**  2
- **Costs:** 13,200 EUR

> :exclamation: **The default deliverables 0a-0d below are mandatory for all milestones**, and deliverable 0e at least for the last one. 

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

No plans, unless further optimization is required to bridge to a full zk based approach.

## Additional Information :heavy_plus_sign:

As stated, I did the initial impl. and I do have sufficient experience both with the theoretical background and the concrete implementation to get it done.