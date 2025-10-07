# Body


## Supported Types

### `components.AaveBorrowParams`

```typescript
const value: components.AaveBorrowParams = {
  token: "WETH",
  amount: 150.5,
  interestRateMode: "variable",
};
```

### `components.AaveRepayParams`

```typescript
const value: components.AaveRepayParams = {
  token: "WETH",
  amount: 150.5,
  interestRateMode: "stable",
};
```

### `components.AaveSupplyParams`

```typescript
const value: components.AaveSupplyParams = {
  token: "WETH",
  amount: 1.5,
};
```

### `components.AaveWithdrawParams`

```typescript
const value: components.AaveWithdrawParams = {
  token: "WETH",
  amount: 1.5,
  recipient: "0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2",
};
```

### `components.AerodromeSlipstreamBuyExactlyParams`

```typescript
const value: components.AerodromeSlipstreamBuyExactlyParams = {
  tokenIn: "WETH",
  tokenOut: "WETH",
  tickSpacing: 100,
  amountOut: 1.5,
  amountInMaximum: 1.6,
};
```

### `components.AerodromeSlipstreamIncreaseLiquidityProvisionParams`

```typescript
const value: components.AerodromeSlipstreamIncreaseLiquidityProvisionParams = {
  tokenId: 800217,
  amount0Desired: "1.5",
  amount1Desired: "1.7",
  amount0Min: "1.4",
  amount1Min: "1.6",
};
```

### `components.AerodromeSlipstreamMintLiquidityProvisionParams`

```typescript
const value: components.AerodromeSlipstreamMintLiquidityProvisionParams = {
  token0: "WETH",
  token1: "USDC",
  tickSpacing: 100,
  tickLower: -1000,
  tickUpper: 1000,
  amount0Desired: "1.5",
  amount1Desired: "1.7",
  amount0Min: "1.4",
  amount1Min: "1.6",
  recipient: "0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B",
};
```

### `components.AerodromeSlipstreamSellExactlyParams`

```typescript
const value: components.AerodromeSlipstreamSellExactlyParams = {
  tokenIn: "WETH",
  tokenOut: "WETH",
  tickSpacing: 100,
  amountIn: 1.5,
  amountOutMinimum: 1.4,
};
```

### `components.AerodromeSlipstreamWithdrawLiquidityProvisionParams`

```typescript
const value: components.AerodromeSlipstreamWithdrawLiquidityProvisionParams = {
  tokenId: 928157,
  percentageForWithdrawal: "25",
};
```

### `components.EthenaDepositParams`

```typescript
const value: components.EthenaDepositParams = {
  amount: 1.5,
};
```

### `components.EthenaRequestToWithdrawParams`

```typescript
const value: components.EthenaRequestToWithdrawParams = {
  amount: 1.5,
};
```

### `components.EthenaUnstakeParams`

```typescript
const value: components.EthenaUnstakeParams = {};
```

### `components.MorphoBorrowParams`

```typescript
const value: components.MorphoBorrowParams = {
  amount: 1.5,
  uniqueMarketKey:
    "0xe7399fdebc318d76dfec7356caafcf8cd4b91287e139a3ec423f09aeeb656fc4",
};
```

### `components.MorphoDepositParams`

```typescript
const value: components.MorphoDepositParams = {
  vaultAddress: "0xbEef047a543E45807105E51A8BBEFCc5950fcfBa",
  amount: 1.5,
};
```

### `components.MorphoRepayParams`

```typescript
const value: components.MorphoRepayParams = {
  amount: 1.5,
  uniqueMarketKey:
    "0xe7399fdebc318d76dfec7356caafcf8cd4b91287e139a3ec423f09aeeb656fc4",
};
```

### `components.MorphoSupplyCollateralParams`

```typescript
const value: components.MorphoSupplyCollateralParams = {
  amount: 1.5,
  uniqueMarketKey:
    "0xe7399fdebc318d76dfec7356caafcf8cd4b91287e139a3ec423f09aeeb656fc4",
};
```

### `components.MorphoWithdrawParams`

```typescript
const value: components.MorphoWithdrawParams = {
  vaultAddress: "0xbEef047a543E45807105E51A8BBEFCc5950fcfBa",
  amount: "1.5",
};
```

### `components.MorphoWithdrawCollateralParams`

```typescript
const value: components.MorphoWithdrawCollateralParams = {
  amount: 1.5,
  uniqueMarketKey:
    "0xe7399fdebc318d76dfec7356caafcf8cd4b91287e139a3ec423f09aeeb656fc4",
};
```

### `components.OdosSwapParams`

