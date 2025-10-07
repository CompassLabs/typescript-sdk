# AaveSupportedTokenMetadata

## Example Usage

```typescript
import { AaveSupportedTokenMetadata } from "@compass-labs/api-sdk/models/components";

let value: AaveSupportedTokenMetadata = {
  symbol: "<value>",
  address: "234 Devonshire Road",
  supplyingEnabled: true,
  borrowingEnabled: true,
};
```

## Fields

| Field                                        | Type                                         | Required                                     | Description                                  |
| -------------------------------------------- | -------------------------------------------- | -------------------------------------------- | -------------------------------------------- |
| `symbol`                                     | *string*                                     | :heavy_check_mark:                           | Token symbol (e.g., 'WETH', 'DAI').          |
| `address`                                    | *string*                                     | :heavy_check_mark:                           | Token contract address.                      |
| `supplyingEnabled`                           | *boolean*                                    | :heavy_check_mark:                           | Whether the token can be used as collateral. |
| `borrowingEnabled`                           | *boolean*                                    | :heavy_check_mark:                           | Whether the token can be borrowed.           |