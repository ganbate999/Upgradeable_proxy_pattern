# DeFi Utils - Token average price
Calculate on-chain average price of tokens on DeFi protocol.

## About
* A keeper pushes a price of token(s).
* Task: Find out the avg price of a token for a given time interval range, without iterating in `loop` (for, while).

## Installation
```console
$ yarn install
```

## Usage

### Build
```console
$ yarn hardhat compile
```

### Typechain
```console
$ yarn hardhat typechain
```

### Test
```console
$ yarn hardhat test
```

### Deploying contracts to localhost Hardhat EVM
#### localhost-1
```console
// on terminal-1
$ yarn hardhat node

// on terminal-2
$ yarn hardhat deploy:defiavgpriceV1 --network localhost1

$ yarn hardhat deploy:defiavgpriceV2 --network localhost1 --proxy <Proxy Address>

$ yarn hardhat deploy:defiavgpriceV3 --network localhost1 --proxy <Proxy Address>
```


### Deploying contracts to Testnet (Public)
#### ETH Testnet - Rinkeby
* Environment variables
	- Create a `.env` file with its values:
```
INFURA_API_KEY=[YOUR_INFURA_API_KEY_HERE]
DEPLOYER_PRIVATE_KEY=[YOUR_DEPLOYER_PRIVATE_KEY_without_0x]
REPORT_GAS=<true_or_false>
```

* Deploy the contracts
```console
$ yarn hardhat deploy:defiavgpriceV1 --network rinkeby

$ yarn hardhat deploy:defiavgpriceV2 --network rinkeby --proxy <Proxy Address> 

$ yarn hardhat deploy:defiavgpriceV3 --network rinkeby --proxy <Proxy Address>
```

### Deploying contracts to Mainnet
#### ETH Mainnet
* Environment variables
	- Create a `.env` file with its values:
```
INFURA_API_KEY=[YOUR_INFURA_API_KEY_HERE]
DEPLOYER_PRIVATE_KEY=[YOUR_DEPLOYER_PRIVATE_KEY_without_0x]
REPORT_GAS=<true_or_false>
```

* Deploy the token on one-chain
```console
$ yarn hardhat deploy:defiavgpriceV1 --network mainnet

$ yarn hardhat deploy:defiavgpriceV2 --network mainnet --proxy <Proxy Address>

$ yarn hardhat deploy:defiavgpriceV3 --network mainnet --proxy <Proxy Address>
```