# Speedrunning the Design of Ethereum as a ZK-L1

**Speakers:** Elias Tazartes - Kakarot ZK-EVM


*Upload Date: 20250301*

*Source: [https://www.youtube.com/watch?v=b--qg5o8muY](https://www.youtube.com/watch?v=b--qg5o8muY)*

### Summary of the Video: "Speedrunning the Design of Ethereum as a ZK-L1"

#### Main Points

1. **Introduction to ZK-L1 Design**
   - The video discusses the design of Ethereum as a ZK-L1 (Zero-Knowledge Layer 1) blockchain.
   - It focuses on the challenges and solutions for making Ethereum provable and scalable using ZK technology.

2. **Key Concepts**
   - **Prover Input Generation**: The process of creating inputs for the prover, which involves extracting necessary data from the Ethereum state.
   - **Trace Generation**: Generating a trace that represents the execution of a block in a provable manner.
   - **Stark Generation**: Creating a proof that verifies the correctness of the trace.

3. **Performance Optimization**
   - The goal is to reduce the time needed to generate proofs from blocks to under 12 seconds.
   - Techniques like parallelization and breaking blocks into smaller chunks are discussed.
   - The importance of hardware acceleration and low-level optimization is highlighted.

4. **Current State of Ethereum Proofs**
   - The average time for generating proofs for Ethereum blocks is around 2 minutes.
   - There are challenges in reducing this time further due to the complexity of the Ethereum execution layer.

5. **Future Directions**
   - Teams are working on hardware acceleration and low-level optimizations.
   - The aim is to make Ethereum provable and scalable within the next year.

#### Key Insights

- **Trace Parallelization**: Parallelizing the trace generation process can significantly reduce the time needed.
- **Hardware Acceleration**: Using specialized hardware like GPUs can speed up the proof generation process.
- **Optimization Techniques**: Various optimization techniques are being explored to make the process faster and more efficient.

#### Practical Takeaways

- **Focus on Optimization**: Teams should focus on optimizing the proof generation process through parallelization and hardware acceleration.
- **Collaboration**: Collaboration between mathematicians, engineers, and hardware experts is crucial for achieving the goal.
- **Continuous Improvement**: Continuous improvement and innovation are necessary to meet the target of proving any blockchain within the desired time frame.

#### Additional Notes

- The video emphasizes the importance of understanding the core concepts of ZK proofs and how they can be applied to Ethereum.
- It also highlights the challenges and potential solutions for making Ethereum a fully provable and scalable ZK-L1.

### Additional Notes

- The video provides a deep dive into the technical aspects of ZK proofs and their application to Ethereum.
- It is aimed at developers and researchers working on ZK technology and Ethereum scalability.