# UserOperationResponse

## Example Usage

```typescript
import { UserOperationResponse } from "@compass-labs/api-sdk/models/components";

let value: UserOperationResponse = {
  to: "<value>",
  data: "<value>",
  value: "<value>",
};
```

## Fields

| Field                                         | Type                                          | Required                                      | Description                                   |
| --------------------------------------------- | --------------------------------------------- | --------------------------------------------- | --------------------------------------------- |
| `to`                                          | *string*                                      | :heavy_check_mark:                            | The target contract address for the operation |
| `data`                                        | *string*                                      | :heavy_check_mark:                            | The calldata for the operation                |
| `value`                                       | *string*                                      | :heavy_check_mark:                            | The ETH value to send with the operation      |