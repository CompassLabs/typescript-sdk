# AaveLiquidityChangeResponse

## Example Usage

```typescript
import { AaveLiquidityChangeResponse } from "@compass-labs/api-sdk/models/components";

let value: AaveLiquidityChangeResponse = {
  liquidityChange: "<value>",
  startTime: new Date("2023-12-20T02:39:56.491Z"),
  endTime: new Date("2023-08-18T07:37:51.082Z"),
};
```

## Fields

| Field                                                                                         | Type                                                                                          | Required                                                                                      | Description                                                                                   |
| --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------- |
| `liquidityChange`                                                                             | *string*                                                                                      | :heavy_check_mark:                                                                            | The change in the liquidity index between the two times, expressed as a percentage.           |
| `startTime`                                                                                   | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | Dateime of starting block                                                                     |
| `endTime`                                                                                     | [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) | :heavy_check_mark:                                                                            | Datetime of ending block                                                                      |