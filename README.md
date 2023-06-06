# Project Title

CrafterToken - A Token created in Solidity

## Description

A simple token smart contract implemented in solidity to meet the following requirements.
1. The contract has public variables that store the details about the coin (Token Name, Token Abbrv., Total Supply)
2. It has a mapping of addresses to balances (address => uint)
3. It has a mint function that takes two parameters: an address and a value. 
   The function then increases the total supply by that number and increases the balance 
   of the “sender” address by that amount
4. It has a burn function, which works the opposite of the mint function, as it will destroy tokens. 
   It will take an address and value just like the mint functions. It will then deduct the value from the total supply 
   and from the balance of the “sender”.
5. Lastly, the burn function has conditionals to make sure the balance of "sender" is greater than or equal 
   to the amount that is supposed to be burned.

## Getting Started

### Installing

* All necessary installations are pre-installed on Remix online IDE
* Copy the raw file "CrafterToken.sol" of this repository 
* Launch the Remix online IDE with the url https://remix.ethereum.org  

### Executing the program

* In Remix, create a new file inside the "contracts" folder on the File explorer displayed on the left
* Paste the raw copy from CrafterToken.sol (as below) in the new file you created.

// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;
contract MyToken {
    // public variables here
    string public tokenName = "CrafterToken";
    string public tokenAbbreviation = "CRT";
    uint public totalSupply = 0;
    // mapping variable here
    mapping(address => uint) public balances;
    // mint function
    function mint(address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }
    // burn function
    function burn(address _address, uint _value) public {
        if (balances[_address] >= _value ) {
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }
}

* Compile the contract by clicking on the "Solidity Compiler" button on the outermost left menu bar (or use the shortcut "Ctrl + S")
* Just below the "Solidity Compiler" button, find and use the "Deploy and Run transactions" button to deploy the smart contract
* On successful deployment, find and click on the "Deployed Contracts" heading to see a drop down of an interface through which the contract can be interacted 
with
* Find the provided test accounts under the "ACCOUNTS" field of the interface on the left
* Copy any of the addresses listed in the format 0x5B3...eddC4 (100 ether) for use as input to the interfaces that require an address when interacting with the contract
* Test interact with the various functions of the smart contract


## Help

Ensure that the smart contract file is names with a ".sol" file extension

## Author(s)

Contributor's name and contact info:

Name: Adeola David Adelakun  
Email: adesdesk@outlook.com


## License

This project is licensed under the MIT License - see the LICENSE.md file for details
