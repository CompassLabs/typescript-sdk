# V1MorphoVaultsRequest

## Example Usage

```typescript
import { V1MorphoVaultsRequest } from "@compass-labs/api-sdk/models/operations";

let value: V1MorphoVaultsRequest = {
  depositToken: "USDC",
};
```

## Fields

| Field                                                                            | Type                                                                             | Required                                                                         | Description                                                                      | Example                                                                          |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `chain`                                                                          | [operations.V1MorphoVaultsChain](../../models/operations/v1morphovaultschain.md) | :heavy_check_mark:                                                               | N/A                                                                              |                                                                                  |
| `depositToken`                                                                   | *string*                                                                         | :heavy_minus_sign:                                                               | Symbol or address of the deposit token to filter vaults by. Optional parameter.  | USDC                                                                             |