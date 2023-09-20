# Fruzhin, Java Polkadot Host Full Node Implementation

- **Team Name:** [LimeChain](https://github.com/LimeChain)
- **Payment Address:** 15reUHgnkE9QeH9zUoduCVYAbksTmQXvpMd6L95rBhTNFuGw

## Project Overview :page_facing_up:

### Overview

This proposal is a continuation of LimeChain's previous proposal, [Treasury Proposal - Polkadot Java Host](https://docs.google.com/document/d/1SSadeH3g6lPIodfUDvihcAlRG7E8Pvdp/edit#heading=h.gjdgxs), which laid the groundwork for the Java full node implementation of the Polkadot Host that our team named Fruzhin. The presence of multiple client implementations is crucial for a mature blockchain protocol like Polkadot, as it reduces the vulnerability to undiscovered bugs and safeguards against centralization of power and control. Such accidents have occurred in the past in most protocols and have led to significant negative impacts - [Ethereum critical bug](https://coingeek.com/ethereum-forks-after-critical-bug-affects-54-of-nodes/), [Cardano outage](https://www.coindesk.com/tech/2023/01/23/cardano-network-quickly-recovers-after-brief-node-outrage/ ), [Solana NFT minting disaster](https://www.coindesk.com/tech/2022/05/03/heres-why-solana-ceased-block-production-for-seven-hours-on-saturday/).


Another pivotal aspect of this proposal is to provide the Java communities with a functional Polkadot client. This would empower enterprises to engage with the Polkadot Network using their preferred programming language, ensuring their confidence in the capabilities of the host system.


LimeChain's team has already demonstrated the feasibility of a Java Host by initially implementing it as a light client. This proposal outlines the necessary steps to advance the Host to the next milestone - the full node implementation. 

### Project Details

#### Problem statement 
Fruzhin's еnd goal is to act as a relaying node, providing valuable benefits to the Polkadot network by diversifying the client base. This is significant because it helps to safeguard the network against the concentration of power and control, preventing a single entity from making unilateral decisions in permissionless protocols like Polkadot. Additionally, client diversification contributes to reducing vulnerability to undiscovered bugs and exploits, thereby enhancing the overall security and resilience of the network. Currently, most nodes are running the Rust-based client developed by Parity, with only a few exceptions. However, Fruzhin's efforts aim to encourage the adoption of various clients, adding more diversity to the network and further fortifying its decentralized nature. By promoting a healthy mixture of clients, Fruzhin contributes to the long-term stability and sustainability of the Polkadot ecosystem.

Moreover, implementing Fruzhin in Java will play a crucial role in attracting a wider pool of talent to actively participate in and enrich the Polkadot ecosystem. Over the past few decades, Java has consistently ranked among the top 5 most widely used programming languages, boasting a massive and thriving community. Notably, Java has also found applications in the blockchain sphere, including its adoption in Ethereum, where around 18% of the consensus nodes currently utilize a Java-based consensus client - Teku.

To ensure a gradual development process, we have embraced an incremental strategy, wherein each increment corresponds to a distinct node type. As a result, the feature set naturally progresses from the already accomplished Light Client in Phase 1 to the full node, followed by the authoring node, and ultimately, the relaying node. This approach allows us to build upon the achievements of each prior phase, steadily advancing toward our final objective of having a fully functional relaying node.

#### Proposal objective(s) or solution(s) 
In order to transition the light client into a full node, we need to extend its existing functionalities. Currently, the light client focuses on following the chain and verifying mainly the grandpa justifications and authority signatures. The steepest milestone is to enable the Host to verify extrinsics and transition to a new state accurately. To achieve this, primary focus would be to implement the Host API and extrinsics validation, considering that the light client can already load Runtimes.

To conform to the full node specification, we will enhance the existing Host by adding new peer-to-peer (p2p) protocols for exchanging transactions and grandpa messages, as well as extend existing ones. Additionally, most RPC methods have to be implemented, as well as extend the state and sync functionality. 

As the Host starts to mature with more features and wider coverage of the specifications, it’s important to dedicate time to strengthening the user experience. This means that the team is going to spend time supporting the first users, researching, benchmarking, and improving the performance, testing the security of the Host, as well as expanding the documentation and the features of the repository.

The transition from a light client to a full node is relatively smaller compared to the leap from a full node to an authoring node. Consequently, in this phase, we envision achieving another milestone by implementing DLEQ proving and verification in Java. These proofs are utilized in the BABE protocol, which is implemented by every authoring node. As no such library currently exists in Java, this contribution would significantly benefit the Java cryptography open-source libraries.

### Ecosystem Fit

- Where and how does your project fit into the ecosystem?
  - The proposal will enable the network participants to utilize a Java-based Node Host implementation as a consensus client. The proposal's milestones are designed to progress toward the ultimate goal of a relaying node. The first milestone involves transitioning the light client into a full node by extending its functionalities. This step is crucial as a full node implementation provides a more robust and comprehensive participation in the network. It enables the Host to verify extrinsics and transition to a new state accurately, contributing to the overall security and reliability of the Polkadot network.

- Who is your target audience (parachain/dapp/wallet/UI developers, designers, your own user base, some dapp's userbase, yourself)?
  - This solution helps all network participants who rely on Polkadot's stability and consistency to conduct their activities safely and efficiently. This includes Node Operations, providers, validators, token holders, developers, and most importantly - the end users.
By increasing the diversification of Host implementations, the proposal enhances decentralization within the network. More diversified client implementations reduce the risk of centralization, ensuring that no single entity gains excessive influence or control over the network.

- What need(s) does your project meet?
  - By diversifying the client implementations, it enhances protocol security and resilience. Having multiple clients reduces the risk of a single point of failure and makes the network less susceptible to potential attacks or vulnerabilities that may be specific to certain client implementations.
- Are there any other projects similar to yours in the Substrate / Polkadot / Kusama ecosystem?
  - There are no other Java Host implementations. 

## Team :busts_in_silhouette:

### Team members

- Georgi Georgiev
- Viktor Todorov
- Murad Hamza
- Stoyan Stoyanov
- Boris Velkovski
- Daniel Ivanov

### Contact

- **Contact Name:** Kristiyan Veselinov
- **Contact Email:** kris@limechain.tech
- **Website:** <https://limechain.tech>

### Legal Structure

- **Registered Address:** Bulgaria, Dragan Tsankov 23A, 1113, Sofia, Bulgaria
- **Registered Legal Entity:** LimeLabs Ltd.

### Team's experience

LimeChain is a blockchain development company with 180+ completed projects and a strong focus on blockchain development infrastructure. LimeChain has built tools for different protocols and networks such as Ethereum, The Graph, Polhttps://github.com/wasmerio/wasmer-javakadot, EOS, Aeternity, Corda, Polygon, Near, and Hedera Hashgraph among others.

At LimeChain, we believe in a multi-chain future, based on interoperability and decentralization. Principles that are built into the core of the Polkadot network. We have been firm believers in the Polkadot ecosystem for the last 3+ years. We possess considerable expertise in developing various tools, including Gosemble, a framework for building substrate-compatible routines in Go, a framework for runtimes in AssemblyScript, and Parachain Validation Conformance Testing. Additionally, we have substantial experience in Rust/WebAssembly developer tooling from Matchstick and have actively contributed to infrastructure projects in Cosmos, Near, Filecoin, Ledger and Hedera Hashgraph.

### Team Code Repos

https://github.com/LimeChain/Fruzhin

Please also provide the GitHub accounts of all team members. If they contain no activity, references to projects hosted elsewhere or live are also fine.

- https://github.com/vikinatora
- https://github.com/georg-getz
- https://github.com/stoyan-lime
- https://github.com/bokoto000
- https://github.com/ablax


### Team LinkedIn Profiles (if available)

- [Viktor Todorov](https://www.linkedin.com/in/viktor-todorov-8a7434122/)
- [Georgi Georgiev](https://www.linkedin.com/in/georgi-georgiev-595591190/)
- [Georgi Spasov](https://www.linkedin.com/in/george-spasov/)
- [Daniel Ivanov](https://www.linkedin.com/in/daniel-k-ivanov/)


## Development Status :open_book:

- https://github.com/limechain/fruzhin - The current implementation for a fully functional Light client
- https://github.com/LimeChain/wasmer-java
- [Research feasibility and design for Java Host](https://github.com/w3f/Grants-Program/pull/1353)
- [Deliverable: Research Feasibility of a Java Host](https://github.com/w3f/Grant-Milestone-Delivery/pull/735)

## Development Roadmap :nut_and_bolt:

### Overview

- **Total Estimated Duration:** 7 months
- **Full-Time Equivalent (FTE):** 5
- **Total Costs:** 314 160 USD
<br/>

### Milestone 1 - Protocols

- **Estimated Duration:** 1 month
- **FTE:**  5
- **Costs:** 46 816 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 1.1 | Transactions substream | Add /transactions/1 protocol message encoding and decoding |                          
| 1.2 | Grandpa substream | \- Add /grandpa/1 protocol messages encoding and decoding:<br>\- Vote message<br>\- Commit message<br>\- Catch-up request message<br>\- Catch-up message |
| 1.3 | Light messages substream | Handle incoming requests for /light/2 |
| 1.4 | Incoming requests for /sync/2 substream | Handle incoming block requests.<br>Handle incoming state requests |
<br/>

### Milestone 2 - Host API

- **Estimated Duration:** 1 month
- **FTE:**  5
- **Costs:** 55 440 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 2.1 | Storage API                   | Implement all Storage API functions. Write unit tests to verify behaviour.|
| 2.2 | Child Storage API             | Implement all Child Storage API functions. Write unit tests to verify behaviour.|
| 2.3 | Crypto API                    | Implement all Crypto API functions. Write unit tests to verify behaviour.|
| 2.5 | Offchain & Offchain index API | Implement all Offchain and Offchain index API functions. Write unit tests to verify behaviour.|
| 2.6 | Trie API                      | Implement all Trie API functions. Write unit tests to verify behaviour.|
| 2.7 | Allocator API                 | Implement all Allocator API functions. Write unit tests to verify behaviour.|
| 2.8 | Logging & Abort handler API   | Implement all Logging and Abort handler API functions. Write unit tests to verify behaviour.|
<br/>

### Milestone 3 - RPC API

- **Estimated Duration:** 2 weeks
- **FTE:**  5
- **Costs:** 25 872 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 3.1 | System | Implement all System RPC methods. Write unit tests to verify behaviour -> Most System RPC methods have already been implemented as part of the light client |
| 3.2 | Chain| Implement all Chain RPC methods. Write unit tests to verify behaviour|
| 3.3 | Offchain | Implement all Offchain RPC methods. Write unit tests to verify behaviour|
| 3.4 | State | Implement all State RPC methods. Write unit tests to verify behaviour|
| 3.5 | Child State| Implement all Child State RPC methods. Write unit tests to verify behaviour |
| 3.6 | Sync | Implement all Sync RPC methods. Write unit tests to verify behaviour |
| 3.7 | Add local/public and safe/unsafe RPC methods separation | Node can be launched with or without some of the method groups |
<br/>

### Milestone 4 - State & Sync

- **Estimated Duration:** 1 month
- **FTE:**  5
- **Costs:** 44 352 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 4.1 | Populate state storage with official genesis state | Host is able to calculate the Merkle root using the genesis data for Polkadot, Kusama, Westend |
| 4.2 | Process genesis hashes and replace the existing hard-coded ones | GenesishHash file is replaced with dynamic calculation of genesis state |
| 4.3 | Change substream identifiers to use genesis hash | Host can be launched with either the old or the new protocol identifiers for Polkadot, Kusama, Westend |
| 4.4 | Add child storage functionality | |
| 4.5 | Add child trie functionality | Calculate merkle value of child trie and store it in the main state. |
| 4.6 | Add extrinsics validation | Host is able to validate extrinsics by communicating with the Runtime. Host tracks peers already aware of transactions. Host gossips transactions by avoiding duplicated;<br>Implement transaction queue<br>Implement validate transactions and store algorithm<br>Implement maintain transaction pool algorithm<br> |
| 4.7 | Add configuration to start full node using either warp or full sync | Host start in either full or warp sync mode and is able to sync correctly |
<br/>

### Milestone 5 - Modularisation

- **Estimated Duration:** 1 week
- **FTE:**  3
- **Costs:** 8 008 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 5.1 | Code base improvements | Common packages of the full node and light client into separate packages that are well encapsulated and reusable |
<br/>

### Milestone 6 - VRF Proofs

- **Estimated Duration:** 1 months
- **FTE:**  5
- **Costs:** 46 816 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 6.1 | DLEQ Proofs Generation   | Function creates a proof for a given input (i), based on the provided transcript(T). Write unit tests in order to verify correct behaviour. |
| 6.2 | DLEQ Proofs Verification | Function verifiers the VRF input (i) against the output(o) with the associated proof and public key(pk) |
<br/>

### Milestone 7 - Light Client & Full Node Support

- **Estimated Duration:** 1 month
- **FTE:**  5
- **Costs:** 38 808 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 7.1 | Light client issues support | Dedicate time and resource for resolving issues that will arise as with any Open-Source project. |
| 7.2 | Full node issues support    | Dedicate time and resource for resolving issues that will arise as with any Open-Source project. |
<br/>

### Milestone 8 - Zombienet tests

- **Estimated Duration:** 1 week
- **FTE:**  3
- **Costs:** 7 392 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 8.1 | Add test to showcase successful block building(full node)               | Be able to run the Zombienet test. |
| 8.2 | Add test to showcase successful block header verification(light client) | Be able to run the Zombienet test. |
| 8.3 | Add test to showcase successful peer finding                            | Be able to run the Zombienet test. |
<br/>

### Milestone 9 - Repository Maintenance

- **Estimated Duration:** 2 weeks
- **FTE:**  2
- **Costs:** 9 240 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 9.1 | Create a [code of conduct](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/adding-a-code-of-conduct-to-your-project). | A markdown file, which describes the rules, responsibilities, standards, scope and enforcements. File must be situated in the code repository and referenced in the README. |
| 9.2 | Add License |  |
| 9.3 | Add Contributor guidelines that outline the steps for contributors | A markdown file, which describes the contributor guidelines. File must be situated in the code repository and referenced in the README. |
| 9.4 | Issues and pull request templates | Issue and pull request templates, used whenever someone wants to open a Github issue or pull request.|
| 9.5 | Changelog| Create a CHANGELOG markdown file, which lists the changes made in each version of the runtime repository.<br>File must be situated in the code repository and referenced in the README. |
| 9.6 | Dependabot setup| Configure Dependabot that creates a PR every time a new version of a dependency is released |
| 9.7 | Binary | 
<br/>

### Milestone 10 - Documentation & Guides

- **Estimated Duration:** 1 week
- **FTE:**  1
- **Costs:** 3 696 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 10.1 | Documentation | Review all previous milestones to ensure they have complete documentation, inline documentation, and maintenance docs |
<br/>

### Milestone 11 - Research

- **Estimated Duration:** 3 weeks
- **FTE:**  2
- **Costs:** 15 400 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 11.1 | Research      | Create a GitHub issue with research results and action plan.<br>Allocate effort towards researching and exploring different methods for improving the Host. |
<br/>

### Milestone 12 - Developer Relations

- **Estimated Duration:** 1 month
- **FTE:**  1
- **Costs:** 12 320 USD

| Number | Deliverable | Specification |
| -----: | ----------- | ------------- |
| 12.1 | Establish a community channel for support, questions and feedback. | Provide link to community channel |
| 12.2 | Host a workshop on using Fruzhin | Host the workshop |
| 12.3 | Produce a Short series of educational content | Provide link to the educational content |
| 12.4 | Produce a public document, which reviews the feedback from the community and parachain teams. | Provide link to the document |

## Future Plans

The main goal of Fruzhin is to serve as a relaying node. This means that if there’s interest from the community and funding, proposals for features related to authoring and relaying nodes will be created. Our hope is that if Fruzhin has a strong impact, the larger ecosystem will provide the funding needed for these efforts. If not, we’re prepared to fund these endeavors ourselves, as long as Fruzhin remains important within the ecosystem.

The goal of Fruzhin is to provide a viable full-node implementation of the Polkadot host in Java, adopted and used by the developer community. In order for this to be achieved, a significant effort needs to be put into education and communication with developer teams. This process is often referred to as “developer relations” and it will cover:

- Establish a community channel for support, questions, and feedback.
- Host a workshop on using Fruzhin
- Produce a short series of educational content
- Produce a public document, which reviews the feedback from the community and parachain teams.

## Additional Information :heavy_plus_sign:

At LimeChain, we believe in a multi-chain future, based on interoperability and decentralization. Principles that are built into the core of the Polkadot network. We have been firm believers in the Polkadot ecosystem for the last 3+ years. As such, we have been exploring different ways to add value to its developer community, starting with Subsembly - a framework used to design and implement Substrate runtimes in Assembly Script, the current development of Gosemble, a light client implementation in Java, and building a Parachain Validation Conformance Testing suite.
