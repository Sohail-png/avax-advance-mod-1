# avax-advance-mod-1
# Local Avalanche Subnet and Smart Contract Deployment

This guide will help you set up a local Avalanche Subnet using the `avalanche-cli` tool and deploy two smart contracts (`token.sol` and `vault.sol`) using Remix and MetaMask.

## What You Need
- **Golang:** Make sure you have Golang installed, as it's needed to build `avalanche-cli`.
- **Node.js:** Install Node.js to run the local Avalanche node.
- **Avalanche CLI:** Follow the [Avalanche CLI Installation Guide](https://docs.avax.network/tooling/cli-guides/install-avalanche-cli) to install `avalanche-cli`.
- **MetaMask:** Install and set up MetaMask to connect to your local Avalanche node.
- **Remix:** Open Remix and create a new workspace.

## Setting Up the Local Subnet

### Configuring the Subnet:
1. Run the `avalanche subnet create` command and follow the prompts to set up your Subnet.
2. Give your Subnet a name (e.g., `mySubnet`).
3. Choose `SubnetEVM` as the VM.
4. Pick a ChainID (e.g., `151511`).
5. Set any other options as needed.

### Deploying the Subnet:
1. Use the `avalanche subnet export` command to export your Subnet configuration file.
2. Deploy your Subnet locally by running the `avalanche subnet deploy --local` command.

## Deploying Smart Contracts

### Compiling Contracts:
1. Import your `token.sol` and `vault.sol` files into Remix.
2. Compile both contracts in Remix.

### Connecting to the Local Node:
1. In Remix, go to the "ENVIRONMENT" dropdown under the "Deploy" tab.
2. Select "Injected Web3" and make sure MetaMask is connected to your local Avalanche node.

### Deploying Contracts:
For each contract:
1. Select the contract in the "Deployer" section of Remix.
2. Enter any constructor arguments if needed.
3. Click "Deploy."
4. Confirm the transaction in MetaMask.

### Interacting with Contracts:
Use the Remix interface to interact with your deployed contracts. You can call functions, read data, and monitor events directly from Remix.
