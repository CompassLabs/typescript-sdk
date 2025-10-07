# VaultPosition

## Example Usage

```typescript
import { VaultPosition } from "@compass-labs/api-sdk/models/components";

let value: VaultPosition = {
  id: "<id>",
  state: {
    pnlUsd: "<value>",
    assets: "<value>",
    assetsUsd: "<value>",
    shares: "<value>",
  },
  vault: {
    address: "66665 Hessel Villages",
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
  },
};
```

## Fields

| Field                                                                                                                                                                              | Type                                                                                                                                                                               | Required                                                                                                                                                                           | Description                                                                                                                                                                        |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `id`                                                                                                                                                                               | *string*                                                                                                                                                                           | :heavy_check_mark:                                                                                                                                                                 | N/A                                                                                                                                                                                |
| `state`                                                                                                                                                                            | [components.CompassApiBackendModelsMorphoReadResponseCheckUserPositionVaultState](../../models/components/compassapibackendmodelsmorphoreadresponsecheckuserpositionvaultstate.md) | :heavy_check_mark:                                                                                                                                                                 | N/A                                                                                                                                                                                |
| `vault`                                                                                                                                                                            | [components.Vault](../../models/components/vault.md)                                                                                                                               | :heavy_check_mark:                                                                                                                                                                 | N/A                                                                                                                                                                                |