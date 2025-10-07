# MorphoVault

## Example Usage

```typescript
import { MorphoVault } from "@compass-labs/api-sdk/models/components";

let value: MorphoVault = {
  address: "5723 E 11th Street",
  symbol: "<value>",
  name: "<value>",
  creationBlockNumber: 34892,
  creationTimestamp: 184536,
  creatorAddress: "<value>",
  whitelisted: true,
  asset: {
    symbol: "<value>",
    address: "662 Gerhold Grove",
    decimals: 902243,
    chain: {
      id: 111446,
    },
  },
  chain: {
    id: 111446,
  },
  state: {
    id: "<id>",
    apy: 7130.98,
    netApy: 5519.29,
    totalAssets: 436664,
    fee: 5855.77,
    timelock: 334586,
  },
};
```

## Fields

| Field                                                                                                                                                              | Type                                                                                                                                                               | Required                                                                                                                                                           | Description                                                                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `address`                                                                                                                                                          | *string*                                                                                                                                                           | :heavy_check_mark:                                                                                                                                                 | N/A                                                                                                                                                                |
| `symbol`                                                                                                                                                           | *string*                                                                                                                                                           | :heavy_check_mark:                                                                                                                                                 | N/A                                                                                                                                                                |
| `name`                                                                                                                                                             | *string*                                                                                                                                                           | :heavy_check_mark:                                                                                                                                                 | N/A                                                                                                                                                                |
| `creationBlockNumber`                                                                                                                                              | *number*                                                                                                                                                           | :heavy_check_mark:                                                                                                                                                 | N/A                                                                                                                                                                |
| `creationTimestamp`                                                                                                                                                | *number*                                                                                                                                                           | :heavy_check_mark:                                                                                                                                                 | N/A                                                                                                                                                                |
| `creatorAddress`                                                                                                                                                   | *string*                                                                                                                                                           | :heavy_check_mark:                                                                                                                                                 | N/A                                                                                                                                                                |
| `whitelisted`                                                                                                                                                      | *boolean*                                                                                                                                                          | :heavy_check_mark:                                                                                                                                                 | N/A                                                                                                                                                                |
| `asset`                                                                                                                                                            | [components.CompassApiBackendModelsMorphoReadResponseGetVaultsAsset](../../models/components/compassapibackendmodelsmorphoreadresponsegetvaultsasset.md)           | :heavy_check_mark:                                                                                                                                                 | N/A                                                                                                                                                                |
| `chain`                                                                                                                                                            | [components.ChainInfo](../../models/components/chaininfo.md)                                                                                                       | :heavy_check_mark:                                                                                                                                                 | N/A                                                                                                                                                                |
| `state`                                                                                                                                                            | [components.CompassApiBackendModelsMorphoReadResponseGetVaultsVaultState](../../models/components/compassapibackendmodelsmorphoreadresponsegetvaultsvaultstate.md) | :heavy_check_mark:                                                                                                                                                 | N/A                                                                                                                                                                |