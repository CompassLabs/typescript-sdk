# MorphoWithdrawCollateralParams

## Example Usage

```typescript
import { MorphoWithdrawCollateralParams } from "@compass-labs/api-sdk/models/components";

let value: MorphoWithdrawCollateralParams = {
  amount: 1.5,
  uniqueMarketKey:
    "0xe7399fdebc318d76dfec7356caafcf8cd4b91287e139a3ec423f09aeeb656fc4",
};
```

## Fields

| Field                                                                                            | Type                                                                                             | Required                                                                                         | Description                                                                                      | Example                                                                                          |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| `actionType`                                                                                     | *string*                                                                                         | :heavy_minus_sign:                                                                               | N/A                                                                                              |                                                                                                  |
| `amount`                                                                                         | *components.MorphoWithdrawCollateralParamsAmount*                                                | :heavy_check_mark:                                                                               | Amount of the token to supply to the market as collateral.                                       | 1.5                                                                                              |
| `uniqueMarketKey`                                                                                | *string*                                                                                         | :heavy_check_mark:                                                                               | The key that uniquely identifies the market. This can be found using the 'Get Markets' endpoint. | 0xe7399fdebc318d76dfec7356caafcf8cd4b91287e139a3ec423f09aeeb656fc4                               |
| `onBehalfOf`                                                                                     | *string*                                                                                         | :heavy_minus_sign:                                                                               | The address on behalf of whom the withdraw is made. Defaults to sender.                          |                                                                                                  |
| `receiver`                                                                                       | *string*                                                                                         | :heavy_minus_sign:                                                                               | The address where the withdrawn collateral will be received. Defaults to sender.                 |                                                                                                  |