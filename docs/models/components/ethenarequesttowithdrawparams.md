# EthenaRequestToWithdrawParams

## Example Usage

```typescript
import { EthenaRequestToWithdrawParams } from "@compass-labs/api-sdk/models/components";

let value: EthenaRequestToWithdrawParams = {
  amount: 1.5,
};
```

## Fields

| Field                                                                                                                                               | Type                                                                                                                                                | Required                                                                                                                                            | Description                                                                                                                                         |
| --------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| `actionType`                                                                                                                                        | *string*                                                                                                                                            | :heavy_minus_sign:                                                                                                                                  | N/A                                                                                                                                                 |
| `amount`                                                                                                                                            | *any*                                                                                                                                               | :heavy_check_mark:                                                                                                                                  | The amount of USDe to request to withdraw from Ethena's vault. If set to 'ALL', your total deposited USDe amount will be requested to be withdrawn. |