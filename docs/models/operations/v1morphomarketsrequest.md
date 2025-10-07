# V1MorphoMarketsRequest

## Example Usage

```typescript
import { V1MorphoMarketsRequest } from "@compass-labs/api-sdk/models/operations";

let value: V1MorphoMarketsRequest = {
  collateralToken: "USDC",
  loanToken: "USDC",
};
```

## Fields

| Field                                                                               | Type                                                                                | Required                                                                            | Description                                                                         | Example                                                                             |
| ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| `chain`                                                                             | [operations.V1MorphoMarketsChain](../../models/operations/v1morphomarketschain.md)  | :heavy_check_mark:                                                                  | N/A                                                                                 |                                                                                     |
| `collateralToken`                                                                   | *string*                                                                            | :heavy_minus_sign:                                                                  | Symbol or address of the collateral token to filter markets by. Optional parameter. | USDC                                                                                |
| `loanToken`                                                                         | *string*                                                                            | :heavy_minus_sign:                                                                  | Symbol or address of the loan token to filter markets by. Optional parameter.       | USDC                                                                                |