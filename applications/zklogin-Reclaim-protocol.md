# Implementing zklogin and Proof of Personhood using Reclaim Protocol 

- **Team Name:** Questbook International Inc
- **Payment Address:** 16DFLp86GpYDFE4qooU3WT4f5b7DD6o7MfaxL2y4Di1JDGmy


## Project Overview :page_facing_up:

### Proposal Context and Problem Overview

Currently, users are accustomed to logging into centralized login systems such as Google, Facebook, and Twitter to access these services, but they have no way to use this on-chain. These conventional login methods are incompatible with on-chain verifications, thus creating a disconnect between user identities on different centralized platforms and restricting their utility on-chain across Dapps.

Reclaim protocol will allow Dapps within the Polkadot ecosystem to provide zk login for its users. It will enable Dapp users to log into any website and generate a zkproof of their login that can be verified onchain. Reclaim Protocol makes https traffic verifiable using Zero-Knowledge Proofs, enabling users to generate verifiable credentials from any of their online user profiles. This unlocks unlimited possibilities as no APIs are required or no changes to be made to the websites to extract private user data, while guaranteeing data integrity. Web2 user data which was elusive to Web3 till now will be available to builders across the Polkadot ecosystem. Reclaim empowers developers to make Web2 composable. This opens up opportunities for a new wave of applications that can support zklogin, proof of personhood, and bot protection. 

