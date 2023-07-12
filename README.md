# TOKEN Creation

This project is a simple token contract implementing the following:
* Minting new tokens
* Burning tokens
* Transferring tokens between accounts

## Description

The project is a simple token contract that can be used to create, burn, and transfer tokens. The contract is implemented in Solidity and can be compiled and deployed using a web3 development environment. The token contract can be used for a variety of purposes, such as creating a new cryptocurrency, implementing a loyalty program, or creating a crowdfunding platform.
Some of the key features of the token contract are:
* The contract allows the owner to mint new tokens.
* The contract allows the owner to burn tokens.
* The contract allows users to transfer tokens to each other.
The token contract is a valuable tool for anyone who wants to create or use decentralized applications. It is easy to use and provides a variety of features that can be used to implement a variety of applications.

## Getting Started

### Installing

* To run this program, you can use Remix, a web-based Solidity IDE. To get started, head to the Remix website at https://remix.ethereum.org/. Once you're on the Remix website, create a new file by clicking the "+" icon in the left-hand sidebar. Save the file with a .sol extension, such as MyToken.sol.

### Executing program

* The contract has three public variables: tName, tAbrv, and totSupply.
* The contract also has a mapping variable called balances.
* The contract has two functions: mint() and burn().
* The mint() function mints new tokens and the burn() function burns tokens.

```
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;
contract MyToken
{   string public tName = "Panchatattva";
    string public tAbrv = "PCT";
    uint public totSupply = 0;
    mapping(address => uint) public balances;

    function mint(address account, uint value) public
    {
      totSupply += value;
      balances[account] += value;
    }

    function burn(address account, uint value) public
    {
      if (balances[account] >= value)
      {  totSupply -= value;
          balances[account] -= value;  }
    }
}
```


## Authors
Mrudhula Dubasi
#Chandigarh University

## License

This project is licensed under the MIT License - see the LICENSE.md file for details
