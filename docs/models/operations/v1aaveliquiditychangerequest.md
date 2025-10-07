# V1AaveLiquidityChangeRequest

## Example Usage

```typescript
import { V1AaveLiquidityChangeRequest } from "@compass-labs/api-sdk/models/operations";

let value: V1AaveLiquidityChangeRequest = {};
```

## Fields

| Field                                                                                          | Type                                                                                           | Required                                                                                       | Description                                                                                    | Example                                                                                        |
| ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| `chain`                                                                                        | [operations.V1AaveLiquidityChangeChain](../../models/operations/v1aaveliquiditychangechain.md) | :heavy_check_mark:                                                                             | N/A                                                                                            |                                                                                                |
| `token`                                                                                        | *string*                                                                                       | :heavy_check_mark:                                                                             | The symbol or address of the asset to get liquidity change for..                               | USDC                                                                                           |
| `startBlock`                                                                                   | *number*                                                                                       | :heavy_check_mark:                                                                             | The start block to calculate liquidity change from.                                            |                                                                                                |
| `endBlock`                                                                                     | *number*                                                                                       | :heavy_check_mark:                                                                             | The end block to calculate liquidity change to.                                                |                                                                                                |