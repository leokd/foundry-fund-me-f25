FundMe Smart Contract

A decentralized crowdfunding smart contract built on Solidity, allowing users to fund a project with ETH. The contract ensures secure and transparent handling of funds, with only the owner having the ability to withdraw.

Features

Accepts ETH contributions.

Enforces a minimum contribution based on USD value (using Chainlink price feeds).

Tracks funders and their contributions.

Allows only the contract owner to withdraw funds.

Optimized cheaperWithdraw() function to reduce gas costs.

How It Works

Users send ETH to the contract by calling fund().

The contract verifies that the amount meets the MINIMUM_USD requirement.

Contributions are recorded, and funders' addresses are stored.

The contract owner can withdraw funds using withdraw() or the optimized cheaperWithdraw().

Installation & Setup

Prerequisites

Foundry

Node.js & npm (optional for frontend integration)

A Solidity development environment (Remix, Hardhat, or Foundry)

Clone Repository

git clone https://github.com/yourusername/FundMe.git
cd FundMe

Running the Project

Compile the Contract

forge build

Run Tests

forge test

Deploy (Local Anvil Network)

anvil &
forge script script/DeployFundMe.s.sol --broadcast --fork-url http://localhost:8545

Smart Contract Functions

fund()

Allows users to send ETH to the contract.

Requires a minimum amount based on USD value.

withdraw()

Allows the owner to withdraw all funds.

cheaperWithdraw()

A gas-optimized version of withdraw().

getPrice()

Fetches the ETH/USD price from Chainlink.

getConversionRate(ethAmount)

Converts ETH amount to USD using Chainlink price feeds.

Contributing

Contributions are welcome! Feel free to submit a pull request or open an issue.

License

This project is licensed under the MIT License.
$ cast --help
```
