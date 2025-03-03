# AltVM Scaling Ethereum: SVM vs. MoveVM vs. Parallel EVM

**Speakers:** Keone Hon - Monad Foundation, Shayan |


*Upload Date: 20250301*

*Source: [https://www.youtube.com/watch?v=AZxl-pteljE](https://www.youtube.com/watch?v=AZxl-pteljE)*

Here's a breakdown of the YouTube video "AltVM Scaling Ethereum: SVM vs. MoveVM vs. Parallel EVM...", formatted as requested:

**1. Main Points:**

*   The panel discusses alternative Virtual Machine (VM) designs for scaling Ethereum, focusing on Solana's VM (SVM), Move VM, and Parallel EVM approaches.
*   Representatives from Monad (Parallel EVM), Movement Labs (Move VM), and Soon (SVM) provide insights into their respective projects and design choices.
*   A major theme is the bottleneck of Ethereum's storage layer and the assumptions made about state access costs.
*   Monad's key innovation is a custom, high-performance database designed to optimize state access, enabling optimistic parallel execution and asynchronous execution.
*   Move VM is highlighted for its focus on safety and developer experience, preventing common smart contract vulnerabilities like reentrancy.
*   SVM's main advantages are its existing large developer ecosystem and user adoption.
*   The panel discusses tradeoffs between performance, security, and developer adoption when choosing a VM, and how important EVM compatibility will be.
*   The importance of execution speed as key bottleneck that is being addressed by new VMs, rather than the VM itself.

**2. Key Insights:**

*   **EVM's Performance Limitations:** Lane Rettig (formerly of Ethereum Foundation) expresses skepticism about the EVM's inherent ability to achieve high performance, especially relative to alternative VMs.
    Keone from Monad argues that the *storage layer*, not the EVM instruction set itself, is the primary bottleneck.  EVM limitations are more about the implementations (databases like LevelDB or PebbleDB) and assumptions (like gas limits per block) than the VM design itself.
*   **Monad's Approach:** Monad's approach tackles this storage bottleneck by building a custom database. This allows them to remove assumptions around slow state access, which in turn opens the door for optimistic parallel execution and asynchronous execution.  This aims to massively increase throughput while maintaining a high degree of decentralization, with a public testnet achieving 200-300 TPS.
*   **Move VM's Safety Focus:**  Movement Labs' core philosophy behind using Move is its inherent safety features. The Move language and VM provide "out-of-the-box" type safety and other features that make it more difficult for developers to accidentally introduce vulnerabilities.
*   **SVM's Adoption Advantage:** Soon recognizes that Solana (and its VM) currently holds a significant lead in terms of developer adoption and active users.  Their strategy is to leverage this existing activity and provide tools ("Decoupled SVM") to bring Solana's performance to other ecosystems, enabling developers to "develop once, deploy everywhere."
*   **Modularity is Key:** The panel agrees that blockchain systems are *modular*. Optimizations are not limited to the VM instruction set; the database, execution pipeline, and consensus mechanisms all play crucial roles.  Improving any of these components can significantly impact overall performance.
*   **Developer Experience and Network Effects:**  The panel acknowledges the significant network effects associated with the EVM and Solidity.  Developers are hesitant to learn new languages, and existing tooling and libraries give the EVM a significant head start.  Shayan, the Movement Labs devrel, says "move is the best designed VM out there".
*  **Different Design for the same goal** Monad is staying with EVM and using parallel processing to address performance issues, but the other panelist don't consider EVM performant enough and choose to design new ones.

**3. Practical Takeaways:**

*   **For Developers:**  Consider the trade-offs between the EVM's familiarity/tooling and the potential performance/safety benefits of alternative VMs like Move or SVM.  If performance is critical, explore projects like Monad, Movement Labs, and Soon.  If security is paramount, investigate Move.
*   **For Investors/Researchers:** Pay close attention to projects that are not *just* building another EVM clone, but are fundamentally rethinking aspects of blockchain architecture, such as the storage layer (Monad).  Follow the developer adoption metrics of different VMs (SVM, Move, EVM).
*   **For Everyone:** The discussions on the panel showed there may be a need for developers to use alternative VM other than the EVM for enhanced performance or security.

**4. Additional Notes:**

*   The panel was relatively informal and conversational, with some friendly debate but no heated arguments.
*   The panelists' projects are all at different stages of development. Monad has a public testnet, while others are earlier.
*   The "spiciness" promised at the beginning of the panel referred to the diversity of opinions and the potential for disagreement, not to conflict.
*  The moderator, Lane, did a better job presenting Monad than Keone, who didn't always understand the questions.