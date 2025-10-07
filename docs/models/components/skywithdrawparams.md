# SkyWithdrawParams

## Example Usage

```typescript
import { SkyWithdrawParams } from "@compass-labs/api-sdk/models/components";

let value: SkyWithdrawParams = {
  amount: "512.05",
};
```

## Fields

| Field                                                                                                               | Type                                                                                                                | Required                                                                                                            | Description                                                                                                         |
| ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| `actionType`                                                                                                        | *string*                                                                                                            | :heavy_minus_sign:                                                                                                  | N/A                                                                                                                 |
| `amount`                                                                                                            | *any*                                                                                                               | :heavy_check_mark:                                                                                                  | The amount of USDS you would like to withdraw. If set to 'ALL', your total deposited USDS amount will be withdrawn. |
| `receiver`                                                                                                          | *string*                                                                                                            | :heavy_minus_sign:                                                                                                  | The address which will receive the withdrawn USDS. Defaults to the sender.                                          |