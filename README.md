# Chandigarh University Summer Internship With Metacrafters Project 03

**Project Objective** For this project, create a simple contract with 2-3 functions. Then show the values of those functions in frontend of the application.

## Introduction To Locker Dapp 

A decentralized application (DApp) known as a "Locker". This application facilitates secure management of digital assets on the Ethereum blockchain through functionalities such as ownership transfer, Ether deposit and withdrawal, and token locking and unlocking. It leverages MetaMask for wallet integration, enabling users to autonomously control and monitor their assets while ensuring transparency and security through blockchain technology.

## Locker Dapp Features 

**Ownership Management:** Users can transfer ownership of the smart contract securely to another Ethereum address, providing flexibility in administrative control over the contract.

**Ether Management:** The DApp allows users to deposit and withdraw Ether (ETH) directly from the smart contract, facilitating secure and auditable transactions on the Ethereum blockchain.

**Token Locking:** Users can lock tokens into the smart contract for a specified period, enhancing security and preventing unauthorized transfers during the lock period.

**Token Unlocking:** After locking tokens, users have the ability to unlock them when needed, providing flexibility in managing their token holdings and liquidity.

**MetaMask Integration:** The application seamlessly integrates with MetaMask, a popular Ethereum wallet browser extension, enabling secure wallet management and transaction signing directly from the user's browser.

**Real-time Updates:** The interface dynamically updates to reflect the current state of transactions and contract interactions, providing users with real-time feedback and visibility into their operations.

**Error Handling:** The DApp includes robust error handling mechanisms to manage exceptions during operations like ownership transfers and token transactions, ensuring smooth user experience and transaction reliability.

**User Interface:** Designed with a clean and intuitive user interface, the DApp offers easy navigation and interaction for users to perform actions such as connecting wallets, checking ownership status, and executing transactions with minimal complexity.

## Application Contract Explanation 

### 1. Ownership Management

- **Current Owner**: The contract initializes with an owner (`owner`) set to the address that deploys the contract.
- **Transfer Ownership**: The current owner can transfer ownership to a new address (`transferOwnership` function).

### 2. Financial Management

- **Balance**: Tracks the current Ether balance (`balance`) held by the contract.
- **Deposit**: Allows the owner to deposit additional Ether into the contract (`deposit` function).
- **Withdraw**: Enables the owner to withdraw Ether from the contract, ensuring the withdrawal amount does not exceed the contract's balance (`withdraw` function).
- **Insufficient Balance Error Handling**: If the withdrawal amount exceeds the contract's balance, it throws an `InsufficientBalance` error.

### 3. Token Locking

- **Locked Tokens**: Implements a mechanism to lock tokens (simulated with Ether) from the contract's balance, associated with specific addresses (`lockTokens` function).
- **Unlock Tokens**: Allows addresses to unlock previously locked tokens, restoring them to the contract's balance (`unlockTokens` function).
- **Balance Check**: Ensures sufficient balance before locking or unlocking tokens to prevent errors (`require` statements).

## Events

The contract emits events to notify external observers about certain actions:

- `Deposit(uint256 amount)`: Triggered when Ether is deposited into the contract.
- `Withdraw(uint256 amount)`: Triggered when Ether is withdrawn from the contract.
- `OwnershipTransferred(address indexed previousOwner, address indexed newOwner)`: Triggered when ownership of the contract is transferred.
- `TokensLocked(address indexed to, uint256 amount)`: Triggered when tokens are locked by an address.
- `TokensUnlocked(address indexed to, uint256 amount)`: Triggered when tokens are unlocked by an address.


## Steps to reproduce

To deploy and interact with the contract:
1. Compile the contract using a Solidity compiler.
2. Deploy the compiled contract to an Ethereum blockchain network.
3. Interact with the deployed contract using Ethereum transactions.
