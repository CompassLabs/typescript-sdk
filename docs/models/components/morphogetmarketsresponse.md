# MorphoGetMarketsResponse

## Example Usage

```typescript
import { MorphoGetMarketsResponse } from "@compass-labs/api-sdk/models/components";

let value: MorphoGetMarketsResponse = {
  markets: [],
};
```

## Fields

| Field                                                                | Type                                                                 | Required                                                             | Description                                                          |
| -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------- |
| `markets`                                                            | [components.MorphoMarket](../../models/components/morphomarket.md)[] | :heavy_check_mark:                                                   |  A list of markets matching the query.                               |