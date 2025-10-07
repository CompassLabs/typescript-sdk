# V1AaveUserPositionSummaryRequest

## Example Usage

```typescript
import { V1AaveUserPositionSummaryRequest } from "@compass-labs/api-sdk/models/operations";

let value: V1AaveUserPositionSummaryRequest = {};
```

## Fields

| Field                                                                                                  | Type                                                                                                   | Required                                                                                               | Description                                                                                            |
| ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------ |
| `chain`                                                                                                | [operations.V1AaveUserPositionSummaryChain](../../models/operations/v1aaveuserpositionsummarychain.md) | :heavy_check_mark:                                                                                     | N/A                                                                                                    |
| `block`                                                                                                | *number*                                                                                               | :heavy_minus_sign:                                                                                     | Optional block number (defaults to latest).                                                            |
| `user`                                                                                                 | *string*                                                                                               | :heavy_check_mark:                                                                                     | The user to get position summary for.                                                                  |