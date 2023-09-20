# Verifiable Reputation System

- **Team Name:** Hungry Cats Studio
- **Payment Address:** TBD

## Project Overview :page_facing_up

Linking git contributions to an on-chain reputation system.

### Overview

Verifiable Reputation is a revolutionary reputation system that leverages zkGit, a proof-of-contribution technology, to verify public and anonymous code contributions. The system allows for integrating git activity into an on-chain reputation score, ensuring transparency, verifiability and security. With a custom and composable rule creation and on-chain SNARKs verification, the system aims to bring even more potential opportunities and contributors to the Polkadot ecosystem.

We are interested in building this project, because we have a vision for how git can power a new reputation system. We would like to provide a bridge between a developer's GitHub activity and their on-chain reputation, thus maintaining a highly respectable - and cryptographically verifiable - score attesting to their skills.

Polkadot is already leading the way to decentralize all protocol components, from the distribution of treasury funds via on-chain voting, to on-chain protocol upgrades. The process of distributing the voting power is still mainly based on sheer token ownership, however. What we propose with the Verifiable Reputation platform is a small, but important step on the road towards bringing the Polkadot network closer to a fair on-chain voting future. Due to the complexity of the runtime protocol upgrades as well as highly technical nature of some treasury proposals, it’s important that the skilled and knowledgeable developers are given a fair share of say in what happens with the network. The Verifiable Reputation platform paves way for this: contributors are recognized by having an on-chain reputation score that intimately ties in with their GitHub activity for the relevant repositories (e.g. `polkadot-sdk`). As a bonus, they can remain anonymous if they so wish, by providing cryptographic proofs of contributuions from multiple GitHub account.

### Project Details

What is the problem that we're trying to address here? It can be summarized as the verifiable on-chain reputation system. The way it works, in brief, is developers who contribute to GitHub repositories can submit proofs of their contributions, and are accordingly rewarded with so-called contribution points or contribution scores that represent their skills. And by skills, I mean skills that are relevant to a specific blockchain project.

Let's dive into a bit more detail of how this works. At the core of the verifiable reputation system is zkGit technology. "zkGit" is a tool that allows developers to prove, in zero-knowledge and succinctly, statements about their contributions to GitHub repositories. The statements can be varied in nature. For example, one might want to say that he has made 10 or more contributions to a certain GitHub repo. Another developer might wish to say that he made five bug fixes among repositories X and Y. Yet the next person might wish to talk about a very specific feature that they have developed for a particular repository. All these statements will be compiled from a high-level description, such as “making 10 contributions to a repository”, to an arithmetic circuit that can then be proved using a SNARK. The proof system need not actually be zero-knowledge (zkSNARK). This is just an optional feature for users who wish to remain fully anonymous. The key property of the proof system is that it is succinct, meaning that the proof length is much smaller than the statement itself (submitting the statement itself would be synonymous with uploading the `git diff` of all your PRs on-chain!).

The way that zkGit technology will be utilized in the reputation system is as follows: The application, in this case the verifiable reputation system, will contain on-chain logic for verifying SNARK proofs. When a user submits such a proof, the verifier will attest that such a proof corresponds to the statement being proved, as well as its validity. If the checks pass, the on-chain logic will assign a reputation score according to the statement submitted.

For the reputation system that we envision, each user account will hold a data structure that maps the repository they contributed to, to a reputation score for that repository. This will form part of the shared reputation chain (a common goods parachain), and users of such data, which typically will be parachains, will configure which repositories are of importance to them, and what weight to assign to each repository. Then, upon querying the users’ reputation, each parachain can aggregate the reputation score differently. For example, the Acala parachain might assign a weight of two to any repository in the Acala organization, and a weight of one to repositories in the `paritytech` organization. On the other hand, Moonbeam might assign a weight of three to `polkadot-sdk`, half to Acala organization, and two to Ethereum org repositories. This way, even with one single database holding the user's contributions, each chain can adapt it to its needs.

### zkGit Features

To gain wide adoption, the app needs to be configurable enough to cover the majority of the use cases, and intuitive enough to lower the bar for less-technical users (e.g. designers, product managers, interviewers). Each specific statement about the user’s contributions will need to be transformed into a circuit that can be fed into a proving system of choice, and each such circuit manually written. Fortunately, many sub-circuits (gadgets) will be re-usable. In the first iteration, MVP, we aim to provide the ability to prove the following statement:
- At least X contributions to repository Y

This will showcase the composability of zkGit, i.e. both the count `X` and repo `Y` are configurable. To convince the verifier, they first need to know what the statement is. This could be done by either the prover telling them: “Hey verifier, my `X = 3` and `Y = tornadocash/tornado-core`” - or simply sending the encoded instance together with the proof.
In the future iterations, we would like to conduct a survey and gather users’ input on what features they care most about. We expect to receive something such as:
- In top-X contributors to repository Y
- At least X contributions to one or more of repositories from set {$Y_1, Y_2, ..., Y_n$}
- Added/modified/deleted X lines in some repository written in Programming Language P with at least S stars

