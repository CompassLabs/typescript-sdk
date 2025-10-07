# CooldownPosition

## Example Usage

```typescript
import { CooldownPosition } from "@compass-labs/api-sdk/models/components";

let value: CooldownPosition = {
  amountInUnderlyingAsset: "<value>",
  cooldownEnd: new Date("2024-06-19T22:17:27.773Z"),
  canBeWithdrawn: false,
};
```

## Fields

| Field                                                         | Type                                                          | Required                                                      | Description                                                   |
| ------------------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------- | ------------------------------------------------------------- |
| `amountInUnderlyingAsset`                                     | *string*                                                      | :heavy_check_mark:                                            | The amount of USDe currently in a cooldown period.            |
| `cooldownEnd`                                                 | *components.CooldownEnd*                                      | :heavy_check_mark:                                            | When the cooldown period ends. ISO 8601 format. UTC timezone. |
| `canBeWithdrawn`                                              | *boolean*                                                     | :heavy_check_mark:                                            | Whether the USDe in cooldown can be withdrawn at this moment. |