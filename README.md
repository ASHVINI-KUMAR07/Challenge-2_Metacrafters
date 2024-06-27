Create a Token

Token Name and Symbol: Firstly, I have creates a token named "Metacrafters Challenge" with the symbol "M C".
Total Supply Management: Keeps track of the total supply of the tokens.
Balance Mapping: Maintains the balance of tokens for each address.
Minting Tokens: Allows new tokens to be created and added to a specified address, increasing the total supply.
Burning Tokens: Allows tokens to be destroyed from a specified address, decreasing the total supply. Includes a check to ensure the address has sufficient balance before burning.

// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

/*
       REQUIREMENTS
    1. Your contract will have public variables that store the details about your coin (Token Name, Token Abbrv., Total Supply)
    2. Your contract will have a mapping of addresses to balances (address => uint)
    3. You will have a mint function that takes two parameters: an address and a value. 
       The function then increases the total supply by that number and increases the balance 
       of the “sender” address by that amount
    4. Your contract will have a burn function, which works the opposite of the mint function, as it will destroy tokens. 
       It will take an address and value just like the mint functions. It will then deduct the value from the total supply 
       and from the balance of the “sender”.
    5. Lastly, your burn function should have conditionals to make sure the balance of "sender" is greater than or equal 
       to the amount that is supposed to be burned.
*/

The MyToken **smart contract** is a simple implementation of a token on the Ethereum blockchain.
This contract which i have written in Solidity, allows for the creation and destruction of tokens i.e it tells how exactly the tokens are created as well as destroyed,
maintaining an accurate record of the total supply and individual balances

contract MyToken {

    // public variables here

    // mapping variable here

    // mint function

    // burn function

}

# Eth Assessment

// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {
    // Public variables here
    string public tokenname= "Metacrafters Challenge";
    string public symbol= " M C";
    uint256 public totalSupply=0;

    // Mapping variables here
    mapping(address => uint256) public balances;

    // Mint function 
    function mint(address _address, uint256 _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

    // Burn function 
    function burn(address _address, uint256 _value) public {
        if(balances[_address]>=_value)
        {
        totalSupply -= _value;
        balances[_address] -= _value;
        }
        else {
            revert("The balance is insufficient to burn");
        }
}
}




//ASHVINI KUMAR
## Help

Any advise for common problems or issues.
```
command to run if program contains helper info
```

## Authors

Contributors names and contact info

GITHUB Link : https://github.com/ASHVINI-KUMAR07/Challenge-2_Metacrafters/edit/main/README.md

Loom Video link :
https://www.loom.com/share/4c5d8082cad440618213464af977f1f3?sid=1dcd3b13-6a51-4ad3-a4e6-a42346728198

## License

This project is licensed under the // SPDX-License-Identifier: MIT License - see the LICENSE.md file for details





