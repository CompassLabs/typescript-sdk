# AaveRateResponse

## Example Usage

```typescript
import { AaveRateResponse } from "@compass-labs/api-sdk/models/components";

let value: AaveRateResponse = {
  supplyApyVariableRate: "<value>",
  supplyAprVariableRate: "<value>",
  borrowApyVariableRate: "<value>",
  borrowAprVariableRate: "<value>",
  borrowApyFixedRate: "<value>",
  borrowAprFixedRate: "<value>",
};
```

## Fields

| Field                           | Type                            | Required                        | Description                     |
| ------------------------------- | ------------------------------- | ------------------------------- | ------------------------------- |
| `supplyApyVariableRate`         | *string*                        | :heavy_check_mark:              | Variable rate APY for deposits. |
| `supplyAprVariableRate`         | *string*                        | :heavy_check_mark:              | Variable rate APR for deposits. |
| `borrowApyVariableRate`         | *string*                        | :heavy_check_mark:              | Variable rate APY for loans.    |
| `borrowAprVariableRate`         | *string*                        | :heavy_check_mark:              | Variable rate APR for loans.    |
| `borrowApyFixedRate`            | *string*                        | :heavy_check_mark:              | Fixed rate APY for loans.       |
| `borrowAprFixedRate`            | *string*                        | :heavy_check_mark:              | Fixed rate APR for loans.       |