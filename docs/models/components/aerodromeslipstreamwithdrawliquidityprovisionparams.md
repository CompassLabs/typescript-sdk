# AerodromeSlipstreamWithdrawLiquidityProvisionParams

Endpoint parameters for liquidity provision withdrawal on aerodrome slipstream.

This action is performed in a multicall on the NonfungiblePosition Manager: https://github.com/AerodromeSlipstream/v3-periphery/blob/0682387198a24c7cd63566a2c58398533860a5d1/contracts/base/Multicall.sol#L11-L27
First, we call decrease liquidity then collect the tokens owed to the user.

## Example Usage

```typescript
import { AerodromeSlipstreamWithdrawLiquidityProvisionParams } from "@compass-labs/api-sdk/models/components";

let value: AerodromeSlipstreamWithdrawLiquidityProvisionParams = {
  tokenId: 928157,
  percentageForWithdrawal: "25",
};
```

## Fields

| Field                                                                                   | Type                                                                                    | Required                                                                                | Description                                                                             | Example                                                                                 |
| --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------- |
| `actionType`                                                                            | *string*                                                                                | :heavy_minus_sign:                                                                      | N/A                                                                                     |                                                                                         |
| `tokenId`                                                                               | *number*                                                                                | :heavy_check_mark:                                                                      | Token ID of the NFT representing the liquidity provisioned position.                    |                                                                                         |
| `percentageForWithdrawal`                                                               | *components.AerodromeSlipstreamWithdrawLiquidityProvisionParamsPercentageForWithdrawal* | :heavy_check_mark:                                                                      | How much liquidity to take out in percentage.                                           | 25                                                                                      |