# SignedAuthorization

## Example Usage

```typescript
import { SignedAuthorization } from "@compass-labs/api-sdk/models/components";

let value: SignedAuthorization = {
  nonce: 1000,
  address: "0xcA11bde05977b3631167028862bE2a173976CA11",
  chainId: 42161,
  r: "0x5f9f3f3226ac91bc01a72dd117141f6c6de1ed30d3af9f95c3423316dc21d615",
  s: "0x78f7982ede9dabc53d7153974c5692fda8a21fc73bdafc42aaf135505e22817c",
  yParity: 0,
};
```

## Fields

| Field                                                              | Type                                                               | Required                                                           | Description                                                        | Example                                                            |
| ------------------------------------------------------------------ | ------------------------------------------------------------------ | ------------------------------------------------------------------ | ------------------------------------------------------------------ | ------------------------------------------------------------------ |
| `nonce`                                                            | *number*                                                           | :heavy_check_mark:                                                 | The nonce of the authorization                                     | 1000                                                               |
| `address`                                                          | *string*                                                           | :heavy_check_mark:                                                 | The address of the authorization                                   | 0xcA11bde05977b3631167028862bE2a173976CA11                         |
| `chainId`                                                          | *number*                                                           | :heavy_check_mark:                                                 | The chain ID                                                       | 42161                                                              |
| `r`                                                                | *components.R*                                                     | :heavy_check_mark:                                                 | The r value of the signature                                       | 0x5f9f3f3226ac91bc01a72dd117141f6c6de1ed30d3af9f95c3423316dc21d615 |
| `s`                                                                | *components.S*                                                     | :heavy_check_mark:                                                 | The s value of the signature                                       | 0x78f7982ede9dabc53d7153974c5692fda8a21fc73bdafc42aaf135505e22817c |
| `yParity`                                                          | *number*                                                           | :heavy_check_mark:                                                 | The y-parity of the signature (0 or 1)                             | 0                                                                  |