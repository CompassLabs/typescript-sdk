# UniswapSellExactlyTransactionResponseTransaction

The unsigned transaction data. User must sign and broadcast to network.


## Supported Types

### `components.UnsignedTransaction`

```typescript
const value: components.UnsignedTransaction = {
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

### `components.UserOperationResponse`

```typescript
const value: components.UserOperationResponse = {
  to: "<value>",
  data: "<value>",
  value: "<value>",
};
```

