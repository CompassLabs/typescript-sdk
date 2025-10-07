# UnwrapWethRequest

Request model for unwrapping WETH back to native ETH.

## Example Usage

```typescript
import { UnwrapWethRequest } from "@compass-labs/api-sdk/models/components";

let value: UnwrapWethRequest = {
  amount: 1.5,
  chain: "ethereum",
  sender: "0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B",
};
```

## Fields

| Field                                                                                                                        | Type                                                                                                                         | Required                                                                                                                     | Description                                                                                                                  | Example                                                                                                                      |
| ---------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| `actionType`                                                                                                                 | *string*                                                                                                                     | :heavy_minus_sign:                                                                                                           | N/A                                                                                                                          |                                                                                                                              |
| `amount`                                                                                                                     | *components.UnwrapWethRequestAmount*                                                                                         | :heavy_check_mark:                                                                                                           | The amount of WETH to unwrap.                                                                                                | 1.5                                                                                                                          |
| `chain`                                                                                                                      | [components.UnwrapWethRequestChain](../../models/components/unwrapwethrequestchain.md)                                       | :heavy_check_mark:                                                                                                           | N/A                                                                                                                          |                                                                                                                              |
| `sender`                                                                                                                     | *string*                                                                                                                     | :heavy_check_mark:                                                                                                           | The address of the transaction sender.                                                                                       | 0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B                                                                                   |
| `estimateGas`                                                                                                                | *boolean*                                                                                                                    | :heavy_minus_sign:                                                                                                           | Determines whether to estimate gas costs for transactions, also verifying that the transaction can be successfully executed. |                                                                                                                              |