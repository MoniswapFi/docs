The protocol smart contracts are relevant to Liquidity & Governance

## Router 

### Contract Addresses:

*Bsc Testnet - [0xc6b776fAD24f4ac2120ff35c88f3a0B83b9f5b29](https://testnet.bscscan.com/address/0xc6b776fAD24f4ac2120ff35c88f3a0B83b9f5b29)*


### Functions:

*`addLiquidityETH(address token, bool stable, uint256 amountTokenDesired, uint256 amountTokenMin, uint256 amountETHMin, address to, uint256 deadline) payable`*

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


*`addLiquidity(address tokenA, address tokenB, bool stable, uint256 amountADesired, uint256 amountBDesired, uint256 amountAMin, uint256 amountBMin, address to, uint256 deadline)`*

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