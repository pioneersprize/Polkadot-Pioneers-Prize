# Treasury Proposal: Polkadot Java Host

**Proponent: 15reUHgnkE9QeH9zUoduCVYAbksTmQXvpMd6L95rBhTNFuGw**

**Date: 21.02.2023**

**Requested allocation:**  **7 days EMA of $315 500 **** - DOT \*to be calculated upon submission\***

**Short description: Alternative Host implementation for JVM**

**1. Context of the bounty and problem statement**

A healthy decentralized network is one where it's difficult or impossible for a single person or entity to gain significant influence. Diversity should be considered essential to Polkadot as it is deep-rooted in the decentralization paradigm. One way to decentralize the protocol is through client diversification. One of the benefits is that it **safeguards the network against the pooling of power and control** , preventing a single entity from making non-unanimous decisions in permissionless protocols such as Polkadot.A second benefit of client diversification is that it makes a network **less vulnerable to undiscovered bugs and exploits**. You have to look no further than the reports of node bugs throughout time that have disrupted the operation of the blockchain protocols in one way or another. Such accidents have occurred in most protocols - [Ethereum critical bug](https://coingeek.com/ethereum-forks-after-critical-bug-affects-54-of-nodes/), [Cardano outage](https://www.coindesk.com/tech/2023/01/23/cardano-network-quickly-recovers-after-brief-node-outrage/) **,** [Solana NFT minting disaster](https://www.coindesk.com/tech/2022/05/03/heres-why-solana-ceased-block-production-for-seven-hours-on-saturday/) etc. We accept the nature of software, that it's never perfect and bugs happen. Being the driving force behind a blockchain - a healthy diversity of node implementations - mitigates the impact of such issues as well as being aligned with the decentralization ideal.

