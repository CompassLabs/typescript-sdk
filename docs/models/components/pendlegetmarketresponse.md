# PendleGetMarketResponse

## Example Usage

```typescript
import { PendleGetMarketResponse } from "@compass-labs/api-sdk/models/components";

let value: PendleGetMarketResponse = {
  marketAddress: "<value>",
  impliedApy: "<value>",
  maturityDate: new Date("2023-10-18T22:09:52.103Z"),
  tokens: {
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
  },
};
```

## Fields

| Field                                                                                                                                                            | Type                                                                                                                                                             | Required                                                                                                                                                         | Description                                                                                                                                                      |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `marketAddress`                                                                                                                                                  | *string*                                                                                                                                                         | :heavy_check_mark:                                                                                                                                               | The address of the market.                                                                                                                                       |
| `impliedApy`                                                                                                                                                     | *string*                                                                                                                                                         | :heavy_check_mark:                                                                                                                                               | The implied APY of the market.                                                                                                                                   |
| `maturityDate`                                                                                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)                                                                    | :heavy_check_mark:                                                                                                                                               | The maturity date of the market. ISO 8601 format. UTC timezone.                                                                                                  |
| `tokens`                                                                                                                                                         | [components.MarketTokens](../../models/components/markettokens.md)                                                                                               | :heavy_check_mark:                                                                                                                                               | N/A                                                                                                                                                              |
| `userPosition`                                                                                                                                                   | [components.CompassApiBackendModelsPendleReadResponseMarketUserPosition](../../models/components/compassapibackendmodelspendlereadresponsemarketuserposition.md) | :heavy_minus_sign:                                                                                                                                               | The user's position in the market.                                                                                                                               |