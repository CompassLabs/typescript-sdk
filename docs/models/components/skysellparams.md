# SkySellParams

## Example Usage

```typescript
import { SkySellParams } from "@compass-labs/api-sdk/models/components";

let value: SkySellParams = {
  tokenOut: "USDC",
  amount: 1.5,
};
```

## Fields

| Field                                                                                | Type                                                                                 | Required                                                                             | Description                                                                          | Example                                                                              |
| ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| `actionType`                                                                         | *string*                                                                             | :heavy_minus_sign:                                                                   | N/A                                                                                  |                                                                                      |
| `tokenOut`                                                                           | [components.SkySellParamsTokenOut](../../models/components/skysellparamstokenout.md) | :heavy_check_mark:                                                                   | The token you would like to swap 1:1 with USDS. Choose from DAI or USDC.             |                                                                                      |
| `amount`                                                                             | *components.SkySellParamsAmount*                                                     | :heavy_check_mark:                                                                   | The amount of USDS you would like to sell 1:1 for 'token_out'.                       | 1.5                                                                                  |