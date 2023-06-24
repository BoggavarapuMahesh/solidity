// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {
    // Public variables to store token details
    string public tokenName;
    string public tokenAbbrv;
    uint public tokenSupply;
    mapping(address => uint) public balances;

    constructor() {
        // Initialize token details
        tokenName = "Ember";
        tokenAbbrv = "EMB";
        tokenSupply = 1000000;
    }

    function mint(address _address, uint _value) public {
        // Increase the balance of the specified address
        balances[_address] += _value;
        // Increase the token supply
        tokenSupply += _value;
    }

    function burn(address _address, uint _value) public returns (string memory) {
        // Check if the address has sufficient balance to burn
        require(balances[_address] >= _value, "Insufficient balance to burn");

        // Deduct the specified value from the balance
        balances[_address] -= _value;
        // Deduct the specified value from the token supply
        tokenSupply -= _value;

        // Return success message
        return "Tokens burned successfully";
    }
}
