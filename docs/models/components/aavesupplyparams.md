# AaveSupplyParams

## Example Usage

```typescript
import { AaveSupplyParams } from "@compass-labs/api-sdk/models/components";

let value: AaveSupplyParams = {
  token: "WETH",
  amount: 1.5,
};
```

## Fields

| Field                                                                                              | Type                                                                                               | Required                                                                                           | Description                                                                                        | Example                                                                                            |
| -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| `actionType`                                                                                       | *string*                                                                                           | :heavy_minus_sign:                                                                                 | N/A                                                                                                |                                                                                                    |
| `token`                                                                                            | *string*                                                                                           | :heavy_check_mark:                                                                                 | The symbol or address of the underlying asset to supply as collateral. You can borrow against it.. | WETH                                                                                               |
| `amount`                                                                                           | *components.AaveSupplyParamsAmount*                                                                | :heavy_check_mark:                                                                                 | The amount of the asset to supply                                                                  | 1.5                                                                                                |
| `onBehalfOf`                                                                                       | *string*                                                                                           | :heavy_minus_sign:                                                                                 | The address on behalf of whom the supply is made. Defaults to the transaction sender.              |                                                                                                    |