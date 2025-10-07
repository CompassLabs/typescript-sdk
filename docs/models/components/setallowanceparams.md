# SetAllowanceParams

Parameters model for setting the token allowance for a given contract.

## Example Usage

```typescript
import { SetAllowanceParams } from "@compass-labs/api-sdk/models/components";

let value: SetAllowanceParams = {
  token: "USDC",
  contract: "AaveV3Pool",
  amount: 1.5,
};
```

## Fields

| Field                                                               | Type                                                                | Required                                                            | Description                                                         | Example                                                             |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- |
| `actionType`                                                        | *string*                                                            | :heavy_minus_sign:                                                  | N/A                                                                 |                                                                     |
| `token`                                                             | *string*                                                            | :heavy_check_mark:                                                  | The symbol or address of the token for which the allowance is set.. | USDC                                                                |
| `contract`                                                          | *components.SetAllowanceParamsContractUnion*                        | :heavy_check_mark:                                                  | The name or address of the contract to set spending allowance for.  | AaveV3Pool                                                          |
| `amount`                                                            | *components.SetAllowanceParamsAmount*                               | :heavy_check_mark:                                                  | The amount to set the allowance to.                                 | 1.5                                                                 |