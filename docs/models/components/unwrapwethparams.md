# UnwrapWethParams

Parameters model for unwrapping WETH back to native ETH.

## Example Usage

```typescript
import { UnwrapWethParams } from "@compass-labs/api-sdk/models/components";

let value: UnwrapWethParams = {
  amount: 1.5,
};
```

## Fields

| Field                               | Type                                | Required                            | Description                         | Example                             |
| ----------------------------------- | ----------------------------------- | ----------------------------------- | ----------------------------------- | ----------------------------------- |
| `actionType`                        | *string*                            | :heavy_minus_sign:                  | N/A                                 |                                     |
| `amount`                            | *components.UnwrapWethParamsAmount* | :heavy_check_mark:                  | The amount of WETH to unwrap.       | 1.5                                 |