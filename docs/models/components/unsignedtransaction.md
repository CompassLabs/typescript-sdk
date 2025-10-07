# UnsignedTransaction

## Example Usage

```typescript
import { UnsignedTransaction } from "@compass-labs/api-sdk/models/components";

let value: UnsignedTransaction = {
  chainId: "<id>",
  data: "<value>",
  from: "<value>",
  gas: null,
  to: "<value>",
  value: "<value>",
  nonce: "<value>",
  maxFeePerGas: "<value>",
  maxPriorityFeePerGas: "<value>",
};
```

## Fields

| Field                                           | Type                                            | Required                                        | Description                                     |
| ----------------------------------------------- | ----------------------------------------------- | ----------------------------------------------- | ----------------------------------------------- |
| `chainId`                                       | *string*                                        | :heavy_check_mark:                              | The chain id of the transaction                 |
| `data`                                          | *string*                                        | :heavy_check_mark:                              | The data of the transaction                     |
| `from`                                          | *string*                                        | :heavy_check_mark:                              | The sender of the transaction                   |
| `gas`                                           | *string*                                        | :heavy_check_mark:                              | The gas of the transaction                      |
| `to`                                            | *string*                                        | :heavy_check_mark:                              | The recipient of the transaction                |
| `value`                                         | *string*                                        | :heavy_check_mark:                              | The value of the transaction                    |
| `nonce`                                         | *string*                                        | :heavy_check_mark:                              | The nonce of the address                        |
| `maxFeePerGas`                                  | *string*                                        | :heavy_check_mark:                              | The max fee per gas of the transaction          |
| `maxPriorityFeePerGas`                          | *string*                                        | :heavy_check_mark:                              | The max priority fee per gas of the transaction |