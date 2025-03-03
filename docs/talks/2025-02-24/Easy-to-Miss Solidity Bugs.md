# Easy-to-Miss Solidity Bugs

**Speakers:** Jonathan Mevs & Michael Boyle - Quantstamp


*Upload Date: 20250224*

*Source: [https://www.youtube.com/watch?v=bXdJPmON_XA](https://www.youtube.com/watch?v=bXdJPmON_XA)*

Here's a summary of the YouTube video "Easy-to-Miss Solidity Bugs | Jonathan Mevs & Michael Boyle - Quantstamp," formatted as requested:

**1. Main Points:**

*   The presentation focuses on *subtle* Solidity bugs that are often overlooked during development and even auditing, but can lead to significant vulnerabilities.  These aren't the "classic" bugs like reentrancy, but rather nuanced issues arising from Solidity/EVM specifics.
*   The examples are drawn from real-world audits conducted by Quantstamp, simplified for presentation.
*   The key areas of focus are: storage vs. memory confusion, incomplete struct initialization, EVM opcode behavior differences across chains (especially L2s), and improper handling of user-supplied data in cross-chain interactions.
* The presentation draws a clear distinction between "easy-to-find" bugs (detectable by static analysis) and "easy-to-miss" bugs (requiring careful manual review).
*   The presenters emphasize the importance of thorough manual audits in *addition* to automated tools.

**2. Key Insights:**

*   **Storage vs. Memory Mishaps:**  Solidity's distinction between `storage` (persistent contract state) and `memory` (temporary, function-scope data) is crucial, and mistakes can lead to unexpected behavior.  Two specific bugs are presented:
    *   **Example 1 (Incorrect Storage Update):**  Updating a *memory* variable that's intended to represent the total staked amount, instead of directly updating the *storage* variable. This leaves the contract's actual state unchanged.
    *   **Example 2 (Incorrect Storage Deletion):** Declaring a struct as `storage` inside a function creates a *pointer* to storage, not a copy.  Deleting this pointer zeroes out the storage, potentially losing user funds if that storage location is used for crucial data before being deleted.  This can lead to accidental reentrancy vulnerabilities.
*   **Incomplete Struct Initialization:**  If a struct is initialized using dot notation (e.g., `myStruct.field1 = value1;`) and some fields are *omitted*, those fields will default to their zero values.  This is *not* a compiler error.  This can lead to unintended behavior if the developer assumes all fields are initialized.  The safer method is complete struct initialization (MyStruct({field1: x, field2: y, field3: z})), which *will* cause a compiler error if any fields are missing which ensures all members have an intentional value.
*   **EVM Opcode Differences (Cross-Chain Compatibility):**  Layer-2 (L2) solutions and other EVM-compatible chains may not perfectly replicate the behavior of Ethereum mainnet.  `SELFDESTRUCT`, while deprecated, is used as an example.  On mainnet, it returns ether but doesn't necessarily destroy the contract, while on some L2s, it might do nothing or revert.  Developers must be aware of these differences and, crucially, *inform auditors* if deployment on multiple chains is planned. Using `block.chainid` can be used to control behavior for specific chains.
* **Unbounded user Data:** Allowing user input for arbitrary bytecode execution in a cross-chain bridging context can lead to various attacks, including stalled or lost transactions. Cross-chain interaction fundamentally breaks atomicity, making it important to sanitize user input (limit operation types, enforce max payload sizes, etc.).

* **Honorable Mentions (briefly covered)**:
    *   **Token Decimals:** Never assume all tokens use the same number of decimals. Always query the token contract's `decimals()` function.
    *   **NFT Marketplaces and CryptoPunks:**  The CryptoPunks contract predates standard token interfaces, so marketplaces must handle it with special care.
    *   **Staking Contract Accounting:**  Carefully separate accounting for user deposits and rewards, especially when different tokens are involved.
    *    **Manual Price Updates:** Systems relying on manually-provided price updates (e.g., reward ratios) are highly vulnerable to front-running and MEV.

**3. Practical Takeaways:**

*   **Always update storage directly:** When modifying persistent contract state, ensure you are interacting with `storage` variables, not temporary `memory` copies.
*   **Use complete struct initialization:**  Prefer `MyStruct({field1: x, field2: y, ...})` over dot notation (`myStruct.field1 = x; myStruct.field2 = y;`) to force a compiler error if any fields are accidentally omitted.
*   **Test thoroughly on *all* target chains:** If your contract is intended for deployment on multiple EVM-compatible chains (especially L2s), test thoroughly on *each* target chain.  Do not assume identical behavior.
*   **Inform auditors about multi-chain plans:**  If targeting multiple chains, clearly inform your auditors to enable them to check for cross-chain compatibility issues.
* **Use** `block.chainid` : This value indicates the specific chain the contract is executing on.
*   **Sanitize user input, especially for cross-chain calls:**  Avoid allowing users to provide arbitrary bytecode for execution. Impose restrictions on the types of operations and data sizes.
* **Declare abstract contracts:** Parent contracts that are *only* meant to be inherited, and never standalone, should be declared `abstract`.
*   **Don't hardcode token decimals:** Query the `decimals()` function of each ERC-20 token.
*  **Compartimentalize logic:** Separate initialization logic for Structs into an init function for clarity and easy auditing.
*   **Combine automated and manual auditing:** Use static analysis tools (like Slither) to catch common issues, but *always* supplement with a thorough manual audit to identify subtle logic flaws.
* **Stay Informed:** Keep up to date with security best practices, recent hacks, and the evolving Web3 landscape (e.g., via Crypto Twitter).

**4. Additional Notes:**

*   The video is a presentation, likely from a conference, and thus assumes a moderate level of familiarity with Solidity and smart contract concepts.
*   The examples presented are simplified versions of real audit findings.  Real-world bugs can be much more complex, nested within larger codebases.
* While the examples focus on relatively subtle errors that "look sound," the overall point of the presentation is to demonstrate that attention must be paid to fine detail.

This summary provides a detailed overview of the video's core message and offers actionable advice for Solidity developers and auditors.