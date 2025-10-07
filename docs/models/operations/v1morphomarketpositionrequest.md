# V1MorphoMarketPositionRequest

## Example Usage

```typescript
import { V1MorphoMarketPositionRequest } from "@compass-labs/api-sdk/models/operations";

let value: V1MorphoMarketPositionRequest = {};
```

## Fields

| Field                                                                                            | Type                                                                                             | Required                                                                                         | Description                                                                                      |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| `chain`                                                                                          | [operations.V1MorphoMarketPositionChain](../../models/operations/v1morphomarketpositionchain.md) | :heavy_check_mark:                                                                               | N/A                                                                                              |
| `userAddress`                                                                                    | *string*                                                                                         | :heavy_check_mark:                                                                               | The user address of the desired market position.                                                 |
| `uniqueMarketKey`                                                                                | *string*                                                                                         | :heavy_check_mark:                                                                               | The key that uniquely identifies the market. This can be found using the 'Get Markets' endpoint. |