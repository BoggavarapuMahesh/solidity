## MyToken

The `MyToken` contract represents a basic implementation of an ERC20 token on the Ethereum blockchain. It allows for token minting and burning, and keeps track of token balances for different addresses.

### Functionality

1. **Constructor**: The constructor function is executed only once during the contract deployment. It takes three parameters: `_name`, `_symbol`, and `_totalSupply`. These parameters are used to set the token's name, symbol, and total supply. The balance of the contract creator (the address that deployed the contract) is set to the total supply.

2. **Minting**: The `mint` function is used to create new tokens and increase the total supply. It takes two parameters: `_to` (the address to receive the newly minted tokens) and `_value` (the amount of tokens to mint). The function increases the total supply by the specified amount and assigns the tokens to the recipient's address.

3. **Burning**: The `burn` function is used to destroy tokens and decrease the total supply. It takes two parameters: `_from` (the address from which to burn tokens) and `_value` (the amount of tokens to burn). The function checks if the balance of the `_from` address is sufficient to burn the requested amount. If the balance is sufficient, it decreases the total supply and updates the `_from` address's balance accordingly.

The contract also includes public variables:

- `name`: A string variable that represents the name of the token.
- `symbol`: A string variable that represents the symbol or abbreviation of the token.
- `totalSupply`: An unsigned integer variable that holds the total supply of the token.

Additionally, there is a `balances` mapping that associates addresses with their respective token balances. The `balances` mapping allows for the retrieval of the balance of any address.

The contract is designed to be deployed on the Ethereum blockchain and interacted with using function calls. It provides basic token functionality, enabling the minting and burning of tokens while maintaining balances and the total token supply.
