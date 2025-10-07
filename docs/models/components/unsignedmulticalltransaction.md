# UnsignedMulticallTransaction

## Example Usage

```typescript
import { UnsignedMulticallTransaction } from "@compass-labs/api-sdk/models/components";

let value: UnsignedMulticallTransaction = {
  chainId: "<id>",
  data: "<value>",
  from: "<value>",
  gas: "<value>",
  to: "<value>",
  value: "<value>",
  nonce: "<value>",
  maxFeePerGas: "<value>",
  maxPriorityFeePerGas: "<value>",
  authorizationList: [
    {
      nonce: 1000,
      address: "0xcA11bde05977b3631167028862bE2a173976CA11",
      chainId: 42161,
      r: "0x5f9f3f3226ac91bc01a72dd117141f6c6de1ed30d3af9f95c3423316dc21d615",
      s: "0x78f7982ede9dabc53d7153974c5692fda8a21fc73bdafc42aaf135505e22817c",
      yParity: 0,
    },
  ],
};
```

## Fields

| Field                                                                              | Type                                                                               | Required                                                                           | Description                                                                        |
| ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- |
| `chainId`                                                                          | *string*                                                                           | :heavy_check_mark:                                                                 | The chain id of the transaction                                                    |
| `data`                                                                             | *string*                                                                           | :heavy_check_mark:                                                                 | The data of the transaction                                                        |
| `from`                                                                             | *string*                                                                           | :heavy_check_mark:                                                                 | The sender of the transaction                                                      |
| `gas`                                                                              | *string*                                                                           | :heavy_check_mark:                                                                 | The gas of the transaction                                                         |
| `to`                                                                               | *string*                                                                           | :heavy_check_mark:                                                                 | The recipient of the transaction                                                   |
| `value`                                                                            | *string*                                                                           | :heavy_check_mark:                                                                 | The value of the transaction                                                       |
| `nonce`                                                                            | *string*                                                                           | :heavy_check_mark:                                                                 | The nonce of the address                                                           |
| `maxFeePerGas`                                                                     | *string*                                                                           | :heavy_check_mark:                                                                 | The max fee per gas of the transaction                                             |
| `maxPriorityFeePerGas`                                                             | *string*                                                                           | :heavy_check_mark:                                                                 | The max priority fee per gas of the transaction                                    |
| `authorizationList`                                                                | [components.SignedAuthorization](../../models/components/signedauthorization.md)[] | :heavy_minus_sign:                                                                 | EIP-7702 authorization                                                             |