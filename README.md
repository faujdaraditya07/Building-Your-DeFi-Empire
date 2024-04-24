# Building-Your-DeFi-Empire

## Avalanche EVM Subnet Tutorial for a DeFi Kingdom Clone

Welcome to our comprehensive tutorial on setting up your very own EVM subnet on the Avalanche network! This tutorial is designed to help you lay the groundwork for building a DeFi Kingdom clone by guiding you through the creation and deployment of a custom subnet. You'll also learn how to deploy two fundamental smart contracts: an ERC20 token contract and a Vault contract. These will serve as the core components for your DeFi game, allowing you to dive into the world of decentralized finance and start building your DeFi empire.

## Overview

1. **Set Up Your EVM Subnet**: Follow our detailed steps and utilize Avalanche documentation to create a custom EVM subnet.
2. **Define Your Native Currency**: Establish your own native currency to be used as the in-game currency for your DeFi Kingdom clone.
3. **Connect to MetaMask**: Integrate your EVM Subnet with MetaMask to enable wallet interactions.
4. **Deploy Basic Building Blocks**: Use Solidity and Remix to deploy smart contracts that will form the backbone of your game, involving battling, exploring, and trading mechanisms.

## Getting Started

### Prerequisites

- Basic understanding of blockchain technology and Solidity
- Node.js and npm installed on your computer
- MetaMask wallet installed in your browser
- Access to the Avalanche network

### Step-by-Step Guide

#### Step 1: Set Up Your EVM Subnet

1. **Visit the Avalanche Documentation**: Start by visiting the [Avalanche Developer Documentation](https://docs.avax.network/) to understand the requirements for creating a subnet.
2. **Install Avalanche CLI**: Install the Avalanche command-line tools necessary for creating and managing subnets.
   ```bash
   npm install -g avalanche-cli
   ```
3. **Create Your Subnet**: Use the Avalanche CLI to create your EVM-compatible subnet.
   ```bash
   avalanche subnet create --name MyDeFiKingdomSubnet --evm
   ```

#### Step 2: Define Your Native Currency

1. **Configure Native Currency**: During the subnet creation process, specify your native currency details, including name, symbol, and initial supply.
2. **Deploy Token Contract**: Use a standard ERC20 token contract as a template to deploy your native currency using Remix.

#### Step 3: Connect to MetaMask

1. **Add Custom RPC**: Follow the steps in our guide to add your subnet as a custom RPC network in MetaMask.
   - Network Name: `MyDeFiKingdomSubnet`
   - New RPC URL: Provided by your subnet setup
   - Chain ID: Specified during the subnet creation
   - Currency Symbol: Your native currency symbol

#### Step 4: Deploy Basic Building Blocks

1. **Write Smart Contracts**: Develop your ERC20 token contract and a Vault contract using Solidity.
2. **Test Locally**: Use Remix or Hardhat for local testing and debugging of your contracts.
3. **Deploy to Subnet**: Once tested, deploy these contracts to your subnet via Remix, connected to your MetaMask.

## Additional Resources

- [Avalanche Documentation](https://docs.avax.network/)
- [Remix IDE](https://remix.ethereum.org/)
- [Solidity Docs](https://docs.soliditylang.org/)

## Example Contracts

Here's a basic template for an ERC20 token contract that you might use:

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";

contract MyGameToken is ERC20 {
    constructor() ERC20("MyGameToken", "MGT") {
        _mint(msg.sender, 1000000 * (10 ** uint256(decimals())));
    }
}
```

## Conclusion

By following this tutorial, you've taken significant steps towards building your own DeFi Kingdom clone on Avalanche. You've learned how to set up an EVM subnet, define a native currency, connect to MetaMask, and deploy essential smart contracts. Continue to explore more complex contract interactions and game mechanics to expand your DeFi game.

Happy building!
