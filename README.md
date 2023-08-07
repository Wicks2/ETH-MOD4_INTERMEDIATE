# Degen Gaming ERC20 Token

This is a smart contract for an ERC20 token named "Degen" (symbol: DGN), designed for Degen Gaming. The token contract includes functionalities for minting, transferring, redeeming, checking balances, and burning tokens.

## Functionality

1. **Minting New Tokens**
    - The owner of the contract can mint new tokens using the `mint` function.
    - The `_mint` function from the ERC20 standard is used to create new tokens and distribute them to specific addresses.
    - Only the owner can call this function to create new tokens.

2. **Transferring Tokens**
    - Players can transfer their tokens to other addresses using the `transferTokens` function.
    - The `_transfer` function from the ERC20 standard is used to facilitate the transfer of tokens between two addresses.

3. **Redeeming Tokens**
    - Players can redeem their tokens for in-game items from the store using the `redeemTokens` function.
    - Players can choose an item (1 to 5) from the store and send a payment along with the function call.
    - The function checks the user's balance and deducts the appropriate amount of tokens, transferring them to the contract owner's address.
    - The name of the redeemed item is concatenated to the `MyTokens` variable for tracking purposes.

4. **Checking Token Balance**
    - Players can check their token balance using any Ethereum wallet or blockchain explorer.
    - The ERC20 standard provides a `balanceOf` function for this purpose.

5. **Burning Tokens**
    - Anyone can burn their tokens using the `burnTokens` function.
    - The `_burn` function from the ERC20 standard is used to destroy tokens from the caller's address.

6. **In-Game Store**
    - The `store` function provides a string representation of the items available in the in-game store along with their prices in tokens.

## Usage

1. Deploy the Contract:
    - Deploy the `DegenToken` contract on the Avalanche network.

2. Minting Tokens:
    - Only the owner can mint new tokens using the `mint` function.
    - Provide the recipient's address and the amount of tokens to mint.

3. Transferring Tokens:
    - Players can transfer tokens to others using the `transferTokens` function.
    - Provide the recipient's address and the amount of tokens to transfer.

4. Redeeming Tokens:
    - Players can redeem tokens for in-game items using the `redeemTokens` function.
    - Provide the chosen item (1 to 5) as an argument and send the appropriate amount of Ether along with the function call.

5. Burning Tokens:
    - Anyone can burn their tokens using the `burnTokens` function.
    - Provide the amount of tokens to burn.

6. Checking Balances:
    - Use any Ethereum wallet or blockchain explorer to check token balances associated with different addresses.

## Disclaimer

- This smart contract is provided for educational purposes only and might need further security audits and improvements before real-world deployment.
- Be cautious while interacting with smart contracts, especially on live networks, as mistakes might result in the loss of funds.
- Consult the documentation of the OpenZeppelin library for more details on ERC20 token implementation: [OpenZeppelin ERC20](https://docs.openzeppelin.com/contracts/4.x/erc20).
