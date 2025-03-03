# Kadena POW: Scaling EVM With Parallel Chains

**Speakers:** Stuart Popejoy & John Wiegley - Kadena


*Upload Date: 20250226*

*Source: [https://www.youtube.com/watch?v=MChDGJYYsCE](https://www.youtube.com/watch?v=MChDGJYYsCE)*

Here's a summary of the YouTube video "Kadena POW: Scaling EVM With Parallel Chains | Stuart Popejoy & John Wiegley - Kadena," formatted as requested:

**1. Main Points:**

*   **Introduction to Kadena:** Kadena is a layer-one, proof-of-work (PoW) blockchain designed for scalability.
*   **Chainweb Architecture:** Kadena uses a unique "Chainweb" architecture that braids multiple, parallel PoW chains together.
*   **True Parallelism:** Unlike sharding or optimistic execution, Chainweb offers *true* parallel processing, similar to having multiple CPUs working simultaneously, rather than threads within a single CPU.
*   **Scaling and Security:** Adding more chains to the Chainweb network *increases* both throughput *and* security due to the nature of PoW and the expander graph structure.
*   **EVM Compatibility:** Kadena is launching "Chainweb-EVM," bringing its parallel-chain scaling solution to the Ethereum Virtual Machine ecosystem.
*   **Kadena-EVM**: Twenty new Kadena chains will run fully standard EVM and solidity after they fork to 50 chains.
*	 **Mint/Burn between Chains:** Assets are not locked up in a bridge when using the Kadena Network.
*   **Developer Preview:** A developer preview of Chainweb-EVM is available, allowing developers to deploy contracts and test the parallel-chain functionality.
*   **$50 Million Grant Program:** Kadena announced a $50 million grant program to encourage development on the Chainweb-EVM platform.
*   **Addressing Ethereum Scaling Issues:** Chainweb-EVM directly addresses the problems of centralization and fragmentation inherent in many current Ethereum scaling solutions (like rollups).
*   **Pact Smart Contract Language:** Kadena uses the "Pact" smart contract language for its native chains, which is designed for security and formal verification, but the new EVM chains support Solidity.
* **Proven Technology**: Kadena's Chainweb has been running in production without interruption for five years, and has undergone testing through attacks and disruptions.

**2. Key Insights:**

*   **Proof-of-Work for Scalability:**  Kadena leverages the inherent properties of Proof-of-Work (its "smooth divisibility") to *enhance* security as the network scales.  This contrasts with the common narrative that PoW is inherently unscalable.  The hash rate is distributed smoothly across all chains, eliminating miner competition.
*   **Expander Graph:** The core of Chainweb's functionality is an "expander graph," a mathematical construct that allows each chain to act as an oracle of the others' histories.  This enables trustless cross-chain communication *without* requiring a central hub or validator network.
*   **True Burn and Mint:**  Kadena's cross-chain transfers involve the *actual* burning and minting of tokens, maintaining a zero-sum balance. This is significantly different from the "lock and mint, burn and release" approach commonly used in bridges, which are often centralized and vulnerable points of failure.
*   **Gas Predictability:**  By adding more chains as demand increases, Kadena aims to provide stable and predictable gas prices, preventing the spikes that can price users out of other networks.
*   **First-Mover Advantage:**  The presenters emphasize that Chainweb-EVM is a very new ecosystem, presenting significant opportunities for developers to establish themselves.
*   **Simplicity as a Core Principle:** Kadena stresses simplicity in blockchain design, arguing that the complex solutions that have emerged for scaling Ethereum have compromised the original goals of decentralization and accessibility.

**3. Practical Takeaways:**

*   **Explore the Developer Preview:** Developers interested in exploring parallel-chain scaling can immediately access the Chainweb-EVM developer preview.
*   **Join the Telegram Group:** Kadena encourages participation in their Telegram group (linked via a QR code in the presentation) for support, updates, and potential giveaways.
*   **Visit the Kadena Booth:** Attendees of ETHDenver were encouraged to visit Kadena's booth to see a live demonstration and interact with the team.
*   **Apply for the Grant Program:** Developers with project ideas relevant to Chainweb-EVM are encouraged to apply for the $50 million grant program.
*   **Port Existing EVM Apps:**  The ease of porting existing EVM/Solidity applications to Kadena is highlighted, making it a potentially attractive option for projects experiencing scaling issues on other platforms.
*   **Consider Pact for Future Projects:** While Chainweb-EVM supports Solidity, developers building on Kadena can leverage Pact for projects requiring high levels of security.

**4. Additional Notes:**

*   The presentation was given at ETHDenver.
*   There is a brief, slightly humorous discussion about avoiding a "live demo" in favor of a pre-recorded video.
*   The presenters, Stuart Popejoy and John Wiegley, have extensive backgrounds in technology and finance, including experience at JP Morgan's blockchain initiative (for Popejoy) and Dfinity (for Wiegley).
* They mention an upcoming Ethereum Improvement Proposal (EIP) to officially document the protocol to share assets across these chains.
* When demand increases on the Kadena chain, they will fork and double the number of chains. There is not limit to the number of times they can fork and increase the number of chains.