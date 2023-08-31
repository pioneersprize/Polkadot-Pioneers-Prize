# ZKP's in decentralised reputation systems 

- **Team Name:** UNIVERSALDOT
- **Payment Address:** 1ZKQxXJC4731Qq7EHNAddaQRdV37qLYMftbE9PN1T9hu2sU

## Project Overview :page_facing_up:

### Overview


UniversalDot is a decentralized freelancing application that revolutionizes the way freelancers and clients interact. By leveraging blockchain technology, UniversalDot eliminates the need for intermediaries, ensuring direct and secure transactions between parties. By using ZKP's Universaldot is building transparent reputation system and fair dispute resolution mechanism fostering a global community of freelancers and clients who can collaborate seamlessly and autonomously.

#### Brief Description

UniversalDot is an innovative decentralized freelancing application built on the Substrate framework. The platform aims to disrupt the traditional freelancing industry by offering a transparent, secure, and efficient ecosystem for freelancers and clients worldwide.

By leveraging Substrate's modular architecture, UniversalDot brings together a set of custom pallets specifically designed to meet the needs of freelancers. These pallets enable features such as identity verification, reputation management, dispute resolution, and secure payment systems, ensuring a seamless and trustworthy experience for all participants.

With UniversalDot, freelancers can create their profiles, showcase their skills, and offer their services directly to clients without intermediaries. Clients, on the other hand, gain access to a global talent pool and can easily find the right freelancers for their projects based on reputation and expertise.

The decentralized nature of UniversalDot ensures that no single entity has control over the platform, promoting fairness, and autonomy. Through the use of blockchain technology, all transactions and interactions are recorded immutably, enhancing transparency and accountability.

UniversalDot aims to create a vibrant freelancing community by facilitating direct peer-to-peer collaboration, reducing fees, and allowing freelancers to retain a higher percentage of their earnings. It also encourages the growth of decentralized governance, enabling platform participants to actively participate in decision-making processes.

We have been building this application for the past 3 years and have been recipients of grants from WEB3 Foundation and Filecoin Foundation. 

### Project Details

The project has been in development for the past 3 years. One of the missing components is establishing zero-knowledge (ZKPs) proof of reputation between freelancers and clients. The freelancers should be able to prove to clients their reputation without revealing their identity, while the clients should be able to provide proof of funds without revealing their identity as well. This essential component of the application has not yet been developed yet, and it is for this reason that we are seeking your support. 

In UniversalDot, ZKPs will play a pivotal role in the verification of key credentials without compromising privacy. Freelancers can maintain their sensitive information, such as educational qualifications or certifications, privately while providing cryptographic proof of their validity. Similarly, clients can validate their project requirements or payment capabilities without disclosing confidential details. This mutual verification process is a breakthrough for establishing initial trust between parties, as both sides can confidently engage without revealing unnecessary personal data.

UniversalDot can utilize ZKPs to cryptographically attest to a freelancer's positive track record without exposing specific project details or client identities. This ensures that freelancers can showcase their capabilities while safeguarding sensitive client data, fostering a more secure environment for all involved. Moreover, ZKPs enhance dispute resolution mechanisms by enabling verifiable claims without revealing private information. In case of conflicts, ZKPs can validate specific aspects of a project or transaction without requiring complete disclosure, streamlining the resolution process and maintaining confidentiality.

By integrating zero-knowledge proofs into the UniversalDot application, we can elevate user confidence, enhance privacy, and ultimately create a system where trust is built upon cryptographic verification rather than the exposure of personal data. This not only aligns with the platform's core values of transparency and security but also positions UniversalDot as a pioneer in harnessing cutting-edge technology for the betterment of freelancers and clients worldwide.


#### Documentation

