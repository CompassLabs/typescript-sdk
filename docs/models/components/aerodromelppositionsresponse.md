# AerodromeLPPositionsResponse

## Example Usage

```typescript
import { AerodromeLPPositionsResponse } from "@compass-labs/api-sdk/models/components";

let value: AerodromeLPPositionsResponse = {
  positions: {},
};
```

## Fields

| Field                                                                                                                                                             | Type                                                                                                                                                              | Required                                                                                                                                                          | Description                                                                                                                                                       |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `positions`                                                                                                                                                       | Record<string, [components.AerodromePosition](../../models/components/aerodromeposition.md)>                                                                      | :heavy_check_mark:                                                                                                                                                | Liquidity provision positions belonging to a particular user. The key is a<br/>tuple of the token0, token1, tick_spacing, tick_lower, and tick_upper of the position. |