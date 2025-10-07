# SkyCheckPositionResponse

## Example Usage

```typescript
import { SkyCheckPositionResponse } from "@compass-labs/api-sdk/models/components";

let value: SkyCheckPositionResponse = {
  usdsValueOfDeposits: "<value>",
  shares: 425127,
};
```

## Fields

| Field                                                                          | Type                                                                           | Required                                                                       | Description                                                                    |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `usdsValueOfDeposits`                                                          | *string*                                                                       | :heavy_check_mark:                                                             | The USDS equivalent value of the user's deposits thus far (principal + yield). |
| `shares`                                                                       | *number*                                                                       | :heavy_check_mark:                                                             | N/A                                                                            |