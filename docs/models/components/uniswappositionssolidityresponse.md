# UniswapPositionsSolidityResponse

## Example Usage

```typescript
import { UniswapPositionsSolidityResponse } from "@compass-labs/api-sdk/models/components";

let value: UniswapPositionsSolidityResponse = {
  nonce: 340867,
  operator: "<value>",
  token0: "<value>",
  token1: "<value>",
  fee: 610272,
  tickLower: 486807,
  tickUpper: 197221,
  liquidity: 6921,
  feeGrowthInside0LastX128: 514327,
  feeGrowthInside1LastX128: 741996,
  tokensOwed0: 287261,
  tokensOwed1: 806792,
};
```

## Fields

| Field                      | Type                       | Required                   | Description                |
| -------------------------- | -------------------------- | -------------------------- | -------------------------- |
| `nonce`                    | *number*                   | :heavy_check_mark:         | N/A                        |
| `operator`                 | *string*                   | :heavy_check_mark:         | N/A                        |
| `token0`                   | *string*                   | :heavy_check_mark:         | N/A                        |
| `token1`                   | *string*                   | :heavy_check_mark:         | N/A                        |
| `fee`                      | *number*                   | :heavy_check_mark:         | N/A                        |
| `tickLower`                | *number*                   | :heavy_check_mark:         | N/A                        |
| `tickUpper`                | *number*                   | :heavy_check_mark:         | N/A                        |
| `liquidity`                | *number*                   | :heavy_check_mark:         | N/A                        |
| `feeGrowthInside0LastX128` | *number*                   | :heavy_check_mark:         | N/A                        |
| `feeGrowthInside1LastX128` | *number*                   | :heavy_check_mark:         | N/A                        |
| `tokensOwed0`              | *number*                   | :heavy_check_mark:         | N/A                        |
| `tokensOwed1`              | *number*                   | :heavy_check_mark:         | N/A                        |
| `lpTokenAddress`           | *string*                   | :heavy_minus_sign:         | N/A                        |