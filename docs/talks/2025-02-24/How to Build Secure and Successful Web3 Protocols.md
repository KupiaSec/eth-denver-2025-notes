# How to Build Secure and Successful Web3 Protocols

**Speakers:** Harikrishnan Mulackal - Spearbit, Cantina


*Upload Date: 20250224*

*Source: [https://www.youtube.com/watch?v=mZMDjGNXiD0](https://www.youtube.com/watch?v=mZMDjGNXiD0)*

Here's a summary of the YouTube video "How to Build Secure and Successful Web3 Protocols | Harikrishnan Mulackal - Spearbit, Cantina," formatted as requested:

**1. Main Points:**

*   **Security is Paramount in Web3:**  Unlike Web2, security breaches in Web3 can be catastrophic, leading to complete project failure and substantial financial loss. The "move fast and break things" approach doesn't work.
*   **"Move slow and don't break things" isn't the solution either:**  Moving too slowly prevents crucial early feedback and can lead to building the wrong product.
*   **Iterative Development (V1, V2, V3...):**  The best approach is to launch a minimal viable product (MVP) or "V1" with a *very* limited feature set, get user feedback, and then iterate rapidly, adding features and complexity in subsequent versions (V2, V3, etc.).
*   **V1 Should Be Extremely Simple:**  The initial version should contain only the *absolute minimum* features necessary to be useful.  This reduces the attack surface and makes security auditing easier and cheaper.
*   **Upgradable Contracts are Okay (with caveats):** Contrary to some Web3 idealism, starting with upgradable contracts is acceptable, *provided* the private keys controlling upgrades are secured with extreme care (e.g., using a multi-signature scheme or hardware security module).
*   **Understand the Difference Between Web2 and Web3 Security:** In Web2, a hack might result in data leaks, reputational damage, and some financial loss, but the company usually survives.  In Web3, a hack can mean the total loss of funds and the end of the project.
*   **Prioritize Product-Market Fit:**  Early feedback is crucial.  A secure but unwanted product is useless.  V1 allows you to test your assumptions and iterate based on actual user needs.
*   **Solidity Is Deceptively Simple:**  While the Solidity language itself might appear simple, building secure smart contracts is significantly harder than building traditional Web2 applications due to the complexities and nuances of the EVM.
*   **Security Escalates with Complexity:** As features and complexity are added (moving from V1 to V2, etc.), the investment in security must increase proportionally.  This may eventually involve hiring dedicated in-house security engineers.

**2. Key Insights:**

*   **The Catastrophic Nature of Web3 Hacks:** Harikrishnan emphasizes the fundamental difference in consequences between Web2 and Web3 hacks. He provides real-world examples (Nomad vs. Retool) to illustrate how Web3 hacks can lead to the complete collapse of a project, even those built by highly skilled teams, whereas Web2 companies can often recover.  The presence of *directly accessible funds* within the protocol changes the game entirely.
*   **The "Trap" of Over-Engineering V1:** Many Web3 founders fall into the trap of building an overly complex initial version (V1) of their protocol. They try to incorporate too many features before getting any real-world user feedback.  This increases the protocol's complexity, making it harder to secure, more expensive to audit, and potentially misaligned with actual user needs.
*   **The Value of Early, Iterative Feedback:** The core of Harikrishnan's advice is the importance of iterative development.  Getting *real* user feedback on a simplified V1 provides invaluable information about what users actually want and need, which is often different from the founders' initial assumptions.  This allows developers to focus their efforts on building the *right* features and avoid wasting time on features that are unnecessary or unwanted.
* **Upgradability's Pragmatic Approach:** The speaker challenges the common "fully decentralized from day one" ideology, recognising the practicality and often the *necessity* of upgradable contracts, *especially* in the early stages. The discussion doesn't advocate for *permanent* upgradability, but a *phased* approach towards decentralization. The key point is the absolute necessity of robustly securing the admin keys associated with upgradability.
*   **The "V2 is the Real Launch" Mindset:** This is a critical conceptual shift.  Founders should view V1 as a learning and testing phase — *not* the final product.  V2 (and subsequent versions) is where the product truly takes shape, informed by real-world usage and feedback from V1.
* **Stages of security investment correlates with project maturity:** Hari suggests that at V1 phase one can rely on external security reviews and bug bounties, and suggests in-sourcing the security only in V2 or V3 phases, when the product complexity and risk justify the expense.


**3. Practical Takeaways:**

*   **Define Your Absolute Minimum V1:** Before writing any code, meticulously define the absolute minimum set of features your protocol *must* have to be useful.  Cut everything else for the V1.
*   **Prioritize Security from Day One (Even with Simplicity):** Even with a stripped-down V1, security *must* be a primary concern. Get a security review or audit, and consider a bug bounty program.
*   **Embrace Upgradability (Responsibly):** Don't be afraid to use upgradable contracts in V1, but *ensure* the upgrade keys are secured using best practices (e.g., multi-sig, HSM).  Plan for an eventual transition towards greater decentralization.
*   **Ship Your V1 Quickly:**  The goal is to get real-world user feedback as soon as possible. Don't get bogged down in perfecting V1.  Focus on getting it live and iterating based on usage data.
*   **Plan for Iterative Development (V2, V3...):**  Always be thinking ahead.  V1 is just the starting point. Have a roadmap for V2, V3, and beyond, incorporating planned feature additions and corresponding security enhancements.
*   **Ramp Up Security Investment Over Time:**  As your protocol grows in complexity and value, increase your investment in security.  This might involve hiring dedicated security engineers or engaging with security auditing firms like Spearbit.
*   **Study Successful Projects (e.g., Uniswap):** Learn from the successes (and failures) of other Web3 protocols.  Analyze how projects like Uniswap evolved through different versions and what lessons can be applied to your project.
* **Don't assume smart contract development is easy:** Get educated about how smart contracts actually work, and the nuances and common vulnerabilities present in Solidity/EVM.

**4. Additional Notes:**

*   **Speaker's Background:** Harikrishnan's experience at Spearbit and Cantina, working with a wide range of Web3 projects, lends significant credibility to his advice. He's seen firsthand what works and what doesn't.
* **Focus on Early-stage Projects**: The advice is primarily targeted at early-stage Web3 protocol development. The dynamics might change for very large, established protocols.
* **Q&A section:** The Q&A section provides concrete answers to concerns like, hiring a security team, and time frame when transition from V1 to V2.
* **Controversial Take:** Stating "starting with upgradable contracts are ok" is controversial and goes against some parts of the community, but the speaker provides rational arguments. It's important to understand this is controversial.