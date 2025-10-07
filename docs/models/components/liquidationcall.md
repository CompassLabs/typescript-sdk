# LiquidationCall

## Example Usage

```typescript
import { LiquidationCall } from "@compass-labs/api-sdk/models/components";

let value: LiquidationCall = {
  id: "<id>",
  timestamp: 906796,
  txHash: "<value>",
  collateralAmount: 3903,
  collateralReserve: {
    symbol: "<value>",
    name: "<value>",
    underlyingAsset: "0x68b3465833fb72A70ecDF485E0e4C7bD8665Fc45",
  },
  principalAmount: 1013.27,
  principalReserve: {
    symbol: "<value>",
    name: "<value>",
    underlyingAsset: "0x68b3465833fb72A70ecDF485E0e4C7bD8665Fc45",
  },
  collateralAssetPriceUSD: 1927.57,
  borrowAssetPriceUSD: 3105.83,
  block: 548176,
};
```

## Fields

| Field                                                                  | Type                                                                   | Required                                                               | Description                                                            |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `id`                                                                   | *string*                                                               | :heavy_check_mark:                                                     | The id of a historical transaction on aave                             |
| `timestamp`                                                            | *number*                                                               | :heavy_check_mark:                                                     | Timestamp in unix time                                                 |
| `txHash`                                                               | *string*                                                               | :heavy_check_mark:                                                     | Transaction hash. You can paste these into the search bar on etherscan |
| `collateralAmount`                                                     | *number*                                                               | :heavy_check_mark:                                                     | N/A                                                                    |
| `collateralReserve`                                                    | [components.Reserve](../../models/components/reserve.md)               | :heavy_check_mark:                                                     | N/A                                                                    |
| `principalAmount`                                                      | *number*                                                               | :heavy_check_mark:                                                     | N/A                                                                    |
| `principalReserve`                                                     | [components.Reserve](../../models/components/reserve.md)               | :heavy_check_mark:                                                     | N/A                                                                    |
| `collateralAssetPriceUSD`                                              | *number*                                                               | :heavy_check_mark:                                                     | N/A                                                                    |
| `borrowAssetPriceUSD`                                                  | *number*                                                               | :heavy_check_mark:                                                     | N/A                                                                    |
| `action`                                                               | *string*                                                               | :heavy_check_mark:                                                     | N/A                                                                    |
| `block`                                                                | *number*                                                               | :heavy_check_mark:                                                     | N/A                                                                    |