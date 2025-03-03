# Building a Self Custodial Debit Card & Smart Permissions Alejandro Perezpaya Jorge Izquierdo Tuyo

*Upload Date: 20250301*

*Source: [https://www.youtube.com/watch?v=BgZ8P8O9txU](https://www.youtube.com/watch?v=BgZ8P8O9txU)*

Here's a summary of the YouTube video "Building a Self Custodial Debit Card & Smart Permissions Alejandro Perezpaya Jorge Izquierdo Tuyo," based on the provided transcript:

**1. Main Points:**

*   **Introduction to Tuyo:** Tuyo is presented as a self-custodial crypto app that allows users to trade, earn, and now spend crypto, emphasizing user experience.  The name "Tuyo" means "yours" in Spanish, highlighting the self-custodial nature.
*   **Problem with Existing Crypto Cards:** The presenters identify problems with current crypto cards:  custodial, prepaid (requiring constant top-ups), and lack of on-chain privacy.
*   **Ideal Crypto Card Properties:**  A "great" crypto card should be non-custodial, feel like a debit card (not prepaid), be "rug-proof" (protected from the company going bankrupt and double-spend attacks), and offer as much privacy as possible.
*   **Smart Account Permissions:**  Tuyo leverages smart account permissions built on *smart contracts*, specifically using infrastructure from ZeroDev. These permissions allow for granular, stateful control over how funds are used.
*   **Periodic Pull Permission:** A key innovation is the "periodic pull permission." This allows the card provider to pull a *limited* amount of funds from the user's account *daily*, behaving like a debit card without requiring the user to constantly top-up a separate balance.  This is the central feature ensuring the "debit card feeling"
*   **Collateral Account:**  A "collateral account" (a sub-account of the user's main account) holds the funds authorized for spending.  This account is controlled by both the user *and* the card provider (via the pull permission).
*   **Card Transaction Flow:** The full transaction flow is explained:  card presentation -> authorization request to Tuyo -> smart contract verification (pull permission check) -> funds move to the collateral account -> settlement with the card provider.
*   **Self-Custody Guarantee:**  Because the funds remain in a smart contract controlled by the user's key, the user retains custody at all times.  An "ejection" mechanism allows users to remove the card provider's permission and regain full, sole control of their funds.
*   **Live Demo:**  The presenters demonstrate a live purchase using the Tuyo card via Apple Pay, showcasing the seamless, real-time spending of crypto (USDC on Base).
*   **Availability and Future Plans:** The card is launched in the US, with plans to expand to South America and eventually Europe.  They are also hiring.

**2. Key Insights:**

*   **Bridging the Gap with Traditional Finance:** Tuyo's primary goal is to make spending crypto as easy and intuitive as using a traditional debit card. They are deliberately mirroring the familiar experience of traditional banking while maintaining the core principles of crypto (self-custody).
*   **Smart Contracts for Enhanced Security and Control:** The use of smart contract permissions, specifically the "periodic pull permission," is *crucial.*  It's not just a convenience feature; it's the mechanism that enforces the limited access granted to the card provider and prevents them from absconding with user funds.  This addresses a major trust issue with existing custodial solutions. The collateral account enforces a strict flow of the money, enhancing user protection.
*   **Privacy Considerations:** Although complete on-chain privacy is impossible with public blockchains, Tuyo aims to *obfuscate* transactions as much as possible to prevent easy tracing of user spending habits. The collateral account helps here since it severs *direct* links between the user's main wallet and spending.
*   **Real-time Authorization:** The system is designed for speed. The authorization process, despite involving smart contract interactions, must be fast enough to feel like a typical card transaction (faster than a transaction lands on-chain).
*   **Automated Rebalancing:** The pull permission is *automatically* triggered, removing the need for manual top-ups and giving the system its debit card "feel." The user doesn't need to actively manage the balance available to the card.

**3. Practical Takeaways:**

*   **For Users:** Users in supported regions can download the Tuyo app and use the card to spend USDC on Base at any merchant accepting Visa. The experience should resemble using a regular debit card, with no fees (setup or monthly) mentioned in this presentation. The "ejection" feature provides a strong safety net.
*   **For Developers:** The presentation demonstrates a practical application of smart contract permissions (specifically, delegated execution via ZeroDev's infrastructure). Developers can consider how similar permissions could be used to create self-custodial solutions in other areas, managing access and control in a secure and user-friendly way.
*   **Understand the Limitations:** On-chain privacy is limited by the nature of public blockchains.  While Tuyo works to improve privacy within these constraints, users should still be aware that some transaction information will be publicly visible.

**4. Additional Notes:**

*   The presentation focuses on the technical architecture and user benefits.  Detailed information about fees (beyond the statement that there are no setup/monthly fees), supported currencies (beyond USDC on Base), and specific regional availability is not deeply covered.
*   There is a strong emphasis on the collaboration with "Rain" as partners.
*   The live demo encountered some minor connectivity issues, highlighting that real-world systems are subject to real-world problems.
* They announce they're hiring at the end.

The video presents a compelling solution for bridging the gap between the crypto and traditional finance worlds, leveraging smart contracts to provide a secure and user-friendly debit card experience while maintaining the key principle of self-custody. The "periodic pull permission" is the core innovation enabling this.