# WrapEthRequest

Request model for wrapping ETH into WETH.

## Example Usage

```typescript
import { WrapEthRequest } from "@compass-labs/api-sdk/models/components";

let value: WrapEthRequest = {
  amount: 1.5,
  chain: "ethereum",
  sender: "0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B",
};
```

## Fields

| Field                                                                                                                        | Type                                                                                                                         | Required                                                                                                                     | Description                                                                                                                  | Example                                                                                                                      |
| ---------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| `actionType`                                                                                                                 | *string*                                                                                                                     | :heavy_minus_sign:                                                                                                           | N/A                                                                                                                          |                                                                                                                              |
| `amount`                                                                                                                     | *components.WrapEthRequestAmount*                                                                                            | :heavy_check_mark:                                                                                                           | The amount of ETH to wrap.                                                                                                   | 1.5                                                                                                                          |
| `chain`                                                                                                                      | [components.WrapEthRequestChain](../../models/components/wrapethrequestchain.md)                                             | :heavy_check_mark:                                                                                                           | N/A                                                                                                                          |                                                                                                                              |
| `sender`                                                                                                                     | *string*                                                                                                                     | :heavy_check_mark:                                                                                                           | The address of the transaction sender.                                                                                       | 0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B                                                                                   |
| `estimateGas`                                                                                                                | *boolean*                                                                                                                    | :heavy_minus_sign:                                                                                                           | Determines whether to estimate gas costs for transactions, also verifying that the transaction can be successfully executed. |                                                                                                                              |