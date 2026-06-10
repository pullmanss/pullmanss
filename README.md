# Hi there, I'm pullmanss! 👋
### Smart Contract Security Researcher & Web3 Auditor 🛡️

Dedicated to securing the decentralized web by conducting deep manual reviews, threat modeling, and advanced automated testing of Solidity-based smart contracts. Specialized in identifying complex logic flaws, integration issues, cross-contract state desynchronization, and economic attack vectors in DeFi protocols.

---

## 🎯 Core Specializations

*   **DeFi Protocol Security:** Auditing lending pools, AMMs, yield aggregators, synthetic assets, and liquid staking protocols.
*   **Economic Attack Vector Analysis:** Identifying vulnerabilities related to oracle manipulation, sandwich attacks, and flash-loan-assisted exploits.
*   **Invariant & Property-Based Testing:** Designing stateful and stateless fuzzing suites to verify protocol invariants under extreme conditions.
*   **Cross-Protocol Integration Testing:** Modeling interactions between lending consumer protocols and external AMM price feeds.
*   **Access Control & Governance Security:** Verifying DAO, multisig, timelock, and upgradeability patterns (UUPS, Transparent proxies, Diamond Pattern).

---

## 🛠️ Technical Arsenal

### Languages & Frameworks
![Solidity](https://img.shields.io/badge/Solidity-%23363636.svg?style=flat-square&logo=solidity&logoColor=white)
![Foundry](https://img.shields.io/badge/Foundry-FF0055?style=flat-square&logo=rust&logoColor=white)
![Hardhat](https://img.shields.io/badge/Hardhat-%233178C6.svg?style=flat-square&logo=javascript&logoColor=white)
![Bash](https://img.shields.io/badge/Shell_Scripting-%23121011.svg?style=flat-square&logo=gnu-bash&logoColor=white)

### Testing, Fuzzing & Static Analysis
*   **Development & Testing:** Foundry (`forge`, `cast`, `anvil`, `chisel`), Hardhat
*   **Static Analyzers & Linters:** Slither, Aderyn, Solhint
*   **Fuzzers & Symbolic Execution:** Foundry Stateful/Stateless Fuzz, Echidna, Halmos (symbolic testing)

### Standards & Tokenomics
*   **Standards:** ERC-20, ERC-721, ERC-1155, ERC-4626 (Tokenized Vaults), EIP-712 (Signatures)
*   **Architectures:** Upgradeable Proxies, Diamond Pattern (ERC-2535), Multi-signature setups

---

## 🔬 Audit & Testing Methodologies

1.  **System Threat Modeling:** Analyzing the protocol's whitepaper and architecture to map out trust assumptions and potential attack surfaces.
2.  **Manual Line-by-Line Code Review:** Verifying business logic, checking for reentrancy, overflow/underflow, access control, and edge-case execution paths.
3.  **Stateful Invariant Fuzzing:** Building handlers to simulate complex user behavior over hundreds of state transitions to find edge-case system failures.
4.  **Static Analysis Integration:** Running security linters to eliminate standard vulnerabilities (SWC Registry) early in the audit pipeline.
5.  **Formal & Symbolic Verification:** Utilizing SMT solvers to mathematically prove that assertions cannot be violated under any execution path.

---

## 📁 Featured Security Projects

### 1. [Read-Only Reentrancy Exploit PoC](https://github.com/pullmanss/defi-readonly-reentrancy)
*Cross-Protocol Economic Exploit Simulation*
*   **Vulnerability Target:** Non-synchronized state variables in AMM core during multi-asset liquidity withdrawals (`view` function vulnerability).
*   **Methodology:** Built an exploit agent executing nested state-query calls within the raw `ETH` transfer callback (fallback function execution).
*   **Exploit Demonstration:** Intercepted the pricing pipeline of a lending consumer protocol, temporarily inflating LP collateral pricing by **~300%** to extract excess stablecoin liquidity.
*   **Remediation:** Evaluated secure pricing architectures including checkpoint-based values, TWAP oracle structures, and external lock-state checks.

### 2. [DeFi Price Oracle Fuzzing Suite](https://github.com/pullmanss/defi-fuzz)
*Stateful Invariant Testing & Security Patch Demonstration*
*   **Vulnerability Target:** Spot-price oracle manipulation via AMM DEX reserve distortion, causing Lending Pool bad debt.
*   **Methodology:** Built a Foundry-based handler testing suite executing bounded mutations (swaps, deposits, borrows).
*   **Exploit Demonstration:** Programmatically forced the fuzzer to discover the exact sequence of actions to cause protocol insolvency.
*   **Remediation:** Integrated a decentralized reference price oracle (`SecurePriceOracle`) and verified system stability across **128,000+ test scenarios**.

### 3. [EtherVault Reentrancy PoC](https://github.com/pullmanss/defi-reentrancy-poc)
*Reentrancy Attack Vector & Mitigation Proof of Concept*
*   **Vulnerability Target:** Broken Checks-Effects-Interactions pattern in an Ethereum vault contract allowing state-reentry before balance updates.
*   **Methodology:** Created a custom attacker contract leveraging fallback functions to programmatically drain vault liquidity.
*   **Exploit Demonstration:** Wrote an automated Foundry test case reproducing a multi-user fund extraction scenario.
*   **Remediation:** Refactored state-update sequence to comply with secure development patterns and validated state-rollback execution.

---

## 📊 Profiles & Contact
*   **GitHub:** Explore my audit repositories and testing environments.
*   **Interests:** Actively analyzing historical DeFi exploits, reviewing post-mortems, and participating in competitive audit contests on **Code4rena** and **Sherlock**.
