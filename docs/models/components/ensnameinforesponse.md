# EnsNameInfoResponse

Response model for ENS name details.

## Example Usage

```typescript
import { EnsNameInfoResponse } from "@compass-labs/api-sdk/models/components";

let value: EnsNameInfoResponse = {
  walletAddress: "0x68b3465833fb72A70ecDF485E0e4C7bD8665Fc45",
  registrant: "0x68b3465833fb72A70ecDF485E0e4C7bD8665Fc45",
};
```

## Fields

| Field                                      | Type                                       | Required                                   | Description                                | Example                                    |
| ------------------------------------------ | ------------------------------------------ | ------------------------------------------ | ------------------------------------------ | ------------------------------------------ |
| `walletAddress`                            | *string*                                   | :heavy_check_mark:                         | The wallet address of the user             | 0x68b3465833fb72A70ecDF485E0e4C7bD8665Fc45 |
| `registrant`                               | *string*                                   | :heavy_check_mark:                         | The registrant of the ENS                  | 0x68b3465833fb72A70ecDF485E0e4C7bD8665Fc45 |