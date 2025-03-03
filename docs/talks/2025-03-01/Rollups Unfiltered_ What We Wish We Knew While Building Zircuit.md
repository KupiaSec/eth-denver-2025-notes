# Rollups Unfiltered: What We Wish We Knew While Building Zircuit

**Speakers:** Martin Derka - Zircuit


*Upload Date: 20250301*

*Source: [https://www.youtube.com/watch?v=oGVHPWnYwtM](https://www.youtube.com/watch?v=oGVHPWnYwtM)*

Here's a comprehensive summary of the YouTube video "Rollups Unfiltered: What We Wish We Knew While Building Zircuit | Martin Derka - Zircuit," formatted as requested:

1.  **Main Points (bullet points)**

*   **Ethereum Upgrades and Rollup Compatibility:** Ethereum upgrades can significantly impact rollups, especially those built on frameworks like the OP Stack.  Rollups need to adapt, and not all Ethereum Improvement Proposals (EIPs) are beneficial for Layer-2 solutions.
*   **EIP-1559 and Base Fee Dynamics:** EIP-1559's introduction of a base fee and priority fee creates challenges for rollups aiming for low and predictable transaction costs. Fast block production on L2s can lead to consistently low base fees, making transaction inclusion dependent on tips.
*   **Multi-Sig Security and Signing Procedures:**  Securely managing multi-signature (multi-sig) controlled smart contracts on rollups is crucial.  Zircuit developed a detailed, rigorous process for signing transactions involving multiple parties, emphasizing technical understanding and verification.
*   **Importance of Comprehensive Testing:** Thorough testing at multiple levels (unit, integration, and staging networks) is essential for identifying issues that might not be apparent in simplified testing environments.
*  **OP Stack Overview:** Briefly touches on the concept and basic workings of an Optimistic Rollup based on OP Stack, and how transactions move from Layer2 to Layer1.

2.  **Key Insights (detailed explanations)**

*   **Rollup Divergence from Ethereum:**  While rollups inherit security from Ethereum (L1), they are designed to innovate and offer features not available on L1. This inherent divergence necessitates careful consideration of Ethereum upgrades.  The speaker highlights that because rollups are tightly coupled with L1 via shared dependencies (specifically in go-lang's single version dependency rule), upgrades to Ethereum can break L2 functionality if not carefully managed. Rollups might *not* want to adopt all EIPs if those changes negatively impact the L2's goals (e.g., increasing transaction costs).
*   **"Ultrasound Money" Phenomenon on Rollups:** The combination of EIP-1559 and rapid L2 block production leads to a situation where the base fee frequently drops to near zero.  This means that the *priority fee (tip)* becomes the primary factor determining transaction inclusion.  In essence, the rollup's native token becomes "ultrasound money" in the sense that transaction fees are primarily paid through tips rather than a predictable, dynamically adjusted base fee. This contrasts with a congested L1, where the base fee would rise significantly.
*   **Multi-Sig Signing as a Human Process:** The presentation strongly emphasizes that secure multi-sig signing isn't just about the technology (hardware wallets, smart contracts). It's fundamentally a human process that requires meticulous planning, technical expertise, and cross-verification.  The Zircuit team's procedure includes:
    *   **Code Review & Verification:**  Multiple technically proficient individuals review the code changes leading to the transaction.
    *   **Trace Simulation:**  Using tools like Foundry or Hardhat, signers simulate the transaction to understand its exact effects on the blockchain state.
    *   **Independent Verification:**  Each signer independently verifies all transaction parameters (method selector, arguments, storage changes) to ensure everyone is aligned.
    *   **Communication and Coordination:** Real-time communication (e.g., a call) is used to discuss any discrepancies or concerns before signing.
    *   **Hardware Wallet Confirmation:**  The final signing on a hardware wallet (e.g., Ledger) occurs only after all verifications are complete, and the displayed payload matches the expected values.
*   **Staging Networks as Crucial Testing Grounds:** Unit tests and local development environments are insufficient for capturing the complexities of a live blockchain network.  Staging networks (e.g., "alphanet," "betanet"), which mimic mainnet conditions more closely, are vital for uncovering issues related to gas price fluctuations, reorgs, and node behavior.

3.  **Practical Takeaways (actionable items)**

*   **Rollup Developers:**
    *   **Carefully evaluate Ethereum upgrades:**  Don't blindly adopt all EIPs. Determine if they align with your rollup's goals and design.  Be prepared to diverge from L1 logic if necessary. Git good.
    *   **Implement robust multi-sig procedures:**  Develop a detailed, well-documented process for multi-sig operations.  This should include code review, transaction simulation, independent verification, and clear communication among signers. Don't just rely on hardware wallets.
    *   **Prioritize comprehensive testing:**  Go beyond unit tests.  Utilize staging networks that replicate live network conditions to uncover potential issues early.
    *   **Understand EIP-1559 implications:**  Be aware of how EIP-1559's base fee mechanism interacts with your rollup's block production rate. Plan for potential "ultrasound money" behavior and user experience implications.
    *   **Use a monorepo:** This type of code repo helps manage dependencies.
    *   **Be prepared for long build times for your system.**
*   **Multi-Sig Participants (Executives, Developers):**
    *   **Technical proficiency is key:**  Even non-technical participants *must* understand the technical details of the transactions they are signing.  Rely on technical experts to explain, but cultivate a baseline understanding.
    *   **Independent verification is paramount:** Never blindly trust a single source of information. Use multiple tools and methods to verify transaction details before signing.
    *   **Communication is essential:** Maintain open communication channels during the signing process to address any concerns or discrepancies immediately.
*   **Users of Rollups**
    *  Be aware that your transaction may be more likely to be quickly included if you include a larger tip.

4.  **Additional Notes (if any)**

*   The speaker, Martin Derka, is the technical lead and co-founder of Zircuit, a zero-knowledge rollup. This context shapes his perspective, particularly regarding the multi-sig security discussion.
*   The talk was delivered at ETHDenver, indicating a developer-focused audience familiar with blockchain concepts.
*   While the talk primarily focuses on the OP Stack, many of the insights apply to other rollup frameworks as well. The challenges of Ethereum upgrades and multi-sig security are universal.
* The OP Stack section briefly discusses the core components: Execution Client (like Geth), Batcher, L1 Client, OP Node, Prover and Proposer, and how they work together. It does not go into much depth, acting as background.
*   The video provides a valuable "lessons learned" perspective, highlighting the practical challenges faced when building real-world rollup solutions. It goes much further than many high level discussions of rollups, getting into real nitty-gritty details.