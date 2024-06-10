#Assesment-2-solidity-metacrafter

REQUIREMENTS / objective 

/*

    1. Your contract will have public variables that store the details about your coin (Token Name, Token Abbrv., Total Supply)
    2. Your contract will have a mapping of addresses to balances (address => uint)
    3. You will have a mint function that takes two parameters: an address and a value. 
       The function then increases the total supply by that number and increases the balance 
       of the address by that amount.
    4. Your contract will have a burn function, which works the opposite of the mint function, as it will destroy tokens. 
       It will take an address and value just like the mint functions. It will then deduct the value from the total supply 
       and from the balance of the address.
    5. Lastly, your burn function should have conditionals to make sure the balance of the account is greater than or equal 
       to the amount that is supposed to be burned.
*/

with keeping the objectives in th mind will start writing code for it .

// SPDX-License-Identifier: MIT

     pragma solidity 0.8.18;
    contract MyToken {

// Public variables here

    string public name;
    string public symbol;
    
//(Token Abbrv same thing )
   
    uint public totalSupply;
// Mapping variable 
    
    mapping(address => uint) public balances;

 // Event to log minting 
 
    event Mint(address indexed to, uint value);
    
// Event to log burning 

    event Burn(address indexed from, uint value);

// Constructor to initialize the token details

    constructor(string memory _name, string memory _symbol) {
        name = _name;
        symbol = _symbol;
        totalSupply = 0; 
// Initial total supply is 0

    }

// Mint function

    function mint(address _to, uint _value) public {
        totalSupply += _value;
        balances[_to] += _value;
        emit Mint(_to, _value); // Emit mint event
    }

 // Burn function
 
    function burn(address _from, uint _value) public {
        require(balances[_from] >= _value, "Insufficient balance to burn");
        totalSupply -= _value;
        balances[_from] -= _value;
        emit Burn(_from, _value); 
 // Emit burn event
 
    }

 // Function to check the balance of a specific address
 
    function balanceOf(address _account) public view returns (uint) {
        return balances[_account];
    }

 // Function to get the total supply
 
    function getTotalSupply() public view returns (uint) {
        return totalSupply;
    }
}
