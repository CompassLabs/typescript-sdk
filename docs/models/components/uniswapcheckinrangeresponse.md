# UniswapCheckInRangeResponse

## Example Usage

```typescript
import { UniswapCheckInRangeResponse } from "@compass-labs/api-sdk/models/components";

let value: UniswapCheckInRangeResponse = {
  inRange: true,
};
```

## Fields

| Field                                                                                                           | Type                                                                                                            | Required                                                                                                        | Description                                                                                                     |
| --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| `inRange`                                                                                                       | *boolean*                                                                                                       | :heavy_check_mark:                                                                                              | Whether the position is in active tick range or not. If not in range, the position is not earning trading fees. |