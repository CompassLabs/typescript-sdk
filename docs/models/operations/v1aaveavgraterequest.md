# V1AaveAvgRateRequest

## Example Usage

```typescript
import { V1AaveAvgRateRequest } from "@compass-labs/api-sdk/models/operations";

let value: V1AaveAvgRateRequest = {};
```

## Fields

| Field                                                                          | Type                                                                           | Required                                                                       | Description                                                                    | Example                                                                        |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `chain`                                                                        | [operations.V1AaveAvgRateChain](../../models/operations/v1aaveavgratechain.md) | :heavy_check_mark:                                                             | N/A                                                                            |                                                                                |
| `block`                                                                        | *number*                                                                       | :heavy_minus_sign:                                                             | Optional block number (defaults to latest).                                    |                                                                                |
| `token`                                                                        | *string*                                                                       | :heavy_check_mark:                                                             | The symbol or address of the token..                                           | USDC                                                                           |
| `days`                                                                         | *number*                                                                       | :heavy_check_mark:                                                             | The number of days for which the average shall be calculated.                  |                                                                                |