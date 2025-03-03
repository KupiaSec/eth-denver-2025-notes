# An introduction to EIP-7702

**Speakers:** Jan Gorzny - Zircuit


*Upload Date: 20250224*

*Source: [https://www.youtube.com/watch?v=WG_0EiHtKlc](https://www.youtube.com/watch?v=WG_0EiHtKlc)*

Here's a comprehensive summary of the YouTube video "An introduction to EIP-7702 | Jan Gorzny - Zircuit," broken down into the requested sections:

**1. Main Points:**

*   **Introduction of EIP-7702:** EIP-7702 is a new Ethereum Improvement Proposal that introduces a new transaction type allowing Externally Owned Accounts (EOAs) to temporarily act like smart contract wallets *for the duration of a single transaction*.
*   **Account Abstraction (AA) Stepping Stone:** EIP-7702 is presented as a step towards full, native account abstraction on Ethereum, addressing immediate user experience (UX) needs.
*   **Delegation Designator:** The core mechanism involves a "delegation designator" – signed data that specifies code an EOA is *temporarily* delegating execution to.
*   **Key Use Cases:** The speaker highlights several key use cases, including transaction batching, transaction sponsorship (gasless transactions), and improved security features like social recovery.
*   **Compatibility:** EIP-7702 is *not* incompatible with other account abstraction proposals like EIP-4337. It's complementary and addresses a different part of the AA problem.
*   **Testnet Availability:** The speaker mentions that testnets supporting EIP-7702 are available, encouraging developers to experiment.
*	**Call to action** The speaker wants better gasless UX, especially for new users who don't understand Ethereum.

**2. Key Insights:**

*   **EOA Limitations Addressed:** EIP-7702 addresses the inherent limitations of EOAs, which are controlled by private keys and lack the programmability of smart contracts.  It does this *without* requiring users to deploy a new smart contract wallet.
*   **Temporary Smart Contract Functionality:** The crucial innovation is the *temporary* nature of the code delegation. An EOA doesn't *become* a smart contract wallet permanently; it only behaves like one for the span of a single transaction. This significantly reduces risk compared to fully switching to a smart contract wallet.
*   **Security Considerations:** The speaker emphasizes security, particularly around the "delegation designator."  He recommends keeping delegated code simple and auditable, highlighting the risks of delegating to untrusted or upgradeable contracts.
*   **Improved UX Focus:** The primary motivation behind EIP-7702 is to dramatically improve the user experience.  The speaker uses the ERC-20 approve/transfer pattern as a prime example of unnecessary complexity that can be streamlined.  Transaction batching and sponsorship are repeatedly emphasized as major UX wins.
*	**Sponsorship for Onboarding.** Sponsoring transactions will especially benefit dApps that need more users.
*   **Complementary, Not Competitive:** EIP-7702 doesn't aim to replace EIP-4337 (the most well-known AA proposal).  4337 aims for fully native AA, while 7702 provides an intermediate solution.
*   **Zircuit's Interest:** Zircuit, the speaker's company (a ZK rollup), is very interested in EIP-7702, particularly for transaction sponsorship to improve user onboarding to their L2. They plan to be one of the first rollups to support it.
*   **No Standards Yet:**  A crucial takeaway is the *lack* of established standards for the delegated code.  The speaker strongly encourages the community to develop and test these standards to avoid security issues.
*   **TX.Origin Invariant Broken:**  EIP-7702 breaks the common assumption (invariant) that `tx.origin` is always equal to `msg.sender`.  Developers building dApps need to be aware of this.

**3. Practical Takeaways:**

*   **For Developers (Immediate):**
    *   **Experiment:** Start experimenting with EIP-7702 on available testnets.
    *   **Design Delegation Code:** Think about use cases where temporary delegation could improve your dApp's UX (e.g., combining approve and transfer, gas sponsorship).
    *   **Security First:** If implementing delegation, prioritize simple, auditable, and *non-upgradeable* contracts for the delegated code.  *Extremely important*.
    *   **Audit Existing Code:** Review existing smart contract code for reliance on the `tx.origin == msg.sender` invariant. This assumption will no longer be valid.

*   **For Developers (Longer Term):**
    *   **Contribute to Standards:**  Participate in discussions and development of standards for delegation designators.
    *   **Build New UX Patterns:** Explore new UX patterns enabled by EIP-7702, such as seamless onboarding experiences where users don't need ETH initially.
    *   **Prepare for Account Abstraction:**  Consider how EIP-7702, and account abstraction in general, will impact your dApps and user onboarding flows.

*   **For Users:**
    *   **Stay Informed:**  Be aware that EIP-7702 is coming and will likely improve the user experience of interacting with dApps.
    *   **Understand Delegation Risks:** When using dApps that leverage EIP-7702, understand *what* you are delegating authority to and for *how long*.
    *   **Be Cautious of Prompts**:  Be extra cautious of contracts asking for approval to interact with your account. Understand that delegation may give far more power than just approving.

**4. Additional Notes:**

*   **Pectra Upgrade:** EIP-7702 is slated for inclusion in the upcoming Ethereum "Pectra" upgrade, indicating its importance and likely widespread adoption. (First on Holi testnet, then Sepolia, then mainnet).
*   **Early Stage:** While EIP-7702 is relatively finalized, the surrounding ecosystem (tools, libraries, standards) is in its early stages. This is explicitly mentioned as a reason for the presentation – to encourage early adoption and development.
*	There is currently no prize at the hackathon for contributions to EIP-7702, but reach out to the Zircuit team if you give good contributions.
*	The Zircuit testnet is coming out "this week".

This summary provides a detailed and actionable overview of the key information presented in the video. The emphasis on security considerations and the call for community involvement in standardizing delegation code are particularly important points to note.