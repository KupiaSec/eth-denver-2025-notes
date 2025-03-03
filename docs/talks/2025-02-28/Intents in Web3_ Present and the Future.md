# Intents in Web3: Present and the Future

**Speakers:** Asad Ahmed - Okto, Apriori Apriori - Anoma


*Upload Date: 20250228*

*Source: [https://www.youtube.com/watch?v=DOs8EbdUnbc](https://www.youtube.com/watch?v=DOs8EbdUnbc)*

Here's a summary of the YouTube video "Intents in Web3: Present and the Future | Asad Ahmed - Okto | Apriori Apriori - Anoma," based on the provided transcript:

**1. Main Points:**

*   **Shift to Intent-Centric Interactions:**  The Web3 space is shifting from transaction-based interactions to intent-centric interactions. Users express *what* they want, not *how* to achieve it.
*   **Anoma's Architecture:** Anoma is a distributed operating system designed for intent-centric applications.  It abstracts over different chains/computers running the Anoma protocol, presenting a unified execution environment.
*   **Solvers:** A core concept in intent-centric systems is the "solver."  Solvers are agents that find the optimal way to fulfill a user's intent.  They handle tasks like counterparty discovery, routing, liquidity provision, and batch optimization.
*   **Two Components of Anoma Protocol:** Anoma has (1) an off-chain component (peer-to-peer intent gossip layer for counterparty/solver discovery) and (2) a settlement component (which can happen on any blockchain running the Anoma protocol, including Ethereum mainnet/rollups, or other chains).
*   **Verifiability Challenges:**  A key challenge in intent-centric systems is verifiability.  How can users be sure that solvers are acting correctly and fulfilling their intents as specified?
*   **Okto's Approach:** Okto is building a chain abstraction stack for "one-click experiences." It's created its own solver network based on "blocks," like Lego bricks, to combine and build composable flows.
*   **Use Cases:**  The discussion explores various use cases, including complex DeFi operations (flash loans, swaps, deposits), NFT transfers, gaming applications, messaging protocols, and crowdfunding.  Anoma is generalized and can handle a wide variety of intents.
*	**Wallet Integration:** The presentation touches that in the future wallets can facilitate intent-centric operations for the user, like one-click operations and natural language descriptions.

**2. Key Insights:**

*   **User Experience Focus:** Intents dramatically improve the user experience.  Users no longer need to understand the complex underlying mechanisms of blockchains (e.g., routing, gas, bridging). They simply state their desired outcome.
*   **Composability:**  Intent-centric systems enable complex, multi-step workflows to be executed with a single signature.  This unlocks new possibilities for DeFi and other applications.
*   **Solver Specialization:**  Solvers are not monolithic. They can specialize in different tasks (computation, routing, liquidity) and can even compete to provide the best execution for a given intent.  This creates a marketplace of solvers.
*   **Verifiability is Crucial:**  Trust in solvers is paramount.  The discussion highlights the need for verifiable computation (using technologies like ZK proofs, TEEs, or MPC) to ensure solvers fulfill intents honestly and optimally.  Different verification strategies offer different trade-offs in terms of speed and cost.
*   **Resource Locking and Delegation:**  Intents often involve locking resources (e.g., tokens) and delegating authority to solvers to act on the user's behalf, within specific constraints (time bounds, price limits, etc.). Session Keys.
*   **Anoma vs. Other Intent Systems:** Anoma is designed to be a general-purpose intent system, in contrast to more specialized solvers focused on specific use cases (e.g., DEX aggregators).
*   **Economic Viability:** The discussion acknowledges that the economic incentives and mechanisms for solvers are still being explored and proven.
*   **Partial Transactions:** Intents, under discussion here, are represented as partial transactions that can be matched, and proofs must ensure that the partial transactions adhere to set constraints.
* Users, when submitting intents, define all necessary steps within it.

**3. Practical Takeaways:**

*   **Explore Intent-Centric Design:** Developers should start thinking about application design in terms of user intents rather than individual transactions.
*   **Consider Solver Integration:**  If building a DeFi application, consider how it might integrate with an intent-centric system and potentially become a solver.
*   **Focus on Verifiability:**  If building a solver, prioritize mechanisms for verifiable computation to build user trust.
*   **Look for Emerging Use Cases:**  Intents open up new design spaces.  Explore creative applications beyond simple swaps, such as complex multi-protocol interactions, game mechanics, and conditional commitments.
*   **Follow Anoma and Okto:**  Keep an eye on the development of Anoma and Okto, as well as other projects in the intent-centric space (mentioned: Cow Swap, Enzo, projects on Near).
* **Build with Blocks:** If using a chain abstraction stack for a project, composing modular intent solvers can improve the user experience.

**4. Additional Notes:**

*   The discussion is relatively technical, assuming some familiarity with blockchain concepts.
*   Anoma is still under development, and its full production system is not yet live, although its codebase is open source.
*   Okto is actively building and has live applications demonstrating its intent-based approach.
*   The speakers emphasize that the intent-centric space is still evolving, with many open questions and challenges remaining.
* There is discussion about some of the research that went into the project, exploring NPC, witness encryption and TEEs