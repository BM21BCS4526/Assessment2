# Assessment2
 **Create a Token**
 This Solidity program is for creating our own token that demonstrates the use of mapping and conditional statements of the Solidity programming language. 
 The purpose of this program is to make it more understandable of creating contracts and map addresses using solidity.

 
**Description**
This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain.
The function then increases the total supply by that number and increases the balance of the “sender” address by that amount .
A burn function, works the opposite of the mint function, as it will destroy tokens.



**Getting Started**
**Executing program**
* To run this program, I'am using Remix, an online Solidity IDE.
* create a new file by clicking on the "+" icon in the left-hand sidebar.  Save the file with a .sol extension (e.g., HelloWorld.sol).
* Copy and paste the following code into the file:
  // SPDX-License-Identifier: MIT
pragma solidity 0.8.18;
contract MyToken {
    string public tokenName = " meta";
    string public tokenAbbrev = " MTA";
    uint public totalSupply=0;

    mapping(address =>uint) public balances;

    function mint (address _address, uint _value) public {
            totalSupply +=_value;
            balances[_address]+=_value;


    }
     function burn (address _address, uint _value) public {
            if(balances[_address]>=_value)
        {   totalSupply -=_value;
            balances[_address]-=_value;

     }
    }

} 
* To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible
version), and then click on the "Compile Mytoken.sol" button.Once the code is compiled,  deploy the contract by clicking on the "Deploy & Run Transactions" tab 
in the left-hand sidebar.
* Select the "MYtoken.sol" contract from the dropdown menu, and then click on the "Deploy" button.
* once the contract is deployed, you can interact with it by calling the mint and burn  functions.
* Click on the "MyToken" contract in the left-hand sidebar, and then click on the "mint" and "burn" function .
* Finally, click on the "transact" button to execute the function and retrieve the value.

**Authors**
Baby Monal
