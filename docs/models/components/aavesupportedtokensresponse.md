# AaveSupportedTokensResponse

## Example Usage

```typescript
import { AaveSupportedTokensResponse } from "@compass-labs/api-sdk/models/components";

let value: AaveSupportedTokensResponse = {
  tokens: [
    {
      symbol: "<value>",
      address: "96133 Milton Road",
      supplyingEnabled: false,
      borrowingEnabled: false,
    },
  ],
};
```

## Fields

| Field                                                                                            | Type                                                                                             | Required                                                                                         | Description                                                                                      |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| `tokens`                                                                                         | [components.AaveSupportedTokenMetadata](../../models/components/aavesupportedtokenmetadata.md)[] | :heavy_check_mark:                                                                               | List of supported tokens with configuration metadata for a given chain.                          |