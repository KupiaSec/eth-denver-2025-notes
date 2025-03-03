# Parallelizing EVM Transaction Processing

**Speakers:** Gary Schulte - Besu


*Upload Date: 20250301*

*Source: [https://www.youtube.com/watch?v=NAAybEFOSMs](https://www.youtube.com/watch?v=NAAybEFOSMs)*

Here's a comprehensive summary of the YouTube video "Parallelizing EVM Transaction Processing | Gary Schulte - Besu," based on the provided transcript:

**1. Main Points:**

*   **EVM Scalability Challenges:**  Ethereum's execution layer (Layer 1) faces increasing demands for faster transaction processing due to higher block gas limits and new cryptographic primitives.  Efficient use of the 4-second execution window within each 12-second slot is crucial.
*  **Sequential vs. Parallel Execution:** The Ethereum Yellow Paper specifies sequential transaction execution to ensure deterministic results across all clients.  However, EIPs 98 and 658 (post-Byzantium) relaxed the requirement for intermediate state roots in transaction receipts, opening the door for parallel execution.
*  **Optimistic Parallel Execution:** Besu leverages optimistic parallel execution. Transactions execute concurrently against copies of the World State.  Conflicts (where transactions access/modify the same state) are detected and resolved through re-execution.
* **Bonsai Tries for Efficient State Management:**  Besu uses Bonsai Tries as its storage format.   Bonsai's key features, such as in-memory overlays and accumulator data structures, facilitate parallel execution and conflict detection. The accumulator tracks reads, writes, and updates for each world state.
*  **Conflict Detection and Resolution Strategy:**  Besu prioritizes efficient conflict detection. It performs account-level checks (nonce, balance, code) first, followed by contract storage checks if necessary. Transactions with detected conflicts are re-executed serially against the updated intermediate state.
*  **Performance Gains and Trade-offs:** Parallel execution in Besu can significantly increase transactions per second, but it's hardware and block-dependent.  It introduces overhead through conflict detection and potential re-execution. It is currently considered experimental.
* **Hardware Recommendations.** The current optimal experience and recommendation is for 8 cores (4 cores with hyperthreading)

**2. Key Insights:**

*   **Relaxation of Serial Execution:**  The crucial insight is that the *necessity* of strict, in-order serial execution was relaxed.  The *output* must be *as if* it were serially executed, but the underlying mechanism doesn't have to be.
*   **Software Transactional Memory (STM):** Bonsai Tries effectively provide a form of Software Transactional Memory.   This is a concurrency control mechanism that allows optimistic parallel execution against shared memory (the World State in this case). Each world state is like a transactional memory instance.
*   **Accumulator as a Conflict Oracle:** The accumulator is the core of the conflict detection mechanism.  By tracking *all* accesses to the World State (reads and writes), it provides a concise summary of how a transaction interacted with the state.  Comparing accumulators allows Besu to quickly determine if two transactions conflict.
*   **Prioritized Conflict Checks:** Besu's multi-stage conflict checking (account-level first, then contract storage if necessary) is a performance optimization.  It aims to quickly identify conflicts with minimal overhead.
*   **"Fail-Fast" Approach:** The conflict detection is designed to "fail fast." Cheaper checks are performed first. If those checks reveal a conflict, more expensive checks are avoided.
*  **FallBack to Serial:** Parallel execution is an optimization, not a replacement for serial. A fail-safe mechanism in place ensures that if the state root calculated after optimization does not matche the state root in the block header all transactions are exectued serially to ensure correctness.
*   **Hardware and Block Composition Matter:** The benefits of parallel execution are not guaranteed. They depend on the hardware (number of cores) and the nature of the transactions within a block (degree of state contention).  A block with many transactions accessing the same state will see less benefit.

**3. Practical Takeaways:**

*   **Enable Parallel Execution in Besu (Experimental):** For high-performance validator nodes or L2 execution clients using Besu, consider enabling the parallel execution feature (currently experimental).  Monitor its performance to assess its impact. *Do not do this until Besu v25.3 release*.
*   **Hardware Considerations:**  To get the best results, consider a machine with at least eight logical cores (or four physical cores with hyperthreading).  More cores *may* not offer significant additional benefit beyond this point.
*  **Monitor Performance.** Because the performance gains are not guarenteed and the approach uses more memory, users should monitor the performance.

**4. Additional Notes:**

*   The presenter emphasizes that this parallel execution is *not* related to Layer 2 scaling solutions.  It's an optimization specifically for Layer 1 execution clients like Besu.
*	The presenter mentions that Nethermind also has a feature called 'Pre-Warming' that provides optimizations by cashing computations.
*   The video focuses primarily on *how* Besu implements parallel execution. The presenter's real-world performance numbers (60-65% of transactions executed in parallel, 160-170 million gas/second throughput on a commodity NUC) provide a concrete example, though results will vary.
*   The presentation highlights the ongoing evolution of Ethereum.  Changes to the protocol (like those in EIPs 98 and 658) can have significant impacts on how execution clients can be optimized.
* The presentation is targeted towards advanced users, validators, and others running ethereum nodes.