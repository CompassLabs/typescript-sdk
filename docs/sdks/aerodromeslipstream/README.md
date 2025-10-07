# AerodromeSlipstream
(*aerodromeSlipstream*)

## Overview

### Available Operations

* [aerodromeSlipstreamLiquidityProvisionPositions](#aerodromeslipstreamliquidityprovisionpositions) - List LP Positions
* [aerodromeSlipstreamPoolPrice](#aerodromeslipstreampoolprice) - Pool Price
* [aerodromeSlipstreamSwapSellExactly](#aerodromeslipstreamswapsellexactly) - Swap - from Specified Amount
* [aerodromeSlipstreamSwapBuyExactly](#aerodromeslipstreamswapbuyexactly) - Swap - into Specified Amount
* [aerodromeSlipstreamLiquidityProvisionMint](#aerodromeslipstreamliquidityprovisionmint) - Open a New LP Position
* [aerodromeSlipstreamLiquidityProvisionIncrease](#aerodromeslipstreamliquidityprovisionincrease) - Increase an LP Position
* [aerodromeSlipstreamLiquidityProvisionWithdraw](#aerodromeslipstreamliquidityprovisionwithdraw) - Withdraw an LP Position

## aerodromeSlipstreamLiquidityProvisionPositions

Retrieve the total number of Liquidity Provider (LP) positions associated with a
specific sender.

This endpoint allows users to query and obtain detailed information about their LP
positions, including the number of active positions they hold. The response model,
AerodromeLPPositionsInfo, provides a structured representation of the LP positions
data, ensuring clarity and ease of use. This functionality is essential for users
managing their liquidity provision activities, enabling them to make informed
decisions based on their current positions.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="v1_aerodrome_slipstream_liquidity_provision_positions" method="get" path="/v1/aerodrome_slipstream/liquidity_provision/positions" -->
```typescript
import { CompassApiSDK } from "@compass-labs/api-sdk";

const compassApiSDK = new CompassApiSDK({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await compassApiSDK.aerodromeSlipstream.aerodromeSlipstreamLiquidityProvisionPositions({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { CompassApiSDKCore } from "@compass-labs/api-sdk/core.js";
import { aerodromeSlipstreamAerodromeSlipstreamLiquidityProvisionPositions } from "@compass-labs/api-sdk/funcs/aerodromeSlipstreamAerodromeSlipstreamLiquidityProvisionPositions.js";

// Use `CompassApiSDKCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const compassApiSDK = new CompassApiSDKCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await aerodromeSlipstreamAerodromeSlipstreamLiquidityProvisionPositions(compassApiSDK, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("aerodromeSlipstreamAerodromeSlipstreamLiquidityProvisionPositions failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.V1AerodromeSlipstreamLiquidityProvisionPositionsRequest](../../models/operations/v1aerodromeslipstreamliquidityprovisionpositionsrequest.md)                       | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[components.AerodromeLPPositionsResponse](../../models/components/aerodromelppositionsresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.HTTPValidationError | 422                        | application/json           |
| errors.APIError            | 4XX, 5XX                   | \*/\*                      |

## aerodromeSlipstreamPoolPrice

This endpoint retrieves the current price of a pool, indicating how many token0
you can purchase for 1 token1.

Note that this is an instantaneous price and may change during any trade. For a more
accurate representation of the trade ratios between the two assets, consider using
the quote endpoint.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="v1_aerodrome_slipstream_pool_price" method="get" path="/v1/aerodrome_slipstream/pool_price" -->
```typescript
import { CompassApiSDK } from "@compass-labs/api-sdk";

const compassApiSDK = new CompassApiSDK({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await compassApiSDK.aerodromeSlipstream.aerodromeSlipstreamPoolPrice({
    tokenOut: "USDC",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { CompassApiSDKCore } from "@compass-labs/api-sdk/core.js";
import { aerodromeSlipstreamAerodromeSlipstreamPoolPrice } from "@compass-labs/api-sdk/funcs/aerodromeSlipstreamAerodromeSlipstreamPoolPrice.js";

// Use `CompassApiSDKCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const compassApiSDK = new CompassApiSDKCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await aerodromeSlipstreamAerodromeSlipstreamPoolPrice(compassApiSDK, {
    tokenOut: "USDC",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("aerodromeSlipstreamAerodromeSlipstreamPoolPrice failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.V1AerodromeSlipstreamPoolPriceRequest](../../models/operations/v1aerodromeslipstreampoolpricerequest.md)                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[components.AerodromeSlipstreamPoolPriceResponse](../../models/components/aerodromeslipstreampoolpriceresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.HTTPValidationError | 422                        | application/json           |
| errors.APIError            | 4XX, 5XX                   | \*/\*                      |

## aerodromeSlipstreamSwapSellExactly

This endpoint allows users to trade a specific amount of one token into another
token using the Aerodrome Slipstream protocol.

The transaction is executed by specifying the exact amount of the input token to be
sold, and the system calculates the amount of the output token that will be
received. The operation ensures that the trade is conducted within the constraints
of the current market conditions, taking into account the liquidity and price
impact. This endpoint is suitable for users who want to sell a precise quantity of a
token and are willing to accept the resulting amount of the other token.
                    <Info>
                    **Required Allowances**

                        In order to make this transaction, token allowances need to be set for the following contracts.

                     - `AerodromeSlipstreamRouter`
                    </Info>
                

### Example Usage

<!-- UsageSnippet language="typescript" operationID="v1_aerodrome_slipstream_swap_sell_exactly" method="post" path="/v1/aerodrome_slipstream/swap/sell_exactly" -->
```typescript
import { CompassApiSDK } from "@compass-labs/api-sdk";

const compassApiSDK = new CompassApiSDK({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await compassApiSDK.aerodromeSlipstream.aerodromeSlipstreamSwapSellExactly({
    tokenIn: "WETH",
    tokenOut: "WETH",
    tickSpacing: 100,
    amountIn: 1.5,
    amountOutMinimum: 1.4,
    chain: "base",
    sender: "0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { CompassApiSDKCore } from "@compass-labs/api-sdk/core.js";
import { aerodromeSlipstreamAerodromeSlipstreamSwapSellExactly } from "@compass-labs/api-sdk/funcs/aerodromeSlipstreamAerodromeSlipstreamSwapSellExactly.js";

// Use `CompassApiSDKCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const compassApiSDK = new CompassApiSDKCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await aerodromeSlipstreamAerodromeSlipstreamSwapSellExactly(compassApiSDK, {
    tokenIn: "WETH",
    tokenOut: "WETH",
    tickSpacing: 100,
    amountIn: 1.5,
    amountOutMinimum: 1.4,
    chain: "base",
    sender: "0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("aerodromeSlipstreamAerodromeSlipstreamSwapSellExactly failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [components.AerodromeSlipstreamSellExactlyRequest](../../models/components/aerodromeslipstreamsellexactlyrequest.md)                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[components.TransactionResponse](../../models/components/transactionresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.HTTPValidationError | 422                        | application/json           |
| errors.APIError            | 4XX, 5XX                   | \*/\*                      |

## aerodromeSlipstreamSwapBuyExactly

This endpoint facilitates the trading of tokens by allowing users to specify the
exact amount of the output token they wish to receive.

Utilizing the Aerodrome Slipstream protocol, the system calculates the necessary
amount of the input token required to achieve the desired output. This operation is
particularly useful for users who have a specific target amount of the output token
in mind and are willing to provide the corresponding input token amount. The
transaction is executed with consideration of current market conditions, including
liquidity and price impact, ensuring that the trade is completed efficiently and
effectively.
                    <Info>
                    **Required Allowances**

                        In order to make this transaction, token allowances need to be set for the following contracts.

                     - `AerodromeSlipstreamRouter`
                    </Info>
                

### Example Usage

<!-- UsageSnippet language="typescript" operationID="v1_aerodrome_slipstream_swap_buy_exactly" method="post" path="/v1/aerodrome_slipstream/swap/buy_exactly" -->
```typescript
import { CompassApiSDK } from "@compass-labs/api-sdk";

const compassApiSDK = new CompassApiSDK({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await compassApiSDK.aerodromeSlipstream.aerodromeSlipstreamSwapBuyExactly({
    tokenIn: "WETH",
    tokenOut: "WETH",
    tickSpacing: 100,
    amountOut: 1.5,
    amountInMaximum: 1.6,
    chain: "base",
    sender: "0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { CompassApiSDKCore } from "@compass-labs/api-sdk/core.js";
import { aerodromeSlipstreamAerodromeSlipstreamSwapBuyExactly } from "@compass-labs/api-sdk/funcs/aerodromeSlipstreamAerodromeSlipstreamSwapBuyExactly.js";

// Use `CompassApiSDKCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const compassApiSDK = new CompassApiSDKCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await aerodromeSlipstreamAerodromeSlipstreamSwapBuyExactly(compassApiSDK, {
    tokenIn: "WETH",
    tokenOut: "WETH",
    tickSpacing: 100,
    amountOut: 1.5,
    amountInMaximum: 1.6,
    chain: "base",
    sender: "0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("aerodromeSlipstreamAerodromeSlipstreamSwapBuyExactly failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [components.AerodromeSlipstreamBuyExactlyRequest](../../models/components/aerodromeslipstreambuyexactlyrequest.md)                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[components.TransactionResponse](../../models/components/transactionresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.HTTPValidationError | 422                        | application/json           |
| errors.APIError            | 4XX, 5XX                   | \*/\*                      |

## aerodromeSlipstreamLiquidityProvisionMint

Initiate a new Liquidity Provider (LP) position by minting tokens.

This endpoint allows users to open a new LP position, enabling them to participate
in liquidity provision. The minting process involves creating a new position with
specified parameters, such as token amounts and pool details. The response will
confirm the successful creation of the LP position, providing users with the
necessary information to manage their newly minted position. This functionality is
crucial for users looking to expand their liquidity provision activities, offering
them the opportunity to engage in decentralized finance (DeFi) markets effectively.
                    <Info>
                    **Required Allowances**

                        In order to make this transaction, token allowances need to be set for the following contracts.

                     - `AerodromeSlipstreamNonfungiblePositionManager`
                    </Info>
                

### Example Usage

<!-- UsageSnippet language="typescript" operationID="v1_aerodrome_slipstream_liquidity_provision_mint" method="post" path="/v1/aerodrome_slipstream/liquidity_provision/mint" -->
```typescript
import { CompassApiSDK } from "@compass-labs/api-sdk";

const compassApiSDK = new CompassApiSDK({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await compassApiSDK.aerodromeSlipstream.aerodromeSlipstreamLiquidityProvisionMint({
    token0: "WETH",
    token1: "USDC",
    tickSpacing: 100,
    tickLower: -1000,
    tickUpper: 1000,
    amount0Desired: "1.5",
    amount1Desired: "1.7",
    amount0Min: "1.4",
    amount1Min: "1.6",
    recipient: "0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B",
    chain: "base",
    sender: "0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { CompassApiSDKCore } from "@compass-labs/api-sdk/core.js";
import { aerodromeSlipstreamAerodromeSlipstreamLiquidityProvisionMint } from "@compass-labs/api-sdk/funcs/aerodromeSlipstreamAerodromeSlipstreamLiquidityProvisionMint.js";

// Use `CompassApiSDKCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const compassApiSDK = new CompassApiSDKCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await aerodromeSlipstreamAerodromeSlipstreamLiquidityProvisionMint(compassApiSDK, {
    token0: "WETH",
    token1: "USDC",
    tickSpacing: 100,
    tickLower: -1000,
    tickUpper: 1000,
    amount0Desired: "1.5",
    amount1Desired: "1.7",
    amount0Min: "1.4",
    amount1Min: "1.6",
    recipient: "0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B",
    chain: "base",
    sender: "0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("aerodromeSlipstreamAerodromeSlipstreamLiquidityProvisionMint failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [components.AerodromeSlipstreamMintLiquidityProvisionRequest](../../models/components/aerodromeslipstreammintliquidityprovisionrequest.md)                                     | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[components.TransactionResponse](../../models/components/transactionresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.HTTPValidationError | 422                        | application/json           |
| errors.APIError            | 4XX, 5XX                   | \*/\*                      |

## aerodromeSlipstreamLiquidityProvisionIncrease

Increase the liquidity of an existing Liquidity Provider (LP) position.

This endpoint allows users to add more tokens to their current LP position,
enhancing their participation in liquidity provision. By increasing liquidity, users
can potentially earn more rewards and improve their position in the pool. The
process involves specifying additional token amounts and updating the pool details.
The response will confirm the successful increase of the LP position, providing
users with updated information about their enhanced position. This functionality is
vital for users aiming to optimize their liquidity provision strategy, enabling them
to adapt to market conditions and maximize their returns in decentralized finance
(DeFi) markets.
                    <Info>
                    **Required Allowances**

                        In order to make this transaction, token allowances need to be set for the following contracts.

                     - `AerodromeSlipstreamRouter`
                    </Info>
                

### Example Usage

<!-- UsageSnippet language="typescript" operationID="v1_aerodrome_slipstream_liquidity_provision_increase" method="post" path="/v1/aerodrome_slipstream/liquidity_provision/increase" -->
```typescript
import { CompassApiSDK } from "@compass-labs/api-sdk";

const compassApiSDK = new CompassApiSDK({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await compassApiSDK.aerodromeSlipstream.aerodromeSlipstreamLiquidityProvisionIncrease({
    tokenId: 312701,
    amount0Desired: "1.5",
    amount1Desired: "1.7",
    amount0Min: "1.4",
    amount1Min: "1.6",
    chain: "base",
    sender: "0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { CompassApiSDKCore } from "@compass-labs/api-sdk/core.js";
import { aerodromeSlipstreamAerodromeSlipstreamLiquidityProvisionIncrease } from "@compass-labs/api-sdk/funcs/aerodromeSlipstreamAerodromeSlipstreamLiquidityProvisionIncrease.js";

// Use `CompassApiSDKCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const compassApiSDK = new CompassApiSDKCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await aerodromeSlipstreamAerodromeSlipstreamLiquidityProvisionIncrease(compassApiSDK, {
    tokenId: 312701,
    amount0Desired: "1.5",
    amount1Desired: "1.7",
    amount0Min: "1.4",
    amount1Min: "1.6",
    chain: "base",
    sender: "0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("aerodromeSlipstreamAerodromeSlipstreamLiquidityProvisionIncrease failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [components.AerodromeSlipstreamIncreaseLiquidityProvisionRequest](../../models/components/aerodromeslipstreamincreaseliquidityprovisionrequest.md)                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[components.TransactionResponse](../../models/components/transactionresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.HTTPValidationError | 422                        | application/json           |
| errors.APIError            | 4XX, 5XX                   | \*/\*                      |

## aerodromeSlipstreamLiquidityProvisionWithdraw

Withdraw an existing Liquidity Provider (LP) position.

This endpoint allows users to remove their tokens from an LP position, effectively
closing their participation in the liquidity pool. The withdrawal process involves
specifying the LP position to be closed, and the response will confirm the
successful removal of liquidity, providing users with details about the withdrawn
tokens and any remaining balances. This functionality is essential for users who
wish to exit their liquidity provision activities, enabling them to reclaim their
assets and potentially reallocate them to other investment opportunities. The
endpoint ensures a smooth and secure withdrawal process, facilitating users'
strategic management of their decentralized finance (DeFi) portfolios.
                    <Info>
                    **Required Allowances**

                        In order to make this transaction, token allowances need to be set for the following contracts.

                     - `AerodromeSlipstreamNonfungiblePositionManager`
                    </Info>
                

### Example Usage

<!-- UsageSnippet language="typescript" operationID="v1_aerodrome_slipstream_liquidity_provision_withdraw" method="post" path="/v1/aerodrome_slipstream/liquidity_provision/withdraw" -->
```typescript
import { CompassApiSDK } from "@compass-labs/api-sdk";

const compassApiSDK = new CompassApiSDK({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await compassApiSDK.aerodromeSlipstream.aerodromeSlipstreamLiquidityProvisionWithdraw({
    tokenId: 415732,
    percentageForWithdrawal: "25",
    chain: "base",
    sender: "0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B",
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { CompassApiSDKCore } from "@compass-labs/api-sdk/core.js";
import { aerodromeSlipstreamAerodromeSlipstreamLiquidityProvisionWithdraw } from "@compass-labs/api-sdk/funcs/aerodromeSlipstreamAerodromeSlipstreamLiquidityProvisionWithdraw.js";

// Use `CompassApiSDKCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const compassApiSDK = new CompassApiSDKCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await aerodromeSlipstreamAerodromeSlipstreamLiquidityProvisionWithdraw(compassApiSDK, {
    tokenId: 415732,
    percentageForWithdrawal: "25",
    chain: "base",
    sender: "0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("aerodromeSlipstreamAerodromeSlipstreamLiquidityProvisionWithdraw failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [components.AerodromeSlipstreamWithdrawLiquidityProvisionRequest](../../models/components/aerodromeslipstreamwithdrawliquidityprovisionrequest.md)                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[components.TransactionResponse](../../models/components/transactionresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.HTTPValidationError | 422                        | application/json           |
| errors.APIError            | 4XX, 5XX                   | \*/\*                      |