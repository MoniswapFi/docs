The protocol smart contracts are relevant to Liquidity & Governance

## Router

### Contract Addresses:

_Bera Bartio - [0x19042106AABFA3A2cDf46Ea160aA6fa9Db31c261](https://bartio.beratrail.io/address/0x19042106AABFA3A2cDf46Ea160aA6fa9Db31c261)_

### Functions:

_`addLiquidityETH(address token, bool stable, uint256 amountTokenDesired, uint256 amountTokenMin, uint256 amountETHMin, address to, uint256 deadline) payable`_

**Description:** Add to existing or create new liquidity by pairing ETH against `token`.

**Parameters:**

- token - Address of token to pair against `ETH`.
- stable - If this is a stable or volatile pair. If `true`, the pair is a stable pair.
- amountTokenDesired - The amount of liquidity that the caller desires to add for `token`.
- amountTokenMin - The least amount of `token` that should go to liquidity.
- amountETHMin - The least amount of `ETH` that should go to liquidity.
- to - The address to mint the liquidity to.
- deadline - Time (in seconds) after which the transaction would be considered invalid.
- msg.value - Amount of `ETH` to deposit for liquidity.

_`addLiquidity(address tokenA, address tokenB, bool stable, uint256 amountADesired, uint256 amountBDesired, uint256 amountAMin, uint256 amountBMin, address to, uint256 deadline)`_

**Description:** Add to existing or create new liquidity by pairing `tokenA` against `tokenB`.

**Parameters:**

- tokenA - Address of first token.
- tokenB - Address of second token.
- stable - If this is a stable or volatile pair. If `true`, the pair is a stable pair.
- amountADesired - The amount of liquidity that the caller desires to add for `tokenA`.
- amountBDesired - The amount of liquidity that the caller desires to add for `tokenB`.
- amountAMin - The least amount of `tokenA` that should go to liquidity.
- amountBMin - The least amount of `tokenB` that should go to liquidity.
- to - The address to mint the liquidity to.
- deadline - Time (in seconds) after which the transaction would be considered invalid.

_`quoteLiquidity(uint256 amountA, uint256 reserveA, uint256 reserveB) returns (uint256 amountB)`_

**Description:** Given an amount of an asset, a set of reserves, returns the equivalent amount in the other token. Useful in determining how much of the second token should go into liquidity. Note that this accounts for only volatile pools, and may return insufficient liquidity for stable pools.

**Parameters:**

- amountA - Amount of first asset
- reserveA - First asset reserve
- reserveB - Second asset reserve

**Returns:**

- amountB - The amount of the other token to deposit

_`quoteAddLiquidity(address tokenA, address tokenB, bool stable, address factory, uint256 amountADesired, uint256 amountBDesired) returns (uint256 amountA, uint256 amountB, uint256 liquidity)`_

**Description:** Given two assets, the respective amounts the caller wishes to deposit, and the pool factory, returns the ideal amounts to be deposited, and the amount of liquidity that would be minted.

**Parameters:**

- tokenA - Address of first token.
- tokenB - Address of second token.
- stable - If this is a stable or volatile pair. If `true`, the pair is a stable pair.
- factory - Pool factory address.
- amountADesired - The amount of liquidity that the caller desires to add for `tokenA`.
- amountBDesired - The amount of liquidity that the caller desires to add for `tokenB`.

**Returns:**

- amountA - Ideal amount of `tokenA` to deposit.
- amountB - Ideal amount of `tokenB` to deposit.
- liquidity - The liquidity that would be minted.

_`removeLiquidity(address tokenA, address tokenB, bool stable, uint256 liquidity, uint256 amountAMin, uint256 amountBMin, address to, uint256 deadline)`_

**Description:** Removes liquidity from an existing pool.

**Parameters:**

- tokenA - Address of first token.
- tokenB - Address of second token.
- stable - If this is a stable or volatile pair. If `true`, the pair is a stable pair.
- liquidity - How much liquidity to remove.
- amountAMin - The least amount of `tokenA` to get back.
- amountBMin - The least amount of `tokenB` to get back.
- to - Address to send tokens to.
- deadline - Time (in seconds) after which the transaction would be considered invalid.

_`removeLiquidityETH(address token, bool stable, uint256 liquidity, uint256 amountTokenMin, uint256 amountETHMin, address to, uint256 deadline)`_

**Description:** Removes liquidity from `ETH`, and `token` pair.

**Parameters:**

- token - Address of token paired against `ETH`.
- stable - If this is a stable or volatile pair. If `true`, the pair is a stable pair.
- liquidity - The amount of liquidity that the caller desires to remove for `token`, and `ETH` pair.
- amountTokenMin - The least amount of `token` that should be sent back to caller.
- amountETHMin - The least amount of `ETH` that should be sent back to caller.
- to - The address to send tokens to.
- deadline - Time (in seconds) after which the transaction would be considered invalid.

_`removeLiquidityETHSupportingFeeOnTransferTokens(address token, bool stable, uint256 liquidity, uint256 amountTokenMin, uint256 amountETHMin, address to, uint256 deadline)`_

**Description:** Removes liquidity from `ETH`, and `token` pair. Covers tokens with transfer fees.

**Parameters:**

- token - Address of token paired against `ETH`.
- stable - If this is a stable or volatile pair. If `true`, the pair is a stable pair.
- liquidity - The amount of liquidity that the caller desires to remove for `token`, and `ETH` pair.
- amountTokenMin - The least amount of `token` that should be sent back to caller.
- amountETHMin - The least amount of `ETH` that should be sent back to caller.
- to - The address to send tokens to.
- deadline - Time (in seconds) after which the transaction would be considered invalid.

_`quoteRemoveLiquidity(address tokenA, address tokenB, bool stable, address factory, uint256 liquidity) returns (uint256 amountA, uint256 amountB)`_

**Description:** Given two tokens, `tokenA`, & `tokenB`, a pool factory, and a liquidity amount, returns the amounts of tokens sent back to the caller.

**Parameters:**

- tokenA - Address of first token.
- tokenB - Address of second token.
- stable - If this is a stable or volatile pair. If `true`, the pair is a stable pair.
- factory - Pool factory address.
- liquidity - Amount of liquidity you intend to remove.

**Returns:**

- amountA - Amount of `tokenA` that would be removed from the pool.
- amountB - Amount of `tokenB` that would be removed from the pool.

## AggregatorRouter

### Contract Addresses:

_Bera Bartio - [0xbcC7Eee299c89CBD285A996d461499c7a9af753A](https://bartio.beratrail.io/address/0xbcC7Eee299c89CBD285A996d461499c7a9af753A)_

### Functions:

_`swap(Trade calldata trade, address to, uint256 fee) payable`_

**Description:** Performs a swap given a trade configuration, an address, and a fee.

**Parameters:**

- trade - The trade configuration. See structure [here](https://github.com/MoniswapFi/contracts/blob/master/contracts/exchange-aggregator/interfaces/IAggregatorRouter.sol)
- to - Address of the trade recipient.
- fee - Fee to charge for the transaction. Must be greater than 0. At least 1% of the traded token is recommended.
- msg.value - `ETH` amount if this is an `ETH` trade.

_`findBestPath(uint256 _amountIn, address _tokenIn, address _tokenOut, uint256 _maxSteps) returns (FormattedOffer memory offer)`_

**Description:** Finds the best trade path between two tokens.

**Parameters:**

- \_amountIn - The amount to swap from.
- \_tokenIn - The token to swap from.
- \_tokenOut - The token to swap to.
- \_maxSteps - The maximum steps (or pathways) to take from `_tokenIn` to `_tokenOut`. Must be greater than 0, and less than 5.

**Returns:**

- offer - The `FormattedOffer` configuration useful for composing the trade object. Structure can be found [here](https://github.com/MoniswapFi/contracts/blob/master/contracts/exchange-aggregator/interfaces/IAggregatorRouter.sol)

_`query(address tokenIn, address tokenOut, uint256 amountIn) returns (Query memory _bestQuery)`_

**Description:** Returns the best query, useful in predicting the outcomes of a swap.

**Parameters:**

- tokenIn - Address of the first token.
- tokenOut - Address of the second token.
- amountIn - Amount of `tokenIn` to send.

**Returns:**

- \_bestQuery - A `Query` item useful for predicting the potential outcomes of a swap. Structure can be found [here](https://github.com/MoniswapFi/contracts/blob/master/contracts/exchange-aggregator/interfaces/IAggregatorRouter.sol)
