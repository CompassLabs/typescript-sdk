# Portfolio

## Example Usage

```typescript
import { Portfolio } from "@compass-labs/api-sdk/models/components";

let value: Portfolio = {
  totalValueInUsd: "10000",
  tokenBalances: [
    {
      amount: "1.5",
      decimals: 18,
      tokenSymbol: "WETH",
      tokenAddress: "0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2",
      price: "2000",
      tokenValueInUsd: "2000",
    },
  ],
};
```

## Fields

| Field                                                                                                                                                                      | Type                                                                                                                                                                       | Required                                                                                                                                                                   | Description                                                                                                                                                                | Example                                                                                                                                                                    |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `totalValueInUsd`                                                                                                                                                          | *string*                                                                                                                                                                   | :heavy_check_mark:                                                                                                                                                         | Total value of the portfolio in USD                                                                                                                                        | 10000                                                                                                                                                                      |
| `tokenBalances`                                                                                                                                                            | [components.CompassApiBackendModelsGenericReadResponsePortfolioTokenBalance](../../models/components/compassapibackendmodelsgenericreadresponseportfoliotokenbalance.md)[] | :heavy_check_mark:                                                                                                                                                         | List of token balances in the portfolio                                                                                                                                    |                                                                                                                                                                            |