# PendleListMarketsResponse

## Example Usage

```typescript
import { PendleListMarketsResponse } from "@compass-labs/api-sdk/models/components";

let value: PendleListMarketsResponse = {
  markets: [
    {
      name: "<value>",
      address: "9178 Rebeca Burgs",
      expiry: new Date("2025-11-13T22:39:31.641Z"),
      pt: "<value>",
      yt: "<value>",
      sy: "<value>",
      underlyingAsset: "<value>",
      details: {
        liquidity: 9561.51,
        pendleApy: 7290.83,
        impliedApy: 7531.51,
        feeRate: 2012.82,
        yieldRange: {
          min: 6331.68,
          max: 8582.82,
        },
        aggregatedApy: 6268.28,
        maxBoostedApy: 9202.72,
      },
      isNew: true,
      isPrime: false,
      timestamp: new Date("2024-03-28T12:44:40.088Z"),
    },
  ],
};
```

## Fields

| Field                                                                | Type                                                                 | Required                                                             | Description                                                          |
| -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- |
| `markets`                                                            | [components.PendleMarket](../../models/components/pendlemarket.md)[] | :heavy_check_mark:                                                   | A list of active markets on the inputted chain.                      |