# The Key Differences Between Cairo and EVM Execution From Marc Egli ChainSecurity

*Upload Date: 20250228*

*Source: [https://www.youtube.com/watch?v=YVquP50220U](https://www.youtube.com/watch?v=YVquP50220U)*

# The Key Differences Between Cairo and EVM Execution

This document summarizes the YouTube video "The Key Differences Between Cairo and EVM Execution" by Marc Egli of ChainSecurity.

## 1. Main Points

* **Cairo's Immutability:** Cairo's memory is immutable, unlike EVM's mutable state.
* **Cairo's Verifiability:** Cairo is designed for verifiable computing, allowing for easy proof generation.
* **Operator Precedence:**  Cairo operators are structured differently than Solidity's, with varying precedence.
* **Storage Variable Packing and Mapping:** Cairo's storage is packed differently, with mappings.
* **Builtin Functions:** Cairo's built-in functions influence the data cost for operations.
* **Transaction Costs:** Differences in transaction costs result from the differing underlying mechanisms of Cairo and EVM.
* **Reentrancy Vulnerability:** Although Solidity's vulnerability to reentrancy is historically significant, Cairo reduces this potential problem.
* **Time Stamps and Block Numbers:** Cairo's time stamps and block numbers are rounded and validated for execution.
* **Proxy and Clone Support:** Cairo natively supports these important development features.
* **Developer Frameworks and Composability:** Cairo frameworks are often conducive to DeFi composability.


## 2. Key Insights

The speaker highlights fundamental differences between Cairo and EVM, moving beyond simplistic comparisons.  Importantly, he emphasizes not just the existence of differences but their practical consequences for developers.  The crucial insights include:

* **Memory Model**: Cairo utilizes a fixed memory model with immutability.  Consequently, writes are not possible once a slot is filled.  This immutability is central to its verifiable security characteristics. Solidity, in contrast, allows for dynamic updates.
* **Verification and Security:** Cairo's design prioritizes verifiable computation, which helps prevent common vulnerabilities in other smart contract platforms. This is due to the immutability of memory, creating a very predictable and deterministic environment.
* **Gas Optimization:**  The speaker indirectly points out that Cairo's underlying design features such as immutability and low-level controls can improve gas efficiency, likely a significant selling point for certain use cases.
* **Developer Experience:** The comparison is not purely technical.  The speaker implicitly discusses the likely developer experience differences between the two platforms. The explicit immutability and type checking might influence development choices.  

## 3. Practical Takeaways

* **Security-Conscious Development:** Developers considering Cairo should prioritize building secure contracts by understanding and leveraging its immutability model, rather than depending on built-in mechanisms to prevent possible errors.
* **Performance and Efficiency:** Developers will need to understand how storage variables and associated costs will affect deployment and execution.
* **Thorough Testing and Validation:** Cairo's unique memory model and operations demand thorough testing to ensure compatibility and validity in their execution environment.
* **Ecosystem Comprehension**: Building on Starknet and adopting Cairo requires a deep understanding of its ecosystem and available tools, including documentation and frameworks.

## 4. Additional Notes

The video transcript reveals a clear explanation of the core differentiators and practical implications for developers. The speaker's experience in smart contract audits likely informs the discussion and makes the material relatable.  Further research into specific tools and resources mentioned in the video would be very beneficial.