# Managing Ledger Devices

**Speakers:** Carl Anderson - Ledger


*Upload Date: 20250301*

*Source: [https://www.youtube.com/watch?v=Y-dU2Sf1Xkg](https://www.youtube.com/watch?v=Y-dU2Sf1Xkg)*

### Managing Ledger Devices | Carl Anderson - Ledger

#### Main Points

1. **Introduction to Ledger Device Management Kit**
   - The Ledger Device Management Kit is a replacement for Ledger JS, addressing its shortcomings.
   - It provides a modular, robust, and modular architecture for interacting with Ledger devices.

2. **Key Features of the New Kit**
   - **Modularity**: The kit is divided into smaller, manageable modules like the signer kit, device action kit, and context module.
   - **Session Management**: It manages device sessions, ensuring consistent state across interactions.
   - **Clear Signing**: A feature that allows for more secure signing by providing context to the user about what they are signing.

3. **Security Enhancements**
   - The context module allows developers to pass metadata to the device, enabling users to understand the transaction they are signing.
   - It addresses issues like the 7702 vulnerability, ensuring secure signing.

4. **Developer-Friendly Features**
   - The kit includes a sample application and debugging tools to simplify development.
   - It supports multiple platforms (iOS, Android) and provides a consistent API for developers.

5. **Future Developments**
   - Future updates will include React Native support and additional debugging tools.
   - The kit will evolve to support new Ledger features and improve developer experience.

#### Key Insights

- The new Ledger Device Management Kit is designed to be more modular, secure, and developer-friendly compared to Ledger JS.
- It introduces features like session management and clear signing to enhance security and user experience.
- Developers can benefit from the kit's modular architecture, which allows them to use only the necessary components for their applications.
- The kit is future-proof, supporting upcoming Ledger features and providing tools for easier development and debugging.

#### Practical Takeaways

- Developers should migrate to the new Ledger Device Management Kit for enhanced security and better user experience.
- The kit's modular design allows for easier integration and management of Ledger devices in applications.
- Utilize the sample application and debugging tools provided to streamline development processes.
- Stay updated with future developments in the kit to leverage new features and improvements.

#### Additional Notes

- The presentation emphasizes the importance of clear signing and context in preventing security issues like the 7702 vulnerability.
- Developers are encouraged to explore the kit's documentation and sample application to understand its capabilities fully.
- The kit is available for integration, and developers can start using it immediately to enhance their applications' security and functionality.