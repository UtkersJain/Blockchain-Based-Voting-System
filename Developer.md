
# Developer Documentation: Blockchain Based Voting System

### Prepared by: Vasu Sethiya

## 1. Project Overview
The Blockchain-Based Voting System is a decentralized application (DApp) aimed at ensuring secure, transparent, and tamper-proof voting using Ethereum smart contracts. This document provides technical details relevant to developers for understanding, building, and maintaining the system.

## 2. System Architecture

### Components:
- Frontend: React.js
- Backend: Node.js + Express
- Blockchain: Ethereum (Local: Ganache, Testnet: Goerli)
- Smart Contracts: Solidity
- Wallet Integration: MetaMask
- IPFS (Optional): For storing voter ID images or documents

## 3. Smart Contract Details

### Contract: Voting.sol
Solidity Version: ^0.8.0

#### Key Structures:
- struct Candidate
- struct Voter

#### Core Functions:
- addCandidate(string memory _name)
- registerVoter(address _voter)
- vote(uint _candidateId)
- getResults()
- getCandidateList()

#### Modifiers:
- onlyOwner
- onlyRegisteredVoter
- hasNotVoted

### Tools:
- Truffle / Hardhat
- Ganache CLI for local testing

## 4. Backend Details

### Tech Stack:
- Node.js
- Express.js
- Web3.js / Ethers.js
- dotenv (for storing contract address and private key)

### Responsibilities:
- Communicate with smart contracts
- Authenticate voters
- Serve API endpoints for frontend
- (Optional) Interact with IPFS and database

### Sample APIs:
- POST /registerVoter
- POST /vote
- GET /results

## 5. Frontend Details

### Tech Stack:
- React.js
- Web3.js / Ethers.js
- Bootstrap / Tailwind CSS

### Pages:
- Home
- Voter Registration
- Voting Dashboard
- Admin Panel
- Result Page

### Features:
- Wallet connection via MetaMask
- Real-time voting updates
- Access control and alerts

## 6. Developer Environment Setup

### Prerequisites:
- Node.js & npm
- Truffle or Hardhat
- Ganache
- MetaMask Extension
- VS Code or preferred IDE

### Steps:
1. Clone the repository
2. Run npm install in root, backend, and frontend directories
3. Start Ganache CLI or GUI
4. Deploy smart contract: truffle migrate
5. Start backend server: npm run dev
6. Start frontend app: npm start

## 7. Deployment
- Smart Contract: Deployed to Goerli Testnet
- Frontend: Deployed on Netlify / Vercel
- Backend: Deployed using Render / Railway / Heroku

## 8. Best Practices
- Use .env for keys and contract addresses
- Add validations in smart contract
- Avoid storing sensitive data on-chain
- Use events for tracking activities

## 9. Future Enhancements
- Multi-factor authentication
- Biometric voter ID integration
- zk-SNARKs for privacy-preserving voting
- Token-based access control

## 10. Resources
- Solidity Docs: https://docs.soliditylang.org/
- Truffle Suite: https://trufflesuite.com/
- Web3.js Docs: https://web3js.readthedocs.io/
- Ethers.js Docs: https://docs.ethers.io/

---
