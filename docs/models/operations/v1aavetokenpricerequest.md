# V1AaveTokenPriceRequest

## Example Usage

```typescript
import { V1AaveTokenPriceRequest } from "@compass-labs/api-sdk/models/operations";

let value: V1AaveTokenPriceRequest = {};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          | Example                                                                              |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `chain`                                                                              | [operations.V1AaveTokenPriceChain](../../models/operations/v1aavetokenpricechain.md) | :heavy_check_mark:                                                                   | N/A                                                                                  |                                                                                      |
| `block`                                                                              | *number*                                                                             | :heavy_minus_sign:                                                                   | Optional block number (defaults to latest).                                          |                                                                                      |
| `token`                                                                              | *string*                                                                             | :heavy_check_mark:                                                                   | The symbol or address of the asset whose price you want..                            | USDC                                                                                 |