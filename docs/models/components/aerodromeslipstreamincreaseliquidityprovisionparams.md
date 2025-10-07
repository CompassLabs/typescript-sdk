# AerodromeSlipstreamIncreaseLiquidityProvisionParams

Endpoint parameters for increasing liquidity provision on aerodrome slipstream.

This action is performed on the NonfungiblePosition Manager to increase the
liquidity of an existing position.

## Example Usage

```typescript
import { AerodromeSlipstreamIncreaseLiquidityProvisionParams } from "@compass-labs/api-sdk/models/components";

let value: AerodromeSlipstreamIncreaseLiquidityProvisionParams = {
  tokenId: 800217,
  amount0Desired: "1.5",
  amount1Desired: "1.7",
  amount0Min: "1.4",
  amount1Min: "1.6",
};
```

## Fields

| Field                                                                          | Type                                                                           | Required                                                                       | Description                                                                    | Example                                                                        |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| `actionType`                                                                   | *string*                                                                       | :heavy_minus_sign:                                                             | N/A                                                                            |                                                                                |
| `tokenId`                                                                      | *number*                                                                       | :heavy_check_mark:                                                             | Token ID of the NFT representing the liquidity provisioned position.           |                                                                                |
| `amount0Desired`                                                               | *components.AerodromeSlipstreamIncreaseLiquidityProvisionParamsAmount0Desired* | :heavy_check_mark:                                                             | The desired amount of the first token to deposit                               | 1.5                                                                            |
| `amount1Desired`                                                               | *components.AerodromeSlipstreamIncreaseLiquidityProvisionParamsAmount1Desired* | :heavy_check_mark:                                                             | The desired amount of the second token to deposit                              | 1.7                                                                            |
| `amount0Min`                                                                   | *components.AerodromeSlipstreamIncreaseLiquidityProvisionParamsAmount0Min*     | :heavy_check_mark:                                                             | The minimum amount of the first token to deposit                               | 1.4                                                                            |
| `amount1Min`                                                                   | *components.AerodromeSlipstreamIncreaseLiquidityProvisionParamsAmount1Min*     | :heavy_check_mark:                                                             | The minimum amount of the second token to deposit                              | 1.6                                                                            |