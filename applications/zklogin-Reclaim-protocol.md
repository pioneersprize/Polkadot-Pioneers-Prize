# Implementing zklogin and Proof of Personhood through Reclaim Protocol


- **Team Name:** Questbook International Inc
- **Payment Address:** 16DFLp86GpYDFE4qooU3WT4f5b7DD6o7MfaxL2y4Di1JDGmy

## Project Overview :page_facing_up:

### Overview

### **Proposal Context and Problem Overview**

Currently, users are accustomed to logging into centralized login systems such as Google, Facebook, and Twitter to access these services, but they have no way to use this on-chain. These conventional login methods are incompatible with on-chain verifications, thus creating a disconnect between user identities on different centralized platforms and restricting their utility on-chain across Dapps.

Reclaim protocol will allow Dapps within the Polkadot ecosystem to provide zk login for its users. It will enable Dapp users to log into any website and generate a zkproof of their login that can be verified on chain. Reclaim Protocol makes https traffic verifiable using Zero-Knowledge Proofs, enabling users to generate verifiable credentials from any of their online user profiles. This unlocks unlimited possibilities as no APIs are required or no changes to be made to the websites to extract user private data, while guaranteeing data integrity. Web2 user data which was elusive to Web3 till now will be available to builders across the Polkadot ecosystem. This opens up opportunities for a new wave of applications that can support zklogin, proof of personhood  and bot protection. 

Additionally, after speaking with the members of the Polkadot Foundation, we have been able to identify zklogin and [epassport](https://github.com/w3f/Grants-Program/blob/master/docs/RFPs/epassport-zk-validation.md) to be an important use case for Dapp builders and users that be implemented uniquely through Reclaim Protocol. Through Reclaim, users can not only validate their login credentials but also provide verifiable proofs of various personal attributes and activities. For instance, they can prove the number of rides taken on Uber, expenditures on Amazon, or their scores on Chess.com, thereby establishing a robust proof of personhood which is instrumental in combating fraudulent actors and bots. Such proof of personhood can now be made available onchain via Reclaim protocol within the Polkadot ecosystem.

We are a small team (20+ members) with finite resources, and want to collaborate with ecosystems that demonstrate a genuine commitment to enable use cases that are likely to scale to a billion users. Our team comprises of primarily engineers who have previously worked at Meta, Microsoft, Google, and have contributed to various web3 open source projects. Given Polkadot's strong emphasis on streamlining user onboarding,  user experience, and implementing bot protection, coupled with our team's expertise and background, we believe that our team is one of the most suited to realise Polkadot's vision of building zk login and implementing Proof of Personhood for Dapps on top of Polkadot.

### Project Details

zk Login Overview


### Ecosystem Fit

Help us locate your project in the Polkadot/Substrate/Kusama landscape and what problems it tries to solve by answering each of these questions:

- Where and how does your project fit into the ecosystem?
- Who is your target audience (parachain/dapp/wallet/UI developers, designers, your own user base, some dapp's userbase, yourself)?
- What need(s) does your project meet?
- Are there any other projects similar to yours in the Substrate / Polkadot / Kusama ecosystem?
  - If so, how is your project different?
  - If not, are there similar projects in related ecosystems?

## Team :busts_in_silhouette:

### Team members

- Name of team leader
- Names of team members

### Contact

- **Contact Name:** Full name of the contact person in your team
- **Contact Email:** Contact email (e.g. john@duo.com)
- **Website:** Your website

### Legal Structure

- **Registered Address:** Address of your registered legal entity, if available. Please keep it in a single line. (e.g. High Street 1, London LK1 234, UK)
- **Registered Legal Entity:** Name of your registered legal entity, if available. (e.g. Duo Ltd.)

### Team's experience

Please describe the team's relevant experience. If your project involves development work, we would appreciate it if you singled out a few interesting projects or contributions made by team members in the past. 

### Team Code Repos

- https://github.com/<your_organisation>/<project_1>
- https://github.com/<your_organisation>/<project_2>

Please also provide the GitHub accounts of all team members. If they contain no activity, references to projects hosted elsewhere or live are also fine.

- https://github.com/<team_member_1>
- https://github.com/<team_member_2>

### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/<person_1>
- https://www.linkedin.com/<person_2>


## Development Status :open_book:

If you've already started implementing your project or it is part of a larger repository, please provide a link and a description of the code here. In any case, please provide some documentation on the research and other work you have conducted before applying. This could be:

- links to improvement proposals or [RFPs](https://github.com/w3f/Grants-Program/tree/master/docs/RFPs) (requests for proposal),
- academic publications relevant to the problem,
- links to your research diary, blog posts, articles, forum discussions or open GitHub issues,
- previous interface iterations, such as mock-ups and wireframes.

## Development Roadmap :nut_and_bolt:

This section should break the development roadmap down into milestones and deliverables. It helps to describe _the functionality we should expect in as much detail as possible_, plus how we can verify and test that functionality. 

> :exclamation: If any of your deliverables is based on somebody else's work, make sure you work and publish _under the terms of the license_ of the respective project and that you **highlight this fact in your milestone documentation** and in the source code if applicable! 

### Overview

- **Total Estimated Duration:** Duration of the whole project (e.g. 2 months)
- **Full-Time Equivalent (FTE):**  Average number of full-time employees working on the project throughout its duration (see [Wikipedia](https://en.wikipedia.org/wiki/Full-time_equivalent), e.g. 2 FTE)
- **Total Costs:** Requested amount in USD for the whole project (e.g. 12,000 USD). 

### Milestone 1 Example — Basic functionality

- **Estimated duration:** 1 month
- **FTE:**  1,5
- **Costs:** 8,000 USD

> :exclamation: **The default deliverables 0a-0d below are mandatory for all milestones**, and deliverable 0e at least for the last one. 

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0 / GPLv3 / MIT / Unlicense |
| **0b.** | Documentation | We will provide both **inline documentation** of the code and a basic **tutorial** that explains how a user can (for example) spin up one of our Substrate nodes and send test transactions, which will show how the new functionality works. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article**/workshop that explains [...] (what was done/achieved as part of the grant). (Content, language and medium should reflect your target audience described above.) |
| 1. | Substrate module: X | We will create a Substrate module that will... (Please list the functionality that will be implemented for the first milestone. You can refer to details provided in previous sections.) |
| 2. | Substrate module: Y | The Y Substrate module will... |
| 3. | Substrate module: Z | The Z Substrate module will... |
| 4. | Substrate chain | Modules X, Y & Z of our custom chain will interact in such a way... (Please describe the deliverable here as detailed as possible) |
| 5. | Library: ABC | We will deliver a JS library that will implement the functionality described under "ABC Library" |
| 6. | Smart contracts: ... | We will deliver a set of ink! smart contracts that will...


### Milestone 2 Example — Additional features

- **Estimated Duration:** 1 month
- **FTE:**  1,5
- **Costs:** 8,000 USD

...


## Future Plans

Please include here

- how you intend to use, enhance, promote and support your project in the short term, and
- the team's long-term plans and intentions in relation to it.

## Additional Information :heavy_plus_sign:

Here you can also add any additional information that you think is relevant to this application but isn't part of it already, such as:

- Work you have already done.
- If there are any other teams who have already contributed (financially) to the project.
