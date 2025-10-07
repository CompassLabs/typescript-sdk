# Vault

## Example Usage

```typescript
import { Vault } from "@compass-labs/api-sdk/models/components";

let value: Vault = {
  address: "777 Legros Union",
  name: "<value>",
  symbol: "<value>",
  whitelisted: false,
  asset: {
    name: "<value>",
    symbol: "<value>",
    address: "2332 Kling Dam",
    decimals: 805213,
    priceUsd: "<value>",
    logoURI: "https://shrill-precedent.info",
  },
  dailyApys: {
    apy: "<value>",
    netApy: "<value>",
  },
  weeklyApys: {
    apy: "<value>",
    netApy: "<value>",
  },
  monthlyApys: {
    apy: "<value>",
    netApy: "<value>",
  },
};
```

## Fields

| Field                                                                                                                                                                        | Type                                                                                                                                                                         | Required                                                                                                                                                                     | Description                                                                                                                                                                  |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `address`                                                                                                                                                                    | *string*                                                                                                                                                                     | :heavy_check_mark:                                                                                                                                                           | N/A                                                                                                                                                                          |
| `name`                                                                                                                                                                       | *string*                                                                                                                                                                     | :heavy_check_mark:                                                                                                                                                           | N/A                                                                                                                                                                          |
| `symbol`                                                                                                                                                                     | *string*                                                                                                                                                                     | :heavy_check_mark:                                                                                                                                                           | N/A                                                                                                                                                                          |
| `whitelisted`                                                                                                                                                                | *boolean*                                                                                                                                                                    | :heavy_check_mark:                                                                                                                                                           | N/A                                                                                                                                                                          |
| `asset`                                                                                                                                                                      | [components.CompassApiBackendModelsMorphoReadResponseCheckUserPositionAsset](../../models/components/compassapibackendmodelsmorphoreadresponsecheckuserpositionasset.md)     | :heavy_check_mark:                                                                                                                                                           | N/A                                                                                                                                                                          |
| `dailyApys`                                                                                                                                                                  | [components.CompassApiBackendModelsMorphoReadResponseCheckUserPositionApyData](../../models/components/compassapibackendmodelsmorphoreadresponsecheckuserpositionapydata.md) | :heavy_check_mark:                                                                                                                                                           | N/A                                                                                                                                                                          |
| `weeklyApys`                                                                                                                                                                 | [components.CompassApiBackendModelsMorphoReadResponseCheckUserPositionApyData](../../models/components/compassapibackendmodelsmorphoreadresponsecheckuserpositionapydata.md) | :heavy_check_mark:                                                                                                                                                           | N/A                                                                                                                                                                          |
| `monthlyApys`                                                                                                                                                                | [components.CompassApiBackendModelsMorphoReadResponseCheckUserPositionApyData](../../models/components/compassapibackendmodelsmorphoreadresponsecheckuserpositionapydata.md) | :heavy_check_mark:                                                                                                                                                           | N/A                                                                                                                                                                          |