# V1UniswapPoolPriceRequest

## Example Usage

```typescript
import { V1UniswapPoolPriceRequest } from "@compass-labs/api-sdk/models/operations";

let value: V1UniswapPoolPriceRequest = {
  tokenOut: "USDC",
};
```

## Fields

| Field                                                                                        | Type                                                                                         | Required                                                                                     | Description                                                                                  | Example                                                                                      |
| -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| `chain`                                                                                      | [operations.V1UniswapPoolPriceChain](../../models/operations/v1uniswappoolpricechain.md)     | :heavy_check_mark:                                                                           | N/A                                                                                          |                                                                                              |
| `tokenIn`                                                                                    | *string*                                                                                     | :heavy_check_mark:                                                                           | The symbol or address of a token in the pool                                                 | USDC                                                                                         |
| `tokenOut`                                                                                   | *string*                                                                                     | :heavy_check_mark:                                                                           | The symbol or address of a token in the pool                                                 | USDC                                                                                         |
| `fee`                                                                                        | [operations.V1UniswapPoolPriceFeeEnum](../../models/operations/v1uniswappoolpricefeeenum.md) | :heavy_check_mark:                                                                           | The fee of the pool                                                                          |                                                                                              |