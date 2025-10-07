# MorphoCheckUserPositionResponse

## Example Usage

```typescript
import { MorphoCheckUserPositionResponse } from "@compass-labs/api-sdk/models/components";

let value: MorphoCheckUserPositionResponse = {
  state: {
    vaultsPnlUsd: "<value>",
    vaultsAssetsUsd: "<value>",
    marketsPnlUsd: null,
    marketsBorrowAssetsUsd: "<value>",
    marketsCollateralUsd: "<value>",
    marketsSupplyAssetsUsd: "<value>",
  },
  vaultPositions: [],
  marketPositions: [],
};
```

## Fields

| Field                                                                    | Type                                                                     | Required                                                                 | Description                                                              |
| ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ | ------------------------------------------------------------------------ |
| `state`                                                                  | [components.UserState](../../models/components/userstate.md)             | :heavy_check_mark:                                                       | N/A                                                                      |
| `vaultPositions`                                                         | [components.VaultPosition](../../models/components/vaultposition.md)[]   | :heavy_check_mark:                                                       | A list of the user's vault positions.                                    |
| `marketPositions`                                                        | [components.MarketPosition](../../models/components/marketposition.md)[] | :heavy_check_mark:                                                       | A list of the user's market positions.                                   |