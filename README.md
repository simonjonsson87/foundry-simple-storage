# Overview
This is a simple storage smart contract written in Solidity using Foundry. 

This is coursework for Patrick Collin's Foundry Fundamentals course.

# A few useful commands

### Setup anvil, a wallet, and publish the contract
Start anvil blockchain
```solidity
anvil
```

Add anvil private key to wallet 
```solidity
cast wallet import anvilAccount1 --interactive
```

Deploy a contract to the anvil chain we just created
```solidity
forge script script/DeploySimpleStorage.s.sol --rpc-url http://127.0.0.1:8545 --broadcast --account anvilAccount1 --sender 0xf39fd6e51aad88f6f4ce6ab8827279cfffb92266
```

### Manually interact with the contract
```solidity
cast send 0x5FbDB2315678afecb367f032d93F642f64180aa3 "store(uint256)" 1337 --rpc-url http://127.0.0.1:8545  --account anvilAccount1 
```

```solidity
cast call 0x5FbDB2315678afecb367f032d93F642f64180aa3 "retrieve()"
```

```solidity
cast --to-base 0x0000000000000000000000000000000000000000000000000000000000000539 dec
```