# OpenPosition

## Example Usage

```typescript
import { OpenPosition } from "@compass-labs/api-sdk/models/components";

let value: OpenPosition = {
  marketId: "<id>",
  pt: {
    valuation: 6423.15,
    balance: "<value>",
  },
  yt: {
    valuation: 1467.38,
    balance: "<value>",
  },
  lp: {
    valuation: 6276.74,
    balance: "<value>",
    activeBalance: "<value>",
  },
};
```

## Fields

| Field                                                                                                                                                                  | Type                                                                                                                                                                   | Required                                                                                                                                                               | Description                                                                                                                                                            |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `marketId`                                                                                                                                                             | *string*                                                                                                                                                               | :heavy_check_mark:                                                                                                                                                     | N/A                                                                                                                                                                    |
| `pt`                                                                                                                                                                   | [components.CompassApiBackendModelsPendleReadResponsePositionsTokenBalance](../../models/components/compassapibackendmodelspendlereadresponsepositionstokenbalance.md) | :heavy_check_mark:                                                                                                                                                     | N/A                                                                                                                                                                    |
| `yt`                                                                                                                                                                   | [components.CompassApiBackendModelsPendleReadResponsePositionsTokenBalance](../../models/components/compassapibackendmodelspendlereadresponsepositionstokenbalance.md) | :heavy_check_mark:                                                                                                                                                     | N/A                                                                                                                                                                    |
| `lp`                                                                                                                                                                   | [components.LpBalance](../../models/components/lpbalance.md)                                                                                                           | :heavy_check_mark:                                                                                                                                                     | N/A                                                                                                                                                                    |