# ResponseV1TransactionBundlerAaveLoop

Successful Response


## Supported Types

### `components.BundlerTransactionResponse`

```typescript
const value: components.BundlerTransactionResponse = {
  transaction: {
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
  },
};
```

### `components.BatchedUserOperationsResponse`

```typescript
const value: components.BatchedUserOperationsResponse = {
  operations: [],
};
```