Polkadot is one of the few protocols that is actively trying to increase decentralization within itself. That however, is still a work in progress as Parity still holds the majority share when it comes to Host and Runtime implementations - half of the Host implementations ( ![](RackMultipart20230901-1-ldoo2j_html_e2f6fd9cdf81e776.png)[polkadot](https://github.com/paritytech/polkadot), ![](RackMultipart20230901-1-ldoo2j_html_e2f6fd9cdf81e776.png)[smoldot](https://github.com/paritytech/smoldot)) as well as ![](RackMultipart20230901-1-ldoo2j_html_e2f6fd9cdf81e776.png)[substrate](https://github.com/paritytech/substrate) are coming from Parity. This combined with the fact that Gossamer and Kagome, the current alternative host implementations, are still not widely adopted, makes the network less resilient than desired.

Runtime diversification has similar advantages to Client diversification and both approaches reduce the centralization of the protocol. We at LimeChain are currently working on an approved treasury proposal for creating a [framework for building Substrate-compatible Runtimes in Go](https://github.com/LimeChain/gosemble). We have also worked on building an [AssemblyScript Runtime from scratch](https://github.com/LimeChain/as-substrate-runtime) and evolving it into a fully capable [framework for building Substrate Runtimes](https://github.com/LimeChain/subsembly).

"_Ecosystems can be much more innovative if there are many teams all doing their own thing." - Dr. Gavin Wood at Polkadot Decoded_

With that being said we clearly see that **growing the ecosystem** is one of Polkadot's main priorities. Still, it's evident that Polkadot has limited involvement in enterprise applications. One of the ways to dive into that world is to have sufficient **Java-based** tooling. Java has consistently been one of the top 5 most used languages in the past few decades, has an enormous community and has even found its uses in the blockchain sphere. Currently 18% of Ethereum consensus nodes run the Java-based consensus client [Teku](https://consensys.net/knowledge-base/ethereum-2/teku/).

This is exactly why as a prerequisite to this proposal, the team at LimeChain undertook a [**research grant**](https://github.com/LimeChain/java-host-research) **to prove or disprove the feasibility of a Java Host**. Such a host will not only increase client diversity and network resilience but also open up Polkadot to the world of Java. Both ecosystems will benefit from exposure to one another and enable a new layer of applications to be built. The research yielded positive results meaning that the necessary tools exist for a Java-based Host to be feasible.

**2. Proposal Objective/solution/s to point 1**

**For us success would be to provide Java communities with a Polkadot client they can utilize**. The goal of this treasury proposal is to create a light client that the Java community members can use to tap into the world of Polkadot. In the next phases, we're going to extend the light client to a full and subsequently an authoring node targeting the enterprise community. We're confident that other Java developers and niches will notice these clients and use them to their advantage or even better - contribute to building on top of them. Moreover, as stated above we believe that multiple implementations should exist in order to improve the client diversification of the protocol.

Based on the [Feasibility Research](https://github.com/LimeChain/java-host-research/blob/main/research/java-host-research-outcome.md), we believe that the most pragmatic strategy would be to build an MVP of the Host - **a Light Client for Polkadot, Kusama and Westend**. Using a light client first approach will allow the team to create a good architectural setup that will serve the team as a solid foundation on which to build the full and authoring nodes and at the same time deliver a functional light client that can be utilized. At the end of the light client phase, the team and the community will be able to continue with a good groundwork towards the next goal of full & authoring node.

Another reason for building the light client first is that this enables it to take on its own separate development path if there's interest in developing a feature rich and optimized Java light client (potentially utilizing ZK to instantly sync to the tip of the network). An advanced version of the Polkadot light client would be able to run efficiently on Android devices and Wallets could use it to trustlessly verify information coming directly from the P2P network. From that point on, sky's the limit as to what integrations could be made with other Android apps. As for the Java full and authoring node, it would allow Enterprises to participate in securing the Polkadot network in their comfortable language and being confident in the Host's capabilities.

When talking about the development plan, there are two main paths we can take when structuring it - the iterative or the incremental approach. Using the incremental one for this project would make sense in terms of development separation as each module could be separated in its own milestone. However, we believe that this approach is not suitable for this specific use-case as it would be difficult (in terms of engineering) to implement all modules of the light client without the need of a major refactoring when each module integrates with another. Another point is that it would result in a functioning light client at the end of the phase once the modules are integrated. This approach isn't very agile in case some feature has to be changed or added. Moreover, it tightens the number of people that are able to give feedback just based on how the team has developed each module without being able to run the client or examine how it works.

The iterative approach inherently allows us to be flexible when working on each milestone, as well as be able to showcase to the community what we've accomplished after each milestone delivery. Furthermore, we believe that this approach is going to make implementing each new milestone iteration more error resistant. For example, if the node was to be separated in logical modules such as - rpc, network, sync, persistence, etc., developing each of them separately without being certain how the implementation and abstraction of the other ones is going to look like is a recipe for refactoring when you realize you've missed a tiny but very important part of a module that may not have been documented well. Iterations spread the implementation curve of the modules over each iteration. As part of each new one, a new or parts of a new module are going to be introduced, plus some of its existing features are going to be upgraded.

**Therefore, we believe that the iterative approach is more suitable due to the size and complexity of the project.** Based on the rationale above, we've defined the following scopes and milestones define the implementation scope of each milestone.

We believe the goal for the Polkadot Java Host can be split into **3 major phases**. In the table below we describe the end goal for each of them, as well as provide detailed scope and description of the deliverables for the first one.

**Phase 1 - Polkadot, Kusama, Westend light client**

During the 1st phase of the project, the team will work on the implementation of the [light client specification](https://spec.polkadot.network/#sect-lightclient). As a final deliverable for this phase and proposal we're aiming for a light client able to sync with Polkadot, Kusama, Westend.

As stated above, [a light client design document](https://github.com/LimeChain/java-host-research/blob/main/research/java-host-light-client-high-level-design.md) was created as part of our research grant which has been the basis for the phase. You can find a more in-depth description on the deliverables [here](https://limechain.notion.site/Light-Client-Milestone-Deliverables-4f8a6362cb0244b0b93e2b530332dbb2), as well as a link for each deliverable in the table below.

| **Milestone** | **Deliverable** | **Notes** |
| --- | --- | --- |
| 1. | [RPC API, Chain Spec & Persistence](https://www.notion.so/limechain/Light-Client-Milestone-Deliverables-4f8a6362cb0244b0b93e2b530332dbb2?pvs=4#17cc99abac014ca4a1517b08423572f5) | Lay the groundwork by introducing the first logic and module bits of the client |
| 2. | [Kademlia P2P & RPC Upgrades](https://www.notion.so/limechain/Light-Client-Milestone-Deliverables-4f8a6362cb0244b0b93e2b530332dbb2?pvs=4#843269dde18040608a7ccca406b5aa03) | Introduce the network module with Kademlia and upgrade RPC functionality |
| 3. | [Substreams & Sync](https://www.notion.so/limechain/Light-Client-Milestone-Deliverables-4f8a6362cb0244b0b93e2b530332dbb2?pvs=4#1e75d5c02e284bc28a5d26011386a3a0) | Add Yamux as a foundational P2P protocol and implement sync logic for the client. |
| 4. | [Wasmer-java, Host APIs & Runtime module](https://www.notion.so/limechain/Light-Client-Milestone-Deliverables-4f8a6362cb0244b0b93e2b530332dbb2?pvs=4#719b8a89332a490bbf755a80c59b2c10) | Patch wasmer-java to suit our needs and introduce the Host APIs in order to load Runtime. |
| 5. | [Documentation](https://www.notion.so/limechain/Light-Client-Milestone-Deliverables-4f8a6362cb0244b0b93e2b530332dbb2?pvs=4#f34ebf5c442d455fb99137a05b274328) | Add a high-level project overview. Make sure the project and each of its modules is well documented, has setup guides & examples. |

**NB!** Explicit delivery for documentation has been included in order for anyone to be able to contribute or build on top of LimeChain's progress.

**Phase 2 - Polkadot, Kusama, Westend Full node**

During this phase the team will extend the functionality of the light client in order to conform to the full node requirements and specification. Having a functioning light-client at the beginning of the phase will be of aid to the team because it allows the team to focus on the logical complexity that the full node specification introduces.

The 2nd phase will build on top of the light client, extending it as per the requirements for the full node, as well as introduce architectural and performance improvements to improve the scalability properties of the node. These requirements include functionalities (and are certainly not an exhaustive list) like:

- Implementing the majority of the RPC and Host methods that were not in Phase 1
- Executing transactions using the Runtime
- Upgrading the state trie logic - update, persist, encode, decode the trie based on the executed transactions and exchanged messages between the nodes
- Exchanging (gossiping) GRANDPA neighbor packets, blocks, transactions with other nodes

At the end of this phase, users will be able to launch either a full node or a light client on Polkadot, Kusama or Westend.

**Phase 3 - Polkadot, Kusama, Westend Authoring node**

This phase will consist of extending full node functionality with more BABE and GRANDPA processes so that the node can participate in the block production process, as well as iterating over the security and performance of the node.

Taking part in the consensus-reaching mechanism is a big milestone on its own with upgrades spanning across all modules of the Host plus implementing some missing features at the time of writing such as generating and verifying DLEQ proofs. These findings are described in more detail in the [research outcome document](https://github.com/LimeChain/java-host-research/blob/main/research/java-host-research-outcome.md#findings-3).

Completing this phase will mark the achievement of our end goal - a Java Authoring node.

The estimation for the duration of the full completion of Phase 1 (Milestones 1-5) is 5-6 months. LimeChain will scale the team after the completion of Milestone 2 with 2 full-time Blockchain Developers in order to complete Phase 1 in a timely manner.

Total team size for Milestone 3 and onwards - 5.5 team members.

After that it will be gradually scaled with the maturity of the Host as additional effort will be required in order to provide outstanding developer documentation, guides, maintenance of the already created codebase and implementation of the required modules.

**Payment conditions:**

The duration & budget of the explained milestones **apply only** for Phase 1. We intend to create follow-up proposals for the next phases. Initial payment **for milestone 1, 2 and 3** to be due on successful proposal approval. Payments for each following milestone **(3 and 4)** to be due on successful delivery of phase 1. The total allocation for milestones 1-3 will be calculated after community discussion/feedback phase, on the day of on-chain submission, using the [7 day EMA provided by Subscan (https://polkadot.subscan.io/tools/charts?type=price).

**Budget per milestone:**

  1. Milestone 1 - $65 000
  2. Milestone 2 - $52 500
  3. Milestone 3 - $82 500
  4. Milestone 4 - $99 000
  5. Milestone 5 - $16 500

The total amount of **$315 500** to be distributed in DOTs to

**15reUHgnkE9QeH9zUoduCVYAbksTmQXvpMd6L95rBhTNFuGw**

DOT amount is calculated based on the [7 day average](https://polkadot.subscan.io/tools/charts?type=price), using on the day of submission. Contact information for the funds managers:

- Zhivko Todorov - zhivko@limechain.tech
- Christian Veselinov - chris@limechain.tech

The project budget is fully dedicated for development costs, the phase 1 team from the start would be the following:

1. Blockchain Architect - Part Time
2. 2x Senior Blockchain Developers - Full Time
3. 1x Mid Blockchain Developer - Full Time
4. Project Manager - Part Time

Total team size - 3.5 team members

Timeline/Duration per milestone:

  1. Milestone 1 - 6 weeks
  2. Milestone 2 - 5 weeks
  3. Milestone 3 - 5 weeks
  4. Milestone 4 - 6 weeks
  5. Milestone 5 - 1 weeks

**Review Deliverables**

Web3 Foundation Spec Team agreed to review the technical deliverables of each milestone and provide technical feedback during the evaluation. The results of the evaluation will be published according to the Grant-Milestone-Delivery repository: [https://github.com/w3f/Grant-Milestone-Delivery](https://github.com/w3f/Grant-Milestone-Delivery).

**About LimeChain**

LimeChain works with companies like [Hedera](https://hedera.com/) (Hedera is a fully open source, proof-of-stake, public network and[governing body](https://www.hedera.com/council/)for building and deploying decentralized applications) which is almost entirely built on Java making us one of the few companies who have production experience with Java in the blockchain sphere. We have extensive experience in building developer tooling specifically with Rust/WebAssembly ( ![](RackMultipart20230901-1-ldoo2j_html_e2f6fd9cdf81e776.png)[matchstick](https://github.com/limeChain/matchstick/)). We are also the sole technical partner of[Cudos network](https://github.com/CudoVentures) (based on Cosmos) which recently had their genesis mainnet release. Recently, LimeChain's team has undertaken another treasury proposal to develop a [Substrate Runtime alternative in Go](https://github.com/LimeChain/gosemble). All of this combined with the positive research outcome leads us to believe that we are a great fit for implementing a Java Host node.

**Future Roadmap**

LimeChain is a blockchain development company with a team of 100+ and we plan to make the Polkadot and Substrate ecosystem a focus point over the next 3 years. Our long term vision is to build a suite of developer tools and infrastructure enabling wider adoption of the Polkadot ecosystem. Creating an alternative Host implementation as well as an [alternative Runtime](https://github.com/LimeChain/gosemble) will certainly prove that our team is fit to be part of Polkadot's builders. A possible future plan that's not included in the 3 phases is working towards upgrading the authoring node into a relaying one or dedicating a separate team to extend the light client functionality and features.

**Comments, Qs&As:** During the open community discussions this section would be updated accordingly.
