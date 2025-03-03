# Deep-Dive Into One-Step Proofs in Arbitrum

**Speakers:** Tsahi Zidenberg - Offchain Labs


*Upload Date: 20250226*

*Source: [https://www.youtube.com/watch?v=J37P0-OYzXk](https://www.youtube.com/watch?v=J37P0-OYzXk)*

Here's a comprehensive summary of the YouTube video "Deep-Dive Into One-Step Proofs in Arbitrum | Tsahi Zidenberg - Offchain Labs", based on the provided transcript:

**1. Main Points:**

*   **Introduction to One-Step Proofs:** The video explains the core concept of one-step proofs in Arbitrum, a crucial component of its optimistic rollup mechanism. It's presented as the most basic way to understand how optimistic rollups like Arbitrum work.
*   **Provable Execution:** Instead of executing computationally heavy tasks directly on Ethereum (which is expensive), Arbitrum executes them off-chain on a deterministic virtual machine called the "Arbitrator." A concise proof of this execution is then submitted to Ethereum.
*   **The Arbitrator VM:** The Arbitrator is a WASM-based virtual machine written in Rust. It's deterministic, hashable, and designed to produce one-step proofs.  Every aspect of the Arbitrator's state (memory, code, stack, program counter) is included in a 32-byte hash.
*   **One-Step Proof Process:** The core process involves taking a known machine state hash, executing a *single* WASM instruction, and then proving the resulting new state hash on-chain (to an Ethereum smart contract).  This proof includes Merkle proofs for necessary data like code segments and stack elements.
*   **Bisection Protocol (Bold Protocol) Implication:** Although not directly the focus, the video makes it explicitly clear that the Bisection, or bold protocol, relies on this one-step proof. Billions of steps are not individually proven; the one-step proof is the fundamental building block for resolving disputes efficiently via that higher-level protocol.
* **Solidity Verification Contract:** A Solidity contract on Ethereum verifies these one-step proofs.  The contract receives the previous state hash and a proof (a byte array), deserializes it, verifies the initial state hash, executes the single instruction *within the Solidity contract*, and verifies the resulting state hash.
* **Stylus Integration:**  The concept of dynamic module loading within the Arbitrator VM is how Stylus (Arbitrum's framework for writing smart contracts in languages other than Solidity) works.
*  **Input and output:** Global state constitutes main input and output of the system.

**2. Key Insights:**

*   **Deterministic Execution is Key:** The entire system hinges on the Arbitrator VM being fully deterministic.  Given the same input and initial state, it will *always* produce the same output and final state hash.  This allows for off-chain execution with on-chain verification.
*   **Hashing as a Commitment:** The 32-byte state hash acts as a cryptographic commitment to the *entire* state of the Arbitrator VM.  Any change, no matter how small, in any part of the VM's state will result in a different hash.
*   **Merkle Proofs for Efficiency:**  The Solidity verifier contract doesn't need the entire state of the Arbitrator VM.  Merkle proofs are used to selectively prove only the parts of the state that are relevant to the specific instruction being executed (e.g., the code for the instruction, the relevant stack elements). This minimizes the data that needs to be provided on-chain.
*   **On-Chain vs. Off-Chain Mirroring:** The Solidity verifier contract essentially *mirrors* the execution of a single instruction of the Arbitrator VM.  This is crucial: the on-chain contract performs the *same computation* as the off-chain VM, but on a much smaller scale (one instruction at a time).
*   **One-Step Proof as the Atomic Unit:** The one-step proof is the fundamental unit of verifiable computation. It's like a single, provable "tick" of the Arbitrum system. The bisection protocol, and thus the entire dispute resolution mechanism, uses the one-step proof.
* **WAVM Instructions:** There is the standard WASM instruction set as well as custom "WAVM" instructions added for functionality specific to Arbitrum, including interacting with the "outside world" (like accessing on chain data.)

**3. Practical Takeaways:**

*   **Understanding Arbitrum's Security Model:** Developers building on Arbitrum (or any optimistic rollup) should understand that the security relies on this provable execution model.  Incorrect off-chain execution *will eventually* be detected and challenged through the dispute resolution process (which uses one-step proofs).
*   **Optimizing for One-Step Proofs (Indirectly):** While developers don't directly interact with one-step proofs when writing typical smart contracts, understanding this underlying mechanism can help in thinking about gas optimization.  Operations that are computationally expensive for the Arbitrator *off-chain* will also be relatively complex to prove *on-chain* within the dispute resolution process. *Fewer* WASM instructions means simpler (and cheaper) proofs if a dispute arises.
*   **Stylus Implications:** The video clarifies *how* Stylus is able to bring Rust (and potentially other languages) to Arbitrum smart contracts.  The dynamic module loading capability of the Arbitrator VM is the key. This gives developers a strong reason to consider Stylus for complex dApps.
*   **Exploring the Nitro Codebase:** The presenter provides a link to the Nitro repository and specifically points out the `proveOneStep` function in the Solidity verifier contract.  This provides a concrete starting point for developers who want to explore the implementation details.
*   **Focus on Determinism in Off-Chain Logic:** If you're building systems that interact with Arbitrum (e.g., creating bridges or oracles), understanding the deterministic nature of the Arbitrator VM is critical.  Any off-chain logic that needs to be provable on Arbitrum must be designed with determinism in mind.

**4. Additional Notes:**

*   The presentation is somewhat "hand-wavy," as the presenter admits, due to the complexity of showing actual code samples in a presentation format.
*   The video focuses on the *mechanism* of one-step proofs rather than the *economic incentives* of the Arbitrum system.  It doesn't go into detail about how validators are rewarded or penalized.
*   The presentation assumes a basic understanding of blockchain concepts like smart contracts, Ethereum Virtual Machine (EVM), and hashing.
*   The example provided (factorial calculation modulo a prime) is a *toy problem* to clarify the concepts of provability and the constraints of on-chain execution.  It's not meant to be a realistic use case.
* This is a very reduced functionality EVM.