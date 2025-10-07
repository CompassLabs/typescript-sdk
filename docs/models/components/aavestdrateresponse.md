# AaveSTDRateResponse

## Example Usage

```typescript
import { AaveSTDRateResponse } from "@compass-labs/api-sdk/models/components";

let value: AaveSTDRateResponse = {
  supplyApyVariableRate: 4033.88,
  supplyAprVariableRate: 9826.18,
  borrowApyVariableRate: 9255.45,
  borrowAprVariableRate: 6487.1,
  borrowApyFixedRate: 585.35,
  borrowAprFixedRate: 1220.65,
};
```

## Fields

| Field                                                     | Type                                                      | Required                                                  | Description                                               |
| --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- | --------------------------------------------------------- |
| `supplyApyVariableRate`                                   | *number*                                                  | :heavy_check_mark:                                        | Standard deviation of the variable rate APY for deposits. |
| `supplyAprVariableRate`                                   | *number*                                                  | :heavy_check_mark:                                        | Standard deviation of the variable rate APR for deposits. |
| `borrowApyVariableRate`                                   | *number*                                                  | :heavy_check_mark:                                        | Standard deviation of the variable rate APY for loans.    |
| `borrowAprVariableRate`                                   | *number*                                                  | :heavy_check_mark:                                        | Standard deviation of the variable rate APR for loans.    |
| `borrowApyFixedRate`                                      | *number*                                                  | :heavy_check_mark:                                        | Standard deviation of the fixed rate APY for loans.       |
| `borrowAprFixedRate`                                      | *number*                                                  | :heavy_check_mark:                                        | Standard deviation of the fixed rate APR for loans.       |