# MorphoSupplyCollateralParams

## Example Usage

```typescript
import { MorphoSupplyCollateralParams } from "@compass-labs/api-sdk/models/components";

let value: MorphoSupplyCollateralParams = {
  amount: 1.5,
  uniqueMarketKey:
    "0xe7399fdebc318d76dfec7356caafcf8cd4b91287e139a3ec423f09aeeb656fc4",
};
```

## Fields

| Field                                                                                                    | Type                                                                                                     | Required                                                                                                 | Description                                                                                              | Example                                                                                                  |
| -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------- |
| `actionType`                                                                                             | *string*                                                                                                 | :heavy_minus_sign:                                                                                       | N/A                                                                                                      |                                                                                                          |
| `amount`                                                                                                 | *components.MorphoSupplyCollateralParamsAmount*                                                          | :heavy_check_mark:                                                                                       | Amount of the token to supply to the market as collateral.                                               | 1.5                                                                                                      |
| `uniqueMarketKey`                                                                                        | *string*                                                                                                 | :heavy_check_mark:                                                                                       | The key that uniquely identifies the market. This can be found using the 'Get Markets' endpoint.         | 0xe7399fdebc318d76dfec7356caafcf8cd4b91287e139a3ec423f09aeeb656fc4                                       |
| `onBehalfOf`                                                                                             | *string*                                                                                                 | :heavy_minus_sign:                                                                                       | The address on behalf of whom the supplied collateral is made. Defaults to sender.                       |                                                                                                          |
| `callbackData`                                                                                           | *Uint8Array*                                                                                             | :heavy_minus_sign:                                                                                       | An optional field for callback byte data that will be triggered upon successful supplying of collateral. |                                                                                                          |