# MorphoBorrowParams

## Example Usage

```typescript
import { MorphoBorrowParams } from "@compass-labs/api-sdk/models/components";

let value: MorphoBorrowParams = {
  amount: 1.5,
  uniqueMarketKey:
    "0xe7399fdebc318d76dfec7356caafcf8cd4b91287e139a3ec423f09aeeb656fc4",
};
```

## Fields

| Field                                                                                            | Type                                                                                             | Required                                                                                         | Description                                                                                      | Example                                                                                          |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| `actionType`                                                                                     | *string*                                                                                         | :heavy_minus_sign:                                                                               | N/A                                                                                              |                                                                                                  |
| `amount`                                                                                         | *components.MorphoBorrowParamsAmount*                                                            | :heavy_check_mark:                                                                               | Amount of the token to borrow from the market.                                                   | 1.5                                                                                              |
| `uniqueMarketKey`                                                                                | *string*                                                                                         | :heavy_check_mark:                                                                               | The key that uniquely identifies the market. This can be found using the 'Get Markets' endpoint. | 0xe7399fdebc318d76dfec7356caafcf8cd4b91287e139a3ec423f09aeeb656fc4                               |
| `onBehalfOf`                                                                                     | *string*                                                                                         | :heavy_minus_sign:                                                                               | The address where the collateral is borrowed against. Defaults to sender.                        |                                                                                                  |
| `receiver`                                                                                       | *string*                                                                                         | :heavy_minus_sign:                                                                               | The address of the receiver of the tokens borrowed. Defaults to the transaction sender.          |                                                                                                  |