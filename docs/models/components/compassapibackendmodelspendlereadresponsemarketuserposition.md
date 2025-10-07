# CompassApiBackendModelsPendleReadResponseMarketUserPosition

## Example Usage

```typescript
import { CompassApiBackendModelsPendleReadResponseMarketUserPosition } from "@compass-labs/api-sdk/models/components";

let value: CompassApiBackendModelsPendleReadResponseMarketUserPosition = {
  claimableYield: "<value>",
  syBalance: "<value>",
  ptBalance: "<value>",
  ytBalance: "<value>",
  lpBalance: "<value>",
  underlyingTokenBalance: "<value>",
};
```

## Fields

| Field                                                            | Type                                                             | Required                                                         | Description                                                      |
| ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- |
| `claimableYield`                                                 | *string*                                                         | :heavy_check_mark:                                               | The amount of yield that can be claimed in the underlying token. |
| `syBalance`                                                      | *string*                                                         | :heavy_check_mark:                                               | The amount of SY tokens the user currently holds.                |
| `ptBalance`                                                      | *string*                                                         | :heavy_check_mark:                                               | The amount of PT tokens the user currently holds.                |
| `ytBalance`                                                      | *string*                                                         | :heavy_check_mark:                                               | The amount of YT tokens the user currently holds.                |
| `lpBalance`                                                      | *string*                                                         | :heavy_check_mark:                                               | The amount of LP tokens the user currently holds.                |
| `underlyingTokenBalance`                                         | *string*                                                         | :heavy_check_mark:                                               | The amount of underlying tokens the user currently holds.        |
| `accountingAssetBalance`                                         | *string*                                                         | :heavy_minus_sign:                                               | The amount of accounting assets the user currently holds.        |