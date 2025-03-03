# Arbitrum Stylus Unveiled: Where Rust Meets the EVM

**Speakers:** Daniel Bigos - OpenZeppelin


*Upload Date: 20250224*

*Source: [https://www.youtube.com/watch?v=VpxTKhL_CyI](https://www.youtube.com/watch?v=VpxTKhL_CyI)*

## Main Points

### 1. Introduction to Arbitrum Stylus
- **Arbitrum Stylus** is a new technology that allows developers to write smart contracts in Rust, a language known for its safety and performance.
- It introduces a **WASM virtual machine** alongside the EVM, enabling developers to write contracts in Rust and deploy them on Arbitrum chains.

### 2. Key Features of Stylus SDK
- **Cargo Stylus Command**: A command-line tool for generating project templates and managing dependencies.
- **Cargo Stylus Macro**: A macro that generates the necessary Rust code to interact with the EVM.
- **Storage and Functionality**: 
  - Uses a **storage macro** to define the contract's storage structure.
  - Uses an **entry macro** to define the contract's public functions.
- **Error Handling**: 
  - Uses a **derive macro** to generate error handling code.
  - Allows for defining custom errors and events.
- **Testing**: 
  - Provides a **unit testing library** for testing smart contracts.
  - Supports **mocking** and **event testing**.

### 3. Deployment and Interaction
- **Deployment**: 
  - Contracts are deployed using the `cargo stylus deploy` command.
  - Deployment involves two transactions: one for deployment and one for activation.
- **Interaction**: 
  - Uses a **main.rs file** with a `print_abi` function to generate a Solidity-like interface.
  - Allows for **overriding functions** from component contracts.

### 4. Advanced Features
- **Contract Composition**: 
  - Supports **inheritance** and **trait implementation**.
  - Allows for **overriding functions** and **trait implementation**.
- **Modifiers**: 
  - Uses Rust tricks for function inlining and loop unrolling to optimize performance.
- **Optimization**: 
  - Utilizes **WASM optimizations** and **Rust compiler optimizations** to improve performance.
  - Demonstrates significant performance improvements over Solidity implementations.

### 5. Use Cases and Future Directions
- **On-Chain Verification**: 
  - Can be used for on-chain verification with ZK proofs.
- **Advanced DeFi Instruments**: 
  - Enables building complex DeFi protocols with high-performance on-chain logic.
- **High-Performance Protocols**: 
  - Allows for moving computationally intensive tasks to Stylus contracts for optimization.

### Practical Takeaways

#### Key Insights
- **Performance**: Stylus offers significant performance improvements over Solidity, especially for computationally intensive tasks.
- **Safety**: Rust's memory safety features can help prevent common smart contract vulnerabilities.
- **Flexibility**: The ability to write contracts in Rust provides more flexibility and power compared to Solidity.

#### Actionable Steps
1. **Set Up Your Environment**: Use `cargo stylus` to set up a new project and generate the necessary files.
2. **Define Storage and Logic**: Use the provided macros to define the contract's storage and implement its logic.
3. **Test Your Contract**: Utilize the testing library to write and run tests for your contract.
4. **Deploy and Interact**: Deploy your contract using the provided tools and interact with it using the generated Solidity interface.

#### Additional Resources
- Explore the **Open Zeppelin** repository for more examples and best practices.
- Consider contributing to the development of the Stylus ecosystem by implementing new features and optimizations.

### Conclusion
Arbitrum Stylus represents a significant advancement in smart contract development, offering developers a powerful and flexible toolset to build high-performance, secure smart contracts. By leveraging Rust's strengths, developers can create more robust and efficient applications on the Arbitrum network.