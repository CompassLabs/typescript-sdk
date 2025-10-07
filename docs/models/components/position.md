# Position

## Example Usage

```typescript
import { Position } from "@compass-labs/api-sdk/models/components";

let value: Position = {
  chainId: 24101,
  totalOpen: 928910,
  totalClosed: 126791,
  totalSy: 622814,
  openPositions: [
    {
      marketId: "<id>",
      pt: {
        valuation: 6423.15,
        balance: "<value>",
      },
      yt: {
        valuation: 1467.38,
        balance: "<value>",
      },
      lp: {
        valuation: 6276.74,
        balance: "<value>",
        activeBalance: "<value>",
      },
    },
  ],
  closedPositions: [
    {
      marketId: "<id>",
      pt: {
        valuation: 6423.15,
        balance: "<value>",
      },
      yt: {
        valuation: 1467.38,
        balance: "<value>",
      },
      lp: {
        valuation: 6276.74,
        balance: "<value>",
        activeBalance: "<value>",
      },
    },
  ],
  syPositions: [
    {
      syId: "<id>",
      balance: "<value>",
    },
  ],
  updatedAt: new Date("2024-12-17T04:58:12.701Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `chainId`                                                                                     | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `totalOpen`                                                                                   | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `totalClosed`                                                                                 | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `totalSy`                                                                                     | *number*                                                                                      | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `openPositions`                                                                               | [components.OpenPosition](../../models/components/openposition.md)[]                          | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `closedPositions`                                                                             | [components.OpenPosition](../../models/components/openposition.md)[]                          | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `syPositions`                                                                                 | [components.SyPosition](../../models/components/syposition.md)[]                              | :heavy_check_mark:                                                                            | N/A                                                                                           |
| `updatedAt`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | N/A                                                                                           |