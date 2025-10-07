# V1EthenaVaultRequest

## Example Usage

```typescript
import { V1EthenaVaultRequest } from "@compass-labs/api-sdk/models/operations";

let value: V1EthenaVaultRequest = {};
```

## Fields

| Field                                                                                                                                          | Type                                                                                                                                           | Required                                                                                                                                       | Description                                                                                                                                    |
| ---------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| `chain`                                                                                                                                        | [operations.V1EthenaVaultChain](../../models/operations/v1ethenavaultchain.md)                                                                 | :heavy_check_mark:                                                                                                                             | N/A                                                                                                                                            |
| `block`                                                                                                                                        | *number*                                                                                                                                       | :heavy_minus_sign:                                                                                                                             | Optional block number (defaults to latest).                                                                                                    |
| `userAddress`                                                                                                                                  | *string*                                                                                                                                       | :heavy_minus_sign:                                                                                                                             | The user address of the desired vault position. Only include if you would like the user position included in the response. Defaults to `None`. |