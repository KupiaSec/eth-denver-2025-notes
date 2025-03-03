# AI Development on Kite AI, the First Purpose-Built AI Layer 1

**Speakers:** Vikas Pandey - Kite AI


*Upload Date: 20250225*

*Source: [https://www.youtube.com/watch?v=HsE1S5D7YrI](https://www.youtube.com/watch?v=HsE1S5D7YrI)*

Here's a comprehensive summary of the YouTube video "AI Development on Kite AI, the First Purpose-Built AI Layer 1 | Vikas Pandey - Kite AI", broken down into the requested sections:

**1. Main Points:**

*   **Kite AI is a Layer 1 blockchain designed specifically for AI.**  It aims to be a foundational infrastructure for AI models and agents, rather than retrofitting AI onto an existing blockchain.
*   **Kite AI modifies the EVM (Ethereum Virtual Machine).** They are building their own "Kite VM" to incorporate AI compute information directly into the blockchain's processes and state.
*   **Proof of Attributed Intelligence (PoAI).**  Kite AI introduces a novel consensus mechanism that rewards contributors (model developers, data providers, agent creators) based on the usage and attribution of their AI contributions.  This is distinct from Proof of Stake or Proof of Work.
*   **On-Chain AI Data Storage and Execution.** Kite AI aims to store AI model metadata (weights, inference results) on-chain, making it transparent, verifiable, and composable.  It also aims for *on-chain execution* of AI computations, unlike many existing solutions that rely on off-chain processing.
*   **Composable AI Economy.**  The goal is to create a "flywheel effect" where builders publish AI agents/models, consumers use them, and contributors are rewarded based on usage, fostering a self-sustaining ecosystem.
*   **Integration with Existing Web3 Infrastructure.** Kite AI leverages and builds upon existing technologies. It's an Avalanche Sovereign chain using the EVM, and considers integrating with existing AI oracles (like Hyper Oracle and Aura) and decentralized storage solutions (IPFS, Arweave, etc.).
*   **Testnet and Mainnet Launch Plans.**  A testnet has already launched, with a second version planned for the end of March and full availability by Summer.  They aim to hit 1 million wallets on testnet.
* **Focus on fair attribution** The team is creating a system to address model/agent creators not benefiting from others using and building on top of their work.

**2. Key Insights:**

*   **Addressing the Limitations of Current AI in Web3:**  Vikas highlights that existing blockchains (including the EVM) aren't designed to handle AI natively.  They lack the opcodes and data structures to store and process the large datasets and complex computations involved in AI, leading to off-chain solutions that lack transparency and verifiability.
*   **The Need for Native AI Integration:**  Simply adding AI-related functions to an existing blockchain isn't sufficient.  Kite AI's approach is to fundamentally change the virtual machine (Kite VM) to *natively* support AI computations, allowing for on-chain execution, data storage, and a new consensus mechanism that aligns with AI workloads.
*  **Gas Optimization and AI-Specific Opcodes** Gas fees can get very expensive, Kite AI plans to optimize these for AI related transactions, and implement AI specific opcodes to add AI data to the stack.
*   **The Importance of Attribution and Ownership:** The PoAI consensus mechanism is crucial for incentivizing AI contributions.  By rewarding contributors based on provable usage, it creates a sustainable economic model and addresses the problem of model/agent creators not being properly rewarded for the value they create. A key problem today, where large platforms benefit, but agent developers don't.
*   **Composability as a Key Driver of Innovation:**  By storing AI model data and execution results on-chain, Kite AI facilitates composability.  Developers can build upon existing models and agents, creating new solutions and fostering a more collaborative AI ecosystem.
*   **Hybrid On-Chain/Off-Chain Approach:** While the core design is focused on on-chain AI, Kite AI recognizes the practical limitations of storing *all* AI data on-chain.  They are exploring hybrid models where large datasets are stored off-chain (using decentralized storage) but linked to the blockchain via hashes and pointers, ensuring verifiability and provenance.
*   **Security and Incentives:** Kite AI considers a "spam" and other MEV-type prevention system. They have 40+ university, and industry, partnerships.
* **EIP contribution** The team is contributing to an EIP to standardize AI compute on EVM.

**3. Practical Takeaways:**

*   **Developers (AI and Web3):** Start exploring the Kite AI platform and its capabilities.  Consider building AI agents or applications on the testnet and provide feedback.  Engage with the Kite AI community. The Testnet is out, and v2 is due end of March, with mainnet launch planned for Summer.
*   **AI Researchers:**  Explore the implications of PoAI and the potential of on-chain AI for your research.  Engage with the Kite AI team to understand how your work could be integrated or contribute to the platform.
*   **Founders:** If you have a project relating to AI and the blockchain, consider working with Kite AI.
*   **Investors:**  Keep Kite AI on your radar as a potential investment opportunity within the rapidly growing AI x Web3 space.  Evaluate its unique approach and its potential market fit.
*   **General Audience:**  This project demonstrates a significant shift towards a more integrated approach to AI and blockchain.  It highlights the need for specialized infrastructure to support the future of decentralized AI.

**4. Additional Notes:**

*   The presentation is relatively technical, assuming some familiarity with blockchain concepts (EVM, consensus mechanisms, etc.).
*   Vikas is clearly passionate and knowledgeable about the project.
*   The project is ambitious, tackling both the technical challenges of on-chain AI and the economic challenges of creating a sustainable AI marketplace.
*   The success of Kite AI will depend on its ability to attract developers and users, and to deliver on its promise of true on-chain AI execution and composability.
* The project is part of the Avalanche Infra Build Program.
* Go to gokite.ai to learn more.