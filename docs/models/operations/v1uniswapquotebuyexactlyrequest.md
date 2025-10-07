# V1UniswapQuoteBuyExactlyRequest

## Example Usage

```typescript
import { V1UniswapQuoteBuyExactlyRequest } from "@compass-labs/api-sdk/models/operations";

let value: V1UniswapQuoteBuyExactlyRequest = {
  tokenOut: "USDC",
  amountOut: 7887.88,
};
```

## Fields

| Field                                                                                                    | Type                                                                                                     | Required                                                                                                 | Description                                                                                              | Example                                                                                                  |
| -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| `chain`                                                                                                  | [operations.V1UniswapQuoteBuyExactlyChain](../../models/operations/v1uniswapquotebuyexactlychain.md)     | :heavy_check_mark:                                                                                       | N/A                                                                                                      |                                                                                                          |
| `tokenIn`                                                                                                | *string*                                                                                                 | :heavy_check_mark:                                                                                       | The symbol or address of the token to swap from.                                                         | USDC                                                                                                     |
| `tokenOut`                                                                                               | *string*                                                                                                 | :heavy_check_mark:                                                                                       | The symbol or address of the token to swap to.                                                           | USDC                                                                                                     |
| `fee`                                                                                                    | [operations.V1UniswapQuoteBuyExactlyFeeEnum](../../models/operations/v1uniswapquotebuyexactlyfeeenum.md) | :heavy_check_mark:                                                                                       | The fee to pay for the swap                                                                              |                                                                                                          |
| `amountOut`                                                                                              | *operations.AmountOut*                                                                                   | :heavy_check_mark:                                                                                       | The amount of the token to swap to                                                                       |                                                                                                          |