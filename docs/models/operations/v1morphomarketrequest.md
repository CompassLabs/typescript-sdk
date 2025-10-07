# V1MorphoMarketRequest

## Example Usage

```typescript
import { V1MorphoMarketRequest } from "@compass-labs/api-sdk/models/operations";

let value: V1MorphoMarketRequest = {};
```

## Fields

| Field                                                                                            | Type                                                                                             | Required                                                                                         | Description                                                                                      |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| `chain`                                                                                          | [operations.V1MorphoMarketChain](../../models/operations/v1morphomarketchain.md)                 | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `uniqueMarketKey`                                                                                | *string*                                                                                         | :heavy_check_mark:                                                                               | The key that uniquely identifies the market. This can be found using the 'Get Markets' endpoint. |