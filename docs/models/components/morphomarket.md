# MorphoMarket

## Example Usage

```typescript
import { MorphoMarket } from "@compass-labs/api-sdk/models/components";

let value: MorphoMarket = {
  uniqueKey: "<value>",
  lltv: 437233,
  oracleAddress: "<value>",
  irmAddress: "<value>",
  state: {
    borrowApy: 9490.74,
    borrowAssets: 879113,
    borrowAssetsUsd: 7585.8,
    supplyApy: 5403.78,
    supplyAssets: 483616,
    supplyAssetsUsd: 1301.15,
    fee: 3764.6,
    utilization: 2497.26,
  },
  weeklyApys: {
    supplyApy: 6781.33,
    netSupplyApy: 6272.25,
    borrowApy: 2605.74,
    netBorrowApy: 8043.69,
  },
  collateralAsset: {
    address: "41621 Harvey View",
    symbol: "<value>",
    name: "<value>",
    decimals: 945019,
  },
  loanAsset: {
    address: "5307 Turner Overpass",
    symbol: "<value>",
    name: "<value>",
    decimals: 824725,
  },
};
```

## Fields

| Field                                                                                                                                                                  | Type                                                                                                                                                                   | Required                                                                                                                                                               | Description                                                                                                                                                            |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `uniqueKey`                                                                                                                                                            | *string*                                                                                                                                                               | :heavy_check_mark:                                                                                                                                                     | N/A                                                                                                                                                                    |
| `lltv`                                                                                                                                                                 | *number*                                                                                                                                                               | :heavy_check_mark:                                                                                                                                                     | N/A                                                                                                                                                                    |
| `oracleAddress`                                                                                                                                                        | *string*                                                                                                                                                               | :heavy_check_mark:                                                                                                                                                     | N/A                                                                                                                                                                    |
| `irmAddress`                                                                                                                                                           | *string*                                                                                                                                                               | :heavy_check_mark:                                                                                                                                                     | N/A                                                                                                                                                                    |
| `state`                                                                                                                                                                | [components.CompassApiBackendModelsMorphoReadResponseGetMarketsMarketState](../../models/components/compassapibackendmodelsmorphoreadresponsegetmarketsmarketstate.md) | :heavy_check_mark:                                                                                                                                                     | N/A                                                                                                                                                                    |
| `weeklyApys`                                                                                                                                                           | [components.WeeklyApys](../../models/components/weeklyapys.md)                                                                                                         | :heavy_check_mark:                                                                                                                                                     | N/A                                                                                                                                                                    |
| `collateralAsset`                                                                                                                                                      | [components.CompassApiBackendModelsMorphoReadResponseGetMarketsAsset](../../models/components/compassapibackendmodelsmorphoreadresponsegetmarketsasset.md)             | :heavy_check_mark:                                                                                                                                                     | N/A                                                                                                                                                                    |
| `loanAsset`                                                                                                                                                            | [components.CompassApiBackendModelsMorphoReadResponseGetMarketsAsset](../../models/components/compassapibackendmodelsmorphoreadresponsegetmarketsasset.md)             | :heavy_check_mark:                                                                                                                                                     | N/A                                                                                                                                                                    |