```typescript
const value: components.OdosSwapParams = {
  tokenIn: "0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48",
  tokenOut: "0xdac17f958d2ee523a2206206994597c13d831ec7",
  amount: 1.5,
  maxSlippagePercent: 0.5,
};
```

### `components.PendleManageLiquidityParams`

```typescript
const value: components.PendleManageLiquidityParams = {
  marketAddress: "0x08a152834de126d2ef83d612ff36e4523fd0017f",
  action: "SUPPLY",
  token: "USDC",
  amountIn: 1.5,
  maxSlippagePercent: 0.5,
};
```

### `components.PendleRedeemYieldParams`

```typescript
const value: components.PendleRedeemYieldParams = {
  marketAddress: "0x08a152834de126d2ef83d612ff36e4523fd0017f",
};
```

### `components.PendleTradePtParams`

```typescript
const value: components.PendleTradePtParams = {
  marketAddress: "0x08a152834de126d2ef83d612ff36e4523fd0017f",
  action: "BUY",
  token: "USDC",
  amountIn: 1.5,
  maxSlippagePercent: 0.5,
};
```

### `components.PendleTradeYtParams`

```typescript
const value: components.PendleTradeYtParams = {
  marketAddress: "0x08a152834de126d2ef83d612ff36e4523fd0017f",
  action: "BUY",
  token: "USDC",
  amountIn: 1.5,
  maxSlippagePercent: 0.5,
};
```

### `components.SetAllowanceParams`

```typescript
const value: components.SetAllowanceParams = {
  token: "USDC",
  contract: "AaveV3Pool",
  amount: 1.5,
};
```

### `components.SkyBuyParams`

```typescript
const value: components.SkyBuyParams = {
  tokenIn: "DAI",
  amount: 1.5,
};
```

### `components.SkyDepositParams`

```typescript
const value: components.SkyDepositParams = {
  amount: 1.5,
};
```

### `components.SkySellParams`

```typescript
const value: components.SkySellParams = {
  tokenOut: "USDC",
  amount: 1.5,
};
```

### `components.SkyWithdrawParams`

```typescript
const value: components.SkyWithdrawParams = {
  amount: "512.05",
};
```

### `components.TokenTransferParams`

```typescript
const value: components.TokenTransferParams = {
  to: "0x68b3465833fb72A70ecDF485E0e4C7bD8665Fc44",
  token: "USDC",
  amount: 1.5,
};
```

### `components.UniswapIncreaseLiquidityProvisionParams`

```typescript
const value: components.UniswapIncreaseLiquidityProvisionParams = {
  tokenId: 952512,
  amount0Desired: "1.5",
  amount1Desired: "1.7",
  amount0Min: "1.4",
  amount1Min: "1.6",
};
```

### `components.UniswapBuyExactlyParams`

```typescript
const value: components.UniswapBuyExactlyParams = {
  tokenIn: "WETH",
  tokenOut: "WETH",
  fee: "0.01",
  amountOut: 1.5,
  maxSlippagePercent: 0.5,
};
```

### `components.UniswapMintLiquidityProvisionParams`

```typescript
const value: components.UniswapMintLiquidityProvisionParams = {
  token0: "WETH",
  token1: "WETH",
  fee: "1.0",
  tickLower: -1000,
  tickUpper: 1000,
  amount0Desired: "1.5",
  amount1Desired: "1.7",
  amount0Min: "1.4",
  amount1Min: "1.6",
  recipient: "0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B",
};
```

### `components.UniswapSellExactlyParams`

```typescript
const value: components.UniswapSellExactlyParams = {
  tokenIn: "WETH",
  tokenOut: "WETH",
  fee: "0.05",
  amountIn: 1.5,
  maxSlippagePercent: 0.5,
};
```

### `components.UniswapWithdrawLiquidityProvisionParams`

```typescript
const value: components.UniswapWithdrawLiquidityProvisionParams = {
  tokenId: 405500,
  percentageForWithdrawal: "25",
};
```

### `components.UnwrapWethParams`

```typescript
const value: components.UnwrapWethParams = {
  amount: 1.5,
};
```

### `components.VaultDepositParams`

```typescript
const value: components.VaultDepositParams = {
  vaultAddress: "0xbEef047a543E45807105E51A8BBEFCc5950fcfBa",
  amount: 1.5,
};
```

### `components.VaultWithdrawParams`

```typescript
const value: components.VaultWithdrawParams = {
  vaultAddress: "0xbEef047a543E45807105E51A8BBEFCc5950fcfBa",
  amount: "1.5",
};
```

### `components.WrapEthParams`

```typescript
const value: components.WrapEthParams = {
  amount: 1.5,
};
```

