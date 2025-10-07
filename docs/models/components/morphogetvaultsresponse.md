# MorphoGetVaultsResponse

## Example Usage

```typescript
import { MorphoGetVaultsResponse } from "@compass-labs/api-sdk/models/components";

let value: MorphoGetVaultsResponse = {
  vaults: [],
};
```

## Fields

| Field                                                              | Type                                                               | Required                                                           | Description                                                        |
| ------------------------------------------------------------------ | ------------------------------------------------------------------ | ------------------------------------------------------------------ | ------------------------------------------------------------------ |
| `vaults`                                                           | [components.MorphoVault](../../models/components/morphovault.md)[] | :heavy_check_mark:                                                 |  A list of vaults matching the query.                              |