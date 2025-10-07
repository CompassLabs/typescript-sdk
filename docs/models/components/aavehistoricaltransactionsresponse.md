# AaveHistoricalTransactionsResponse

Response model for getting Aave historical transactions.

## Example Usage

```typescript
import { AaveHistoricalTransactionsResponse } from "@compass-labs/api-sdk/models/components";

let value: AaveHistoricalTransactionsResponse = {
  offset: 942972,
  limit: 82751,
  transactions: [],
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `offset`                                                                                                                                  | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Specifies how many transactions to skip before returning results, letting you choose the starting point for the data you want to receive. |
| `limit`                                                                                                                                   | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Sets the maximum number of transactions to include in the response, helping control the size of the returned dataset.                     |
| `transactions`                                                                                                                            | *components.AaveHistoricalTransactionsResponseTransaction*[]                                                                              | :heavy_check_mark:                                                                                                                        | N/A                                                                                                                                       |