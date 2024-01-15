# Requirements
git
  You'll know you did it right if you can run  `git --version` and you see a response like `git version x.x.x`
Nodejs
  You'll know you've installed nodejs right if you can run:
`node --version` and get an ouput like: `vx.x.x`
Yarn instead of `npm`
  You'll know you've installed yarn right if you can run:
  `yarn --version` and get an output like: `x.x.x`
  You might need to install it with npm


The provided `deploy.js` script facilitates the deployment of a Solidity smart contract, `SimpleStorage.sol`, to the Ethereum blockchain. It uses the ethers.js library to interact with the Ethereum network, and the deployment involves compiling and deploying the contract using the contract's ABI (Application Binary Interface) and bytecode.

The `SimpleStorage.sol` contract is a basic example that includes functionality for storing and retrieving a favorite number, as well as adding people with associated favorite numbers to a list. It utilizes state variables, a struct, and a mapping in Solidity.

To deploy the contract, the script reads the ABI and bytecode from the compiled contract artifacts, deploys the contract to the Ethereum network using the provided RPC URL and private key, and then performs some basic operations like retrieving and updating the stored favorite number.

This deployment script can be a helpful reference for deploying and interacting with Ethereum smart contracts, especially for developers looking to understand the deployment process and how to use ethers.js for contract deployment and interaction.

### Sepolia Testnet

This project utilizes the Sepolia testnet for testing and deploying the Ethereum smart contract. Sepolia is a testnet environment that allows developers to experiment with their contracts without using real Ether. It provides a simulated Ethereum network for testing and debugging purposes, ensuring that the smart contract functions correctly before deployment on the mainnet.

### API KEY
`wzaK3od-fjdHEqbCESXAPogUsNNmPQ-_`

### RPC URL
`https://eth-sepolia.g.alchemy.com/v2/wzaK3od-fjdHEqbCESXAPogUsNNmPQ-_`

### Ganache Local Blockchain
![Screenshot 2024-01-15 193446](https://github.com/shrxyeh/Ether.js-Smart-Contract/assets/77315155/b3dbd0f9-d8b2-45bf-ad1f-9bf3247eb8bc)
![Screenshot 2024-01-15 193541](https://github.com/shrxyeh/Ether.js-Smart-Contract/assets/77315155/f5b7034a-d5c5-4efd-98b4-44b1e69c01f8)

This project leverages Ganache, a local blockchain for Ethereum development, to facilitate the testing and development of the Ethereum smart contract. Ganache provides a simple and convenient way to run a local Ethereum blockchain, allowing developers to deploy and interact with smart contracts in a controlled and local environment. It's particularly useful for testing contract functionality, debugging, and ensuring the correctness of smart contract logic before deploying to a public testnet

## Usage

1.Run your ganache local chain, by hitting quickstart on your ganache application.

Copy the `RPC SERVER` sting in your ganache CLI, and place it into your `.env` file similar to what's in .env.example.

`.env` Example:

`RPC_URL=http://127.0.0.1:8545`

3.Hit the key on one of the accounts, and copy the key you see and place it into your .env file, similar to what you see in .env.example.

`.env` Example:

PRIVATE_KEY=8a2de4fbe03484c93d6edbd52d145a7592954986f7c65e85d4b73c4e8a224a55

4.Compile your code
  -Run
  -`yarn compile`

You'll see files `SimpleStorage_sol_SimpleStorage.abi` and `SimpleStorage_sol_SimpleStorage.bin` be created.

5.Run your application
  -`node deploy.js`

For WSL users
1.Run
  -`yarn add ganache`
2.Change Server settings in Ganache
  -Settings > Server > Host Name

3.Change Host Name to vEthernet (WSL)

  -Run your application
  -`node deploy.js`
