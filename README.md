# Calculator Smart Contract

This project is a simple Calculator smart contract that I created. It performs basic arithmetic operations such as addition, subtraction, and multiplication. It allows you to retrieve the result.

## Features

- Add numbers
- Subtract numbers
- Multiply numbers
- Retrieve the result

## Getting Started

### Prerequisites

To deploy and interact with this smart contract, I used [Remix IDE](https://remix.ethereum.org/), a powerful web-based tool for developing and deploying smart contracts.

### Creating the Contract

1. **Open Remix IDE**  
   I started by going to [Remix IDE](https://remix.ethereum.org/).

2. **Create a New File**  
   In the Remix file explorer, I clicked on the `+` button to create a new file. I named it `Calculator.sol`.

3. **Add the Contract Code**  
   I wrote the following code into `Calculator.sol`:

    ```solidity
    // SPDX-License-Identifier: MIT

    pragma solidity ^0.8.25;

    contract Calculator {
    
      uint256 result = 0;

      function add(uint256 num) public {
        result += num;
      }

      function sub(uint256 num) public {
        result -= num;
      }

      function multiply(uint256 num) public {
        result *= num;
      }

      function get() public view returns (uint256) {
        return result;
      }
    }


### Compiling the Contract

1. **Compile the Contract**  
   In Remix, I navigated to the `Solidity Compiler` tab on the left sidebar. I made sure that the compiler version is set to `^0.8.25` (matching the version in the contract). I then clicked `Compile Calculator.sol`.

### Deploying the Contract

1. **Deploy the Contract**  
   I went to the `Deploy & Run Transactions` tab on the left sidebar. I selected `Remix VM (Cancun)` as the environment. Then, I clicked the `Deploy` button.

2. **Interact with the Contract**  
   Once deployed, the contract appears under `Deployed Contracts` at the bottom of the `Deploy & Run Transactions` tab. I expanded the contract to see the available functions.

### Using the Contract

1. **Add**
    - I inputted a value in the `add` field and clicked the `add` button to add the value to the result.
    ```solidity
    function add(int256 a) public
    ```

2. **Subtract**
    - I inputted a value in the `sub` field and clicked the `sub` button to subtract the value from the result.
    ```solidity
    function sub(int256 a) public
    ```

3. **Multiply**
    - I inputted a value in the `multiply` field and clicked the `multiply` button to multiply the result by the value.
    ```solidity
    function multiply(int256 a) public
    ```

4. **Get Result**
    - I clicked the `get` button to retrieve the current result.
    ```solidity
    function get() public view returns (int256)
    ```
    
## Deployed to Blockchain

I deployed the Calculator smart contract to the Sepolia test network. Here’s how I did it:

1. **Get Free ETH**: I used the Sepolia faucet to obtain free ETH for the deployment. The faucet provides the necessary test ETH to cover gas fees.

2. **Deploy using MetaMask**: I connected my MetaMask wallet to Remix IDE. After ensuring I had enough test ETH, I selected the "Injected Provider - MetaMask" environment in the `Deploy & Run Transactions` tab of Remix IDE, which connects to my MetaMask wallet. Then, I deployed the contract to the Sepolia test network. Please see below Etherscan screenshot. 

![Screenshot Placeholder](https://via.placeholder.com/800x400.png)


## License

This project is licensed under the MIT License.
