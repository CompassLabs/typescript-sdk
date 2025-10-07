# Details

## Example Usage

```typescript
import { Details } from "@compass-labs/api-sdk/models/components";

let value: Details = {
  liquidity: 4182.98,
  pendleApy: 2079.32,
  impliedApy: 122.5,
  feeRate: 7216.92,
  yieldRange: {
    min: 6331.68,
    max: 8582.82,
  },
  aggregatedApy: 821.33,
  maxBoostedApy: 3012.82,
};
```

## Fields

| Field                                                                        | Type                                                                         | Required                                                                     | Description                                                                  |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| `liquidity`                                                                  | *number*                                                                     | :heavy_check_mark:                                                           | N/A                                                                          |
| `pendleApy`                                                                  | *number*                                                                     | :heavy_check_mark:                                                           | N/A                                                                          |
| `impliedApy`                                                                 | *number*                                                                     | :heavy_check_mark:                                                           | N/A                                                                          |
| `feeRate`                                                                    | *number*                                                                     | :heavy_check_mark:                                                           | N/A                                                                          |
| `movement10Percent`                                                          | [components.Movement10Percent](../../models/components/movement10percent.md) | :heavy_minus_sign:                                                           | N/A                                                                          |
| `yieldRange`                                                                 | [components.YieldRange](../../models/components/yieldrange.md)               | :heavy_check_mark:                                                           | N/A                                                                          |
| `aggregatedApy`                                                              | *number*                                                                     | :heavy_check_mark:                                                           | N/A                                                                          |
| `maxBoostedApy`                                                              | *number*                                                                     | :heavy_check_mark:                                                           | N/A                                                                          |