# CompassApiBackendModelsGenericReadResponsePortfolioTokenBalance

## Example Usage

```typescript
import { CompassApiBackendModelsGenericReadResponsePortfolioTokenBalance } from "@compass-labs/api-sdk/models/components";

let value: CompassApiBackendModelsGenericReadResponsePortfolioTokenBalance = {
  amount: "1.5",
  decimals: 18,
  tokenSymbol: "WETH",
  tokenAddress: "0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2",
  price: "2000",
  tokenValueInUsd: "2000",
};
```

## Fields

| Field                                       | Type                                        | Required                                    | Description                                 | Example                                     |
| ------------------------------------------- | ------------------------------------------- | ------------------------------------------- | ------------------------------------------- | ------------------------------------------- |
| `amount`                                    | *string*                                    | :heavy_check_mark:                          | Amount of tokens a particular address holds | 1.5                                         |
| `decimals`                                  | *number*                                    | :heavy_check_mark:                          | Number of decimals of the token             | 18                                          |
| `tokenSymbol`                               | *string*                                    | :heavy_check_mark:                          | Symbol of the token.                        | WETH                                        |
| `tokenAddress`                              | *string*                                    | :heavy_check_mark:                          | Address of the token                        | 0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2  |
| `price`                                     | *string*                                    | :heavy_check_mark:                          | Price of the token in USD                   | 2000                                        |
| `tokenValueInUsd`                           | *string*                                    | :heavy_check_mark:                          | Value of the token balance in USD           | 2000                                        |