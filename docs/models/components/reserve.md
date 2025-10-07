# Reserve

## Example Usage

```typescript
import { Reserve } from "@compass-labs/api-sdk/models/components";

let value: Reserve = {
  symbol: "<value>",
  name: "<value>",
  underlyingAsset: "0x68b3465833fb72A70ecDF485E0e4C7bD8665Fc45",
};
```

## Fields

| Field                                      | Type                                       | Required                                   | Description                                | Example                                    |
| ------------------------------------------ | ------------------------------------------ | ------------------------------------------ | ------------------------------------------ | ------------------------------------------ |
| `symbol`                                   | *string*                                   | :heavy_check_mark:                         | Symbol of token.                           |                                            |
| `decimals`                                 | *number*                                   | :heavy_minus_sign:                         | Number of decimals of token.               |                                            |
| `name`                                     | *string*                                   | :heavy_check_mark:                         | Name of token                              |                                            |
| `underlyingAsset`                          | *string*                                   | :heavy_check_mark:                         | Checksum address of Token.                 | 0x68b3465833fb72A70ecDF485E0e4C7bD8665Fc45 |