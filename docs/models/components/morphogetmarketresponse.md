# MorphoGetMarketResponse

## Example Usage

```typescript
import { MorphoGetMarketResponse } from "@compass-labs/api-sdk/models/components";

let value: MorphoGetMarketResponse = {
  whitelisted: false,
  lltv: "<value>",
  dailyApys: {
    borrowApy: "<value>",
    netBorrowApy: "<value>",
    netSupplyApy: "<value>",
    supplyApy: "<value>",
  },
  weeklyApys: {
    borrowApy: "<value>",
    netBorrowApy: "<value>",
    netSupplyApy: "<value>",
    supplyApy: "<value>",
  },
  monthlyApys: {
    borrowApy: "<value>",
    netBorrowApy: "<value>",
    netSupplyApy: "<value>",
    supplyApy: "<value>",
  },
  yearlyApys: {
    borrowApy: "<value>",
    netBorrowApy: "<value>",
    netSupplyApy: "<value>",
    supplyApy: "<value>",
  },
  allTimeApys: {
    borrowApy: "<value>",
    netBorrowApy: "<value>",
    netSupplyApy: "<value>",
    supplyApy: "<value>",
  },
  collateralAsset: {
    address: "4769 E Washington Street",
    symbol: "<value>",
    name: "<value>",
    decimals: 652972,
    priceUsd: "<value>",
    logoURI: "https://speedy-marksman.com",
  },
  loanAsset: {
    address: "820 Heloise Valleys",
    symbol: "<value>",
    name: "<value>",
    decimals: 419252,
    priceUsd: "<value>",
    logoURI: "https://phony-pacemaker.name/",
  },
  state: {
    utilization: "<value>",
    borrowAssets: "<value>",
    liquidityAssets: "<value>",
    totalLiquidity: "<value>",
  },
};
```

## Fields

| Field                                                                                                                                                                | Type                                                                                                                                                                 | Required                                                                                                                                                             | Description                                                                                                                                                          |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `whitelisted`                                                                                                                                                        | *boolean*                                                                                                                                                            | :heavy_check_mark:                                                                                                                                                   | Whether the market is whitelisted or not.                                                                                                                            |
| `lltv`                                                                                                                                                               | *string*                                                                                                                                                             | :heavy_check_mark:                                                                                                                                                   | (Liquidation Loan-To-Value) Maximum borrowing percentage before liquidation risk. Scaled by 1e18.                                                                    |
| `dailyApys`                                                                                                                                                          | [components.CompassApiBackendModelsMorphoReadResponseGetMarketApyData](../../models/components/compassapibackendmodelsmorphoreadresponsegetmarketapydata.md)         | :heavy_check_mark:                                                                                                                                                   | N/A                                                                                                                                                                  |
| `weeklyApys`                                                                                                                                                         | [components.CompassApiBackendModelsMorphoReadResponseGetMarketApyData](../../models/components/compassapibackendmodelsmorphoreadresponsegetmarketapydata.md)         | :heavy_check_mark:                                                                                                                                                   | N/A                                                                                                                                                                  |
| `monthlyApys`                                                                                                                                                        | [components.CompassApiBackendModelsMorphoReadResponseGetMarketApyData](../../models/components/compassapibackendmodelsmorphoreadresponsegetmarketapydata.md)         | :heavy_check_mark:                                                                                                                                                   | N/A                                                                                                                                                                  |
| `yearlyApys`                                                                                                                                                         | [components.CompassApiBackendModelsMorphoReadResponseGetMarketApyData](../../models/components/compassapibackendmodelsmorphoreadresponsegetmarketapydata.md)         | :heavy_check_mark:                                                                                                                                                   | N/A                                                                                                                                                                  |
| `allTimeApys`                                                                                                                                                        | [components.CompassApiBackendModelsMorphoReadResponseGetMarketApyData](../../models/components/compassapibackendmodelsmorphoreadresponsegetmarketapydata.md)         | :heavy_check_mark:                                                                                                                                                   | N/A                                                                                                                                                                  |
| `collateralAsset`                                                                                                                                                    | [components.CompassApiBackendModelsMorphoReadResponseGetMarketAsset](../../models/components/compassapibackendmodelsmorphoreadresponsegetmarketasset.md)             | :heavy_check_mark:                                                                                                                                                   | N/A                                                                                                                                                                  |
| `loanAsset`                                                                                                                                                          | [components.CompassApiBackendModelsMorphoReadResponseGetMarketAsset](../../models/components/compassapibackendmodelsmorphoreadresponsegetmarketasset.md)             | :heavy_check_mark:                                                                                                                                                   | N/A                                                                                                                                                                  |
| `state`                                                                                                                                                              | [components.CompassApiBackendModelsMorphoReadResponseGetMarketMarketState](../../models/components/compassapibackendmodelsmorphoreadresponsegetmarketmarketstate.md) | :heavy_check_mark:                                                                                                                                                   | N/A                                                                                                                                                                  |