# PendleListUserPositionsResponse

## Example Usage

```typescript
import { PendleListUserPositionsResponse } from "@compass-labs/api-sdk/models/components";

let value: PendleListUserPositionsResponse = {
  positions: [
    {
      chainId: 211076,
      totalOpen: 614836,
      totalClosed: 518056,
      totalSy: 794888,
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
      updatedAt: new Date("2024-03-19T22:46:00.938Z"),
    },
  ],
};
```

## Fields

| Field                                                        | Type                                                         | Required                                                     | Description                                                  |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| `positions`                                                  | [components.Position](../../models/components/position.md)[] | :heavy_check_mark:                                           | A list of the user's positions on the given chain.           |