# Pi Squared: Bringing All Programming Languages to Web3

**Speakers:** Grigore Rosu - Pi Squared


*Upload Date: 20250301*

*Source: [https://www.youtube.com/watch?v=hIzcUoEZCVY](https://www.youtube.com/watch?v=hIzcUoEZCVY)*

Here's a comprehensive summary of the YouTube video "Pi Squared: Bringing All Programming Languages to Web3 | Grigore Rosu - Pi Squared," based on the provided transcript:

**1. Main Points:**

*   **Pi Squared's Mission:** To make all programming languages accessible to Web3 developers, addressing the issue of ecosystem fragmentation.
*   **Universality as the Solution:** Pi Squared aims to achieve universality at three levels: programming languages/program execution, verifiability/proof mechanisms, and distributed consensus protocols.
*   **The Universality Stack:** This stack comprises three components: Universal Language Machine (ULM), Universal Settlement Layer (USL), and Universal Consensus Protocol (UCP).
*   **Universal Language Machine (ULM):** A blockchain architecture that allows developers to write smart contracts in *any* programming language (existing or new).  It uses the K Framework.
*   **Universal Settlement Layer (USL):** Enables the generation of proofs of execution for any programming language, supporting cross-ecosystem proofs. Offers fast and low-latency settlement. It supports mathematical proofs and zero-knowledge proofs.
*   **Universal Consensus Protocol (UCP):** A consensus protocol for claims that are true, *not* based on a total order of transactions.  Achieves consensus "at the speed of light."
*   **Correctness and Performance:** Pi Squared leverages formal semantics and the K Framework to achieve mathematically verifiable correctness *and* high performance.
*   **ZK-Proof of Mathematical Proof:** The system generates zero-knowledge proofs of the underlying mathematical proofs of program execution correctness.
*   **Open Source and Benchmarking:** The system is designed with openness in mind and is used in a large ZK-VM benchmark.

**2. Key Insights:**

*   **Fragmentation is a Major Problem:**  The Web3 space suffers from a significant fragmentation problem, with different blockchains, programming languages, and ecosystems competing for users and liquidity. This negatively impacts user experience.
*   **Formal Semantics are Key:**  The core of Pi Squared's approach relies on the use of *formal semantics*.  Every programming language is treated as a mathematical theory. This rigorous mathematical foundation enables automated generation of tools (interpreters, compilers, verifiers) and ensures execution correctness.
*   **"Proof of Proof" Concept:**  Instead of directly sharing large, complex mathematical proofs of execution (which would be resource-intensive), Pi Squared generates *zero-knowledge proofs* of the *existence* of these mathematical proofs. This provides very high assurance of correctness without the computational overhead of handling the full proofs directly.  ZK proofs are just "proofs that mathematical proofs exist".
*   **Separation of Computation and Cryptography:**  Pi Squared separates the computational aspects (program execution, formal verification) from the cryptographic aspects (zero-knowledge proof generation).  This allows for optimization of each independently.
*   **Universality Doesn't Mean One Language:** Pi Squared advocates for using *any* language, not creating yet another "ultimate" language.  This contrasts with approaches that attempt to unify everything through a single language.
*   **Performance Gains:**  The rigorous mathematical approach, combined with optimizations in the K Framework, results in significant performance improvements (15x faster than before the talk was prepared). This is achieved through one year of engineering efforts.

**3. Practical Takeaways:**

*   **Developers Can Use Familiar Languages:** Web3 developers can use their existing skills and preferred programming languages without needing to learn new, blockchain-specific languages.
*   **Reduced Development Barriers:** Lowering the entry barriers for developers can drive greater innovation and adoption in the Web3 space.
*  **The value of formal semantics**. Developers are accustomed to discussing program behavior via informal means. The presentation clarifies that without formal semantics of the language, there's no way to truly discuss correctness.
*   **Improved Trust and Security:** The provable correctness and verifiability of Pi Squared's system offer significantly enhanced trust and security for Web3 applications.
*   **Faster Transactions:** The Universal Consensus Protocol (UCP) promises near-instant finality, dramatically improving the speed of Web3 applications.
*   **Cross-Chain Interoperability Potential:** The universal settlement layer and proof mechanisms facilitate communication and interaction between different blockchains, improving interoperability.
*  **Check out Pi Squared**: view the demos on YouTube and visit their booth.

**4. Additional Notes:**

* Grigore Rosu emphasizes his academic background and the long history of research (since 2003) behind the K Framework, highlighting its rigor and maturity, especially in the area of formal methods. The company was formed in 2023, at the same time of the ETHDenver conference last year.
*   The presentation strongly pitches the *necessity* of formal methods and mathematical proofs for true program correctness, contrasting this with the more common, less rigorous approaches used in software development.
*   The phrase "speed of light" is used metaphorically to represent near-instantaneous consensus, related to the minimal communication (round-trip message) required between client and verifier.
*  The Pi Squared team integrated with Wormhole using USL as an alternative to the Guardians.
*   The "ULM blockchain architecture" is still in the lab as a proof of Concept.