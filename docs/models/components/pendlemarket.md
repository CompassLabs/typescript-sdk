# PendleMarket

## Example Usage

```typescript
import { PendleMarket } from "@compass-labs/api-sdk/models/components";

let value: PendleMarket = {
  name: "<value>",
  address: "22458 Abshire Plains",
  expiry: new Date("2023-04-18T01:20:41.264Z"),
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
  timestamp: new Date("2025-09-13T17:20:16.991Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `name`                                                                                        | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `address`                                                                                     | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `expiry`                                                                                      | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `pt`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `yt`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `sy`                                                                                          | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `underlyingAsset`                                                                             | *string*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `details`                                                                                     | [components.Details](../../models/components/details.md)                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `isNew`                                                                                       | *boolean*                                                                                     | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `isPrime`                                                                                     | *boolean*                                                                                     | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `timestamp`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |