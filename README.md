# ERC-721 NFT Tutorial - Solidity

## 1. OpenZeppelin - Contracts Wizard

https://docs.openzeppelin.com/contracts/4.x/wizard

- Select ERC721

- Change Name and Symbol
- Edit Base URI - for your tokens
- Features
  - Mintable + Auto Increment Ids
  - Pauseable
  - Enumerable

### Click on 'Open in Remix'

## 2. Remix - Ethereum IDE

https://remix.ethereum.org/

- Divide the code up into sections using comments
  - 1. Property Variables
  - 2. Lifecycle Methods
  - 3. Pauseable Functions
  - 4. Minting Functions
  - 5. Other Functions

### Modifications

- Remove `onlyOwner` modifier from `safeMint`
- Add in `MINT_PRICE` in ether. Add corresponding `require` statement in `safeMint()
- Add `MAX_SUPPLY` for total number of tokens. Add corresponding `require` statement in `safeMint()`
- In the constructor, call `_tokenIdCounter.increment()` to start the token at 1
- Add in `withdraw()` function

## 3. Remix - Deploy

- Check compiler version at the type of the Solidity File:
  `pragma solidity ^0.8.4;`

- Select the compiler from the left hand side of the page and select the corresponding compiler version - 0.8.4 or whatever the newest version is out.

- Compile the contract

- Select the `Deploy & Run Transactions` tab.
  Environment: JavaScript VM
  Account: Make note of what account you deploy it on
  Contract: Select `YourContract.sol` from the bottom of the dropdown list.

- View the deployed contract and examine transactions.
