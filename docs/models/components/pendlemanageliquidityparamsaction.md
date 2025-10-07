# PendleManageLiquidityParamsAction

Specifies the direction of the liquidity operation for the Pendle market. Valid values are `SUPPLY` (to add liquidity) or `WITHDRAW` (to remove liquidity).

## Example Usage

```typescript
import { PendleManageLiquidityParamsAction } from "@compass-labs/api-sdk/models/components";

let value: PendleManageLiquidityParamsAction = "SUPPLY";
```

## Values

```typescript
"SUPPLY" | "WITHDRAW"
```