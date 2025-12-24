# Crimson Venturer (Built for Base)

Crimson Venturer is a browser-first Base inspection toolkit designed to validate network connectivity, inspect blockchain data, and provide verifiable results through read-only probes using Coinbase Wallet SDK and Base RPC endpoints.

## What this repository does

This tool serves as a verification surface for Base network integrity, offering easy-to-use methods for confirming chain identity, checking balances, inspecting blocks, and more. All queries are read-only and do not broadcast any transactions.

---

## Repository layout

- app/crimson-venturer.ts  
  Browser-based script that connects a Coinbase Wallet and performs onchain RPC queries.

- config/base.networks.json  
  Static configuration file for Base Mainnet and Base Sepolia (RPC URLs, explorers, chainIds).

- scripts/sample-addresses.json  
  Sample addresses for repeatable read-only probes.

- contracts/  
  Solidity contracts deployed to Base Sepolia for testnet validation:
  - control_srtructure.sol — demonstrates the use of conditional statements
  - arrays.sol — defines dynamic or fixed-size arrays  

- package.json  
  Dependency manifest referencing Coinbase SDKs and multiple Base and Coinbase repositories.

- README.md  
  Primary technical documentation for the repository.

---

## Supported networks

Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  

Base Mainnet  
chainId (decimal): 8453  
Explorer: https://basescan.org  

---

## Tooling and dependencies

This repository uses the following key dependencies:
- Coinbase Wallet SDK for EIP-1193 wallet connection  
- OnchainKit for Base-compatible primitives and tools  
- viem for efficient, typed RPC communication with Base networks  
- Several Base and Coinbase repositories referenced as direct dependencies  

---

## Author contacts:

GitHub: https://github.com/headway-mordant  

Email: headway_mordant.0z@icloud.com

---

## Testnet Deployment (Base Sepolia)

As part of pre-production validation, one or more contracts may be deployed to the Base Sepolia test network to confirm correct behavior and tooling compatibility.

Network: Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  

Contract control_srtructure.sol address:  
0xf3C6931B64De685764020deC329161D23fbDeE73 

Deployment and verification:
- https://sepolia.basescan.org/address/0xf3C6931B64De685764020deC329161D23fbDeE73 
- https://sepolia.basescan.org/0xf3C6931B64De685764020deC329161D23fbDeE73/0#code  

Contract arrays.sol address:  
0x67a72D9B6671C6A7B52458696030066B7Dc9a3db

Deployment and verification:
- https://sepolia.basescan.org/address/0x67a72D9B6671C6A7B52458696030066B7Dc9a3db
- https://sepolia.basescan.org/0x67a72D9B6671C6A7B52458696030066B7Dc9a3db/0#code  

These testnet deployments provide a controlled environment for validating Base tooling, account abstraction flows, and read-only onchain interactions prior to Base Mainnet usage.

---

## License

MIT License

Copyright (c) 2025 YOUR_NAME
