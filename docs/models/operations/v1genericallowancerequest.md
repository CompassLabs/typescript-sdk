# V1GenericAllowanceRequest

## Example Usage

```typescript
import { V1GenericAllowanceRequest } from "@compass-labs/api-sdk/models/operations";

let value: V1GenericAllowanceRequest = {
  contract: "OdosRouter",
};
```

## Fields

| Field                                                                                    | Type                                                                                     | Required                                                                                 | Description                                                                              | Example                                                                                  |
| ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- |
| `chain`                                                                                  | [operations.V1GenericAllowanceChain](../../models/operations/v1genericallowancechain.md) | :heavy_check_mark:                                                                       | N/A                                                                                      |                                                                                          |
| `user`                                                                                   | *string*                                                                                 | :heavy_minus_sign:                                                                       | The user to get the ERC20 allowance of.                                                  |                                                                                          |
| `token`                                                                                  | *string*                                                                                 | :heavy_check_mark:                                                                       | The symbol or address of the token for which the allowance is checked.                   | USDC                                                                                     |
| `contract`                                                                               | *operations.Contract*                                                                    | :heavy_check_mark:                                                                       | The name or address of the contract to check allowance for.                              |                                                                                          |