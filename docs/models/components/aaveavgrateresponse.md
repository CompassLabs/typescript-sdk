# AaveAvgRateResponse

## Example Usage

```typescript
import { AaveAvgRateResponse } from "@compass-labs/api-sdk/models/components";

let value: AaveAvgRateResponse = {
  supplyApyVariableRate: 274.71,
  supplyAprVariableRate: 1087.07,
  borrowApyVariableRate: 5500.69,
  borrowAprVariableRate: 8575.73,
  borrowApyFixedRate: 1753.58,
  borrowAprFixedRate: 7302.79,
};
```

## Fields

| Field                                       | Type                                        | Required                                    | Description                                 |
| ------------------------------------------- | ------------------------------------------- | ------------------------------------------- | ------------------------------------------- |
| `supplyApyVariableRate`                     | *number*                                    | :heavy_check_mark:                          | Mean of the variable rate APY for deposits. |
| `supplyAprVariableRate`                     | *number*                                    | :heavy_check_mark:                          | Mean of the variable rate APR for deposits. |
| `borrowApyVariableRate`                     | *number*                                    | :heavy_check_mark:                          | Mean of the variable rate APY for loans.    |
| `borrowAprVariableRate`                     | *number*                                    | :heavy_check_mark:                          | Mean of the variable rate APR for loans.    |
| `borrowApyFixedRate`                        | *number*                                    | :heavy_check_mark:                          | Mean of the fixed rate APY for loans.       |
| `borrowAprFixedRate`                        | *number*                                    | :heavy_check_mark:                          | Mean of the fixed rate APR for loans.       |