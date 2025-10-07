# MarketTokens

## Example Usage

```typescript
import { MarketTokens } from "@compass-labs/api-sdk/models/components";

let value: MarketTokens = {
  underlyingToken: {
    address: "46793 Schneider Mount",
    symbol: "<value>",
    name: "<value>",
    decimals: 348593,
  },
  sy: {
    address: "15508 Walnut Close",
    symbol: "<value>",
    name: "<value>",
    decimals: 149197,
  },
  pt: {
    address: "7177 Kirlin Motorway",
    symbol: "<value>",
    name: "<value>",
    decimals: 845477,
  },
  yt: {
    address: "8060 Reilly Underpass",
    symbol: "<value>",
    name: "<value>",
    decimals: 36127,
  },
  accountingAsset: {
    address: "191 Kling Lights",
    symbol: "<value>",
    name: "<value>",
    decimals: 507596,
  },
};
```

## Fields

| Field                                                        | Type                                                         | Required                                                     | Description                                                  |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| `underlyingToken`                                            | [components.Erc20Data](../../models/components/erc20data.md) | :heavy_check_mark:                                           | N/A                                                          |
| `sy`                                                         | [components.Erc20Data](../../models/components/erc20data.md) | :heavy_check_mark:                                           | N/A                                                          |
| `pt`                                                         | [components.Erc20Data](../../models/components/erc20data.md) | :heavy_check_mark:                                           | N/A                                                          |
| `yt`                                                         | [components.Erc20Data](../../models/components/erc20data.md) | :heavy_check_mark:                                           | N/A                                                          |
| `accountingAsset`                                            | [components.Erc20Data](../../models/components/erc20data.md) | :heavy_check_mark:                                           | N/A                                                          |