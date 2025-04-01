# 🔗 NeutraLink Token (NTL)

This repository contains the official smart contract for the **NeutraLink Token (NTL)** – an ERC-20 token designed to represent **pre-certified and certified carbon credits** generated through real-time solar energy production, verified by IoT devices.

---

## 🪙 Token Purpose

The **NTL token** is the core digital asset within the NeutraLink ecosystem.  
It enables transparent and verifiable tracking, trading, and certification of carbon credits using blockchain technology.

---

## ⚙️ Features

- ✅ **ERC-20 standard** token
- 🧾 `mint()` function restricted to the NeutraLink platform
- 🔐 Controlled token issuance based on solar data via API/IoT
- ♻️ **Proxy architecture (Upgradeable)** using OpenZeppelin's UUPS pattern
- 💼 Web3 integration with MetaMask and other wallets
- 📜 Audit-ready structure for future validation

---

## 🛠️ Tech Stack

- **Solidity**
- **OpenZeppelin Contracts**
- **Hardhat** or **Foundry** for development & testing
- **Remix IDE** for manual deployment and testing
- **Ethers.js** / **Web3.js** for integration

---

## 📦 Project Structure

```
neutralink-token/
├── contracts/
│   └── NeutraLinkToken.sol
├── scripts/
│   └── deploy.js (or deploy.ts for TypeScript)
├── test/
│   └── token.test.js
├── hardhat.config.js
├── README.md
└── package.json
```

---

## 🚀 Getting Started

1. Clone the repository:
```bash
git clone https://github.com/neutralinkeco/neutralink-token.git
cd neutralink-token
```

2. Install dependencies:
```bash
npm install
```

3. Compile the contracts:
```bash
npx hardhat compile
```

4. Run tests:
```bash
npx hardhat test
```

5. Deploy to testnet:
```bash
npx hardhat run scripts/deploy.js --network sepolia
```

---

## 🧠 Key Functions

```solidity
function mint(address to, uint256 amount) external onlyOwner
```
> Mints new NTL tokens. Only callable by the NeutraLink platform.

```solidity
function initialize() public initializer
```
> Replaces the constructor in proxy contracts. Must be called during deployment.

---

## 🔐 Security

- Proxy contracts use `initialize()` instead of constructors
- `mint()` access is restricted to NeutraLink’s verified wallet
- Upgradable via UUPS pattern to support future changes (e.g., auditing, certification layer)
- Recommended: External audit before mainnet deployment

---

## 📬 Contact

- 🌐 Website: [neutralinkeco.com](https://neutralinkeco.com)
- 🧠 Tech: dev@neutralinkeco.com
- 🐙 GitHub: [github.com/neutralinkeco](https://github.com/neutralinkeco)

---

## 📄 License

Licensed under the **MIT License**.  
See [LICENSE](./LICENSE) for more information.

---

## 🛡️ Disclaimer

This token does not represent speculative financial instruments.  
It represents **real-world environmental impact** backed by solar generation data, and should only be used within the NeutraLink ecosystem.
```
