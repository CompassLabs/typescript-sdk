# PendleRedeemYieldParams

## Example Usage

```typescript
import { PendleRedeemYieldParams } from "@compass-labs/api-sdk/models/components";

let value: PendleRedeemYieldParams = {
  marketAddress: "0x08a152834de126d2ef83d612ff36e4523fd0017f",
};
```

## Fields

| Field                                                                                            | Type                                                                                             | Required                                                                                         | Description                                                                                      | Example                                                                                          |
| ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------ |
| `actionType`                                                                                     | *string*                                                                                         | :heavy_minus_sign:                                                                               | N/A                                                                                              |                                                                                                  |
| `marketAddress`                                                                                  | *string*                                                                                         | :heavy_check_mark:                                                                               | The address of the market identifying which Yield Token (YT) you would like to claim yield from. | 0x08a152834de126d2ef83d612ff36e4523fd0017f                                                       |