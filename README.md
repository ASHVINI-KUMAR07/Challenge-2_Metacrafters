The MyToken **smart contract** is a simple implementation of a token on the Ethereum blockchain.
This contract which i have written in Solidity, allows for the creation and destruction of tokens i.e it tells how exactly the tokens are created as well as destroyed,
maintaining an accurate record of the total supply and individual balances.

The main key Features:
Token Name and Symbol: Firstly, I have creates a token named "Metacrafters Challenge" with the symbol "M C".
Total Supply Management: Keeps track of the total supply of the tokens.
Balance Mapping: Maintains the balance of tokens for each address.
Minting Tokens: Allows new tokens to be created and added to a specified address, increasing the total supply.
Burning Tokens: Allows tokens to be destroyed from a specified address, decreasing the total supply. Includes a check to ensure the address has sufficient balance before burning.


**I have implemented it as follows:**

**i) Created Public variables here**
    string public tokenname= "Metacrafters Challenge";
    string public symbol= " M C";
    uint256 public totalSupply=0;

**ii) Mapping variables are created  here**
    mapping(address => uint256) public balances;

**iii) Mint function is used for authentication purpose**
    function mint(address _address, uint256 _value) public {
        totalSupply += _value;
        balances[_address] += _value;
    }

iv) This is used to destroy the token 
    function burn(address _address, uint256 _value) public {
        if(balances[_address]>=_value)
        {
        totalSupply -= _value;

THANK YOU!!