Regardless of the actual statements to be proved, we expect to see a pattern, where the first part of the statement is about the nature of the contributions to be proved, and the second part is about the conditions of such contributions (or: where the contributions has happened). Our goal in the second iteration will be to provide composability of *Contribution Type* + *Contribution Condition*, for a crowd-sourced list of *Contribution Types* and *Contribution Conditions*.

### Are all contributions equal?

Now, the natural question that arises is whether all contributions should be treated equally. The answer is clearly no. Imagine a user submitting 10 typo fixes versus another user developing an important feature for the protocol. In the naive scenario, the first user would be rewarded 10 times the reputation score of the second, which is clearly not what we want.

Instead, there must be a way to rate the contributions, according to their difficulty, importance, type, and level of skill used. We will present three approaches to this problem.

The first approach relies on manual tagging of issues and pull requests on GitHub by their repository maintainers with labels, such as "difficulty: medium, type: bug fix" or "difficulty: hard, type: feature". Then, alongside the SNARK proof that a user would submit, they would need to supply auxiliary information that later will be verified by an API call to GitHub. This has two obvious problems: the first being reliance on manual classification of contributions. While some repositories already do this, few have adopted the practice, and so the set of repositories where this information is present is limited, not to mention the human factor involved. The second issue is the reliance on an oracle network to query GitHub and provide the large amounts of API results on-chain. There have been multiple attacks on oracle networks in the past, and even assuming a perfectly secure oracle network, there would still be reliance on a centralized third-party provider, GitHub, to not interfere with the metadata.

The second approach circumvents the need to manually tag contributions. It relies on an AI model that is trained on contribution histories and is able to provide a few labels or scores upon feeding it a `git diff` of a contribution. With the recent surge of LLMs, we’ve seen just how good AI can be at classifying data. This approach, however, poses an equal risk of reliance on a centralized third-party as the earlier solution, since the inference needs to be provided by an oracle network anyway, and unless the AI model inference comes from a decentralized network, relies on a single trusted party to provide correct results.

The third approach goes a step further and considers a provable machine learning model. One of the recent hot topics in the zero-knowledge field is ZKML, which aims exactly at solving the issue of provable inference on queried data. For various reasons, turning a machine learning model into an arithmetic circuit is a challenging field of research and engineering. The challenge lies in the sheer size of the computation, and the fact that turning arbitrary computations into arithmetic circuits is hard. It usually carries a few orders of magnitude overhead over the native computation of just running the machine learning model itself. Some projects have demonstrated simple machine learning models for which efficient SNARKs can be designed. While we are not yet at the point of proving LLMs with parameter sets the size of ChatGPT, such a model is actually overkill for our reputation system. We don't need to hold a conversation with the model, but rather simply obtain a label. This is just a classification task, and this area of machine learning has been around for much longer than deep learning models. Due to its relative simplicity, they are much easier to emulate inside of SNARK compared to deep learning models.

### Ecosystem Fit

Now, why is this a good fit for the Polkadot system? First of all, due to its customizability and modularity, Polkadot is a fairly complex blockchain relative to other networks. This implies that understanding, working with, and developing on Polkadot requires a certain level of expertise that is scarce among developers.

Developers with deep technical knowledge and years of expertise should be fairly represented in decisions which involve the future of the network, including runtime upgrades, on-chain voting, or treasury spending proposals.

There is already a movement inside Polkadot to reward highly skilled contributors through the fellowship program. In the spirit of decentralization, the verifiable reputation system takes a step closer towards a fair and trustless way to achieve similar things as the fellowship. We imagine the verification system and the fellowship to, at least initially, remain two separate systems but with potential to interplay at a later point in time.

The verifiable reputation system is a common good that will benefit not only the relay chain of Polkadot but also each parachain that wishes to use the data provided by the system. As such, we are aiming to build the verifiable reputation system as a common goods parachain.

## Team :busts_in_silhouette:

### Team members

- Marcin
- Antonio
- Hossein

### Contact

- **Contact Name:** Marcin Górny
- **Contact Email:** marcin-pioneers-prize.ng73a@slmails.com

### Legal Structure

- **Registered Address:** Switzerland
- **Registered Legal Entity:** Hungry Cats Studio GmbH

### Team's experience

- Marcin (Project Lead) was a Technical Grants Evaluator, and later a Research Engineer, at the Web3 Foundation.
Since 2 years he's been contributing to the arkworks libraries in Rust, where he's now a core maintainer. 