- [Solution Architecture](https://drive.google.com/file/d/13C9IRIX49AjfZEB-MI9dXG3gX-cdTgBp/view?usp=sharing)
- [Software Requirements Document](https://drive.google.com/file/d/1HvYvb7N1A9uT_9UhrAq1mV38RtjyfVv-/view?usp=sharing)
- [IPFS Design Document](https://drive.google.com/file/d/1ov7jfAPMTuotbHRwTMIRvLKomt1c1e3f/view?usp=sharing)
- [Personalized Recommendation System Architecture](https://drive.google.com/file/d/1rscD1VDG8EkaGTh9M7BUa3u7nRoBgcwJ/view?usp=sharing)



##### Architecture Diagram

![Architecture](https://raw.githubusercontent.com/UniversalDot/documents/master/designs/architecture/3Tier_Architecturev3.png)


### Ecosystem Fit


- Where and how does your project fit into the ecosystem?
  We intend to become a Polkadot parachain.
- Who is your target audience (parachain/dapp/wallet/UI developers, designers, your own user base, some dapp's userbase, yourself)?
  Freelancers and people offering remote work.
- What need(s) does your project meet?
  Ability to find/seek work.
- Are there any other projects similar to yours in the Substrate / Polkadot / Kusama ecosystem?
  Gitcoin.
  - If so, how is your project different?
  Work is offered to freelancers based on individual profile.

## Team :busts_in_silhouette:

### Team members

- Name of team leader: Igor Stojanov
- Names of team members: Freelancers hired on demand

### Contact

- **Contact Name:** Igor Stojanov
- **Contact Email:** igor.stojanov@universaldot.foundation
- **Website:** [universaldot.foundation](https://universaldot.foundation/)

### Legal Structure

- **Registered Address:** Harju maakond, Tallinn, Kesklinna linnaosa, Ahtri tn 12, 15551
- **Registered Legal Entity:** [UNIVERSALDOT OÜ](https://ariregister.rik.ee/eng/company/16716249/UNIVERSALDOT-O%C3%9C)

### Team's experience

Please describe the team's relevant experience. If your project involves development work, we would appreciate it if you singled out a few interesting projects or contributions made by team members in the past. 

### Team Code Repos

- https://github.com/UniversalDot
- https://github.com/UniversalDot/front-end
- https://github.com/UniversalDot/universal-dot-node
- https://github.com/UniversalDot/compose-service
- https://github.com/UniversalDot/ansible

Please also provide the GitHub accounts of all team members. If they contain no activity, references to projects hosted elsewhere or live are also fine.

- https://github.com/stojanov-igor


### Team LinkedIn Profiles (if available)

- https://www.linkedin.com/in/igor-stojanov-96364ba/


## Development Status :open_book:

- [Mock-up](https://github.com/UniversalDot/documents/blob/master/designs/documents/DAODesign2.pdf)

- [Landing Page](https://universaldot.me)
- [MVP](https://app.universaldot.me)
- [App Docs](https://docs.universaldot.me)

Implemented pallets:
- [Profile](https://github.com/UniversalDot/universal-dot-node/blob/universal-develop/pallets/profile/src/lib.rs)
- [Task](https://github.com/UniversalDot/universal-dot-node/blob/universal-develop/pallets/task/src/lib.rs)
- [DAO](https://github.com/UniversalDot/universal-dot-node/blob/universal-develop/pallets/dao/src/lib.rs)

Pallet Demonstration through a React Front-end
- [Profile](https://www.youtube.com/watch?v=Gaoo6LoZydg)
- [Task](https://www.youtube.com/watch?v=ssTMk1nGbk8)
- [DAO](https://www.youtube.com/watch?v=K9-v016fGVs)

## Development Roadmap :nut_and_bolt:

This section should break the development roadmap down into milestones and deliverables. It helps to describe _the functionality we should expect in as much detail as possible_, plus how we can verify and test that functionality. 


### Overview

- **Total Estimated Duration:** 3 months
- **Full-Time Equivalent (FTE):**  2.25 FTE
- **Total Costs:**  8,000 DOT (approximately 35,000 USD)  

### Milestone 1 - Research and Design

- **Estimated duration:** 1.5 months
- **FTE:**  2
- **Costs:** 4,000 DOT


| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0  |
| **0b.** | Documentation | We will provide **sufficient documentation** of the code and a basic **tutorial** that explains how a user can use the solution. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article**/workshop that explains  (what was done/achieved as part of the grant). (Content, language and medium should reflect your target audience described above.) |
| 1. | ZKP Design Document | We will create a document that outlines how to ZKP solution integrates within the existing solution. |
| 2. | ZKP Rust implementation| An example implementation of Zero knowledge proof implemented in Rust |
| 3. | Unit tests| Unit test that test the implemented functionality |


### Milestone 2 - Integration 

- **Estimated Duration:** 1.5 months
- **FTE:**  2.5
- **Costs:** 4,000 DOT

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| **0a.** | License | Apache 2.0  |
| **0b.** | Documentation | We will provide **sufficient documentation** of the code and a basic **tutorial** that explains how a user can use the solution. |
| **0c.** | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. In the guide, we will describe how to run these tests. |
| **0d.** | Docker | We will provide a Dockerfile(s) that can be used to test all the functionality delivered with this milestone. |
| 0e. | Article | We will publish an **article**/workshop that explains  (what was done/achieved as part of the grant). (Content, language and medium should reflect your target audience described above.) |
| 1. | ZKP Pallet integration | We will integrate the previously implemented ZKP witt existing pallets |
| 2. | Unit tests | We will add unit tests that test the new functionality |
| 3. | Benchmarking |  Added benchmarks for new extrinsic functions |


## Future Plans

We intend to continue building the application through support of the ecosystem and existing community.

## Additional Information :heavy_plus_sign:

Here you can also add any additional information that you think is relevant to this application but isn't part of it already, such as:

- We have already completed 80% of the development for the application. 
- The Filecoin foundation and WEB3 Foundation have already financially contributed toward building this application. 
