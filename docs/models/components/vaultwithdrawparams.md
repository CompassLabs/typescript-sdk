# VaultWithdrawParams

## Example Usage

```typescript
import { VaultWithdrawParams } from "@compass-labs/api-sdk/models/components";

let value: VaultWithdrawParams = {
  vaultAddress: "0xbEef047a543E45807105E51A8BBEFCc5950fcfBa",
  amount: "1.5",
};
```

## Fields

| Field                                                                                                                  | Type                                                                                                                   | Required                                                                                                               | Description                                                                                                            | Example                                                                                                                |
| ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| `actionType`                                                                                                           | *string*                                                                                                               | :heavy_minus_sign:                                                                                                     | N/A                                                                                                                    |                                                                                                                        |
| `vaultAddress`                                                                                                         | *string*                                                                                                               | :heavy_check_mark:                                                                                                     | The vault address you are withdrawing from.                                                                            | 0xbEef047a543E45807105E51A8BBEFCc5950fcfBa                                                                             |
| `amount`                                                                                                               | *any*                                                                                                                  | :heavy_check_mark:                                                                                                     | The amount of tokens to withdraw from the vault. If set to 'ALL', your total deposited token amount will be withdrawn. |                                                                                                                        |
| `receiver`                                                                                                             | *string*                                                                                                               | :heavy_minus_sign:                                                                                                     | The address which will receive the tokens withdrawn. Defaults to the sender.                                           |                                                                                                                        |