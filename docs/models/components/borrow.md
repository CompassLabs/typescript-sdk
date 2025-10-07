# Borrow

## Example Usage

```typescript
import { Borrow } from "@compass-labs/api-sdk/models/components";

let value: Borrow = {
  id: "<id>",
  timestamp: 132507,
  txHash: "<value>",
  amount: 5726.04,
  borrowRateMode: 1,
  reserve: {
    symbol: "<value>",
    name: "<value>",
    underlyingAsset: "0x68b3465833fb72A70ecDF485E0e4C7bD8665Fc45",
  },
  assetPriceUSD: 1903.46,
  block: 106046,
};
```

## Fields

| Field                                                                                                              | Type                                                                                                               | Required                                                                                                           | Description                                                                                                        | Example                                                                                                            |
| ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------ |
| `id`                                                                                                               | *string*                                                                                                           | :heavy_check_mark:                                                                                                 | The id of a historical transaction on aave                                                                         |                                                                                                                    |
| `timestamp`                                                                                                        | *number*                                                                                                           | :heavy_check_mark:                                                                                                 | Timestamp in unix time                                                                                             |                                                                                                                    |
| `txHash`                                                                                                           | *string*                                                                                                           | :heavy_check_mark:                                                                                                 | Transaction hash. You can paste these into the search bar on etherscan                                             |                                                                                                                    |
| `amount`                                                                                                           | *number*                                                                                                           | :heavy_check_mark:                                                                                                 | Quantity of token                                                                                                  |                                                                                                                    |
| `borrowRateMode`                                                                                                   | [components.Borrowratemode](../../models/components/borrowratemode.md)                                             | :heavy_check_mark:                                                                                                 | The interest rate mode to borrow: 1 represents stable interest rate mode. 2 represents variable interest rate mode | 1                                                                                                                  |
| `reserve`                                                                                                          | [components.Reserve](../../models/components/reserve.md)                                                           | :heavy_check_mark:                                                                                                 | N/A                                                                                                                |                                                                                                                    |
| `assetPriceUSD`                                                                                                    | *number*                                                                                                           | :heavy_check_mark:                                                                                                 | Price of token in USD                                                                                              |                                                                                                                    |
| `action`                                                                                                           | *string*                                                                                                           | :heavy_check_mark:                                                                                                 | The type of transaction                                                                                            |                                                                                                                    |
| `block`                                                                                                            | *number*                                                                                                           | :heavy_check_mark:                                                                                                 | N/A                                                                                                                |                                                                                                                    |