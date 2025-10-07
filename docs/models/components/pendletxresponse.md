# PendleTxResponse

## Example Usage

```typescript
import { PendleTxResponse } from "@compass-labs/api-sdk/models/components";

let value: PendleTxResponse = {
  transaction: {
    chainId: "<id>",
    data: "<value>",
    from: "<value>",
    gas: "<value>",
    to: "<value>",
    value: "<value>",
    nonce: "<value>",
    maxFeePerGas: "<value>",
    maxPriorityFeePerGas: "<value>",
  },
  amountOutQuote: "<value>",
};
```

## Fields

| Field                                                                                                                                                                                                        | Type                                                                                                                                                                                                         | Required                                                                                                                                                                                                     | Description                                                                                                                                                                                                  |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `transaction`                                                                                                                                                                                                | *components.PendleTxResponseTransaction*                                                                                                                                                                     | :heavy_check_mark:                                                                                                                                                                                           | The unsigned transaction data. User must sign and broadcast to network.                                                                                                                                      |
| `amountOutQuote`                                                                                                                                                                                             | *string*                                                                                                                                                                                                     | :heavy_check_mark:                                                                                                                                                                                           | The estimated amount out for the transaction. The actual output amount for this transaction is guaranteed be within the acceptable threshold, defined by the `max_slippage_percent`, relative to this quote. |