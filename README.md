# Metacrafters
##CREATING A TOKEN

This Solidity program demonstrates fundamental syntax and functionality in the process of creating a token. It serves as an initial reference for individuals new to Solidity, aiding in their comprehension of its operations. The objective of this program is to generate tokens and foster acquaintance with the Solidity programming language.

#Understanding

This Solidity program is the main contract written for smart contracts on the Ethereum blockchain. It contains variables such as public and mapping as well as minting and burning functions. This program provides an excellent introduction to Solidity programming and provides a simple understanding of the syntax. It serves as a springboard for beginners and provides them with a foundation for tackling more complex projects in the future.

#Getting Started

To execute the Program Use Remix, an online Integrated Development Environment (IDE) for Solidity, kindly proceed to the official Remix website at https://remix.ethereum.org/. Utilize this platform to initiate the program's execution.

Upon accessing the Remix website, kindly initiate the creation of a new file by selecting the "+" icon located on the left-hand sidebar. It is recommended to save the file with a .sol extension, for instance, MyToken.sol. Subsequently, kindly proceed to copy and paste the code provided below into the newly created file.

//SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {

// public variables here
string public tokenname = "LOKI";
string public tokenabbrv = "LOK";
uint public totalsupply = 0;

// mapping variable here
mapping(address => uint) public balances;

// mint function
function mint (address _address, uint _value) public {
    totalsupply += _value;
    balances[_address] += _value;
}

// burn function
function burn (address _address, uint _value) public {
    if (balances[_address] >= _value) {
    totalsupply -= _value;
    balances[_address] -= _value;
    }
}
}

To compile the code, kindly navigate to the "Solidity Compiler" tab located on the left-hand sidebar. Ensure that the "Compiler" option is appropriately configured to "0.8.4" or any other compatible version, and subsequently click on the "Compile MyToken.sol" button.

After compiling the code, the contract can be deployed by accessing the "Deploy & Run Transactions" tab located in the left-hand sidebar. From the dropdown menu, choose the "MyToken" contract and proceed by clicking the "Deploy" button.

Upon deployment of the contract, one may engage with it by invoking the mint and burn functions. To do so, navigate to the "MyToken" contract located in the left-hand sidebar, and select the tokenname, tokenabbrv, and totelsupply options. Subsequently, select the "mint" function and execute it by clicking on the "transact" button to generate coins. Similarly, to remove coins, select the "burn" function.

#License

This project is licensed under SPDX-License-Identifier: MIT
