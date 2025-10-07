# TokenBalanceResponse

Response model for token balance information.

## Example Usage

```typescript
import { TokenBalanceResponse } from "@compass-labs/api-sdk/models/components";

let value: TokenBalanceResponse = {
  amount: "1.5",
  decimals: 18,
  tokenSymbol: "<value>",
  tokenAddress: "0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2",
};
```

## Fields

| Field                                       | Type                                        | Required                                    | Description                                 | Example                                     |
| ------------------------------------------- | ------------------------------------------- | ------------------------------------------- | ------------------------------------------- | ------------------------------------------- |
| `amount`                                    | *string*                                    | :heavy_check_mark:                          | Amount of tokens a particular address holds | 1.5                                         |
| `decimals`                                  | *number*                                    | :heavy_check_mark:                          | Number of decimals of the token             | 18                                          |
| `tokenSymbol`                               | *string*                                    | :heavy_check_mark:                          | Symbol of the token                         |                                             |
| `tokenAddress`                              | *string*                                    | :heavy_check_mark:                          | Address of the token                        | 0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2  |