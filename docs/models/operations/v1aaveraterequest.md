# V1AaveRateRequest

## Example Usage

```typescript
import { V1AaveRateRequest } from "@compass-labs/api-sdk/models/operations";

let value: V1AaveRateRequest = {};
```

## Fields

| Field                                                                    | Type                                                                     | Required                                                                 | Description                                                              | Example                                                                  |
| ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ |
| `chain`                                                                  | [operations.V1AaveRateChain](../../models/operations/v1aaveratechain.md) | :heavy_check_mark:                                                       | N/A                                                                      |                                                                          |
| `block`                                                                  | *number*                                                                 | :heavy_minus_sign:                                                       | Optional block number (defaults to latest).                              |                                                                          |
| `token`                                                                  | *string*                                                                 | :heavy_check_mark:                                                       | The symbol or address of the token to fetch the user's position on..     | USDC                                                                     |