# MyToken Contract

The "MyToken" contract is a custom token contract written in Solidity for the Ethereum blockchain. This contract allows you to create, destroy, and track token balances for different addresses.

## Functionality

The contract provides the following functionality:

1. **Token Information**: The contract stores the name and abbreviation of the token, accessible through the public variables `tokenName` and `tokenAbbrv`.

2. **Total Supply**: The contract tracks the total number of tokens in circulation using the public variable `totalSupply`.

3. **Balance Tracking**: The contract utilizes a mapping variable `balances` to associate addresses with their corresponding token balances. This mapping is publicly accessible, allowing external parties to view token balances associated with specific addresses.

4. **Minting**: The `mint` function allows you to create new tokens and assign them to a specified address. It takes two parameters: `_address` representing the recipient's address and `_value` representing the number of tokens to mint. The total supply is increased by the minted amount, and the recipient's token balance is updated accordingly.

5. **Burning**: The `burn` function enables the destruction of tokens by a specified address. It takes the same parameters as the `mint` function: `_address` and `_value`. Before reducing the total supply and updating the balance, the function verifies if the `_address` has sufficient tokens to burn. If the condition is met, the total supply is decreased by the specified amount, and the `_address` balance is reduced accordingly.

## Usage

To use the "MyToken" contract, follow these steps:

1. Deploy the contract to the Ethereum blockchain using a compatible development environment or platform.

2. Once deployed, you can interact with the contract using a web interface, command-line tools, or programmatically through other smart contracts.

3. Access the contract's public variables to retrieve information about the token, such as the name, abbreviation, and total supply.

4. Call the `mint` function to create new tokens and assign them to a specific address. Provide the recipient's address and the desired token amount as function arguments.

5. Use the `burn` function to destroy tokens held by a specified address. Pass the address and the amount of tokens to be burned as function arguments.

6. Monitor and track token balances by accessing the `balances` mapping variable. This allows you to view the token balances associated with different addresses.


## License

This contract is provided under the [MIT License](https://opensource.org/licenses/MIT).

