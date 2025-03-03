# Challenges of Bringing a zkTrie to the OP Stack

**Speakers:** Jan Gorzny - Zircuit


*Upload Date: 20250301*

*Source: [https://www.youtube.com/watch?v=HydzerzxNHA](https://www.youtube.com/watch?v=HydzerzxNHA)*

Here's a comprehensive summary of the YouTube video "Challenges of Bringing a zkTrie to the OP Stack | Jan Gorzny - Zircuit", formatted as requested:

**1. Main Points:**

*   Zircuit is building a zero-knowledge (ZK) rollup on the OP Stack (but not on the Superchain).
*   The core challenge discussed is replacing the OP Stack's default Merkle Patricia Trie (MPT) with a ZK-friendly alternative, specifically a zkTrie that uses the Poseidon hash function.
*   The MPT, with its use of Keccak-256, is inefficient for ZK proofs due to the high computational cost of proving Keccak operations within a ZK circuit. Poseidon is significantly more ZK-friendly.
*   Replacing the MPT is extremely complex because the MPT is deeply integrated into *every* core component of the OP Stack (op-node/sequencer, op-geth, op-proposer, derivation, fault proofs, etc.).
*    Zircuit implemented a "flexible approach". The system can operate using both MPT and zkTrie, publishing MPT roots on-chain and providing ZK proofs of the zkTrie.
* This dual-trie approach maintains compatibility with existing OP Stack tooling (which expects MPT) while reaping the performance benefits of the ZK-friendly trie for proof generation.
*   Zircuit plans to open-source their modified OP Stack codebase.
* Long term there is interest is adopting a general purpose zkVM, such as Risc0.
* The talk emphasizes how deeply embedded the state trie is within an EVM rollup, making changes challenging, but crucial for ZK rollup efficiency.

**2. Key Insights:**

*   **State Trie as a Bottleneck:** The speaker highlights that the state trie, which stores account balances, contract code, and other essential data, is a central component that *every* part of a rollup interacts with constantly. Therefore, its efficiency is critical for the overall performance of the rollup.
*   **Keccak-256 vs. Poseidon:**  The presentation explains the fundamental difference between the hash functions used in the standard MPT (Keccak-256) and the zkTrie (Poseidon).  Keccak-256, while a strong cryptographic hash function, is computationally expensive to prove within a ZK-SNARK/STARK.  Poseidon, designed specifically for ZK proofs, is substantially faster to compute *inside a proving system*. This difference in proving cost is the driving force behind the change.
*   **Pervasiveness of the MPT in the OP Stack:** The speaker emphasizes that the MPT isn't just "one component" that can be swapped out.  It's deeply ingrained in how the OP Stack handles state, withdrawals, transactions, and block processing. Changes to the MPT require extensive modifications across multiple parts of the codebase. This shows a high level of coupling.
*   **Compatibility vs. Efficiency Trade-off:** Zircuit's "flexible approach" represents a crucial compromise.  They achieve ZK performance gains without sacrificing immediate compatibility with the broader OP Stack ecosystem. Tools and infrastructure built around the MPT will continue to function, which, in turn, helps adoption.
*   **Future Modularity (and Vitalik's Tweet):** The speaker briefly touches on the long-term vision of a more modular OP Stack and even the possibility of Ethereum itself adopting a ZK-friendly hash function (like Poseidon).  This highlights the broader industry trend towards ZK-proofs and more efficient, verifiable computation. Vitalik's mentioned Tweet supports this future vision.

**3. Practical Takeaways:**

*   **For Developers Building on OP Stack:** Understand the centrality of the state trie (currently MPT) and how deeply intertwined it is with every part of the OP Stack.  Any modifications require careful consideration of these dependencies.  Zircuit's work exemplifies this.
*   **For ZK Rollup Developers:** The MPT vs. zkTrie dilemma is a core challenge for *any* ZK rollup built on existing EVM infrastructure (not just the OP Stack). The presentation provides a case study in how to approach this challenge.
*   **Consider ZK-Friendly Primitives from the Outset:** If designing a new system, choose cryptographic primitives (like hash functions) that are optimized for zero-knowledge proofs to avoid costly refactoring later.
*     **Open-Source Contribution is Key:** Zircuit's intention to open-source their modifications is a valuable contribution.  It can serve as a reference implementation for other teams tackling similar challenges and stimulate further innovation.
*  **Anticipate ecosystem changes**: Future changes, including Ethereum mainet switching to a zkVm or zk-friendly hashing function, would necessitate further adjustments to the OP stack.

**4. Additional Notes:**

*   The speaker assumes a basic understanding of rollups, ZK proofs, and the OP Stack.
*   The "flexible approach" is a bridging strategy. It allows Zircuit to launch and function while minimizing disruption, not their long-term solution.
* The talk provides a good practical example of how deep cryptographic choices (like the hash function) can have significant ramifications throughout the application and stack.