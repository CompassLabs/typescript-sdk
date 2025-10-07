# UniswapBuyQuoteInfoResponse

## Example Usage

```typescript
import { UniswapBuyQuoteInfoResponse } from "@compass-labs/api-sdk/models/components";

let value: UniswapBuyQuoteInfoResponse = {
  amountIn: "<value>",
  priceAfter: "<value>",
};
```

## Fields

| Field                                                                                            | Type                                                                                             | Required                                                                                         | Description                                                                                      |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| `amountIn`                                                                                       | *string*                                                                                         | :heavy_check_mark:                                                                               | The amount of token_in you would need to give to the pool.                                       |
| `priceAfter`                                                                                     | *string*                                                                                         | :heavy_check_mark:                                                                               | The price of the pool after this trade would happen. (How much token0 you need to buy 1 token1.) |