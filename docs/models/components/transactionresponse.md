# TransactionResponse

## Example Usage

```typescript
import { TransactionResponse } from "@compass-labs/api-sdk/models/components";

let value: TransactionResponse = {
  transaction: {
    to: "<value>",
    data: "<value>",
    value: "<value>",
  },
};
```

## Fields

| Field                                                                   | Type                                                                    | Required                                                                | Description                                                             |
| ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- | ----------------------------------------------------------------------- |
| `transaction`                                                           | *components.TransactionResponseTransaction*                             | :heavy_check_mark:                                                      | The unsigned transaction data. User must sign and broadcast to network. |