# The Unseen Threat: Why Attackers See What Developers Miss

**Speakers:** Bartosz Barwikowski - Hacken


*Upload Date: 20250226*

*Source: [https://www.youtube.com/watch?v=RdZJGjVsH2E](https://www.youtube.com/watch?v=RdZJGjVsH2E)*

Here's a comprehensive summary of Bartosz Barwikowski's presentation, "The Unseen Threat: Why Attackers See What Developers Miss," based on the provided transcript:

**1. Main Points:**

*   **Hacker Mindset:** Attackers exploit vulnerabilities by thinking differently than developers, driven by curiosity and a "what if" approach.  They disassemble, experiment, and constantly question assumptions.
*   **Common Vulnerability Patterns:**  Bartosz identifies ten recurring vulnerability patterns that he frequently encounters during security audits and bug bounty programs.
*   **Code Porting Issues:**  Porting code between different platforms or languages (e.g., Solidity to Solana/Sui/Aptos, Rust to Move, or between 32-bit and 64-bit architectures) is a significant source of vulnerabilities if developers lack platform-specific knowledge. He highlights an oracle manipulation example.
*   **Algorithm Implementation Errors:**  Inadequate understanding of algorithms (sorting, finding medians, mathematical calculations, base58 vs base64 encoding) and their complexities often leads to vulnerabilities.  A significant example using Base58 encoding instead of Base64, allowing a DoS, is given. He also touches upon AI tools (ChatGPT) not recognizing potential issues.
*   **Team Dynamics and Code Quality:**  Uneven skill distribution within development teams (where one experienced developer leads and others follow) can lead to vulnerabilities being overlooked.  Focusing on the weakest code segments is crucial.
*  **Legacy Code Updates** Updating and changing old code, legacy code, is dangerous.
*   **Inadequate Third-Party Integration:**  Insufficient consideration of failure scenarios and potential abuse when integrating with third-party components (e.g., oracles) creates vulnerabilities.
*   **Complex Code and Lack of Testing:**  Highly complex code (e.g., zero-knowledge proofs, decentralized exchanges, lending markets) with insufficient testing is a major "red flag."
* **Reinventing the wheel** Developers coding everything by their hands, like custom cryptography, or serialization when other tools exist increases risk.
*   **Economic Attacks:** Attackers can exploit the economic models of decentralized applications (e.g., manipulating collateral prices in lending platforms).
*   **Multi-Step Operations:**  Operations involving multiple transactions or steps create numerous edge cases that are often not considered, leading to vulnerabilities.

**2. Key Insights:**

*   **Developer Blind Spots:** Developers often focus on the intended functionality ("happy path") and overlook edge cases, unintended interactions, or the implications of using specific algorithms or libraries. They might make incorrect assumptions about the behavior of underlying systems.
*   **The Importance of Curiosity:** A hacker's mindset is characterized by a constant desire to understand how things work and how they can be broken. This contrasts with a developer's focus on building functionality.
*   **Platform-Specific Expertise:**  Porting code requires a deep understanding of the nuances of the target platform.  Copying code without considering platform-specific behaviors is a recipe for disaster.
*   **Algorithm Choice Matters:**  Even seemingly simple algorithms can have significant security implications if their complexity, edge cases, and limitations are not understood.  The difference between similar encoding systems (Base58/Base64) underscores this.
*   **Testing is Paramount:**  Comprehensive testing, especially for complex code and edge cases, is critical to identify vulnerabilities. The absence of tests for complex logic is a strong indicator of potential problems. *Insufficient* testing is almost as bad.
*   **Economic Model Vulnerabilities:** Decentralized applications are susceptible to attacks that exploit their economic models. Attackers can manipulate prices, liquidity, or other economic parameters to gain an unfair advantage.  Auditors also might not understand the economics.
*   **The Value of Experience:** Bartosz's extensive experience in cybersecurity (including his early hacking experiences and work with bug bounty programs) allows him to identify recurring vulnerability patterns that less experienced developers might miss.

**3. Practical Takeaways:**

*   **Adopt a Hacker Mindset:** Encourage developers to think like attackers. Ask "what if" questions, challenge assumptions, and explore edge cases.  Foster a culture of curiosity and experimentation.
*   **Prioritize Thorough Testing:**  Implement comprehensive testing strategies that cover not only the "happy path" but also edge cases, error handling, and potential abuse scenarios.  Focus on testing complex logic and multi-step operations. Make testing a priority that is not skipped.
*   **Seek Platform-Specific Expertise:**  When porting code, ensure that developers have the necessary expertise in the target platform to avoid introducing platform-specific vulnerabilities.
*   **Understand Algorithm Limitations:**  Developers should have a solid understanding of the algorithms they use, including their complexity, limitations, and potential security implications.
*   **Review Third-Party Integrations Carefully:**  Thoroughly analyze third-party components and consider how they could fail or be abused.  Implement robust error handling and security measures.
*   **Don't Reinvent the Wheel Unnecessarily:**  Leverage existing, well-tested libraries and frameworks whenever possible.  Avoid creating custom solutions (especially for cryptography) unless absolutely necessary.
*   **Consider Economic Attacks:** Design and audit decentralized applications with economic attacks in mind.  Analyze how attackers could manipulate economic parameters to gain an advantage.
*   **Promote Code Reviews and Collaboration:**  Implement code review processes to identify vulnerabilities that individual developers might miss. Encourage collaboration and knowledge sharing within development teams.
*   **Continuous Learning:**  The cybersecurity landscape is constantly evolving.  Encourage continuous learning and professional development for developers to stay up-to-date on the latest threats and vulnerabilities.
* **Prioritize Audits:** Run code through security audits like those provided by Hacken.

**4. Additional Notes:**

*   The presentation emphasizes real-world examples from Bartosz's experience, making the concepts more concrete and relatable.
*   The mention of AI tools like ChatGPT highlights the current limitations of AI in identifying subtle but critical vulnerabilities.
*   The video acts as a strong advertisement for Hacken's auditing services, showcasing their expertise and successful track record.
*   The presentation is slightly disorganized and lacks specific details on *how* to implement the suggestions. It focuses on *where* to look for errors, but doesn't go deep into remediation techniques. The examples are used as quick illustrations of *types* of vulnerabilities, but not detailed walkthroughs.
* The lack of slides or code shown on the "screen" is a limitation. The transcript alone gives a good overview, but the educational benefit would be higher with visual aids.