# TokenTransferParams

Parameters model for transferring ETH or ERC20 tokens.

## Example Usage

```typescript
import { TokenTransferParams } from "@compass-labs/api-sdk/models/components";

let value: TokenTransferParams = {
  to: "0x68b3465833fb72A70ecDF485E0e4C7bD8665Fc44",
  token: "USDC",
  amount: 1.5,
};
```

## Fields

| Field                                           | Type                                            | Required                                        | Description                                     | Example                                         |
| ----------------------------------------------- | ----------------------------------------------- | ----------------------------------------------- | ----------------------------------------------- | ----------------------------------------------- |
| `actionType`                                    | *string*                                        | :heavy_minus_sign:                              | N/A                                             |                                                 |
| `to`                                            | *string*                                        | :heavy_check_mark:                              | The recipient of the tokens.                    | 0x68b3465833fb72A70ecDF485E0e4C7bD8665Fc44      |
| `token`                                         | *string*                                        | :heavy_check_mark:                              | The symbol or address of the token to transfer. | USDC                                            |
| `amount`                                        | *components.TokenTransferParamsAmount*          | :heavy_check_mark:                              | Amount of token to transfer                     | 1.5                                             |