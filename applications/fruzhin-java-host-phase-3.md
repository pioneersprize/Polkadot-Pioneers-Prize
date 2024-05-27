# fruzhin-java-host-phase-3

# Fruzhin, Java Authoring node

- **Team Name:** [LimeChain](https://github.com/LimeChain)
- **Payment Address:** 15reUHgnkE9QeH9zUoduCVYAbksTmQXvpMd6L95rBhTNFuGwre

## Project Overview

### Overview

This proposal is a continuation of LimeChain’s previous proposal, [Java Full Node](https://github.com/pioneersprize/Polkadot-Pioneers-Prize/blob/main/applications/fruzhin-java-host-phase-2.md), which laid the groundwork for the Java authoring node implementation of the Polkadot Host that our team named Fruzhin. 

The presence of multiple client implementations is crucial for
a mature blockchain protocol like Polkadot, as it reduces the
vulnerability to undiscovered bugs and safeguards against centralization
of power and control.

Another pivotal aspect of this proposal is to provide the Java
communities with a functional Polkadot client. This would empower
enterprises to engage with the Polkadot Network using their preferred
programming language, ensuring their confidence in the capabilities of
the host system.

LimeChain’s team has already demonstrated the feasibility of a Java
Host by initially implementing it as a light client and later on
upgrading it to a full node. This proposal outlines the necessary steps
to advance the Host to the next milestone - authoring node.

### Project Details

Fruzhin’s еnd goal is to act as a relaying node, providing valuable
benefits to the Polkadot network by diversifying the client base. This
is significant because it helps to safeguard the network against the
concentration of power and control, preventing a single entity from
making unilateral decisions in permissionless protocols like Polkadot.
Additionally, client diversification contributes to reducing
vulnerability to undiscovered bugs and exploits, thereby enhancing the
overall security and resilience of the network. Currently, most nodes
are running the Rust-based client developed by Parity, with only a few
exceptions. However, Fruzhin’s efforts aim to encourage the adoption of
various clients, adding more diversity to the network and further
fortifying its decentralized nature. By promoting a healthy mixture of
clients, Fruzhin contributes to the long-term stability and
sustainability of the Polkadot ecosystem.

Moreover, implementing Fruzhin in Java will play a crucial role in
attracting a wider pool of talent to actively participate in and enrich
the Polkadot ecosystem. Over the past few decades, Java has consistently
ranked among the top 5 most widely used programming languages, boasting
a massive and thriving community. Notably, Java has also found
applications in the blockchain sphere, including its adoption in
Ethereum, where around 18% of the consensus nodes currently utilize a
Java-based consensus client - Teku.

To ensure a gradual development process, we have embraced an
incremental strategy, wherein each increment corresponds to a distinct
node type. As a result, the feature set naturally progresses from the
already accomplished Light Client in Phase 1 and Full node in Phase 2 to
an authoring node, and ultimately, the relaying node. This approach
allows us to build upon the achievements of each prior phase, steadily
advancing toward our final objective of having a fully functional
relaying node.

### Proposal objective(s) or solution(s)

The transition from Full Node to Authoring Node is a significant endeavour, given that up until now Fruzhin has only been a passive participant of the network. The biggest objective of this proposal is to advance our Host to becoming an active participant of the network by implementing block building and consensus protocols, namely BABE and GRANDPA.

Another high priority objective is to have an abundance of unit and integration tests that cover a wide range of scenarios that the Host could find itself it. This will reduce the chances of incompatibility problems, as well as give confidence in adopters.

Fruzhin uses wasmer-java to enable Host <-> Runtime communication. As such it’s an integral part of the node, however it currently lacks useful features like being able to deploy multiple binaries for different CPU architectures. Currently, this problem is handled locally in Fruzhin, which is suboptimal due to the increased size of the repository.

### Ecosystem Fit

- Where and how does your project fit into the ecosystem?
    - The proposal will enable the network participants to utilize a
    Java-based Node Host implementation as a consensus client. The
    proposal’s milestones are designed to progress from a Full node to an
    Authoring node. This will significantly help to decentralize the network
    as upgrading to an active participant of the network who produces blocks
    and votes in GRANDPA will surely draw more new users in.
- Who is your target audience (parachain/dapp/wallet/UI developers,
designers, your own user base, some dapp’s userbase, yourself)?
    - This solution helps all network participants who rely on Polkadot’s
    stability and consistency to conduct their activities safely and
    efficiently. This includes Node Operations, providers, validators, token
    holders, developers, and most importantly - the end users. By increasing
    the diversification of Host implementations, the proposal enhances
    decentralization within the network. More diversified client
    implementations reduce the risk of centralization, ensuring that no
    single entity gains excessive influence or control over the
    network.
- What need(s) does your project meet?
    - By diversifying the client implementations, it enhances protocol
    security and resilience. Having multiple clients reduces the risk of a
    single point of failure and makes the network less susceptible to
    potential attacks or vulnerabilities that may be specific to certain
    client implementations.
- Are there any other projects similar to yours in the Substrate /
Polkadot / Kusama ecosystem?
    - There are no other Java Host implementations.

## Team

### Team members

- Georgi Georgiev
- Viktor Todorov
- Murad Hamza

### Contact

- **Contact Name:** Kristiyan Veselinov
- **Contact Email:** kris@limechain.tech
- **Website:** [https://limechain.tech](https://limechain.tech/)

### Legal Structure

- **Registered Address:** Bulgaria, Dragan Tsankov 23A,
1113, Sofia, Bulgaria
- **Registered Legal Entity:** LimeLabs Ltd.

### Team’s experience

LimeChain is a blockchain development company with 220+ completed
projects and a strong focus on blockchain development infrastructure.
LimeChain has built tools for different protocols and networks such as
Ethereum, The Graph, Polkadot, EOS, Aeternity, Starknet, Corda, Polygon,
Near, Scroll, and Hedera Hashgraph among others.

At LimeChain, we believe in a multi-chain future, based on
interoperability and decentralization. Principles that are built into
the core of the Polkadot network. We have been firm believers in the
Polkadot ecosystem for the last 3+ years. We possess considerable
expertise in developing various tools, including Gosemble, a framework
for building substrate-compatible routines in Go, a framework for
runtimes in AssemblyScript, and Parachain Validation Conformance
Testing. Additionally, we have substantial experience in
Rust/WebAssembly developer tooling from Matchstick and have actively
contributed to infrastructure projects in Cosmos, Near, Filecoin, Ledger
and Hedera Hashgraph.

We also have extensive Polkadot ecosystem knowledge as in addition to
all the projects mentioned above we have successfully upgraded our host
to a Full node and take active part in coferences such as Polkadot
Decoded. 

### Team Code Repos

- https://github.com/LimeChain/Fruzhin
- https://github.com/LimeChain/wasmer-java

Please also provide the GitHub accounts of all team members. If they
contain no activity, references to projects hosted elsewhere or live are
also fine.

- https://github.com/georg-getz
- https://github.com/vikinatora
- https://github.com/ablax

### Team LinkedIn Profiles (if available)

- [Viktor
Todorov](https://www.linkedin.com/in/viktor-todorov-8a7434122/)
- [Georgi
Georgiev](https://www.linkedin.com/in/georgi-georgiev-595591190/)
- [Murad
Hamza](https://www.linkedin.com/in/muradhamza/)

## Development Status

- https://github.com/limechain/fruzhin - The current Java implementation
of a light client and full node
- https://github.com/LimeChain/wasmer-java
- [Research
feasibility and design for Java Host](https://github.com/w3f/Grants-Program/pull/1353)
- [Deliverable:
Research Feasibility of a Java Host](https://github.com/w3f/Grant-Milestone-Delivery/pull/735)

## Development Roadmap

### Overview

- **Total Estimated Duration:** 9 months
- **Full-Time Equivalent (FTE):** 4
- **Total Costs:** 502,400 USD

### Milestone 0 - Block execution improvements

- **Estimated duration:** 2 weeks
- **FTE:** 4
- **Costs:** 25,600 USD

| Number | Deliverable | Specification |
| --- | --- | --- |
| 0a. | License | Apache 2.0 |
| 0b. | Documentation | Mostly inline documentation will be added. |
| 0c. | Testing and Testing Guide | A milestone further down the line handles the heavy integration runtime tests. Unit tests will be written. |
| 1. | Research | All possible solutions will require a certain amount of refactoring so making sure we taking the correct approach is mandatory. |
| 2. | Abolish all Singletons related to the HostAPI | This will help us decouple the runtime calls. |
| 3. | Decouple Spring and Polkadot Runtime | Right now we need a working Spring instance (with all of its components) to make ANY runtime call. These 2 shouldn’t be coupled so hard. |
| 4. | Storage HostAPI functions remodelling | As storage access is one of the most important and slowest features, it would greatly help out node to have them remodelled so that trie root calculation can happen in parallel.  |

### Milestone 1 - BABE

- **Estimated duration:** 6 weeks
- **FTE:** 4
- **Costs:** 76,800 USD

| Number | Deliverable | Specification |
| --- | --- | --- |
| 0a. | License | Apache 2.0 |
| 0b. | Documentation | In addition to inline documentation we will have a dedicated README file for the BABE protocol. |
| 0c. | Testing and Testing Guide | Multitude of unit tests will be written as opposed to integration tests which will be decided on a case by case basis. |
| 1. | Research and design | Gather the whole team and have them read and take part in the design meeting going over all the details for implementing the BABE algorithms. |
| 2. | Block authoring session key pair | Creation of said key pair is a necessary step for the block production lottery. |
| 3. | Block Production Lottery | Implement the block production lottery algorithm as well as the underlying required functions and Runtime calls. |
| 4. | Slot Number Calculation | Implement using NTP (Network Time Protocol) for now as the docs suggest it is currently the safer choice. |
| 5. | Epoch Randomness | Implement the logic for getting the randomness seed through the Runtime and through consensus messages. |
| 6. | Verify Authorship Right | Implement the algorithm as well as any underlying functions like Verify Slot Winner. |
| 7. | Build Block | Implement the algorithm as well as any underlying functions with the exception of Median Algorithm as we will be using NTP instead. |
| 8. | Invoke Block Authoring | Implement the algorithm as well as any underlying functions. Also announce the block once created. |

### Milestone 2 - GRANDPA

- **Estimated Duration:** 9 weeks
- **FTE:** 4
- **Costs:** 115,200 USD

| Number | Deliverable | Specification |
| --- | --- | --- |
| 0a. | License | Apache 2.0 |
| 0b. | Documentation | In addition to inline documentation we will have a dedicated README file for the GRANDPA protocol. |
| 0c. | Testing and Testing Guide | Multitude of unit tests will be written as opposed to integration tests which will be decided on a case by case basis. |
| 1. | Research and design | Gather the whole team and have them read and take part in the design meeting going over all the details for implementing the GRANDPA algorithms. |
| 2. | GRANDPA GHOST | Implement the algorithm. |
| 3. | Best Final Candidate | Implement the algorithm and update the GRANDPA GHOST algorithm. |
| 4. | Best PreVote Candidate | Implement the algorithm. |
| 5. | Finalizable | Implement the algorithm. |
| 6. | Attempt to Finalize At Round | Implement the algorithm as well as any underlying functions. |
| 7. | Initiate GRANDPA | Implement the algorithm which requires fully implementing Play GRANDPA Round algorithm as well as some smaller algorithms like Derive Primary. |
| 8. | Forced authority set changes detection and handling | Implement logic behind the handling and detection of forced authority set changes. |
| 9. | Catchup request sending | Implement logic for sending catchupo requests. |
| 10. | Process Catchup request | Implement the algorithm as well as any underlying functions. |
| 11. | Process Catchup response | Implement the algorithm as well as any underlying functions. |
| 12. | Disable Validators | Faulty validators should be reported. |

### Milestone 3 - BEEFY

- **Estimated Duration:** 7 weeks
- **FTE:** 4
- **Costs:** 89,600 USD

| Number | Deliverable | Specification |
| --- | --- | --- |
| 0a. | License | Apache 2.0 |
| 0b. | Documentation | In addition to inline documentation we will have a dedicated README file for the BEEFY protocol. |
| 0c. | Testing and Testing Guide | Multitude of unit tests will be written as opposed to integration tests which will be decided on a case by case basis. |
| 1. | Research and design | Gather the whole team and have them read and take part in the design meeting going over all the details for implementing BEEFY and clearing up the MMR structure. |
| 2. | BEEFY session key pair | Ensure the existing Secp256k1 functionality in the project is sufficient to produce a BEEFY session key pair and add whatever necessary. |
| 3. | Create MMR | Create the MMR (Merkle mountain ranges) structure. This milestone objective will be further split into more granular tasks. |
| 4. | Sign and gossip payload |  |
| 5. | Committing witnesses  | The relayer should collect the gossiped votes. |
| 6. | Requesting signed commitments  | Light clients should be able to request signatures from the relayer |
| 7. | Participate in BEEFY Consensus | Implement session, the logic for mandatory and non mandatory blocks, BEEFY round number algorithm, validate and broadcast votes. |

### Milestone 4 - Upgrading the Full Sync

- **Estimated duration:** 7 weeks
- **FTE:** 4
- **Costs:** 89,600 USD

| Number | Deliverable | Specification |
| --- | --- | --- |
| 0a. | License | Apache 2.0 |
| 0b. | Documentation | Inline documentation. |
| 0c. | Testing and Testing Guide | Multitude of unit tests will be written as opposed to integration tests which will be decided on a case by case basis. |
| 1. | Implement block tree pruning | It’s necessary to have access to the pruned block tree for the correct execution of part of the following algorithms. |
| 2. | Retrieve authorities from Runtime | Make the necessary Runtime calls to get the authority list. |
| 3. | Add consensus message to header | In the case of a change to the authority list during a state transition we want to add an appropriate consensus message to the block header. |
| 4. | Complete the implementation of Import and Validate Block | Finish the algorithm by adding the Verify Authorship Right and Verify Block Justification algorithms to it and extract it to a separate function. Also announce the block to the network. |
| 5. | Improve peer finding | Update Nabu dependency to latest version and ensure we can keep a two digit number of peers connected and synching at all times. Revisit log frequency/level after to avoid log clogging. |
| 6. | Ensure network compatibility | Host is able to sync up to the head of the chain. Requires testing with all networks (polkadot, kusama, westend). |
| 7.  | Correctly load a block state  | We are currently saving a valid block state but lack the of getting it and using it which would save a lot of syncing time. |
| 8.  | Improve syncing strategy | So far the user is required to manually select whether he wants the node to sync in full or warp mode. Given that node reputation is something we want to keep high it would be better to think of a strategy where most of the synching happens with warp sync. |

### Milestone 5 - Upgrading wasmer-java

- **Estimated duration:** 2 weeks
- **FTE:** 4
- **Costs:** 25,600 USD

| Number | Deliverable | Specification |
| --- | --- | --- |
| 0a. | License | MIT |
| 0b. | Documentation | Greatly improve the README of the project by deleting obsolete information and restructuring it in a better way with also adding the latest functionality updates there as well. |
| 0c. | Testing and Testing Guide | Not much testing will be needed for the changes in this milestone. |
| 1. | Research and implement a way to release all necessary binaries | Java has no way of interacting with wasm files and therefore we are using native functions - in this case Rust which makes Fruzhin platform dependant. The best way to deal with this problem is to have binaries for different OS+Chip combinations but GitHub doesn’t offer apple runners for free. There are probably other ways we can have the ARM binaries be built and that would help up remove the manual setup process in Fruzhin. |
| 2. | Logging | Add an abundance of logs of different levels so that Runtime calls can more easily be tracked and debugged. |
| 3. | Minor refactoring | There are a lot of parts in the code that could be refactored for better readability and effectiveness since they were written a long time ago with an older Rust version. |

### Milestone 6 - Compatibility, monitoring and Docker

- **Estimated duration:** 2 weeks
- **FTE:** 4
- **Costs:** 25,600 USD

| Number | Deliverable | Specification |
| --- | --- | --- |
| 0d | Docker | Make Fruzhin runnable via Docker. |
| 1. | Set up Prometheus  | Add Prometheus metrics monitoring to Fruzhin. |
| 2. | CLI arguments improvement | Ensure synchronisation between the CLI arguments used in polkadot to improve user experience. |
| 3. | Ensure network compatibility | Make sure the node works the exact same way across all networks. Reinforce with tests. |

### Milestone 7 - Testing

- **Estimated duration:** 2 weeks
- **FTE:** 4
- **Costs:** 25,600 USD

| Number | Deliverable                  | Specification                                                                                                                                                                                                                      |
| --- |------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1. | Consensus integration tests  | Consensus is a very important part of the network and to make sure our authoring node is acting exactly the way it is supposed to. Therefore our team will add an abundance of integration tests in order to verify the behaviour. |
| 2. | Runtime integration tests    | Add multiple integration tests which specifically focus on the Runtime class and Runtime exported functions.                                                                                                                       |
| 3. | Integrate in cloud           | Deploy Fruzhin to cloud.                                                                                                                                                                                                           |
| 4. | Implement Todo.md changes    | We have a file in Fruzhin called Todo.md in which we have test and refactoring ideas.                                                                                                                                              |

### Milestone 8 - Documentation and article

- **Estimated duration:** 3 weeks
- **FTE:** 1
- **Costs:** 9,600 USD

| Number | Deliverable | Specification |
|--------| --- | --- |
| 0e     | Article | Publish an article about the new functionalities. |
| 1.     | Readme improvements | Improve the documentation and add a comprehensive guide of how to use the authoring node. |
| 2.     | Minor docs improvements | We will also revisit the documentation we’ve written so far and refactor it wherever necessary. |

### Milestone 9 - Developer Relations
#### **Part of the milestone items are transferred from the previous proposal and cost 0**

- **Estimated duration:** 6 weeks
- **FTE:** 1
- **Costs:** 9,600 USD

| Number | Deliverable               | Specification                                                                              |
|--------|---------------------------|--------------------------------------------------------------------------------------------|
| 1.     | Workshop                  | Host a workshop on how to use the authoring node.                                          |
| 2.     | Update educational videos | Update the videos about Fruzhin with he newly added functionalities.                       |
| 3.     | Gather feedback           | Use the community channel to gather feedback.                                              |
| 4.     | User issues support       | Dedicate time to address issues raised by users.                                           |
| 5.     | Upgrade Host              | Upgrade the Host by improving on the parts which have received the most negative feedback. |

### Milestone 10 - Research relaying node scope

- **Estimated duration:** 3 weeks
- **FTE:** 1
- **Costs:** 9,600 USD

| Number | Deliverable | Specification |
| --- | --- | --- |
| 1. | Relaying node | Create the scope for the next phase - relaying node. |
| 2. | User feedback | Analyse the user feedback and the changes in the ecosystem and scope the important changes for the next phase. |

## Future Plans

The main goal of Fruzhin is to serve as a relaying node. This means
that if there’s interest from the community and funding, proposals for
features related to relaying node will be created. Our hope is that if
Fruzhin has a strong impact, the larger ecosystem will provide the
funding needed for these efforts. If not, we’re prepared to fund these
endeavors ourselves, as long as Fruzhin remains important within the
ecosystem.

## Additional Information

At LimeChain, we believe in a multi-chain future, based on
interoperability and decentralization. Principles that are built into
the core of the Polkadot network. We have been firm believers in the
Polkadot ecosystem for the last 3+ years. As such, we have been
exploring different ways to add value to its developer community,
starting with Subsembly - a framework used to design and implement
Substrate runtimes in Assembly Script, the current development of
Gosemble, a Full node implementation in Java, and building a Parachain
Validation Conformance Testing suite.
