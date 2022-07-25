# UUPS

Sample upgradeable smart-contract

## Run Locally

Intialize hardhat the project

```bash
  npx hardhat
```

Install all the required dependencies

```bash
  npm i @openzeppelin/contracts-upgradeable @openzeppelin/hardhat-upgrades @nomiclabs/hardhat-etherscan dotenv --save-dev
```

Create a new file called Pizza.sol inside the contracts directory and add the following code:

```bash
  Already there in the repo, feel free to use your own smart-contract
```

Update the hardhat.config.js accordingly

Create a new file called .env and add the following contents:

```bash
PRIVATE_KEY = <<DEPLOYER_PRIVATE_WALLET_KEY>>
ETHERSCAN_API_KEY = <<ETHERSCAN_API_KEY>>
INFURA_API_KEY=  <<INFURA_API_KEY>>
```

Deploy the contracts by running the following command

```bash
npx hardhat run --network kovan  ./scripts/deploy-pizza-v1.js
```

Fetch both contract address from etherscan - proxy contract and actual smart-contract

Verify your smart-contract with the following command

```bash
npx hardhat verify --network kovan <<REPLACE_CONTRACT_ADDRESS>>
```

Later during the workshop we will upgrade our smart-contract with the second version
