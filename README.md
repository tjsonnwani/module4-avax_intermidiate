## DegenToken Solidity Contract ##
This Solidity contract implements a basic ERC20 token named DegenToken. It also includes additional functionalities for redeeming items, setting item prices, and listing available items.

## OverView ##
The contract extends the ERC20 and Ownable contracts from the OpenZeppelin library.
It defines events, mappings, and functions to manage tokens and items.

## Functions ##
mint: Allows the owner to mint new tokens and distribute them to a specified address.
burn: Allows users to burn their own tokens.
redeemItem: Allows users to redeem an item by providing the item name and paying the corresponding price in tokens.
transferCoin: Allows users to transfer tokens to another address.
setItemPrice: Allows the owner to set or update the price of an item.
getItemPrice: Retrieves the price of a specific item.
getUserItem: Retrieves the item owned by a specific user.
listAvailableItems: Lists all available items along with their prices.

## Usage ##
Deploy the contract on an Ethereum-compatible blockchain.
Use a wallet or script to interact with the contract's functions.

## Example ##
```javascript
// Deploy the contract
const DegenToken = artifacts.require('DegenToken');
module.exports = function (deployer) {
  deployer.deploy(DegenToken);
};

// Interact with the contract
const contract = new web3.eth.Contract(DegenToken.abi, 'CONTRACT_ADDRESS');
contract.methods.mint('RECEIVER_ADDRESS', 'AMOUNT').send({ from: 'OWNER_ADDRESS' })
```
## Author ##
tanuj


