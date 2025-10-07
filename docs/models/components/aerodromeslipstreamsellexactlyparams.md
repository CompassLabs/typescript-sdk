# AerodromeSlipstreamSellExactlyParams

Parameters model for selling exactly an amount of tokens.

## Example Usage

```typescript
import { AerodromeSlipstreamSellExactlyParams } from "@compass-labs/api-sdk/models/components";

let value: AerodromeSlipstreamSellExactlyParams = {
  tokenIn: "WETH",
  tokenOut: "WETH",
  tickSpacing: 100,
  amountIn: 1.5,
  amountOutMinimum: 1.4,
};
```

## Fields

| Field                                                             | Type                                                              | Required                                                          | Description                                                       | Example                                                           |
| ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------- |
| `actionType`                                                      | *string*                                                          | :heavy_minus_sign:                                                | N/A                                                               |                                                                   |
| `tokenIn`                                                         | *string*                                                          | :heavy_check_mark:                                                | The symbol or address of the token to swap from.                  | WETH                                                              |
| `tokenOut`                                                        | *string*                                                          | :heavy_check_mark:                                                | The symbol or address of the token to swap to.                    | WETH                                                              |
| `tickSpacing`                                                     | *number*                                                          | :heavy_check_mark:                                                | The tick spacing of the pool                                      | 100                                                               |
| `amountIn`                                                        | *components.AerodromeSlipstreamSellExactlyParamsAmountIn*         | :heavy_check_mark:                                                | The amount of the token to swap from                              | 1.5                                                               |
| `amountOutMinimum`                                                | *components.AerodromeSlipstreamSellExactlyParamsAmountOutMinimum* | :heavy_minus_sign:                                                | The minimum amount of the token to swap to, defaults to 0         | 1.4                                                               |