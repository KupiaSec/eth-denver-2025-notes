# How to Build a Quantum Computer Resistant Blockchain With QRL

**Speakers:** Michael Strike - QRL


*Upload Date: 20250226*

*Source: [https://www.youtube.com/watch?v=QFuIU1S92E4](https://www.youtube.com/watch?v=QFuIU1S92E4)*

Okay, here's a comprehensive summary of the YouTube video "How to Build a Quantum Computer Resistant Blockchain With QRL | Michael Strike - QRL", structured as requested:

**1. Main Points:**

*   **Quantum Threat to Blockchains:** Existing blockchains, particularly those relying on ECDSA (like Bitcoin), are vulnerable to attacks from sufficiently powerful quantum computers using Shor's algorithm.
*   **QRL's Solution:** The Quantum Resistant Ledger (QRL) is a blockchain designed from the ground up to be resistant to quantum computer attacks. It uses a NIST-recommended, post-quantum secure digital signature algorithm (DSA).
*   **XMSS to Dilithium** QRL has been running its layer-one blockchain since _2018_, originally utilizing the XMSS signature scheme, it's planning to migrate to Dilithium around 2025.
*   **Bitcoin's Vulnerability:** Bitcoin's (and most altcoins') use of ECDSA makes them susceptible.  The public key is exposed during transactions, making them a target.  "Store now, decrypt later" attacks are a real threat, where attackers harvest public keys for future cracking.
*   **Hard Fork Challenges:** Migrating an existing blockchain like Bitcoin to a post-quantum secure DSA is extremely difficult, requiring community consensus, a hard fork, and manual migration of funds, potentially leaving some funds orphaned.
*   **QRL's Upcoming "Project Zand" Hard Fork:** QRL is transitioning to proof-of-stake and adding Solidity compatibility, meaning developers familiar with Ethereum can build on QRL.  This is a significant upgrade to an *already quantum-resistant chain*.
*   **Post-Quantum Security Checklist:** Strike presents a checklist for evaluating whether a blockchain is truly post-quantum secure, emphasizing the importance of being secure *from the genesis block*.
* NFA: Not financial advice

**2. Key Insights:**

*   **The ECDLP Problem:** The Elliptic Curve Discrete Logarithm Problem (ECDLP) is the foundation of ECDSA's security.  Classical computers find it incredibly difficult to solve, but Shor's algorithm on a quantum computer can solve it efficiently.  This breaks the one-way function that protects private keys derived from public keys.
*   **Public Key Exposure:** A key vulnerability of Bitcoin is the exposure of the public key during a transaction.  While the address itself is a hash of the public key, the act of spending Bitcoin reveals the underlying public key.  This gives a quantum attacker a target, even if it takes years for sufficiently powerful quantum computers to become available.
*   **Immutability as a Double-Edged Sword:**  Blockchain immutability is a strength, but it also means that vulnerable transactions (those exposing public keys) remain permanently vulnerable on the chain.  There's no going back to fix them.
*   **The Difficulty of Migration:** Upgrading an existing, widely-used blockchain like Bitcoin to a post-quantum secure system is a logistical and social nightmare.  Getting community agreement on the new DSA, the timing of the fork, and the manual process of users moving funds introduces huge risks and potential for loss.
*   **NIST Standardization:** QRL's use of a NIST-recommended DSA is crucial.  NIST (National Institute of Standards and Technology) is a leading authority on cryptographic standards, and their recommendation provides strong assurance of the algorithm's security against both classical and known quantum attacks.
*   **"Project Zand" and EVM Compatibility:** QRL's move to Proof-of-Stake and Solidity (EVM) compatibility represents a strategic shift.  It aims to make the QRL platform more attractive to developers already familiar with the Ethereum ecosystem, facilitating the creation of post-quantum secure dApps.
*   **First-Mover Advantage:** QRL has a significant advantage by having been designed for post-quantum security from the beginning.  Other blockchains claiming post-quantum security are often adding it as an afterthought, which is a much less robust approach.
*   **Beyond Shor's Algorithm:** The speaker touches very briefly on Grover's algorithm, another quantum algorithm that poses a threat to symmetric cryptography (like hashing). While Grover's algorithm offers only a quadratic speedup (compared to Shor's exponential speedup), it's a reminder that quantum threats extend beyond just breaking digital signatures.

**3. Practical Takeaways:**

*   **Evaluate Quantum Risk:** If you're involved in blockchain development or investment, seriously assess the quantum risk to the systems you're using.  ECDSA-based systems are vulnerable.
*   **Prioritize NIST-Recommended DSAs:** When considering post-quantum secure solutions, look for those that use NIST-recommended algorithms (like Dilithium and others in development).  Avoid custom or unproven cryptographic schemes.
*   **"Genesis Block Security":** Understand that for true post-quantum security, the *entire* blockchain, from its very first block, must use a secure DSA. Retrofitting quantum resistance is far less secure.
*   **Explore QRL:** If you're a developer looking for a post-quantum secure platform, investigate QRL, especially with its upcoming "Project Zand" upgrade offering Solidity compatibility.
*   **Run Your Own Node:** The presentation stresses the importance of running your own node to be sure of the rules a chain is adopting.
*   **Be Wary of "Post-Quantum" Claims:** Be skeptical of blockchains that claim to be post-quantum secure without meeting the stringent criteria outlined by Strike (NIST-approved DSA, secure from genesis block, etc.).  Many projects may be overstating their security.
*   **Consider Future-Proofing:** If you're building a new blockchain-based system, strongly consider using a post-quantum secure DSA from the start. It avoids the immense challenges of migrating later.

**4. Additional Notes:**

*   The presentation is somewhat informal, with some repetitions and asides. However, the core message is clear and technically sound.
*   The speaker emphasizes the urgency of preparing for the quantum threat, even though large-scale, fault-tolerant quantum computers are not yet available. The "store now, decrypt later" attack is a real possibility.
*   The presentation focuses on the vulnerability of Bitcoin, but the same principles apply to most other cryptocurrencies using ECDSA.
*   The presentation is biased toward QRL which is understandable, given the speaker and presentation title.
*   The video mentions that QRL's beta testnet is live.