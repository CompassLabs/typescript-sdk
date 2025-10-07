# MulticallAuthorizationResponse

Response model for multicall authorization.

## Example Usage

```typescript
import { MulticallAuthorizationResponse } from "@compass-labs/api-sdk/models/components";

let value: MulticallAuthorizationResponse = {
  nonce: 12345,
  address: "5549 W 5th Street",
  chainId: 1,
};
```

## Fields

| Field                                         | Type                                          | Required                                      | Description                                   | Example                                       |
| --------------------------------------------- | --------------------------------------------- | --------------------------------------------- | --------------------------------------------- | --------------------------------------------- |
| `nonce`                                       | *number*                                      | :heavy_check_mark:                            | A unique nonce value for this authorization   | 12345                                         |
| `address`                                     | *string*                                      | :heavy_check_mark:                            | The Ethereum address authorized for multicall |                                               |
| `chainId`                                     | *number*                                      | :heavy_check_mark:                            | The chain ID for the blockchain network       | 1                                             |