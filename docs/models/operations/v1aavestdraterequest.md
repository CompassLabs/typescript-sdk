# V1AaveStdRateRequest

## Example Usage

```typescript
import { V1AaveStdRateRequest } from "@compass-labs/api-sdk/models/operations";

let value: V1AaveStdRateRequest = {};
```

## Fields

| Field                                                                          | Type                                                                           | Required                                                                       | Description                                                                    | Example                                                                        |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `chain`                                                                        | [operations.V1AaveStdRateChain](../../models/operations/v1aavestdratechain.md) | :heavy_check_mark:                                                             | N/A                                                                            |                                                                                |
| `block`                                                                        | *number*                                                                       | :heavy_minus_sign:                                                             | Optional block number (defaults to latest).                                    |                                                                                |
| `token`                                                                        | *string*                                                                       | :heavy_check_mark:                                                             | The symbol or address of the token..                                           | USDC                                                                           |
| `days`                                                                         | *number*                                                                       | :heavy_check_mark:                                                             | The number of days for which the standard deviation shall be calculated.       |                                                                                |