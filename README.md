# Polkadot Pioneers Prize

<p align="center">
  <img src="static/pioneersprize.png" style="width:1300px" />
</p>

- [Introduction](#introduction)
- [Guidelines](#guidelines)
  - [General](#general)
  - [Categories](#categories)
- [Curator Team](#curator-team)
- [Processs](#process)

## Introduction
The Polkadot Pioneers Prize helps to propel technical innovation on the Polkadot network, as well as to model ways in which the community can achieve more agency and support in directing how on-chain treasury funds are spent. By offering an incentive prize program that funds research in targeted areas, we advance the state of not just the Polkadot network but blockchain as an alternative infrastructure to Web 2.0—ushering in Web 3.0.

As Polkadot matures as an Ecosystem, requirements for ongoing infrastructure development present a technical argument for a prize program, particularly in areas where bold innovation is possible. 
- The first category in which we observe a need for creative and directed action is the **utilization of zero-knowledge (“ZK”) proofs**, also known as ZK protocols. ZK cryptography ushers in a new way to protect users by bringing privacy to on-chain data, and so has a far-reaching impact, not just for Polkadot but for blockchain and Web 3.0 more broadly. The Web3 Foundation’s research team has begun looking into potential areas in which ZK technology shows the most potential to be applied on Polkadot, and this research will inform how the Pioneers Prize can support innovation in secure and private transactions on the Polkadot network.
- The second category we deem impactful is the further development of **Polkadot infrastructure**. Specifically, this prize offers attractive bounties to incentivize the implementation and delivery of alternative implementations of Polkadot nodes: full nodes, authoring nodes, and/or collator nodes. With this, we create a more resilient network and provide builders with more options to build and integrate with Polkadot in the languages they love. 

## Guidelines

### General 

Generally, your project will have better chances of being accepted if:
- It presents a well-researched or tested concept for which, ideally, you are able to show some prior work.
- You can demonstrate that the project will be maintained after the completion of the prize.
- Your team has proven experience with the relevant languages and technologies and/or a solid technical background. You will be asked to provide the GitHub profiles of your team members as part of your application, which we will examine for past activity and code quality. Naturally, you can also link to projects on other platforms.
- The team can provide documentation that reinforces registration, tax ID, and previous project experience.
- Your application is rich in technical details and well-defined.

Additionally, it must fulfill the following requirements:
- All code produced as part of a grant must be open-sourced, and it must also not rely on closed-source software for full functionality. 
- We do not award prizes for projects that have been the object of a token sale.
- Applications must not mention a specific token. Furthermore, the focus of the application should lie on the software that is being implemented/research being carried out as part of the grant and less on your project/venture/operation. For the purpose of the application and delivery, think about how others might also benefit from your work.
As a general rule, teams are asked to finish a grant before applying for another one.
- Lastly, we do not fund projects that actively encourage gambling, illicit trade, money laundering, or criminal activities in general.
- We require all projects to create documentation that explains how their project works. At a minimum, written documentation is required.

### Categories

- **Zero-Knowledge**: The first ambitious technical initiatives we are supporting are in the area of ZK innovation. ZK (Zero-Knowledge) Primitives in Substrate is a set of modules that provides the necessary tools for integrating privacy-preserving computations into the Substrate blockchain framework. These primitives are essentially the building blocks used to create applications that require zero-knowledge proofs, such as zk-SNARKs or zk-STARKs. They allow nodes to verify transactions without revealing specific information about the transaction, which is key for privacy-centric applications. Substrate, developed by Parity Technologies, is a modular framework that allows developers to build custom blockchains for their decentralized applications. By integrating ZK Primitives into this framework, developers can seamlessly incorporate high-level privacy functionalities into their blockchain solutions, offering users more secure and private transactions while maintaining the open and decentralized nature of blockchain systems.
These ZK Primitives include cryptographic functions, proof generation and verification algorithms, and various components related to the creation and validation of zero-knowledge proofs. Their implementation in Substrate takes advantage of Rust's safety and performance features, making the development of privacy-centric blockchains more efficient and reliable.
Examples of areas of interest in the ZK space can be found at https://hackmd.io/@rgbPIkIdTwSICPuAq67Jbw/S1rQ3-Iy2, in an article posted by Jeff Burdges (W3F Research Team) for the recent Berkeley Hackathon.

- **Infrastructure**: To build a light client for Polkadot, a candidate should possess a thorough understanding of the Polkadot network architecture, as well as the technical requirements for implementing a light client. Additionally, the candidate should have experience with programming languages and frameworks compatible with Polkadot, such as Rust or Java.
Specifically, the candidate should be familiar with the light client specification provided by the Polkadot documentation, which outlines the necessary modules and logic required for the light client. The candidate should also have experience working with the Polkadot JSON-RPC API, which is used to interact with the network.
In addition to technical expertise, the candidate should possess a strong understanding of blockchain security and cryptography. This includes an understanding of Merkle proofs, signature verification, and other cryptographic techniques used to ensure the trustlessness of the light client.
The candidate should also have experience working in decentralized networks and be familiar with the challenges and opportunities presented by a decentralized architecture. This includes understanding the importance of network resilience and the need for multiple implementations to ensure diversity and security in the network.
Overall, the ideal candidate for building a light client for Polkadot should possess a combination of technical expertise, blockchain security knowledge, and experience working in decentralized networks. This will enable them to build a light client that is efficient, secure, and compatible with the Polkadot network architecture.

## Payment conditions
The total prize pool for this bounty is 993286.08 DOT. It is split between ZK:Infra roughly in a ratio of 5:1. The incentive prize program will be structured as a set of child bounties, agreed upon by the Administrative Curator group. 
If either the Web3 Foundation research team or the community suggests a further prize area that is deemed likely to benefit strongly from an incentive prize, further categories may be added later on, again, in consultation with the community and the Administrative Curator group.

As a note, neither the Web3 Foundation nor Parity Technologies GmbH will be the recipient of any amount of funds, as the aim of the program is to support and incentivize the community.
Each milestone will not represent a treasury submission; the total amount requested will cover winner payouts, and milestones are intended as officially reported program updates. 

The amount requested from the on-chain treasury in this proposal covers funding to be paid to program winners; all marketing, communications, and operational costs up to and supporting the successful completion of the program are executed by Parity Technologies as part of an operating SLA with the Web3 Foundation, and the Web3 Foundation itself. 
No installments will be due until the completion of milestones, which will be determined by the curator/s. While we may not time-bound these challenges or the program itself, in order not to sacrifice innovation impact or quality over speed, we will be doing bi-annual assessments of progress with the teams. 

## Curator Team 
The following group of individuals are acting as the Administrative Curator group, who control the funds via a [proxy account](https://polkadot.subscan.io/account/15AysydMuDH9XnzZsNTBezB5uLPjAGFBYtVVEu3p3MZqcSzC):
- Alistair Stewart, Head of Research, Web3 Foundation 
- David Hawig, Technical Advisor, Web3 Foundation 
- Raul Romanutti, Polkadot On-Chain Council Member
- Bryan Chen, Co-Founder of Acala
- Ricardo Rius, Polkadot Ecosystem Tech Lead, Parity Technologies

In addition to the Administrative Curator group, an advisory team of technical specialists was created (via off-chain coordination) to advise the group on things like the assessment of deliverable submissions, challenge guidelines, and future challenge creation. 

## Process 
1. Fork this repository.
2. In the newly created fork, create a copy of the application template ([`applications/application-template.md`](applications/application-template.md)). Make sure you **do not modify the template file directly**. Name the new file after your project: `project_name.md` and fill out the template.
3. Once you're done, create a pull request in the original [Polkadot-Pioneers-Prize repository](https://github.com/pioneersprize/Polkadot-Pioneers-Prize). The pull request should only contain _one new file_—the Markdown file you created from the template.
4. Curators issue comments and request changes on the pull request
5. Clarifications and amendments made in the comments need to be included in the application. You may address feedback by directly modifying your application and leaving a comment once you're done. Generally, if you don't reply within two weeks, the application will be closed due to inactivity, but you're always free to reopen it as long as it hasn't been rejected.
6. The application will be accepted and merged as soon as it receives three approvals or closed after two weeks of inactivity. 
8. Milestones are to be delivered on the [Milestone Delivery repository](https://github.com/pioneersprize/Milestone-Delivery) following the [process](https://github.com/pioneersprize/Milestone-Delivery#mailbox-milestone-delivery-process) described there.
