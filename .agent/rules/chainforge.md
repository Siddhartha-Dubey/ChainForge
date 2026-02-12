---
trigger: always_on
---

# ChainForge Project Rules & Context

## 1. Project Context & Objectives
[cite_start]You are building **ChainForge**, a decentralized governance layer for open-source collaboration[cite: 2, 20]. [cite_start]The goal is to solve the problem of centralized control in open source [cite: 8] [cite_start]by creating a transparent, trustless system for managing contributions[cite: 3].

### Core Workflow to Implement:
1.  [cite_start]**Repository Registration:** Users register a GitHub repository on-chain[cite: 26, 56].
2.  [cite_start]**Contribution Submission:** Contributors submit a hash of their Pull Request (PR) to the blockchain[cite: 27, 33, 57].
3.  [cite_start]**DAO Governance:** The community votes on the PR via a DAO mechanism[cite: 22, 28, 58].
4.  [cite_start]**Resolution:** The PR is accepted or rejected transparently based on the vote[cite: 29].
5.  [cite_start]**Reputation:** Accepted contributions update the contributor's on-chain reputation score[cite: 30, 36, 60].

## 2. Technology Stack
Strictly adhere to the following stack for this Hackathon project:
* [cite_start]**Blockchain:** Solidity Smart Contracts (deploying to Polygon/Ethereum Testnet)[cite: 40, 41].
* [cite_start]**Frontend:** React.js [cite: 43] [cite_start]with Ethers.js [cite: 44] for blockchain interaction.
* [cite_start]**Identity:** Metamask for wallet connection and identity[cite: 45, 52].
* [cite_start]**Storage:** IPFS for optional metadata (like detailed PR descriptions)[cite: 47].

## 3. Global Development Rules (Hackathon Mode)

### A. Code Quality & Best Practices
* **Smart Contract Security:** Prioritize security. [cite_start]Use `OpenZeppelin` libraries where applicable. ensuring no single point of control[cite: 53].
* **React Components:** Keep components functional and reusable. Use hooks for state management.
* **Hardhat/Foundry:** Use standard development environments for compiling and testing Solidity.
* **Speed vs. Perfection:** This is a hackathon project. [cite_start]Prioritize a working "Happy Path" (Connect Wallet -> Vote -> Update Score) over complex edge-case handling.

### B. Syntax & Verification Checks
* **Pre-Flight Check:** Before presenting code, strictly verify syntax.
    * For Solidity: Ensure code compiles with `npx hardhat compile`.
    * For React: Ensure no unused variables or breaking syntax errors.
* **Linter Compliance:** adhere to standard linting (e.g., `solhint` for Solidity, `ESLint` for React).
* **Self-Correction:** If you generate a smart contract, immediately generate a corresponding test script to verify the basic flow (e.g., "test voting adds to count").

## 4. Key Features Implementation Guide
When asked to implement specific features, recall these specifications:
* [cite_start]**Immutable History:** Ensure all contribution records (PR hashes) are stored permanently on-chain[cite: 23, 35].
* [cite_start]**Portable Reputation:** The reputation score must be tied to the wallet address, allowing it to be portable across platforms[cite: 24, 76].
* [cite_start]**Trustless Verification:** The system must not rely on a central server to approve PRs; it must be purely code/DAO driven[cite: 49].

## 5. Hackathon Deliverables Checklist
1.  [ ] Smart Contract: Registry & Voting logic.
2.  [ ] Frontend: Connect Wallet & Dashboard.
3.  [ ] Integration: React frontend calling Smart Contract functions.
4.  [cite_start][ ] Demo Flow: A script demonstrating the full "Connect -> Vote -> Reputation" cycle.