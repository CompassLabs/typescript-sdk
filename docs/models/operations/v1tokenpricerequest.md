# V1TokenPriceRequest

## Example Usage

```typescript
import { V1TokenPriceRequest } from "@compass-labs/api-sdk/models/operations";

let value: V1TokenPriceRequest = {
  token: "USDC",
};
```

## Fields

| Field                                                                        | Type                                                                         | Required                                                                     | Description                                                                  | Example                                                                      |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| `chain`                                                                      | [operations.V1TokenPriceChain](../../models/operations/v1tokenpricechain.md) | :heavy_check_mark:                                                           | N/A                                                                          |                                                                              |
| `block`                                                                      | *number*                                                                     | :heavy_minus_sign:                                                           | Optional block number (defaults to latest).                                  |                                                                              |
| `token`                                                                      | *string*                                                                     | :heavy_check_mark:                                                           | The symbol or address of the token for which to get the price..              | USDC                                                                         |