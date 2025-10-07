# V1AerodromeSlipstreamPoolPriceRequest

## Example Usage

```typescript
import { V1AerodromeSlipstreamPoolPriceRequest } from "@compass-labs/api-sdk/models/operations";

let value: V1AerodromeSlipstreamPoolPriceRequest = {
  tokenOut: "USDC",
};
```

## Fields

| Field                                                                                                            | Type                                                                                                             | Required                                                                                                         | Description                                                                                                      | Example                                                                                                          |
| ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| `chain`                                                                                                          | [operations.V1AerodromeSlipstreamPoolPriceChain](../../models/operations/v1aerodromeslipstreampoolpricechain.md) | :heavy_check_mark:                                                                                               | N/A                                                                                                              |                                                                                                                  |
| `tokenIn`                                                                                                        | *string*                                                                                                         | :heavy_check_mark:                                                                                               | The symbol or address of a token in the pool.                                                                    | USDC                                                                                                             |
| `tokenOut`                                                                                                       | *string*                                                                                                         | :heavy_check_mark:                                                                                               | The symbol or address of a token in the pool.                                                                    | USDC                                                                                                             |
| `tickSpacing`                                                                                                    | *number*                                                                                                         | :heavy_minus_sign:                                                                                               | The tick spacing of the pool                                                                                     |                                                                                                                  |