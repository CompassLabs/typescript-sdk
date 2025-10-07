# UniswapMintLiquidityProvisionParams

## Example Usage

```typescript
import { UniswapMintLiquidityProvisionParams } from "@compass-labs/api-sdk/models/components";

let value: UniswapMintLiquidityProvisionParams = {
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

## Fields

| Field                                                                                    | Type                                                                                     | Required                                                                                 | Description                                                                              | Example                                                                                  |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `actionType`                                                                             | *string*                                                                                 | :heavy_minus_sign:                                                                       | N/A                                                                                      |                                                                                          |
| `token0`                                                                                 | *string*                                                                                 | :heavy_check_mark:                                                                       | The symbol or address of the first token in the pair.                                    | WETH                                                                                     |
| `token1`                                                                                 | *string*                                                                                 | :heavy_check_mark:                                                                       | The symbol or address of the second token in the pair.                                   | WETH                                                                                     |
| `fee`                                                                                    | [components.FeeEnum](../../models/components/feeenum.md)                                 | :heavy_check_mark:                                                                       | The transaction fee of a Uniswap pool in bips.<br/><br/>Uniswap supports 4 different fee levels. |                                                                                          |
| `tickLower`                                                                              | *number*                                                                                 | :heavy_check_mark:                                                                       | The lower tick of the range to mint the position in                                      | -1000                                                                                    |
| `tickUpper`                                                                              | *number*                                                                                 | :heavy_check_mark:                                                                       | The upper tick of the range to mint the position in                                      | 1000                                                                                     |
| `amount0Desired`                                                                         | *components.UniswapMintLiquidityProvisionParamsAmount0Desired*                           | :heavy_check_mark:                                                                       | The desired amount of the first token to deposit                                         | 1.5                                                                                      |
| `amount1Desired`                                                                         | *components.UniswapMintLiquidityProvisionParamsAmount1Desired*                           | :heavy_check_mark:                                                                       | The desired amount of the second token to deposit                                        | 1.7                                                                                      |
| `amount0Min`                                                                             | *components.UniswapMintLiquidityProvisionParamsAmount0Min*                               | :heavy_check_mark:                                                                       | The minimum amount of the first token to deposit                                         | 1.4                                                                                      |
| `amount1Min`                                                                             | *components.UniswapMintLiquidityProvisionParamsAmount1Min*                               | :heavy_check_mark:                                                                       | The minimum amount of the second token to deposit                                        | 1.6                                                                                      |
| `recipient`                                                                              | *string*                                                                                 | :heavy_minus_sign:                                                                       | The address that will receive the LP tokens                                              | 0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B                                               |