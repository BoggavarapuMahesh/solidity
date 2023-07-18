## MyToken
This contract defines a simple token with the following features:

A name and symbol
A total supply of tokens
A mapping of token balances to addresses

# Functions to mint new tokens, burn existing tokens, and transfer tokens between addresses

The constructor initializes the token with an initial supply.
The mint function allows new tokens to be minted, increasing the total supply.
The burn function allows existing tokens to be burned, decreasing the total supply.
The transfer function allows tokens to be transferred between addresses.

The maximum supply of tokens is 1000000. The burn function now checks if the total supply will be below 0 after the burn. The transfer function now checks if the sender and recipient addresses are valid.

# Functions
mint(address _recipient, uint256 _amount) - Mints new tokens and increases the total supply.
burn(address _holder, uint256 _amount) - Burns tokens and decreases the total supply.
transfer(address _from, address _to, uint256 _amount) - Transfers tokens from one address to another.

# Events
Transfer(address indexed from, address indexed to, uint256 value) - Emitted when tokens are transferred.
Mint(address indexed to, uint256 value) - Emitted when tokens are minted.
Burn(address indexed from, uint256 value) - Emitted when tokens are burned.

# Usage
To use the contract, you can create a new instance of the contract and then call the functions on the contract. For example, to mint 100 new tokens and assign them to an address, you would call the mint function like this:

contract MyToken myToken = new MyToken("MyToken", "MTK", 1000000);
myToken.mint(0x1234567890abcdef, 100);

Additionally, there is a `balances` mapping that associates addresses with their respective token balances. The `balances` mapping allows for the retrieval of the balance of any address.
