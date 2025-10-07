# V1AaveHistoricalTransactionsRequest

## Example Usage

```typescript
import { V1AaveHistoricalTransactionsRequest } from "@compass-labs/api-sdk/models/operations";

let value: V1AaveHistoricalTransactionsRequest = {};
```

## Fields

| Field                                                                                                        | Type                                                                                                         | Required                                                                                                     | Description                                                                                                  |
| ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------ |
| `offset`                                                                                                     | *number*                                                                                                     | :heavy_minus_sign:                                                                                           | The offset of the first item to return.                                                                      |
| `limit`                                                                                                      | *number*                                                                                                     | :heavy_minus_sign:                                                                                           | The number of items to return.                                                                               |
| `chain`                                                                                                      | [operations.V1AaveHistoricalTransactionsChain](../../models/operations/v1aavehistoricaltransactionschain.md) | :heavy_check_mark:                                                                                           | N/A                                                                                                          |
| `userAddress`                                                                                                | *string*                                                                                                     | :heavy_check_mark:                                                                                           | The address of the user to get historical transactions for.                                                  |