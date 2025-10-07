# OdosTransactionResponse

## Example Usage

```typescript
import { OdosTransactionResponse } from "@compass-labs/api-sdk/models/components";

let value: OdosTransactionResponse = {
  transaction: {
    to: "<value>",
    data: "<value>",
    value: "<value>",
  },
  amountOutQuote: "<value>",
};
```

## Fields

| Field                                                                                                                                                                                                        | Type                                                                                                                                                                                                         | Required                                                                                                                                                                                                     | Description                                                                                                                                                                                                  |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `transaction`                                                                                                                                                                                                | *components.OdosTransactionResponseTransaction*                                                                                                                                                              | :heavy_check_mark:                                                                                                                                                                                           | The unsigned transaction data. User must sign and broadcast to network.                                                                                                                                      |
| `amountOutQuote`                                                                                                                                                                                             | *string*                                                                                                                                                                                                     | :heavy_check_mark:                                                                                                                                                                                           | The estimated amount out for the transaction. The actual output amount for this transaction is guaranteed be within the acceptable threshold, defined by the `max_slippage_percent`, relative to this quote. |