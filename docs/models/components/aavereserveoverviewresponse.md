# AaveReserveOverviewResponse

## Example Usage

```typescript
import { AaveReserveOverviewResponse } from "@compass-labs/api-sdk/models/components";

let value: AaveReserveOverviewResponse = {
  tvl: 4647.39,
  totalBorrowed: 658.65,
  utilizationRatio: 3833.45,
};
```

## Fields

| Field                                                                                                                                     | Type                                                                                                                                      | Required                                                                                                                                  | Description                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------- |
| `tvl`                                                                                                                                     | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Total tokens supplied in an Aave Reserve in USD. E.G. How much WBTC has been supplied on Aave in USD.                                     |
| `totalBorrowed`                                                                                                                           | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Total tokens borrowed in an Aave Reserve converted to USD. E.G. How much WBTC has been supplied on Aave (in USD).                         |
| `utilizationRatio`                                                                                                                        | *number*                                                                                                                                  | :heavy_check_mark:                                                                                                                        | Total borrowed divided by total supplied in an Aave Reserve. E.G. How much WBTC has been borrowed on Aaave divided by the amount supplied |