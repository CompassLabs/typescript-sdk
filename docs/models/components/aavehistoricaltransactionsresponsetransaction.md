# AaveHistoricalTransactionsResponseTransaction


## Supported Types

### `components.Borrow`

```typescript
const value: components.Borrow = {
  id: "<id>",
  timestamp: 132507,
  txHash: "<value>",
  amount: 5726.04,
  borrowRateMode: 1,
  reserve: {
    symbol: "<value>",
    name: "<value>",
    underlyingAsset: "0x68b3465833fb72A70ecDF485E0e4C7bD8665Fc45",
  },
  assetPriceUSD: 1903.46,
  block: 106046,
};
```

### `components.LiquidationCall`

```typescript
const value: components.LiquidationCall = {
  id: "<id>",
  timestamp: 906796,
  txHash: "<value>",
  collateralAmount: 3903,
  collateralReserve: {
    symbol: "<value>",
    name: "<value>",
    underlyingAsset: "0x68b3465833fb72A70ecDF485E0e4C7bD8665Fc45",
  },
  principalAmount: 1013.27,
  principalReserve: {
    symbol: "<value>",
    name: "<value>",
    underlyingAsset: "0x68b3465833fb72A70ecDF485E0e4C7bD8665Fc45",
  },
  collateralAssetPriceUSD: 1927.57,
  borrowAssetPriceUSD: 3105.83,
  block: 548176,
};
```

### `components.RedeemUnderlying`

```typescript
const value: components.RedeemUnderlying = {
  id: "<id>",
  timestamp: 728000,
  txHash: "<value>",
  amount: 3604.23,
  reserve: {
    symbol: "<value>",
    name: "<value>",
    underlyingAsset: "0x68b3465833fb72A70ecDF485E0e4C7bD8665Fc45",
  },
  assetPriceUSD: 8661.96,
  action: "<value>",
  block: 663426,
};
```

### `components.Repay`

```typescript
const value: components.Repay = {
  id: "<id>",
  timestamp: 529023,
  txHash: "<value>",
  amount: 9272.21,
  reserve: {
    symbol: "<value>",
    name: "<value>",
    underlyingAsset: "0x68b3465833fb72A70ecDF485E0e4C7bD8665Fc45",
  },
  assetPriceUSD: 3951.28,
  block: 361702,
};
```

### `components.Supply`

```typescript
const value: components.Supply = {
  id: "<id>",
  timestamp: 177043,
  txHash: "<value>",
  amount: 5023.38,
  reserve: {
    symbol: "<value>",
    name: "<value>",
    underlyingAsset: "0x68b3465833fb72A70ecDF485E0e4C7bD8665Fc45",
  },
  assetPriceUSD: 2731.57,
  block: 626983,
};
```

### `components.SwapBorrowRate`

```typescript
const value: components.SwapBorrowRate = {
  id: "<id>",
  timestamp: 661095,
  txHash: "<value>",
  borrowRateModeFrom: 740235,
  borrowRateModeTo: 239047,
  variableBorrowRate: 179223,
  stableBorrowRate: 225369,
  reserve: {
    symbol: "<value>",
    name: "<value>",
    underlyingAsset: "0x68b3465833fb72A70ecDF485E0e4C7bD8665Fc45",
  },
  block: 364832,
};
```

### `components.UsageAsCollateral`

```typescript
const value: components.UsageAsCollateral = {
  id: "<id>",
  timestamp: 393669,
  txHash: "<value>",
  fromState: false,
  toState: false,
  reserve: {
    symbol: "<value>",
    name: "<value>",
    underlyingAsset: "0x68b3465833fb72A70ecDF485E0e4C7bD8665Fc45",
  },
  block: 936532,
};
```

