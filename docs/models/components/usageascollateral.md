# UsageAsCollateral

## Example Usage

```typescript
import { UsageAsCollateral } from "@compass-labs/api-sdk/models/components";

let value: UsageAsCollateral = {
  id: "<id>",
  timestamp: 393669,
  txHash: "<value>",
  fromState: false,
  toState: false,
  reserve: {
    symbol: "<value>",
    name: "<value>",
    underlyingAsset: "0x68b3465833fb72A70ecDF485E0e4C7bD8665Fc45",
  },
  block: 936532,
};
```

## Fields

| Field                                                                  | Type                                                                   | Required                                                               | Description                                                            |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `id`                                                                   | *string*                                                               | :heavy_check_mark:                                                     | The id of a historical transaction on aave                             |
| `timestamp`                                                            | *number*                                                               | :heavy_check_mark:                                                     | Timestamp in unix time                                                 |
| `txHash`                                                               | *string*                                                               | :heavy_check_mark:                                                     | Transaction hash. You can paste these into the search bar on etherscan |
| `fromState`                                                            | *boolean*                                                              | :heavy_check_mark:                                                     | N/A                                                                    |
| `toState`                                                              | *boolean*                                                              | :heavy_check_mark:                                                     | N/A                                                                    |
| `reserve`                                                              | [components.Reserve](../../models/components/reserve.md)               | :heavy_check_mark:                                                     | N/A                                                                    |
| `action`                                                               | *string*                                                               | :heavy_check_mark:                                                     | The type of transaction                                                |
| `block`                                                                | *number*                                                               | :heavy_check_mark:                                                     | N/A                                                                    |