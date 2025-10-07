# UniswapBuyExactlyTransactionResponse

## Example Usage

```typescript
import { UniswapBuyExactlyTransactionResponse } from "@compass-labs/api-sdk/models/components";

let value: UniswapBuyExactlyTransactionResponse = {
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
  amountInQuote: "<value>",
};
```

## Fields

| Field                                                                                                                                                                                                      | Type                                                                                                                                                                                                       | Required                                                                                                                                                                                                   | Description                                                                                                                                                                                                |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `transaction`                                                                                                                                                                                              | *components.UniswapBuyExactlyTransactionResponseTransaction*                                                                                                                                               | :heavy_check_mark:                                                                                                                                                                                         | The unsigned transaction data. User must sign and broadcast to network.                                                                                                                                    |
| `amountInQuote`                                                                                                                                                                                            | *string*                                                                                                                                                                                                   | :heavy_check_mark:                                                                                                                                                                                         | The estimated amount in for the transaction. The actual input amount for this transaction is guaranteed be within the acceptable threshold, defined by the `max_slippage_percent`, relative to this quote. |