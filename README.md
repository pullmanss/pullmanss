# Hi there, I'm pullmanss! 👋
### Smart Contract Security Researcher & Web3 Auditor 🛡️

Dedicated to securing the decentralized web by conducting deep manual reviews, threat modeling, and advanced automated testing of Solidity-based smart contracts. Specialized in identifying complex logic flaws, integration issues, and economic attack vectors in DeFi protocols.

---

## 🎯 Core Specializations

*   **DeFi Protocol Security:** Auditing lending pools, AMMs, yield aggregators, and synthetic asset protocols.
*   **Economic Attack Vector Analysis:** Identifying vulnerabilities related to oracle manipulation, sandwich attacks, and flash-loan-assisted exploits.
*   **Invariant & Property-Based Testing:** Designing stateful and stateless fuzzing suites to verify protocol invariants under extreme conditions.
*   **Static & Dynamic Code Analysis:** Integrating automated tooling pipelines to detect common vulnerability patterns and code quality issues.
*   **Access Control & Governance Security:** Verifying DAO, multisig, and upgradeability patterns (UUPS, Transparent proxies).

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

---

## 📁 Featured Security Projects

### [DeFi Price Oracle Fuzzing Suite](https://github.com/pullmanss/defi-fuzz)
*Stateful Invariant Testing & Security Patch Demonstration*
*   **Vulnerability Target:** Spot-price oracle manipulation via AMM DEX reserve distortion, causing Lending Pool bad debt.
*   **Methodology:** Built a Foundry-based handler testing suite executing bounded mutations (swaps, deposits, borrows).
*   **Exploit Reproduction:** Programmatically forced the fuzzer to discover the exact sequence of actions to cause protocol insolvency.
*   **Remediation:** Integrated a decentralized reference price oracle (`SecurePriceOracle`) and verified system stability across **128,000+ test scenarios**.

---

## 📊 Profiles & Contact
*   **GitHub:** Explore my audit repositories and testing environments.
*   **Interests:** Actively analyzing historical DeFi exploits, reviewing post-mortems, and participating in competitive audit contests.
