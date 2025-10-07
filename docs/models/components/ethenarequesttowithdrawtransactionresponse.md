# EthenaRequestToWithdrawTransactionResponse

## Example Usage

```typescript
import { EthenaRequestToWithdrawTransactionResponse } from "@compass-labs/api-sdk/models/components";

let value: EthenaRequestToWithdrawTransactionResponse = {
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
  cooldownDurationDays: 864385,
};
```

## Fields

| Field                                                                                                                                   | Type                                                                                                                                    | Required                                                                                                                                | Description                                                                                                                             |
| --------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| `transaction`                                                                                                                           | *components.EthenaRequestToWithdrawTransactionResponseTransaction*                                                                      | :heavy_check_mark:                                                                                                                      | The unsigned transaction data. User must sign and broadcast to network.                                                                 |
| `cooldownDurationDays`                                                                                                                  | *number*                                                                                                                                | :heavy_check_mark:                                                                                                                      | The duration of days that must pass before a position can be withdrawn from the Ethena vault after a request to withdraw has been made. |