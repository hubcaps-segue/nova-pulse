# Nova Pulse (Built for Base)

Nova Pulse is a powerful, read-only onchain tool developed for Base Mainnet and Base Sepolia. It helps you validate network integrity, explore blockchain states, and verify contract deployments via Coinbase Wallet SDK, with results cross-checked through Basescan.

---

## Main Features

- **Seamless Wallet Integration** via the **Coinbase Wallet SDK** (EIP-1193)  
- **Base ChainId Validation** for Mainnet (8453) and Sepolia (84532)  
- **Snapshot Capabilities** to fetch block height, gas price, and gas usage  
- **Address Analysis** to retrieve balance, transaction counts, and check bytecode  
- **ERC-20 Token Analysis** for token metadata, total supply, and balance  
- **Basescan Verification** to independently validate contract and address data  

---

## Project Structure

- **app/nova-pulse.ts**  
  The core application script that interacts with Coinbase Wallet and queries Base RPC for blockchain data.

- **config/base.networks.json**  
  A configuration file containing RPC URLs, explorers, and chainIds for Base networks (Mainnet and Sepolia).

- **docs/testnet-validation.md**  
  A record of validation steps and results during deployments to Base Sepolia.

- **scripts/sample-addresses.json**  
  A collection of example addresses for testing and validation.

- **contracts/**  
  Solidity contracts deployed on Base Sepolia for testnet validation:
  - `ERC20.sol` — defines a fungible token where all tokens are identical.
  - `mapping.sol` — used for storing balances, permissions, or relationships between keys and values

- **package.json**  
  The dependency manifest, including references to the necessary SDKs and repositories from Coinbase and Base.

- **README.md**  
  This file, which provides an overview of the repository and its usage.

---

## Supported Networks

- **Base Sepolia**  
  ChainId (decimal): 84532  
  Explorer: [sepolia.basescan.org](https://sepolia.basescan.org)

- **Base Mainnet**  
  ChainId (decimal): 8453  
  Explorer: [basescan.org](https://basescan.org)

---

## Functionality and Use Cases

Nova Pulse offers a robust solution for developers to validate the functionality of Base networks before full production use. With it, you can:
- Connect to Coinbase Wallet via **Coinbase Wallet SDK**
- Inspect real-time data on Base, including block details, gas price, and balances
- Verify deployed contracts through **Basescan** links for transparency
- Perform read-only operations with no modifications to the network state

---

## Dependencies and Tools

This repository integrates the following tools:
- **Coinbase Wallet SDK** for connecting with user wallets  
- **OnchainKit** for interacting with Base’s native primitives  
- **Viem** for efficient and type-safe communication with Base’s RPC  
- Direct references to repositories from **Base** and **Coinbase GitHub**

---

## License

MIT License

Copyright (c) 2025 YOUR_NAME

---

## Author Information

GitHub: [https://github.com/hubcaps-segue](https://github.com/hubcaps-segue)  

Email: hubcaps-segue.0i@icloud.com 

X: [https://x.com/buzabandis28](https://x.com/buzabandis28)  

---

## Testnet Deployment on Base Sepolia

To ensure the correct functionality of tooling and network interactions, the following contracts have been deployed to Base Sepolia for validation:

**Network**: Base Sepolia  
**ChainId (decimal)**: 84532  
**Explorer**: [sepolia.basescan.org](https://sepolia.basescan.org)

**Contract ERC20.sol address**:  
0xe22DA3A4C27033718A7dcE83fE3E9dD2FD5Cf107

Deployment and verification:
- [Deployment link](https://sepolia.basescan.org/address/0xe22DA3A4C27033718A7dcE83fE3E9dD2FD5Cf107)
- [Code verification](https://sepolia.basescan.org/0xe22DA3A4C27033718A7dcE83fE3E9dD2FD5Cf107/0#code)

**Contract mapping.sol address**:  
0xAb02aDc81922Ffb76E35e9E46f396e6D1cadEb68

Deployment and verification:
- [Deployment link](https://sepolia.basescan.org/address/0xAb02aDc81922Ffb76E35e9E46f396e6D1cadEb68)
- [Code verification](https://sepolia.basescan.org/0xAb02aDc81922Ffb76E35e9E46f396e6D1cadEb68/0#code)

These deployments confirm that the Base tools and network are functioning as expected, and will be used to ensure compatibility before moving to the Base Mainnet.
