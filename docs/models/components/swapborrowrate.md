# SwapBorrowRate

## Example Usage

```typescript
import { SwapBorrowRate } from "@compass-labs/api-sdk/models/components";

let value: SwapBorrowRate = {
  id: "<id>",
  timestamp: 661095,
  txHash: "<value>",
  borrowRateModeFrom: 740235,
  borrowRateModeTo: 239047,
  variableBorrowRate: 179223,
  stableBorrowRate: 225369,
  reserve: {
    symbol: "<value>",
    name: "<value>",
    underlyingAsset: "0x68b3465833fb72A70ecDF485E0e4C7bD8665Fc45",
  },
  block: 364832,
};
```

## Fields

| Field                                                                  | Type                                                                   | Required                                                               | Description                                                            |
| ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| `id`                                                                   | *string*                                                               | :heavy_check_mark:                                                     | The id of a historical transaction on aave                             |
| `timestamp`                                                            | *number*                                                               | :heavy_check_mark:                                                     | Timestamp in unix time                                                 |
| `txHash`                                                               | *string*                                                               | :heavy_check_mark:                                                     | Transaction hash. You can paste these into the search bar on etherscan |
| `borrowRateModeFrom`                                                   | *number*                                                               | :heavy_check_mark:                                                     | N/A                                                                    |
| `borrowRateModeTo`                                                     | *number*                                                               | :heavy_check_mark:                                                     | N/A                                                                    |
| `variableBorrowRate`                                                   | *number*                                                               | :heavy_check_mark:                                                     | N/A                                                                    |
| `stableBorrowRate`                                                     | *number*                                                               | :heavy_check_mark:                                                     | N/A                                                                    |
| `reserve`                                                              | [components.Reserve](../../models/components/reserve.md)               | :heavy_check_mark:                                                     | N/A                                                                    |
| `action`                                                               | *string*                                                               | :heavy_check_mark:                                                     | N/A                                                                    |
| `block`                                                                | *number*                                                               | :heavy_check_mark:                                                     | N/A                                                                    |