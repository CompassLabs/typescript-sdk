# V1UniswapQuoteSellExactlyRequest

## Example Usage

```typescript
import { V1UniswapQuoteSellExactlyRequest } from "@compass-labs/api-sdk/models/operations";

let value: V1UniswapQuoteSellExactlyRequest = {
  tokenOut: "USDC",
  amountIn: 3717.62,
};
```

## Fields

| Field                                                                                                      | Type                                                                                                       | Required                                                                                                   | Description                                                                                                | Example                                                                                                    |
| ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- |
| `chain`                                                                                                    | [operations.V1UniswapQuoteSellExactlyChain](../../models/operations/v1uniswapquotesellexactlychain.md)     | :heavy_check_mark:                                                                                         | N/A                                                                                                        |                                                                                                            |
| `tokenIn`                                                                                                  | *string*                                                                                                   | :heavy_check_mark:                                                                                         | The symbol or address of the token to swap from.                                                           | USDC                                                                                                       |
| `tokenOut`                                                                                                 | *string*                                                                                                   | :heavy_check_mark:                                                                                         | The symbol or address of the token to swap to.                                                             | USDC                                                                                                       |
| `fee`                                                                                                      | [operations.V1UniswapQuoteSellExactlyFeeEnum](../../models/operations/v1uniswapquotesellexactlyfeeenum.md) | :heavy_check_mark:                                                                                         | The fee to pay for the swap                                                                                |                                                                                                            |
| `amountIn`                                                                                                 | *operations.AmountIn*                                                                                      | :heavy_check_mark:                                                                                         | The amount of the token to swap from                                                                       |                                                                                                            |