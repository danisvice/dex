# DEX Smart Contract 🌐

Welcome to the Decentralized Exchange (DEX) Smart Contract documentation! This comprehensive guide will take you through the features and functionalities of our DEX contract, empowering you to understand and utilize it effectively. Let's dive in! 🚀

## Table of Contents

- [Introduction](#introduction)
- [Enums and Structs](#enums-and-structs)
- [State Variables](#state-variables)
- [Events](#events)
- [Constructor](#constructor)
- [Functions](#functions)
- [Modifiers](#modifiers)
- [Usage Examples](#usage-examples)
- [Contributing](#contributing)
- [License](#license)

## Introduction

The DEX Smart Contract enables users to trade ERC20 tokens on a decentralized platform. It's designed to provide a secure, transparent, and efficient way to exchange tokens within the Ethereum ecosystem.

## Enums and Structs

- **Side**: Represents the side of the trade (BUY or SELL).
- **Token**: Defines token information, including ticker and address.
- **Order**: Represents a trading order with various attributes.

## State Variables

- `tokens`: A mapping of token tickers to token information.
- `tokenList`: An array of available token tickers.
- `traderBalances`: Tracks the token balances of traders.
- `orderBook`: Stores the order book data.
- `admin`: Address of the contract administrator.
- `nextOrderId`: Auto-incrementing ID for orders.
- `nextTradeId`: Auto-incrementing ID for trades.
- `DAI`: Ticker for DAI token.

## Events

- `NewTrade`: Fired when a trade is executed.

## Constructor

Initializes the contract and sets the admin address.

## Functions

- `getOrders`: Retrieves orders for a given token and side.
- `getTokens`: Retrieves information about available tokens.
- `addToken`: Allows the admin to add a new token.
- `deposit`: Enables users to deposit tokens into their trading balance.
- `withdraw`: Allows users to withdraw tokens from their balance.
- `createLimitOrder`: Users can create limit orders for trading.
- `createMarketOrder`: Users can create market orders for trading.

## Modifiers

- `tokenIsNotDai`: Prevents trading with DAI token.
- `tokenExist`: Ensures the token exists in the exchange.
- `onlyAdmin`: Restricts specific functions to the admin.

## Usage Examples

- **Creating a Limit Order**:
  ```solidity
  createLimitOrder("ETH", 1, 2500, Side.BUY);
  ```

- **Depositing Tokens**:
  ```solidity
  deposit(100, "ETH");
  ```

- **Withdrawing Tokens**:
  ```solidity
  withdraw(50, "ETH");
  ```

- **Getting Orders**:
  ```solidity
  getOrders("ETH", Side.SELL);
  ```

## Contributing

Contributions are welcome! If you find issues or have enhancements to propose, please open a pull request. Let's make the DEX Smart Contract even better together!

## License

This project is licensed under the [MIT License](LICENSE). Feel free to use and modify the contract according to the terms.

---

Explore our DEX Smart Contract, enhance your trading experience, and enjoy seamless token exchange within the Ethereum network. Happy trading! 📈🌐
