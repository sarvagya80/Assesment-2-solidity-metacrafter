# Project Title
Getting Started with Solidity Create a Token
## Description

We will create a contract together to fulfill the following requirements:

Your contract will have public variables that store the details about your coin (Token Name, Token Abbrv., Total Supply)
Your contract will have a mapping of addresses to balances (address => uint)
You will have a mint function that takes two parameters: an address and a value. The function then increases the total supply by that number and increases the balance of the address by that amount.
Your contract will have a burn function, which works the opposite of the mint function, as it will destroy tokens. It will take an address and value just like the mint functions. It will then deduct the value from the total supply and from the balance of the address.
Lastly, your burn function should have conditionals to make sure the balance of account is greater than or equal to the amount that is supposed to be burned.

## Getting Started

### Installing

In this evaluation, we will  use Remix IDE. Remix IDE is an online tool that makes creating, assembling, implementing, and testing Ethereum blockchain smart contracts easier.

use remix ide of version 0.8.18 to run code properly

### Executing program

**Deploy the Contract**

Open Remix IDE in your web browser.

Create a new Solidity file and name it Token.sol.

Copy and paste the sample contract code into the file.

Compile the contract using the appropriate Solidity compiler version.

Deploy the contract on a local or test Ethereum network.

**Minting Tokens**

After deploying, go to the "Deploy & Run Transactions" tab in Remix.

Select the mint function, enter the desired address and value, and click "Transact" to mint new tokens.

**Burning Tokens**

Select the burn function, enter the desired address and value, and click "Transact" to burn tokens.

Ensure the address has enough balance before attempting to burn tokens to avoid errors.

## Help

use remix ide of version 0.8.18 to run code properly

## Authors

Contributors names and contact info

Sarvagya pathak 

 adittyapathak8081@gmail.com


## License

This project is licensed under the Sarvagya pathak  
