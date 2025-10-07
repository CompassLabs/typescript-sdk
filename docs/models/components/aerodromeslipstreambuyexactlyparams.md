# AerodromeSlipstreamBuyExactlyParams

Parameters model for buying exactly an amount of tokens.

## Example Usage

```typescript
import { AerodromeSlipstreamBuyExactlyParams } from "@compass-labs/api-sdk/models/components";

let value: AerodromeSlipstreamBuyExactlyParams = {
  tokenIn: "WETH",
  tokenOut: "WETH",
  tickSpacing: 100,
  amountOut: 1.5,
  amountInMaximum: 1.6,
};
```

## Fields

| Field                                                           | Type                                                            | Required                                                        | Description                                                     | Example                                                         |
| --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------------- |
| `actionType`                                                    | *string*                                                        | :heavy_minus_sign:                                              | N/A                                                             |                                                                 |
| `tokenIn`                                                       | *string*                                                        | :heavy_check_mark:                                              | The symbol of the token to swap from.                           | WETH                                                            |
| `tokenOut`                                                      | *string*                                                        | :heavy_check_mark:                                              | The symbol of the token to swap to.                             | WETH                                                            |
| `tickSpacing`                                                   | *number*                                                        | :heavy_check_mark:                                              | The tick spacing of the pool                                    | 100                                                             |
| `amountOut`                                                     | *components.AerodromeSlipstreamBuyExactlyParamsAmountOut*       | :heavy_check_mark:                                              | The amount of the token to swap to                              | 1.5                                                             |
| `amountInMaximum`                                               | *components.AerodromeSlipstreamBuyExactlyParamsAmountInMaximum* | :heavy_check_mark:                                              | The maximum amount of the token to swap from                    | 1.6                                                             |