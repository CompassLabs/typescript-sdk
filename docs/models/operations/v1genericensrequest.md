# V1GenericEnsRequest

## Example Usage

```typescript
import { V1GenericEnsRequest } from "@compass-labs/api-sdk/models/operations";

let value: V1GenericEnsRequest = {};
```

## Fields

| Field                                                                        | Type                                                                         | Required                                                                     | Description                                                                  |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------- |
| `chain`                                                                      | [operations.V1GenericEnsChain](../../models/operations/v1genericenschain.md) | :heavy_check_mark:                                                           | N/A                                                                          |
| `ensName`                                                                    | *string*                                                                     | :heavy_minus_sign:                                                           | The ENS name to resolve.                                                     |