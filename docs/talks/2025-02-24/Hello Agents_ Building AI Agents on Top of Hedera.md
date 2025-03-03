# Hello Agents: Building AI Agents on Top of Hedera

**Speakers:** Jake Hall - Hedera


*Upload Date: 20250224*

*Source: [https://www.youtube.com/watch?v=h8D6vi2m8LQ](https://www.youtube.com/watch?v=h8D6vi2m8LQ)*

Here's a summary of the YouTube video "Hello Agents: Building AI Agents on Top of Hedera | Jake Hall - Hedera", broken down into the requested sections:

**1. Main Points:**

*   **Web3 UX Problem:** The presenter, Jake Hall, starts by highlighting the user experience (UX) challenges in Web3, particularly for newcomers.  He posits that AI agents can help solve this.
*   **AI Agents on Hedera:** The core of the presentation is demonstrating how to build AI agents on the Hedera network.
*   **Hedera Agent Kit SDK:**  Hall introduces a JavaScript/TypeScript SDK called the "Hedera Agent Kit" that simplifies interacting with Hedera's services for AI agent development.  It's designed to be relatively opinionated, but interoperable with other AI agent frameworks.
*   **Eliza Plugin and LangChain Integration:** A practical demonstration focuses on using the Hedera Agent Kit with the Eliza plugin (an AI agent framework) and showing its integration with LangChain (another popular AI framework, more widely used in the "Web2 world").
* **Live Coding Demo:** Jake walks through a live coding demonstration, showing how to set up the environment, interact with the agent, and perform actions like creating and transferring tokens on Hedera.
*   **Bounties:**  He mentions Hedera bounties, specifically highlighting a significant bounty for AI agent development, encouraging community participation.
*   **Open Source Contribution:** Jake encourages contributing to the open-source SDKs.
*   **Hash Scan Demonstration:**  He shows the transactions executed by the AI agent on Hash Scan, Hedera's block explorer.

**2. Key Insights:**

*   **AI Agents as a Bridge:** AI agents are presented as a potential solution to bridge the gap between the complexity of Web3 and the average user. They can automate tasks, simplify interactions, and reduce the learning curve.
*   **Deterministic Actions:** AI agents, unlike LLMs alone, combine the reasoning of LLMs with deterministic actions (code execution).  This allows them to interact with systems like Hedera in predictable ways.  The LLM decides *what* to do, the deterministic code *does* it.
*   **Hedera's Suitability:** Hedera's features (fast finality, low fees, security) are implicitly presented as being well-suited for AI agent interactions, particularly for microtransactions and frequent on-chain actions.
*   **"Character Files" for Agent Personality:**  The concept of "character files" (JSON files in the demo) allows developers to define the personality and capabilities of their AI agents, guiding their behavior and responses.
*   **LangChain's Role:**  The integration with LangChain demonstrates a way to leverage the strengths of both Web2 and Web3 AI development. LangChain provides a broader set of tools and integrations (Twitter, Discord, etc.), while Hedera provides the decentralized infrastructure.
* **Human in the loop:** The presenter highlights the LangChain capability for "human in the loop", which provides a greater level of user oversight for riskier transactions.
* **Agent Kit Simplification:** The Hedera Agent Kit abstracts away a lot of the complexity of interacting with the Hedera network, making it more approachable for developers less familiar with the specific APIs.

**3. Practical Takeaways:**

*   **Explore the Hedera Agent Kit:** Developers interested in building AI agents on Hedera should investigate the Hedera Agent Kit SDK on GitHub.
*   **Check the Google Doc:** The presenter shares a Google Doc (linked in his pinned tweet on Twitter, and via a QR code in the video) with instructions and resources for setting up the demo environment.
*   **Participate in Bounties:** Developers can potentially earn rewards by participating in Hedera's AI agent bounties.
*   **Integrate Existing Frameworks:**  The Hedera Agent Kit can be integrated with existing AI agent frameworks like Eliza and LangChain, allowing developers to leverage their existing skills and tools.
*   **Consider the UX Implications:** When building dApps, consider how AI agents could simplify the user experience and make the application more accessible to a broader audience.
*   **Experiment with "Character Files":** Explore creating different "character files" to give your AI agents unique personalities and behaviors.
* **Contribute to the open source community:** Help to develop agent kits and contribute to increasing the functionality and stability of using AI agents with Hedera.

**4. Additional Notes:**

*   The presentation is geared towards developers with some familiarity with AI and blockchain concepts.
*   The live coding demo provides a concrete example of how to build a simple agent, but more complex agents would require deeper knowledge of AI agent frameworks and Hedera's services.
*   The presentation is a good starting point for exploring the intersection of AI and Web3 on Hedera, showcasing the potential of this combination.
* The presenter mentioned the use of different types of cryptographic keys (ED25519 and ECDSA) and how developers that currently use MetaMask can continue to do so.
*   The presenter encourages interaction and questions throughout the talk, indicating a willingness to support and guide developers.