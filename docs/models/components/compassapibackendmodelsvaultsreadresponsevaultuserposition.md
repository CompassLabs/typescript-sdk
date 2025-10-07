# CompassApiBackendModelsVaultsReadResponseVaultUserPosition

## Example Usage

```typescript
import { CompassApiBackendModelsVaultsReadResponseVaultUserPosition } from "@compass-labs/api-sdk/models/components";

let value: CompassApiBackendModelsVaultsReadResponseVaultUserPosition = {
  amountOfShares: "<value>",
  amountInUnderlyingToken: "<value>",
};
```

## Fields

| Field                                                                                                         | Type                                                                                                          | Required                                                                                                      | Description                                                                                                   |
| ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- |
| `amountOfShares`                                                                                              | *string*                                                                                                      | :heavy_check_mark:                                                                                            | The number of vault share tokens representing the user’s proportional ownership of the assets in the vault.   |
| `amountInUnderlyingToken`                                                                                     | *string*                                                                                                      | :heavy_check_mark:                                                                                            | The equivalent value of the user’s vault shares, denominated in the vault’s underlying asset (deposit token). |