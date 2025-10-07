# MarketPosition

## Example Usage

```typescript
import { MarketPosition } from "@compass-labs/api-sdk/models/components";

let value: MarketPosition = {
  market: {
    uniqueKey: "<value>",
  },
  healthFactor: "<value>",
  priceVariationToLiquidationPrice: "<value>",
  state: {
    pnlUsd: "<value>",
    borrowAssets: "<value>",
    borrowShares: "<value>",
    borrowAssetsUsd: "<value>",
    collateral: "<value>",
    collateralUsd: "<value>",
    supplyAssets: "<value>",
    supplyShares: "<value>",
    supplyAssetsUsd: "<value>",
  },
};
```

## Fields

| Field                                                                                                                                                                                | Type                                                                                                                                                                                 | Required                                                                                                                                                                             | Description                                                                                                                                                                          |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `market`                                                                                                                                                                             | [components.Market](../../models/components/market.md)                                                                                                                               | :heavy_check_mark:                                                                                                                                                                   | N/A                                                                                                                                                                                  |
| `healthFactor`                                                                                                                                                                       | *string*                                                                                                                                                                             | :heavy_check_mark:                                                                                                                                                                   | N/A                                                                                                                                                                                  |
| `priceVariationToLiquidationPrice`                                                                                                                                                   | *string*                                                                                                                                                                             | :heavy_check_mark:                                                                                                                                                                   | N/A                                                                                                                                                                                  |
| `state`                                                                                                                                                                              | [components.CompassApiBackendModelsMorphoReadResponseCheckUserPositionMarketState](../../models/components/compassapibackendmodelsmorphoreadresponsecheckuserpositionmarketstate.md) | :heavy_check_mark:                                                                                                                                                                   | N/A                                                                                                                                                                                  |