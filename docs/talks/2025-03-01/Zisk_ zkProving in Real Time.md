# Zisk: zkProving in Real Time

**Speakers:** Jordi Baylina - Polygon


*Upload Date: 20250301*

*Source: [https://www.youtube.com/watch?v=N4JibRTHsVc](https://www.youtube.com/watch?v=N4JibRTHsVc)*

Here's a summary of the YouTube video "Zisk: zkProving in Real Time | Jordi Baylina - Polygon," based on the provided transcript:

**1. Main Points:**

*   **Introduction of Zisk:** Zisk is a new, open-source, 64-bit RISC-V zkVM (Zero-Knowledge Virtual Machine) developed by Jordi Baylina and the Polygon team.  It's designed for real-time zero-knowledge proof generation.
*   **Rust-Based Development:**  Developers can write programs and circuits in Rust, which are then compiled to a RISC-V executable (ELF file). This makes ZK proof development more accessible.
*   **Real-Time Proof Generation:** Zisk's primary goal is to minimize latency and generate proofs as quickly as possible, even if it slightly increases the cost.
*   **Decentralized and Parallel Processing:** Zisk uses a modular architecture called "vOPs" (virtual OPs) that allows the proof generation process to be split into smaller, independent "sub-proofs." These can be processed concurrently on multiple servers, enabling horizontal scaling and decentralization.
*   **Proof Aggregation:**  A "recursor" component allows the aggregation of multiple sub-proofs into a single, final proof. This significantly reduces the verification burden.
*   **Based on Existing Polygon Tech:** Zisk leverages the technology and experience gained from Polygon's previous projects, including Hermes, Plonky2, and Plonky3.
*   **Use Cases:**  The primary use cases discussed is validating Ethereum blocks and rollup blocks in real-time, facilitating interoperability, and enabling fast cross-chain transfers.  It is emphasized how it has wider applicability.
* **Open Source:** Zisk code is publicly available.

**2. Key Insights:**

*   **Shifting Paradigm from Monolithic Proofs:** The traditional approach to zkVMs often involves creating a single, large, complex proof. Zisk's vOPs system fundamentally changes this by breaking the proof into smaller, manageable, and parallelizable units.
*   **"Bus" for Inter-Process Communication:** The vOPs communicate via a "bus," where one state machine can "assume" a result and add it to the bus. Other state machines can then "subtract" that result, ensuring consistency and correctness. This is a novel method for handling dependencies between the sub-proofs.  This concept is central to handling continuations and memory alignment.
*   **Trade-off: Speed vs. Cost:** Baylina explicitly states they prioritize proof generation *speed* over minimizing proof *cost*. While the costs are already "very low," the focus on real-time generation is paramount.
*   **RISC-V as a Strategic Choice:** Choosing the RISC-V architecture allows for broad compatibility and leveraging existing compiler toolchains (like Rust's). It also makes it possible to prove the execution of arbitrary programs, not just specific circuits.
*   **Importance of Real-Time Proofs for Scalability:** The ability to generate proofs quickly is critical for scaling solutions like rollups.  By proving blocks in real-time, cross-rollup communication and asset transfers can be made much faster and more secure.  It also allows for one chain to prove the correctness of another *without* needing full node infrastructure, which is impossible at scale.
*   **Proof Packing:** Within the recursor, proofs are "packed" efficiently to minimize space and ensure that no computational resources ("cells") are wasted during the aggregation process.
* **Modularity is Key to Optimization and Parallelism.** The architecture is designed from the ground up to support breaking down a large proving task into smaller pieces that can be computed in parallel.

**3. Practical Takeaways:**

*   **Explore Zisk for Real-Time Applications:** If you're working on a project that requires real-time zero-knowledge proofs (e.g., fast cross-chain bridges, decentralized exchanges with instant finality, privacy-preserving computations), Zisk is a viable and cutting-edge option to consider.
*   **Leverage Rust Expertise:**  If you have Rust developers on your team, Zisk provides a low barrier to entry for building ZK applications.
*   **Contribute to the Open-Source Project:** Since Zisk is open-source, developers can contribute to its development, report bugs, or propose improvements.
* **Consider Decentralized Proving Networks:** Zisk's architecture lends itself well to the creation of decentralized proving networks, where multiple independent entities contribute to generating proofs. You can think about how that might be applicable in a system.
* **Start Experimenting, but Be Mindful of Audit Status**: While available and working, the presenter notes that there are still some audits and improvements in the backlog.

**4. Additional Notes:**

*   The presentation is quite technical, delving into the specifics of Zisk's internal architecture (vOPs, bus, recursor, etc.).
*   The presenter emphasizes that Zisk is a general-purpose zkVM, not limited to blockchain applications.
*   The presentation highlights current performance metrics (e.g., proving an Ethereum block in under 12 seconds), which are likely to improve further.
*   While GPU acceleration is mentioned as being in the "backlog" and "not public yet," it's clearly a near-term goal. This will dramatically improve performance.
* The presenter ends by encouraging interested parties to engage with them.
*   The speaker mentions specifically 300Mhz speed for single processor, but *many* sub-proofs can be computed in parallel.