# BatchedUserOperationsRequest

Request model for batching user operations.

Used for smart account batching and 5792 batching.

## Example Usage

```typescript
import { BatchedUserOperationsRequest } from "@compass-labs/api-sdk/models/components";

let value: BatchedUserOperationsRequest = {
  chain: "ethereum",
  sender: "0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B",
  operations: [
    {
      body: {
        token: "USDC",
        contract: "UniswapV3Router",
        amount: "1000",
      },
    },
  ],
};
```

## Fields

| Field                                                                                                                        | Type                                                                                                                         | Required                                                                                                                     | Description                                                                                                                  | Example                                                                                                                      |
| ---------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| `chain`                                                                                                                      | [components.BatchedUserOperationsRequestChain](../../models/components/batcheduseroperationsrequestchain.md)                 | :heavy_check_mark:                                                                                                           | N/A                                                                                                                          |                                                                                                                              |
| `sender`                                                                                                                     | *string*                                                                                                                     | :heavy_check_mark:                                                                                                           | The address of the transaction sender.                                                                                       | 0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B                                                                                   |
| `estimateGas`                                                                                                                | *boolean*                                                                                                                    | :heavy_minus_sign:                                                                                                           | Determines whether to estimate gas costs for transactions, also verifying that the transaction can be successfully executed. |                                                                                                                              |
| `operations`                                                                                                                 | [components.UserOperation](../../models/components/useroperation.md)[]                                                       | :heavy_check_mark:                                                                                                           | List of possible user operations                                                                                             | {<br/>"body": {<br/>"action_type": "SET_ALLOWANCE",<br/>"amount": "1000",<br/>"contract": "UniswapV3Router",<br/>"token": "USDC"<br/>}<br/>} |