- Antonio (Cryptography Engineer) has a PhD in algebraic number theory from Universität Duisburg-Essen.
He has a good theoretical understanding of cryptographic protocols and hands on experience building proof systems in Rust.

- Hossein (Cryptography Engineer) is currently finishing his Masters degree in Computer Science at EPFL, focusing on proof systems, cryptography and SNARKs. He codes proficiently in C++ & Rust.


We plan to hire three more developers to work on the project full-time by the end of the year, to bring the team count to a total of 6 people:
- 3 Cryptography/Rust Engineers @ $120,000
- 1 Cryptography Engineer / Project Lead @ $120,000
- 1 Senior Rust Engineer @ $140,000
- 1 Full-stack Engineer @ $100,000

### Team Code Repos

You can see our public activity in the various org repos/forks:
- https://github.com/orgs/HungryCatsStudio

## Development Status :open_book:

We are in the planning phase.

## Development Roadmap :nut_and_bolt:

### Overview

- **Total Estimated Duration:** 2 years
- **Full-Time Equivalent (FTE):**  6
- **Total Costs:** USD $1,440,000

### Milestone 1 - zkGit technology

- **Estimated duration:** 6 months
- **FTE:** 4
- **Costs:** USD $240,000

Milestone one will be dedicated to the development of the zkGit technology. By the end of Milestone one, we hope to have a bare Proof of Concept of the zkGit tool, which will lay a foundation for the future work of integrating this into blockchain logic.

The work involved in Milestone one will be cryptographically heavy. We will need to develop arithmetic circuits for the operations needed in zkGit, namely hashing and GPG signature verification. These will later have to be combined to allow users to submit a single proof of contribution, and the verifier logic will check that the signatures are valid, and that the hashes have been performed correctly.

### Milestone 2 - Standalone & functional chain

- **Estimated duration:** 6 months
- **FTE:** 6
- **Costs:** USD $360,000

Milestone two will focus on creating a first version of a standalone substrate chain that integrates the zkGit technology and allows users to prove simple statements about their contributions. As part of Milestone two, we'd also like to demonstrate how an independent parachain would interact with this verifiable reputation system and query and aggregate contribution results to award reputation points to some of its users, in their own customizable way. This means developing a pallet that such a chain would import into the runtime, allowing for seamless integration with the verifiable reputation system, and for hooking into important actions that a user could get involved in, such as voting. Note that Milestone two and the project in general will involve an oracle network. Unlike what we described before, this network will not provide comprehensive data about the contributions. Rather, the only thing that the verifiable reputation system will need to verify contributions will be a digest of the latest commit in any particular repository, thus absolutely minimizing the trust assumption placed on the oracle.

### Milestone 3 - zkGit composability

- **Estimated duration:** 2 months
- **FTE:** 6
- **Costs:** USD $120,000

The scope of M3 will be to incorporate the composability features detailed in the [zkGit Features](#zkgit-features) section.

This will involve designing user-friendly APIs that would allow developers to easily compose statements about their contributions, and then compile them into arithmetic circuits that can be proved succinctly. This will be a crucial milestone for the project, as it will allow users to prove more complex statements about their contributions, and thus allow for a more fine-grained reputation system.

### Milestone 4 - Provable classification model

- **Estimated duration:** 6 months
- **FTE:** 6
- **Costs:** USD $360,000

Milestone four will focus on integrating a scoring mechanism into the system, such that different contributions are rated according to the skill level required, as described above. This will entail either compiling a state-of-the-art "classical" machine learning model into an arithmetic circuit (nontrivial!) or leveraging an existing project that already does this and adjusting it to our needs. Due to the fast-moving nature of the field, especially the incredible advances in ZKML in the recent months, it's difficult to predict just how far the field will advance by the end of Milestone two, so for now this is just a tentative description.

Should it so happen that it's still infeasible to succinctly prove a meaningful AI model for our purposes, as a backup we will revert to utilizing GitHub APIs to provide the scores. However, we are confident that by mid-2024, provable classification models will turn out to be a relatively straightforward objective.

### Milestone 5 - Common Goods Parachain

- **Estimated duration:** 6 months
- **FTE:** 6
- **Costs:** USD $360,000

Milestone five will be dedicated to bringing together all the features developed in Milestones 1 through 3 and preparing the project for integration as a common good parachain. This is quite a complex task and will likely require deep collaboration with the relevant Parity team knowledgeable about common good parachains.

## Future Plans

After launch, we plan to further continue the project development by integrating with the ecosystem more deeply (e.g. with voting mechanism, providing tools to periodically submit proofs, connecting with the fellowship). We also plan to continue the research on the provable classification models and integrate any new advances into the system.

We have a good track record of contributing to and maintaining open source software.
