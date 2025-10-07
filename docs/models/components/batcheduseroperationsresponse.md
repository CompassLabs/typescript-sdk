# BatchedUserOperationsResponse

## Example Usage

```typescript
import { BatchedUserOperationsResponse } from "@compass-labs/api-sdk/models/components";

let value: BatchedUserOperationsResponse = {
  operations: [],
};
```

## Fields

| Field                                                                                  | Type                                                                                   | Required                                                                               | Description                                                                            |
| -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| `operations`                                                                           | [components.UserOperationResponse](../../models/components/useroperationresponse.md)[] | :heavy_check_mark:                                                                     | List of user operations to be batched and executed by the smart account.               |