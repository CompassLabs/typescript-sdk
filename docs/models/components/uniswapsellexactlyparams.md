# UniswapSellExactlyParams

Parameters model for selling exactly an amount of tokens.

## Example Usage

```typescript
import { UniswapSellExactlyParams } from "@compass-labs/api-sdk/models/components";

let value: UniswapSellExactlyParams = {
  tokenIn: "WETH",
  tokenOut: "WETH",
  fee: "0.05",
  amountIn: 1.5,
  maxSlippagePercent: 0.5,
};
```

## Fields

| Field                                                                                    | Type                                                                                     | Required                                                                                 | Description                                                                              | Example                                                                                  |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `actionType`                                                                             | *string*                                                                                 | :heavy_minus_sign:                                                                       | N/A                                                                                      |                                                                                          |
| `tokenIn`                                                                                | *string*                                                                                 | :heavy_check_mark:                                                                       | The symbol or address of the token to sell..                                             | WETH                                                                                     |
| `tokenOut`                                                                               | *string*                                                                                 | :heavy_check_mark:                                                                       | The symbol or address of the token to buy..                                              | WETH                                                                                     |
| `fee`                                                                                    | [components.FeeEnum](../../models/components/feeenum.md)                                 | :heavy_check_mark:                                                                       | The transaction fee of a Uniswap pool in bips.<br/><br/>Uniswap supports 4 different fee levels. |                                                                                          |
| `amountIn`                                                                               | *components.UniswapSellExactlyParamsAmountIn*                                            | :heavy_check_mark:                                                                       | The amount of the `token_in` to sell                                                     | 1.5                                                                                      |
| `maxSlippagePercent`                                                                     | *number*                                                                                 | :heavy_check_mark:                                                                       | The maximum slippage allowed in percent. e.g. `1` means `1 %` slippage allowed.          | 0.5                                                                                      |