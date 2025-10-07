# SkyDepositParams

## Example Usage

```typescript
import { SkyDepositParams } from "@compass-labs/api-sdk/models/components";

let value: SkyDepositParams = {
  amount: 1.5,
};
```

## Fields

| Field                                                                 | Type                                                                  | Required                                                              | Description                                                           | Example                                                               |
| --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- | --------------------------------------------------------------------- |
| `actionType`                                                          | *string*                                                              | :heavy_minus_sign:                                                    | N/A                                                                   |                                                                       |
| `amount`                                                              | *components.SkyDepositParamsAmount*                                   | :heavy_check_mark:                                                    | The amount of USDS you would like to deposit for sUSDS to earn yield. | 1.5                                                                   |
| `receiver`                                                            | *string*                                                              | :heavy_minus_sign:                                                    | The address which will receive the sUSDS. Defaults to the sender.     |                                                                       |