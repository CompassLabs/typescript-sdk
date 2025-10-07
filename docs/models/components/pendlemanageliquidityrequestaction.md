# PendleManageLiquidityRequestAction

Specifies the direction of the liquidity operation for the Pendle market. Valid values are `SUPPLY` (to add liquidity) or `WITHDRAW` (to remove liquidity).

## Example Usage

```typescript
import { PendleManageLiquidityRequestAction } from "@compass-labs/api-sdk/models/components";

let value: PendleManageLiquidityRequestAction = "SUPPLY";
```

## Values

```typescript
"SUPPLY" | "WITHDRAW"
```