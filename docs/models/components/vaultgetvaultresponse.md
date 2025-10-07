# VaultGetVaultResponse

## Example Usage

```typescript
import { VaultGetVaultResponse } from "@compass-labs/api-sdk/models/components";

let value: VaultGetVaultResponse = {
  name: "<value>",
  symbol: "<value>",
  decimals: 345654,
  totalAssets: "<value>",
  totalSupply: "<value>",
  sharePrice: "<value>",
  underlyingToken: {
    address: "90228 Bosco Shoals",
    name: "<value>",
    symbol: "<value>",
    decimals: 84128,
  },
  apy: {
    current: "<value>",
    apy1Day: "<value>",
    apy7Day: "<value>",
    apy30Day: "<value>",
  },
};
```

## Fields

| Field                                                                                                                                                          | Type                                                                                                                                                           | Required                                                                                                                                                       | Description                                                                                                                                                    |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `name`                                                                                                                                                         | *string*                                                                                                                                                       | :heavy_check_mark:                                                                                                                                             | Name of the vault.                                                                                                                                             |
| `symbol`                                                                                                                                                       | *string*                                                                                                                                                       | :heavy_check_mark:                                                                                                                                             | Symbol of the vault.                                                                                                                                           |
| `decimals`                                                                                                                                                     | *number*                                                                                                                                                       | :heavy_check_mark:                                                                                                                                             | Number of decimals used for the vault's share precision.                                                                                                       |
| `totalAssets`                                                                                                                                                  | *string*                                                                                                                                                       | :heavy_check_mark:                                                                                                                                             | Total amount of assets deposited in the vault.                                                                                                                 |
| `totalSupply`                                                                                                                                                  | *string*                                                                                                                                                       | :heavy_check_mark:                                                                                                                                             | Total amount of shares issued from the vault.                                                                                                                  |
| `sharePrice`                                                                                                                                                   | *string*                                                                                                                                                       | :heavy_check_mark:                                                                                                                                             | The price of one vault share in terms of the underlying asset.                                                                                                 |
| `underlyingToken`                                                                                                                                              | [components.UnderlyingToken](../../models/components/underlyingtoken.md)                                                                                       | :heavy_check_mark:                                                                                                                                             | N/A                                                                                                                                                            |
| `apy`                                                                                                                                                          | [components.Apy](../../models/components/apy.md)                                                                                                               | :heavy_check_mark:                                                                                                                                             | N/A                                                                                                                                                            |
| `userPosition`                                                                                                                                                 | [components.CompassApiBackendModelsVaultsReadResponseVaultUserPosition](../../models/components/compassapibackendmodelsvaultsreadresponsevaultuserposition.md) | :heavy_minus_sign:                                                                                                                                             | The user's position in the vault.                                                                                                                              |