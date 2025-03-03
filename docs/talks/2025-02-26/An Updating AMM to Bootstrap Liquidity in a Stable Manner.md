# An Updating AMM to Bootstrap Liquidity in a Stable Manner

**Speakers:** Neel Tiruviluamala - Forte


*Upload Date: 20250226*

*Source: [https://www.youtube.com/watch?v=Qy0uqozXT10](https://www.youtube.com/watch?v=Qy0uqozXT10)*

Here's a summary of the YouTube video "An Updating AMM to Bootstrap Liquidity in a Stable Manner | Neel Tiruviluamala - Forte," based on the provided transcript:

**1. Main Points:**

*   **Introduction to Forte:** Forte provides on-chain and off-chain tools for developers to create market economies around their assets.
*   **Problem with Existing AMMs:** Traditional AMMs (Automated Market Makers) like constant product market makers (e.g., Uniswap V2) require upfront collateral and have fixed bonding curves, making liquidity bootstrapping challenging and inflexible.  Limit order books are complex and expensive.
*   **ALBC (Adjustable Linear Bonding Curve):** Forte introduces a new AMM called ALBC, which addresses the limitations of traditional AMMs.
*   **Dynamic Slope Adjustment:** The ALBC dynamically adjusts its slope based on trading activity, mimicking a dynamic limit order book without needing upfront liquidity.
*   **Smart Fees:** The ALBC incorporates "smart fees" that incentivize early participants, helping with bootstrapping.
*   **Price Stability:**  The system is geared towards projects wanting price stability through a configurable parameter.
*   **Collateral Conservation:**  ALBC aims for collateral conservation, meaning deposited collateral isn't withdrawn erratically.
*   **Path Independence:** The slope of the bonding curve depends on the total outstanding supply, making it less susceptible to manipulation.
*   **MEV Resistance:** ALBC has properties that provide bounded maximum extractable value, making it more resistant to sandwich attacks and wash trading.
*   **Comparison to Uniswap V3:** The presentation demonstrates how ALBC can achieve price discovery and stability compared to a fixed-range Uniswap V3 position, *without* requiring third-party LPs.
*   **Trading Game Launch:** Forte will launch a trading game at ETH Denver 2025 using the ALBC.

**2. Key Insights:**

*   **Order Books as Inspiration:**  The ALBC is fundamentally designed to mimic the behavior of a continuously updating limit order book. The speaker uses the concept of order book slope frequently to explain how ALBC responds to trades.  A steeper slope means more liquidity and less price impact.
*   **Slope as a Key Parameter:** The slope of the ALBC's linear bonding curve is *the* central dynamic element.  It changes proportionally to trade sizes, increasing with buys (making the curve steeper, providing more liquidity) and, in a mirror effect, allowing sellers to re-enter the market.
*   **Continuous vs. Discrete:** The speaker emphasizes the conceptual shift from discrete limit order books (individual orders at specific prices) to a continuous representation (the ALBC curve).  The area under the curve represents fractional quantities and costs.
*   **Axiomatic Design:** The ALBC's behavior is defined by three key axioms:
    *   **Continuity:** Allows for selling fractional quantities.
    *   **Linearity:** The order book is always a straight line.
    *   **Collateral Conservation:**  Trades don't cause collateral to leave the system; sellers become buyers.
*   **Smart Fees as "Rising" TBC:** The smart fee mechanism, where the bonding curve gradually rises, is mathematically equivalent to a traditional Token Bonding Curve (TBC). This "rising TBC" effect incentivizes early participation by effectively giving early buyers a better average price.
* **Bootstrapping Focus**: The system presented prioritizes the bootstrapping phase. The system dynamically changes to improve this phase.

**3. Practical Takeaways:**

*   **For Developers Building Web3 Economies:** Consider using the ALBC (or understanding its principles) for token launches and liquidity management, especially if price stability during bootstrapping is a priority.
*   **Alternative to Traditional AMMs:**  The ALBC offers a different approach to liquidity provision that doesn't rely solely on external LPs. This could be beneficial for projects with limited initial resources.
*   **Understanding MEV Resistance:** The bounded MEV property of ALBC is an important consideration for projects concerned about front-running and manipulation.
*   **Explore Forte's Tools:**  If you're a developer in the web3 space (particularly in gaming, DeFi, or involving RWAs), investigate Forte's platform and the ALBC specifically.
*   **Participate in the Trading Game:** Engage with Forte's trading game at ETH Denver 2025 to get hands-on experience with the ALBC.

**4. Additional Notes:**

*   The presentation is fairly technical, involving concepts from market microstructure and calculus (integration). However, the speaker does a good job of providing visual aids and explaining the core concepts.
*   The whitepaper is mentioned as a source for more detailed mathematical proofs and explanations.
* Forte presented initial information during the presentation. The "V2" with external liquidity providers will be added, and is expected to be released around March.
* The presenter doesn't explicitly define what the "stability parameter", "W", actually represents, although it is stated that this value can be configured by the developer. It is implied that this setting controls how much the curve changes based on transactions.
* The presenter did not elaborate on *how* smart-fees are distributed.