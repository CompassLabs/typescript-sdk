# V1TokenBalanceRequest

## Example Usage

```typescript
import { V1TokenBalanceRequest } from "@compass-labs/api-sdk/models/operations";

let value: V1TokenBalanceRequest = {};
```

## Fields

| Field                                                                            | Type                                                                             | Required                                                                         | Description                                                                      | Example                                                                          |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `chain`                                                                          | [operations.V1TokenBalanceChain](../../models/operations/v1tokenbalancechain.md) | :heavy_check_mark:                                                               | N/A                                                                              |                                                                                  |
| `user`                                                                           | *string*                                                                         | :heavy_check_mark:                                                               | The user to get the token balance of.                                            |                                                                                  |
| `token`                                                                          | *string*                                                                         | :heavy_check_mark:                                                               | The symbol or address of the token for which the balance is checked.             | USDC                                                                             |