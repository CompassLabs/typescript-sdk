# Repay

## Example Usage

```typescript
import { Repay } from "@compass-labs/api-sdk/models/components";

let value: Repay = {
  id: "<id>",
  timestamp: 529023,
  txHash: "<value>",
  amount: 9272.21,
  reserve: {
    symbol: "<value>",
    name: "<value>",
    underlyingAsset: "0x68b3465833fb72A70ecDF485E0e4C7bD8665Fc45",
  },
  assetPriceUSD: 3951.28,
  block: 361702,
};
```

## Fields

| Field                                                                  | Type                                                                   | Required                                                               | Description                                                            |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `id`                                                                   | *string*                                                               | :heavy_check_mark:                                                     | The id of a historical transaction on aave                             |
| `timestamp`                                                            | *number*                                                               | :heavy_check_mark:                                                     | Timestamp in unix time                                                 |
| `txHash`                                                               | *string*                                                               | :heavy_check_mark:                                                     | Transaction hash. You can paste these into the search bar on etherscan |
| `amount`                                                               | *number*                                                               | :heavy_check_mark:                                                     | Quantity of token                                                      |
| `reserve`                                                              | [components.Reserve](../../models/components/reserve.md)               | :heavy_check_mark:                                                     | N/A                                                                    |
| `assetPriceUSD`                                                        | *number*                                                               | :heavy_check_mark:                                                     | N/A                                                                    |
| `action`                                                               | *string*                                                               | :heavy_check_mark:                                                     | The type of transaction                                                |
| `block`                                                                | *number*                                                               | :heavy_check_mark:                                                     | N/A                                                                    |