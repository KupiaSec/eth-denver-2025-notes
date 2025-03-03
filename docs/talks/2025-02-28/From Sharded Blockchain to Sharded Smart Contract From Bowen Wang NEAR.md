# From Sharded Blockchain to Sharded Smart Contract From Bowen Wang NEAR

*Upload Date: 20250228*

*Source: [https://www.youtube.com/watch?v=cG-JyJYj6LY](https://www.youtube.com/watch?v=cG-JyJYj6LY)*

Here's a summary of the YouTube video "From Sharded Blockchain to Sharded Smart Contract From Bowen Wang NEAR", based on the provided transcript:

**1. Main Points:**

*   **Sharding Introduction:** The video starts with a brief explanation of sharding as a technique to scale blockchains. Unlike traditional blockchains (e.g., Bitcoin, Ethereum mainnet) where all nodes process all transactions, sharding divides the network into "shards," each acting like its own blockchain.
*   **NEAR's Sharding Approach:** NEAR Protocol uses a unique sharding approach where there's only *one* logical chain.  Each block contains "chunks," which are shard blocks from every shard. This simplifies things compared to traditional sharding with separate shard chains and a beacon/main chain.
*   **Problems with Traditional Sharding:** Traditional sharding can become very complex, especially with cross-shard transactions and the potential for forks on individual shard chains.
* **Asynchronous Execution:** Cross-shard transactions in NEAR work asynchronously. A transaction is first executed on the originating shard, and then "receipts" are sent to the destination shard for execution.
*   **Scalability and State Growth:**  Sharding addresses both scalability (throughput) and state growth problems.  With more shards, the network's throughput increases, and the state is divided among the shards, preventing individual nodes from needing to store the entire blockchain state.
*   **Smart Contract Bottleneck:** Even with sharding, a single, highly popular smart contract (like a DeFi application with millions of users) can become a bottleneck.  Its throughput is limited by the throughput of the single shard it resides on.
*   **Sharded Smart Contracts (The Solution):** NEAR introduces "Sharded Smart Contracts" to address this.  A sharded smart contract exists simultaneously on *all* shards.
*   **Global Contract Code:**  The contract *code* is global and available on every shard. This is achieved by deploying the contract code to a special global state rather deploying it to any single account, making it available for all shards.
*   **User-Centric Storage:**  Instead of storing user data within the smart contract's account, user data is stored within the *user's* account, under a specific namespace associated with the contract.
*   **Linear Scalability for Contracts:** Because user data is stored on user accounts, and user accounts are already sharded, the smart contract's storage and throughput scale *linearly* with the number of shards.
*   **Example (USDT):** The video uses a USDT-like fungible token contract as an example. In a traditional sharded setup, all USDT balances are kept on usdt.near.  With a sharded smart contract, each user's USDT balance is stored under a namespace (like `alice.near/usdt.near`) within their own account..
* **Two Key Components of Sharded Contract:**
  1. Deploying Global Contract Code to the shared global state.
  2. Storing the relevant data on the *user's* account.

**2. Key Insights:**

*   **Simplified Sharding:** NEAR's "single chain with chunks" design greatly simplifies sharding and avoids many complexities of traditional sharding designs, particularly for developers and users who can think of it operating as a single blockchain.
*   **True Scalability:** Sharded smart contracts provide a crucial additional layer of scalability. Traditional sharding improves *overall* network throughput, but a single, popular smart contract could still be a bottleneck.  Sharded smart contracts directly address this limitation.
*   **Paradigm Shift in Storage:** The core innovation is shifting the storage of contract-related user data from the contract's account to the *user's* account.  This leverages the inherent sharding of user accounts in NEAR.
*   **Complete Scaling Solution:** By combining blockchain sharding with sharded smart contracts, NEAR achieves scalability both in terms of overall network throughput and in terms of the throughput and state management of individual, high-demand smart contracts.
*   **Global Contract Code is Expensive:** There is mention that deploying a "Global Contract Code" is very expensive, as it implies burning tokens. This is a built-in mechanism to ensure it only happens when absolutely needed and avoid spam or unnecessary global state allocation.

**3. Practical Takeaways:**

*   **Developers Should Consider Sharded Contracts:**  If developing on NEAR and anticipating high usage or significant state growth for a smart contract, developers should seriously consider the sharded smart contract approach.
*   **Understand the Storage Model:** The key to building a sharded smart contract is understanding the user-centric storage model.  Data isn't stored in the contract's storage; it's stored in the user's storage, namespaced to the contract.
*   **Leverage Existing Sharding:** NEAR's existing sharding of user accounts is crucial to making sharded smart contracts work effectively. This means less work for the developer.
* **Global Contract Code are for some specific use cases:** Deploying Global Contract Code has more complexity and cost implication, so only do this if it is really needed.

**4. Additional Notes:**

*   The video mentions that the "Global Contract Code" component is already implemented, and the user-centric storage part is under development.
*   The presenter does not go into the deep technical runtime details of how the sharding and cross-shard communication are handled.
* It appears that this presentation is introducing this sharded smart contract technology, and not presenting a finished, fully implemented system. However, the foundational elements are in place.
* While the example uses a basic fungible token, the concept applies to more complex contracts as well, such as popular DeFi applications.