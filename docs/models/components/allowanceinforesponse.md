# AllowanceInfoResponse

Response model for token allowance information.

## Example Usage

```typescript
import { AllowanceInfoResponse } from "@compass-labs/api-sdk/models/components";

let value: AllowanceInfoResponse = {
  amount: "1.5",
  decimals: 18,
  tokenSymbol: "WETH",
  tokenAddress: "0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2",
  contractAddress: "0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B",
};
```

## Fields

| Field                                           | Type                                            | Required                                        | Description                                     | Example                                         |
| ----------------------------------------------- | ----------------------------------------------- | ----------------------------------------------- | ----------------------------------------------- | ----------------------------------------------- |
| `amount`                                        | *string*                                        | :heavy_check_mark:                              | Amount of tokens allowed to be spent by spender | 1.5                                             |
| `decimals`                                      | *number*                                        | :heavy_check_mark:                              | Number of decimals of the token                 | 18                                              |
| `tokenSymbol`                                   | *string*                                        | :heavy_check_mark:                              | Symbol of the token.                            | WETH                                            |
| `tokenAddress`                                  | *string*                                        | :heavy_check_mark:                              | Address of the token                            | 0xC02aaA39b223FE8D0A0e5C4F27eAD9083C756Cc2      |
| `contractAddress`                               | *string*                                        | :heavy_check_mark:                              | Address of the contract                         | 0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B      |