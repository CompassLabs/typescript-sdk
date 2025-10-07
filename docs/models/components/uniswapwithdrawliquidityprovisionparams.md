# UniswapWithdrawLiquidityProvisionParams

Endpoint parameters for liquidity provision withdrawal on uniswap v3.

This action is performed in a multicall on the NonfungiblePosition Manager: https://github.com/Uniswap/v3-periphery/blob/0682387198a24c7cd63566a2c58398533860a5d1/contracts/base/Multicall.sol#L11-L27
First, we call decrease liquidity then collect the tokens owed to the user.

## Example Usage

```typescript
import { UniswapWithdrawLiquidityProvisionParams } from "@compass-labs/api-sdk/models/components";

let value: UniswapWithdrawLiquidityProvisionParams = {
  tokenId: 405500,
  percentageForWithdrawal: "25",
};
```

## Fields

| Field                                                                       | Type                                                                        | Required                                                                    | Description                                                                 | Example                                                                     |
| --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| `actionType`                                                                | *string*                                                                    | :heavy_minus_sign:                                                          | N/A                                                                         |                                                                             |
| `tokenId`                                                                   | *number*                                                                    | :heavy_check_mark:                                                          | Token ID of the NFT representing the liquidity provisioned position.        |                                                                             |
| `percentageForWithdrawal`                                                   | *components.UniswapWithdrawLiquidityProvisionParamsPercentageForWithdrawal* | :heavy_check_mark:                                                          | How much liquidity to take out in percentage.                               | 25                                                                          |