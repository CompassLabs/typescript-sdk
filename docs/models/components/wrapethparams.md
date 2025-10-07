# WrapEthParams

Parameters model for wrapping ETH into WETH.

## Example Usage

```typescript
import { WrapEthParams } from "@compass-labs/api-sdk/models/components";

let value: WrapEthParams = {
  amount: 1.5,
};
```

## Fields

| Field                            | Type                             | Required                         | Description                      | Example                          |
| -------------------------------- | -------------------------------- | -------------------------------- | -------------------------------- | -------------------------------- |
| `actionType`                     | *string*                         | :heavy_minus_sign:               | N/A                              |                                  |
| `amount`                         | *components.WrapEthParamsAmount* | :heavy_check_mark:               | The amount of ETH to wrap.       | 1.5                              |