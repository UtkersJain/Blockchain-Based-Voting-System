
# Tester Documentation: Blockchain Based Voting System

### Prepared by: Utkers Dongre

## 1. Introduction
This document outlines the testing strategy, test cases, and results for the Blockchain-Based Voting System. It ensures the system is reliable, functional, and secure.

## 2. Testing Objectives
- Validate smart contract logic and security
- Ensure frontend and backend functions operate correctly
- Confirm system performance and scalability
- Verify correct wallet integration and transaction handling

## 3. Testing Scope
### Functional Testing:
- Voter registration
- Candidate registration (admin)
- Voting process
- Result tally

### Non-Functional Testing:
- Security (replay attack prevention, tampering detection)
- Performance (transaction throughput and latency)
- Usability (UX on various browsers and screen sizes)

## 4. Test Environment
- Ganache (Local Ethereum Blockchain)
- Goerli Testnet
- MetaMask for transaction signing
- Browser: Chrome, Firefox, Edge
- OS: Windows 11, Ubuntu 22.04

## 5. Test Cases

| Test Case ID | Description | Input | Expected Output | Status |
|--------------|-------------|-------|------------------|--------|
| TC_01 | Register new voter | Wallet address | Registered successfully | Pass |
| TC_02 | Double voter registration | Same wallet | Error: Already registered | Pass |
| TC_03 | Vote for candidate | Voter ID, Candidate ID | Vote recorded | Pass |
| TC_04 | Vote again | Same Voter | Error: Already voted | Pass |
| TC_05 | View results | None | Candidate vote count | Pass |
| TC_06 | Unauthorized candidate addition | Non-admin wallet | Error: Only admin | Pass |
| TC_07 | Voting outside voting period | Time constraint | Error: Voting not allowed | Pass |

## 6. Testing Tools Used
- Truffle Test
- Hardhat Test Suite (Mocha/Chai)
- Postman (for backend API testing)
- Jest/React Testing Library (Frontend unit tests)
- Lighthouse (Performance and accessibility audits)

## 7. Bug Tracking & Reporting
All bugs were logged and tracked using GitHub Issues with the following labels:
- Severity: High/Medium/Low
- Type: UI/Logic/Blockchain/API

## 8. Known Issues
- Gas fees during peak hours might delay vote confirmation on testnet
- No biometric authentication implemented

## 9. Suggestions for Improvement
- Add automated browser testing (e.g., Selenium/Cypress)
- Enhance backend rate-limiting and logging
- Expand smart contract testing coverage

## 10. Approval
All functional test cases passed on both local and testnet environments. The system is recommended for deployment.

---
