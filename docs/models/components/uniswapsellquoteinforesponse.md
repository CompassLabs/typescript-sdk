# UniswapSellQuoteInfoResponse

## Example Usage

```typescript
import { UniswapSellQuoteInfoResponse } from "@compass-labs/api-sdk/models/components";

let value: UniswapSellQuoteInfoResponse = {
  amountOut: "<value>",
  priceAfter: "<value>",
};
```

## Fields

| Field                                                                                            | Type                                                                                             | Required                                                                                         | Description                                                                                      |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| `amountOut`                                                                                      | *string*                                                                                         | :heavy_check_mark:                                                                               | The amount of token_out you would receive from the pool.                                         |
| `priceAfter`                                                                                     | *string*                                                                                         | :heavy_check_mark:                                                                               | The price of the pool after this trade would happen. (How much token0 you need to buy 1 token1.) |