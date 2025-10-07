# OdosSwapParams

## Example Usage

```typescript
import { OdosSwapParams } from "@compass-labs/api-sdk/models/components";

let value: OdosSwapParams = {
  tokenIn: "0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48",
  tokenOut: "0xdac17f958d2ee523a2206206994597c13d831ec7",
  amount: 1.5,
  maxSlippagePercent: 0.5,
};
```

## Fields

| Field                                                                          | Type                                                                           | Required                                                                       | Description                                                                    | Example                                                                        |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `actionType`                                                                   | *string*                                                                       | :heavy_minus_sign:                                                             | N/A                                                                            |                                                                                |
| `tokenIn`                                                                      | *string*                                                                       | :heavy_check_mark:                                                             | The symbol or address of the token that is to be sold.                         | 0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48                                     |
| `tokenOut`                                                                     | *string*                                                                       | :heavy_check_mark:                                                             | The symbol or address of the token that is to be bought.                       | 0xdac17f958d2ee523a2206206994597c13d831ec7                                     |
| `amount`                                                                       | *components.OdosSwapParamsAmount*                                              | :heavy_check_mark:                                                             | The amount of token_in to be sold.                                             | 1.5                                                                            |
| `maxSlippagePercent`                                                           | *number*                                                                       | :heavy_check_mark:                                                             | The maximum slippage allowed in percent. e.g. `1` means `1%` slippage allowed. | 0.5                                                                            |