Additionally, after speaking with the members of the Polkadot Foundation, we have been able to identify zklogin and [epassport](https://github.com/w3f/Grants-Program/blob/master/docs/RFPs/epassport-zk-validation.md) to be important use cases for Dapp builders and users that can be implemented uniquely through Reclaim Protocol. Through Reclaim, users can not only validate their login credentials but also provide verifiable proofs of various personal attributes and activities. For instance, they can prove the number of rides taken on Uber, expenditures on Amazon, or their scores on Chess.com, thereby establishing a robust proof of personhood which is instrumental in combating fraudulent actors and bots. Such proof of personhood can now be made available on-chain via Reclaim protocol within the Polkadot ecosystem.

We are a small team (20+ members) with finite resources and want to collaborate with ecosystems that demonstrate a genuine commitment to enable use cases that are likely to scale to a billion users. Our team comprises primarily engineers who have previously worked at Meta, Microsoft, Google and have contributed to various web3 open source projects. Given Polkadot's strong emphasis on streamlining user onboarding,  user experience, and implementing bot protection, coupled with our team's expertise and background, we believe that our team is one of the most suited to realise Polkadot's vision of building zk login and implementing Proof of Personhood for Dapps on top of Polkadot.



### Project Details

[zk Login Overview](https://questbook.notion.site/Implementing-zklogin-and-Proof-of-Personhood-using-Reclaim-Protocol-6a1d31a7d70c46c482682742abbbe0cb#:~:text=using%20Reclaim%20Protocol-,zk%20Login%20Overview,-Reclaim%20Protocol%20Overview)

**Reclaim Protocol Technical Deep Dive**

Reclaim empowers users to generate Zero-Knowledge Proofs for any online user profile. To generate a claim, users first need to log into the relevant website. This login process, involving an HTTPS request and its subsequent response, is channeled through an HTTPS Proxy Server known as an 'attestor'. This attestor oversees the encrypted data exchange between the user and the website. Subsequently, users provide keys that disclose non-sensitive parts of the request to the attestor. With this, the attestor can view the request in its entirety, barring confidential details like authentication data, and can confirm its legitimacy.

The website's encrypted response is then processed by a zk-circuit, which identifies a regex match within the encrypted data using a decryption key as a confidential input. The attestor further validates that the zk-circuit's public input was indeed the encrypted data sourced from the website. With these attestations on both the request and the encrypted response, coupled with the zk-proof, any third-party application, whether on-chain or off-chain, can verify the existence of data that exists on the user’s profile.

[Reclaim Protocol Overview](https://questbook.notion.site/Implementing-zklogin-and-Proof-of-Personhood-using-Reclaim-Protocol-6a1d31a7d70c46c482682742abbbe0cb#:~:text=Reclaim%20Protocol%20Overview)

[zk Circuit](https://questbook.notion.site/Implementing-zklogin-and-Proof-of-Personhood-using-Reclaim-Protocol-6a1d31a7d70c46c482682742abbbe0cb#:~:text=Reclaim%20Protocol%20Overview-,zk%20Circuit,-Comments%20from%20Polkadot)

User credentials in Reclaim Protocol are generated and stored completely on the client side. Using Reclaim, users can generate Proofs(Groth16) in less than 10 secs even on a 2015 Android Device! 

[Reclaim Protocol Demo](https://www.loom.com/share/c54d572a1e894395b5160cfad6bb3e08)

Website - https://www.reclaimprotocol.org/

Whitepaper - https://drive.google.com/file/d/1wmfdtIGPaN9uJBI1DHqN903tP9c_aTG2/view?usp=sharing

Reclaim SDK- https://docs.reclaimprotocol.org/

Github - https://github.com/reclaimprotocol

Explainer - https://blog.reclaimprotocol.org/posts/what-is-reclaimprotocol/, https://blog.reclaimprotocol.org/posts/reclaim-explained/

ZK Circuit Security Audit - https://blog.reclaimprotocol.org/posts/chacha-circuit-audit/

**Adoption**

Reclaim Protocol is live on production and is currently used by experienced Dapp developers to build novel use cases such as a [whistleblower protocol](https://whistleblower-frontend-acez.onrender.com/),  [decentralised P2P exchange](https://www.p2px.finance/)**,** which has already done [~$135,000](https://dune.com/p2px/metrics) in volumes in just nine weeks after launch.


### Ecosystem Fit

### **Problem Statement**

Currently, there is no way for users to login and interact with on-chain Dapps using the same logins they are accustomed to on Web 2 apps such as Google, Facebook, Twitter logins. Furthermore, there is no way to bridge user’s data from Web2 to Web 3. Oracles such as chainlink are effective at bridging publicly available data. However, private data that often resides behind a user login is inaccessible on-chain. e.g. number of Uber rides a user has taken is accessible only after the user has successfully logged in. This lack of a seamless bridge for private data between Web2 and Web3 creates a disconnect between user identities on different centralized platforms and restricts their utility on-chain across Dapps.

**Comments from Polkadot’s community members on the forum**

[Comment - 1](https://questbook.notion.site/Implementing-zklogin-and-Proof-of-Personhood-using-Reclaim-Protocol-6a1d31a7d70c46c482682742abbbe0cb#:~:text=Polkadot%20Community%20Members-,Comment%20%2D%201,-Comment%20%2D%202)


[Comment - 2](https://questbook.notion.site/Implementing-zklogin-and-Proof-of-Personhood-using-Reclaim-Protocol-6a1d31a7d70c46c482682742abbbe0cb#:~:text=Comment%20%2D%201-,Comment%20%2D%202,-Comment%20%2D%203)


[Comment - 3](https://questbook.notion.site/Implementing-zklogin-and-Proof-of-Personhood-using-Reclaim-Protocol-6a1d31a7d70c46c482682742abbbe0cb#:~:text=Comment%20%2D%202-,Comment%20%2D%203,-A%20case%20for)


[A case for building Proof of Personhood Primitives](https://twitter.com/stanikulechov/status/1717194504787100145?s=46&t=ZmnjQV9BqONGTPrJcABIeg)

The absence of a streamlined user onboarding process is keeping potentially millions, if not billions, of users from embracing and experiencing the benefits of Web3. Presently, developers lack the means to seamlessly integrate popular OAuth providers and user profiles into their dApps' onboarding processes, primarily because of the absence of foundational tools and comprehensive documentation related to primitives such as zkLogin. As other ecosystems build their own solutions to address this challenge in future, the Polkadot ecosystem risks the possibility of falling behind.

### Proposed Solution

We believe that the integration of familiar login systems (such as Google login, as opposed to wallets) along with robust on-chain bot protection will significantly enhance the value proposition of on-chain applications, thereby paving the way for millions, if not billions, of users to reap the benefits offered by these dApps.

A critical use case of blockchains lies in their capacity for establishing and keeping irrefutable commitments. Commitments are the backbone of human civilization. Today, commitments are often articulated on paper or verbally, hinging on the pillars of social dynamics and the legal framework for trust. **While this is useful for numerous use cases, social dynamics have low friction and low integrity; while legal system has high friction and high integrity.**

Blockchains allow for **low friction and high integrity commitments** and transactions that can be modeled using an expressive programming language given the availability of correct data to settle the commitment. A wide spectrum of agreements/commitments—ranging from rental agreements and freelancing contracts to claims made while dating—are ideal use cases to move onchain, provided the required infrastructure is in place.

For billions of users to start using on-chain applications, we need three foundational pillars.

1. **Low-Friction Transactional Engagement:** Transactions should transcend the conventional bounds of sending and swapping tokens to include diverse forms of agreements and commitments.

2. **Counterparty Trust:** Knowing that the other side is a human or a non-sybil bot, is crucial to engage in an agreement. It's undesirable to enter a commitment with a counterparty that could disappear.

3. **Programmatic Correctness:** Agreeing on the logic to settle an agreement and having ways to deterministically come to a fair conclusion is essential to enter a commitment on-chain. This property is accessible to builders thanks to programmable blockchains. Providing access to the right data sources will make these agreements more expressive.

**Benefits of zk Login and Proof of Personhood through Reclaim’s Integration with Polkadot:**

- **Familiar login on dapps Transitioning from Wallets to familiar logins** such as Google Login will offer a streamlined onboarding experience for users. By establishing a gas tank, a dApp’s front end can enable users to engage on-chain without the necessity of a wallet. Subsequently, dApps can identify users on-chain through off-chain logins. This represents a substantial user experience enhancement compared to the current requirement of installing a wallet prior to interacting on-chain. zkLogin makes wallets a beneficial but non-essential component for dApp usage.
- **Bot Protection** -  By leveraging data from off-chain real-world actions, a robust proof of personhood construct can be built. For instance, if a user has completed 50 Uber rides, spent $1000 on Amazon, and holds an 1100 rating on Chess.com, the likelihood of them being a bot is significantly reduced. Rather than relying on on-chain activity, which can be easily manipulated to ascertain whether a user is a bot, utilizing off-chain data to formulate a user's humanness profile can effectively weed out bots that significantly hampers Web3 usability today.

**Target Audience**

Reclaim protocol empowers developers to make Web2 composable. Our proposal primarily aims to benefit **builders** to seamlessly leverage Reclaim protocol into their Dapps and get access to Web2 user data gated by Web2 servers to build innovative use cases. Moreover, these builders can leverage zkLogin, Proof of Personhood,  and bot protection primitives built by our team to significantly enhance new user onboarding and user experience. 

Moreover, all end users will significantly benefit from the primitives such as zklogin, proof of personhood, thereby experiencing a significant user experience enhancement across Dapps within the Polkadot ecosystem. 

**Other Similar Projects**

Similar products, including zkPass and TLSNotary, are currently in the testnet phase, whereas Gitcoin passport offers a centralised solution. Reclaim protocol is the only solution live on main net that empowers users to generate proofs zk proofs **on a mobile phone in under 10 seconds against their claims** in a privacy-preserving way without making any changes to the server. More specifically, Sui ecosystem recently launched [Sui zk Login](https://sui.io/), which is natively built for Sui and supports providers that work with Open ID Connect built on top of OAuth 2 framework. However, Sui only works with very limited number of logins such as Google/Facebook/Twitch login whereas Reclaim works for any OAuth and non OAuth based logins.

**Why build on Polkadot Ecosystem?**

We are a small team with finite resources, and want to collaborate with ecosystems that demonstrate a genuine commitment to enable use cases that are likely to scale to a billion users. Specifically, we want to build on ecosystems that exhibit a strong desire to leverage Web2 sources to provide seamless user onboarding and bot protection. To our knowledge, there hasn't been any other ecosystem that has declared its dedication to [streamlining user onboarding and experience](https://forum.polkadot.network/t/the-best-ui-ux-in-the-polkadot-ecosystem/370) and [bot protection](https://github.com/w3f/Grants-Program/blob/master/docs/RFPs/epassport-zk-validation.md).

Moreover, our conversation with members of the Web3 Foundation and community regarding the necessity and use cases surrounding user experience and onboarding gave us a clear understanding of Polkadot's ecosystem's priorities which strongly aligns with our approach to enhance user experience through zk login and bot protection.


## Team :busts_in_silhouette:

### Team members

Reclaim Protocol is built by the team at CreatorOS Inc. We are a 20+ member engineering and web3 product development & research team including ZKP researchers and with previous affiliations to Stanford, Microsoft, Meta and Google . We have also built - [Questbook.app](http://Questbook.app), an industry leading on-chain grants management tool that has been/is being used by some of the major L1/L2s including Polygon, Solana, Compound, Arbitrum, and TON, among others.  CreatorOS is a YC W21 company.

- Madhavan Malolan : CEO, Reclaim Protocol
    - Building in crypto since 2016.
    - Among first 5 contributors to Plasma (ethereum scaling solution) specifications.
    - Open source contributor.
    - ex-Microsoft, Computer Science IIIT-H.
    - [LinkedIn.](https://www.linkedin.com/in/madhavanmalolan/) [Github](https://github.com/madhavanmalolan)
- Abhilash Inumella : Co-founder, Leads Product
    - Building in Crypto since 2019.
    - ex-CEO of Samosa Labs (10M users, funded by Sequoia, Xiaomi).
    - Ex-Google, Ex-Facebook, Computer Science IIIT-H.
    - [LinkedIn](https://www.linkedin.com/in/abhilash-inumella-89a92421/).
    
- Max Allman, Mechanism Design Researcher
    - PhD from Stanform in Mechanism Design and Game Theory
    - Co- author of the [Reclaim Whitepaper](https://drive.google.com/file/d/1wmfdtIGPaN9uJBI1DHqN903tP9c_aTG2/view)
    
- [Kirill Kutsenok](https://www.linkedin.com/in/kirill-kutsenok/), Cryptography & Security Researcher
- [Adhiraj](https://www.linkedin.com/in/adiwajshing/) Singh: Lead Developer
- [Sweta](https://www.linkedin.com/in/sweta-shaw/) Shaw: Developer Relations
- Aleksai Ermishkin: Lead Blockchain Developer


### Contact

Contact Name : Ruchil Sharma 
Contact Email - ruchil@creatoros.co
Website - https://www.reclaimprotocol.org/

### Legal Structure

- **Registered Address:** 2nd Floor, Ellen L. Skelton Building, Fishers Lane, Road Town,Tortola, British Virgin Islands, VG 1110.
- **Registered Legal Entity:** Questbook International Inc

### Team's experience

Reclaim Protocol is built by the team at CreatorOS Inc. We are a 20+ member engineering and web3 product development & research team including ZKP researchers and with previous affiliations to Stanford, Microsoft, Meta and Google . We have also built - [Questbook.app](http://Questbook.app), an industry leading on-chain grants management tool that has been/is being used by some of the major L1/L2s including Polygon, Solana, Compound, Arbitrum, and Ton, among others.  CreatorOS is a YC W21 company.

- Madhavan Malolan : CEO, Reclaim Protocol
    - Building in crypto since 2016.
    - Among first 5 contributors to Plasma (ethereum scaling solution) specifications.
    - Open source contributor.
    - ex-Microsoft, Computer Science IIIT-H.
    - [LinkedIn.](https://www.linkedin.com/in/madhavanmalolan/) [Github](https://github.com/madhavanmalolan)
- Abhilash Inumella : Co-founder, Leads Product
    - Building in Crypto since 2019.
    - ex-CEO of Samosa Labs (10M users, funded by Sequoia, Xiaomi).
    - Ex-Google, Ex-Facebook, Computer Science IIIT-H.
    - [LinkedIn](https://www.linkedin.com/in/abhilash-inumella-89a92421/).
    
- Sriharsha Karamchati : Co-founder, Leads Community
    - Compound Grants Program 2.0 Lead
    - Building communities since 2019.
    - ex-Intuit, Computer Science IIIT-H.
    - [LinkedIn](https://www.linkedin.com/in/sriharsha-karamchati-0730947b/)
- Subhash Karri : Co-founder, Leads BD and Partnerships
    - Investing in crypto since 2017.
    - Led Mytrah Solar Energy $400M AUM co.
    - MBA from ISB, Computer Science IIIT-H.
    
- Max Allman, Mechanism Design Researcher
    - PhD from Stanform in Mechanism Design and Game Theory
    - Co- author of the [Reclaim Whitepaper](https://drive.google.com/file/d/1wmfdtIGPaN9uJBI1DHqN903tP9c_aTG2/view)
    
- [Kirill Kutsenok](https://www.linkedin.com/in/kirill-kutsenok/), Cryptography & Security Researcher
- [Adhiraj](https://www.linkedin.com/in/adiwajshing/) Singh: Lead Developer
- [Sweta](https://www.linkedin.com/in/sweta-shaw/) Shaw: Developer Relations
- Aleksai Ermishkin: Lead Blockchain Developer

### Team Code Repos

Reclaim Protocol - https://github.com/reclaimprotocol

Questbook - https://github.com/questbook

SDK - https://docs.reclaimprotocol.org/


### Team LinkedIn and GitHub Profiles

Madhavan Malolan : CEO, Reclaim Protocol

- Building in crypto since 2016.
- Among first 5 contributors to Plasma (ethereum scaling solution) specifications.
- Open source contributor.
- ex-Microsoft, Computer Science IIIT-H.
- [LinkedIn.](https://www.linkedin.com/in/madhavanmalolan/) [Github](https://github.com/madhavanmalolan)
- Abhilash Inumella : Co-founder, Leads Product
    - Building in Crypto since 2019.
    - ex-CEO of Samosa Labs (10M users, funded by Sequoia, Xiaomi).
    - Ex-Google, Ex-Facebook, Computer Science IIIT-H.
    - [LinkedIn](https://www.linkedin.com/in/abhilash-inumella-89a92421/).
    
- Max Allman, Mechanism Design Researcher
    - PhD from Stanform in Mechanism Design and Game Theory
    - Co- author of the [Reclaim Whitepaper](https://drive.google.com/file/d/1wmfdtIGPaN9uJBI1DHqN903tP9c_aTG2/view)
    
- [Kirill Kutsenok](https://www.linkedin.com/in/kirill-kutsenok/), Cryptography & Security Researcher
- [Adhiraj](https://www.linkedin.com/in/adiwajshing/) Singh: Lead Developer
- [Sweta](https://www.linkedin.com/in/sweta-shaw/) Shaw: Developer Relations
- Aleksai Ermishkin: Lead Blockchain Developer


## Development Status :open_book:

With Reclaim protocol now live on production, we are keen on working with Polkadot to build identity specific use cases more specifically zklogin and proof of personhood to fast forward Polkadot’s growth. Moreover, after speaking with the members of Web3 foundation and community members, we are confident that the proposed use cases align perfectly fit with the Polkadot’s ecosystems current focus areas such as ZkLogin, [bot protection](https://github.com/w3f/Grants-Program/blob/master/docs/RFPs/epassport-zk-validation.md)**,** [streamlining user onboarding and experience](https://forum.polkadot.network/t/the-best-ui-ux-in-the-polkadot-ecosystem/370),  [epassport](https://github.com/w3f/Grants-Program/blob/master/docs/RFPs/epassport-zk-validation.md) etc. 

Reclaim protocol has received critical acclaim and appreciation from leading crypto researchers such as [Andrew Miller](https://twitter.com/socrates1024), [Sreeram Kannan](https://twitter.com/sreeramkannan) etc. Our team, primarily comprised of core crypto researchers and talented engineers, has dedicated ~ two years, split between research and development, to advance Reclaim protocol to its production stage. We are confident in our abilities to build zkLogin and proof of personhood on top of Polkadot using Reclaim. We plan to adopt a milestone based iterative approach across different phases in order to achieve the stated goals of this proposal, while also continually obtaining feedback from the Polkadot foundation and community regarding our progress.

Reclaim Protocol - https://github.com/reclaimprotocol

Questbook - https://github.com/questbook

SDK - https://docs.reclaimprotocol.org/

Whitepaper - https://drive.google.com/file/d/1wmfdtIGPaN9uJBI1DHqN903tP9c_aTG2/view

Website - https://www.reclaimprotocol.org/

Explainer Blogposts - https://blog.reclaimprotocol.org/

## Development Roadmap :nut_and_bolt:

### **Phase - 1**

In the first phase of the project, we will integrate the Reclaim protocol with Polkadot to establish the proof of personhood and bot protection infrastructure, along with publishing comprehensive documentation to assist developers in enabling these use cases within their dApps.

**Total Estimated Duration** 
~ 3 weeks

**Cost**

$45,000

We will offer the Polkadot ecosystem ongoing development support for four months post-integration led by Integration Support Developer and provided by Reclaim Protocol.

**Milestones, Deliverables and FTEs required**

1. Milestone - 1 : Reclaim Polkadot Integration - $40,000, FTE - 3

Deliverables

| Number | Deliverable | Specification |
| --- | --- | --- |
| 0a. | License | GPL  |
| 0b. | Documentation  | We will provide both inline documentation of the code |
| 0c.  | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. |
| 0d.  | Docker  | We will provide Dockerfile(s) (if any) that can be used to test all the functionality delivered with this milestone. |
| 1.  | Integrating Reclaim Protocol with Polkadot | We will deploy Reclaim contracts as a  pallet on Polkadot in RUST, ensuring compatibility with Polkadot's runtime environment. Currently, the Reclaim contracts are implemented in Solidity. The Solidity code can be found https://github.com/reclaimprotocol/solidity-sdk/blob/main/contracts/Reclaim.sol#L229C11-L229C22 |
| 2.  | Optimising zkProofs  | We will optimize zkProof verification for Polkadot’s constraints, including time, gas and computational resource efficiency. |
| 3.  | Integration and Testing  | We will develop and execute a suite of tests, including unit, integration, and stress tests, to validate the functionality and performance. Testing will be automated using a CI/CD pipeline to ensure that each build is verified, which will include code coverage and performance benchmarks.|

2. Milestone - 2: Comprehensive documentation, blogposts, and community calls within the Polkadot ecosystem  - $5,000, FTE - 2

Deliverables

| Number | Deliverable | Specification |
| --- | --- | --- |
| 0e. | Article | We will publish an article/workshop that explains this integration  |
| 1.  | Detailed Documentation and Guides  | We will publish detailed documentation, blogposts and participate in atleast 2 community calls to educate, seed ideas to the Polkadot developer community about how to use Reclaim Protocol for implementing Proof of Personhood and Bot protection primitives within their Dapps. Documentation will include a technical guide, API references, and example use cases to facilitate developer integration. |

### **Phase - 2**

After laying out the proof of personhood/bot protection infrastructure on top of Polkadot, in phase - 2, we will implement zk Login on Polkadot and publish comprehensive documentation and guides 

**Total Estimated Duration**
~2 months 

**Cost**

$180,000

Milestone - 1: Design and Architecture, Amount - $40,000, FTE: 3

Deliverables

| Number | Deliverable | Specification |
| --- | --- | --- |
| 0b. | Documentation | We will provide both inline documentation of the code |
| 1.  | zklogin Design and Architecture Documentation  | We will publish a comprehensive architecture document detailing the zkLogin system's components, including sequence diagrams for authentication flows, smart contract interactions, data and user flow, and the integration points with Polkadot's Substrate framework. |
| 2.  | API and SDK Requirements Specification | We will publish a detailed specification document that outlines the API endpoints, data models, and SDK functionality required to support zkLogin, including sequence diagrams and use-case scenarios for Dapp developers. |

Milestone - 2: SDK Development - $50,000, FTE: 3

Deliverables

| Number | Deliverable | Specification |
| --- | --- | --- |
| 0a. | License | AGPL |
| 0b. | Documentation | We will provide both inline documentation of the code |
| 0c. | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. |
| 0d. | Docker | We will provide Dockerfile(s) (if any) that can be used to test all the functionality delivered with this milestone. |
| 1.  | SDK Development for zkLogin | We will build a robust SDK to facilitate the integration of zkLogin into Dapps, complete with modular components and clear abstraction layers. |
| 2.  | Detailed Documentation and Tutorials for SDK usage  | We will create in-depth technical documentation, API references, and step-by-step tutorials for the SDKs, ensuring they are accessible to developers with varying levels of expertise. |
| 3.  | Publishing SDK Testing Frameworks  | We will design and implement a suite of automated testing frameworks for the SDKs, including unit, integration, and end-to-end tests, with continuous integration setup to validate all code commits. |

Milestone - 3: Testing and Security Audits - $50,000, FTE: 3

Deliverables

| Number | Deliverable | Specification |
| --- | --- | --- |
| 0c. | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. |
| 1.  | Security audit of zk Login implementation  | We will contract a reputable third-party security firm to conduct an exhaustive security audit of the zkLogin implementation, including smart contracts and integration layers, with a detailed report of findings and remediation strategies. For instance, https://www.zksecurity.xyz/blog/posts/reclaim/ of Reclaim protocol. We are working closely with them to get other modules audited.  |
| 2.  | Integration Testing with Polkadot  | We will execute a series of integration tests to ensure that the zkLogin system works seamlessly within the Polkadot ecosystem, including cross-chain interactions and transaction handling. |
| 3.  | Performance Testing and Optimization | We will perform comprehensive performance testing to benchmark and optimize the zkLogin system, ensuring it meets the scalability and efficiency standards required for Polkadot's environment. |

Milestone - 4: Dapp Builder Toolkit - $40,000, FTE: 3

Deliverables

| Number | Deliverable | Specification |
| --- | --- | --- |
| 0a. | License | AGPL |
| 0b. | Documentation | We will provide both inline documentation of the code |
| 0c. | Testing and Testing Guide | Core functions will be fully covered by comprehensive unit tests to ensure functionality and robustness. |
| 0d. | Docker | We will provide Dockerfile(s) (if any) that can be used to test all the functionality delivered with this milestone. |
| 1.  | Creating Dapp Builder Toolkit  | We will create and publish a toolkit for Dapp builders including templates, UI/UX components, testing tools, and other utilities to aid developers in building, testing, and deployment purposes. It will also include examples, best practices, troubleshooting guides, and community-driven resources to help Dapp developers at different stages of the development lifecycle |
| 2.  | Developer Advocacy, Educational Content, and Documentation  | We will host online workshops/webinars for Dapp builders to educate them about zklogin, toolkit, SDKs,  and Reclaim protocol  |
| 3.  | Community engagement and support channels  | We will create community engagement and support channels on Discord/Telegram for developer support including regular AMAs, feedback sessions, and contribution guides. |

### Summary

1. Milestone - 1: $40,000
2. Milestone - 2: $5,000
3. Milestone - 3: $40,000
4. Milestone - 4: $50,000
5. Milestone - 5: $50,000
6. Milestone - 6: $40,000

Total: $225,000 in DOTs

We request the DOT amount to be calculated based on the [7-day average](https://polkadot.subscan.io/tools/charts?type=price), starting from the day of submission.


## Future Plans

Reclaim Protocol is built by the team at CreatorOS Inc. We are a 20+ member engineering and web3 product development & research team including ZKP researchers and with previous affiliations to Stanford, Microsoft, Meta and Google. Creatoros is a YC’21 company. Our long-term vision is to unlock a new design space empowering builders to build novel solutions that leverage the identity and credentials of users which they have accrued over time all over the internet. We are also keen to engage closely with the ecosystems/partners who share our vision and can help us realise it. 

To accomplish this, our immediate goal is to provide a seamless Reclaim integration experience to all developers and users using Reclaim by streamlining its various touchpoints such as developer documentation, Reclaim SDKs, developer journey, user journey, etc. 



