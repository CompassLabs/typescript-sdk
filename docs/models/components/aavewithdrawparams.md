# AaveWithdrawParams

## Example Usage

```typescript
import { AaveWithdrawParams } from "@compass-labs/api-sdk/models/components";

let value: AaveWithdrawParams = {
  token: "WETH",
  amount: 1.5,
  recipient: "0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2",
};
```

## Fields

| Field                                                | Type                                                 | Required                                             | Description                                          | Example                                              |
| ---------------------------------------------------- | ---------------------------------------------------- | ---------------------------------------------------- | ---------------------------------------------------- | ---------------------------------------------------- |
| `actionType`                                         | *string*                                             | :heavy_minus_sign:                                   | N/A                                                  |                                                      |
| `token`                                              | *string*                                             | :heavy_check_mark:                                   | The symbol of the underlying asset to withdraw..     | WETH                                                 |
| `amount`                                             | *components.AaveWithdrawParamsAmount*                | :heavy_check_mark:                                   | The amount of the asset to withdraw                  | 1.5                                                  |
| `recipient`                                          | *string*                                             | :heavy_check_mark:                                   | The address of the recipient of the withdrawn funds. | 0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2           |