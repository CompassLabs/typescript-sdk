# SkyBuyParams

## Example Usage

```typescript
import { SkyBuyParams } from "@compass-labs/api-sdk/models/components";

let value: SkyBuyParams = {
  tokenIn: "DAI",
  amount: 1.5,
};
```

## Fields

| Field                                                                            | Type                                                                             | Required                                                                         | Description                                                                      | Example                                                                          |
| -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| `actionType`                                                                     | *string*                                                                         | :heavy_minus_sign:                                                               | N/A                                                                              |                                                                                  |
| `tokenIn`                                                                        | [components.SkyBuyParamsTokenIn](../../models/components/skybuyparamstokenin.md) | :heavy_check_mark:                                                               | The token you would like to swap 1:1 for USDS. Choose from DAI or USDC.          |                                                                                  |
| `amount`                                                                         | *components.SkyBuyParamsAmount*                                                  | :heavy_check_mark:                                                               | The amount of USDS you would like to buy 1:1 with 'token_in'.                    | 1.5                                                                              |