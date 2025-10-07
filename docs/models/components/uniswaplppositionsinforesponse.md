# UniswapLPPositionsInfoResponse

## Example Usage

```typescript
import { UniswapLPPositionsInfoResponse } from "@compass-labs/api-sdk/models/components";

let value: UniswapLPPositionsInfoResponse = {
  positions: {},
};
```

## Fields

| Field                                                                                                                      | Type                                                                                                                       | Required                                                                                                                   | Description                                                                                                                |
| -------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| `positions`                                                                                                                | Record<string, [components.UniswapPositionsSolidityResponse](../../models/components/uniswappositionssolidityresponse.md)> | :heavy_check_mark:                                                                                                         |  Liquidity provision positions belonging to a particular user keyed by the<br/>        token of owner index of the position.  |