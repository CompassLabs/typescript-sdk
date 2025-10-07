# AaveBorrowParams

## Example Usage

```typescript
import { AaveBorrowParams } from "@compass-labs/api-sdk/models/components";

let value: AaveBorrowParams = {
  token: "WETH",
  amount: 150.5,
  interestRateMode: "variable",
};
```

## Fields

| Field                                                                                                    | Type                                                                                                     | Required                                                                                                 | Description                                                                                              | Example                                                                                                  |
| -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| `actionType`                                                                                             | *string*                                                                                                 | :heavy_minus_sign:                                                                                       | N/A                                                                                                      |                                                                                                          |
| `token`                                                                                                  | *string*                                                                                                 | :heavy_check_mark:                                                                                       | The symbol or address of the underlying asset to borrow..                                                | WETH                                                                                                     |
| `amount`                                                                                                 | *components.AaveBorrowParamsAmount*                                                                      | :heavy_check_mark:                                                                                       | The amount of the asset to borrow                                                                        | 150.5                                                                                                    |
| `interestRateMode`                                                                                       | [components.InterestRateMode](../../models/components/interestratemode.md)                               | :heavy_check_mark:                                                                                       | On AAVE there are 2 different interest modes.<br/><br/>A stable (but typically higher rate), or a variable rate. |                                                                                                          |
| `onBehalfOf`                                                                                             | *string*                                                                                                 | :heavy_minus_sign:                                                                                       | The address on behalf of whom the supply is made                                                         |                                                                                                          |