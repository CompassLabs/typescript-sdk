# UniswapV3
(*uniswapV3*)

## Overview

### Available Operations

* [uniswapQuoteBuyExactly](#uniswapquotebuyexactly) - Get Quote - to Specified Amount
* [uniswapQuoteSellExactly](#uniswapquotesellexactly) - Get quote - From Specified Amount
* [uniswapPoolPrice](#uniswappoolprice) - Pool Price
* [uniswapLiquidityProvisionInRange](#uniswapliquidityprovisioninrange) - Check if LP is Active.
* [uniswapLiquidityProvisionPositions](#uniswapliquidityprovisionpositions) - List LP
* [uniswapSwapBuyExactly](#uniswapswapbuyexactly) - Buy exact amount
* [uniswapSwapSellExactly](#uniswapswapsellexactly) - Sell exact amount
* [uniswapLiquidityProvisionMint](#uniswapliquidityprovisionmint) - Open a new LP position
* [uniswapLiquidityProvisionIncrease](#uniswapliquidityprovisionincrease) - Increase an LP position
* [uniswapLiquidityProvisionWithdraw](#uniswapliquidityprovisionwithdraw) - Withdraw an LP position

## uniswapQuoteBuyExactly

This endpoint calculates the amount of input tokens required to purchase a
specified amount of output tokens from a Uniswap pool.

It also provides the resulting price after the transaction. The calculation takes
into account the current pool state and the specified fee tier.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="v1_uniswap_quote_buy_exactly" method="get" path="/v1/uniswap/quote/buy_exactly" -->
```typescript
import { CompassApiSDK } from "@compass-labs/api-sdk";

const compassApiSDK = new CompassApiSDK({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await compassApiSDK.uniswapV3.uniswapQuoteBuyExactly({
    tokenOut: "USDC",
    amountOut: 9572.21,
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { CompassApiSDKCore } from "@compass-labs/api-sdk/core.js";
import { uniswapV3UniswapQuoteBuyExactly } from "@compass-labs/api-sdk/funcs/uniswapV3UniswapQuoteBuyExactly.js";

// Use `CompassApiSDKCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const compassApiSDK = new CompassApiSDKCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await uniswapV3UniswapQuoteBuyExactly(compassApiSDK, {
    tokenOut: "USDC",
    amountOut: 9572.21,
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("uniswapV3UniswapQuoteBuyExactly failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.V1UniswapQuoteBuyExactlyRequest](../../models/operations/v1uniswapquotebuyexactlyrequest.md)                                                                       | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[components.UniswapBuyQuoteInfoResponse](../../models/components/uniswapbuyquoteinforesponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.HTTPValidationError | 422                        | application/json           |
| errors.APIError            | 4XX, 5XX                   | \*/\*                      |

## uniswapQuoteSellExactly

This endpoint calculates the amount of input tokens required to purchase a
specified amount of output tokens from a Uniswap pool.

It also provides the resulting price after the transaction. The calculation takes
into account the current pool state and the specified fee tier.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="v1_uniswap_quote_sell_exactly" method="get" path="/v1/uniswap/quote/sell_exactly" -->
```typescript
import { CompassApiSDK } from "@compass-labs/api-sdk";

const compassApiSDK = new CompassApiSDK({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await compassApiSDK.uniswapV3.uniswapQuoteSellExactly({
    tokenOut: "USDC",
    amountIn: 4736.09,
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { CompassApiSDKCore } from "@compass-labs/api-sdk/core.js";
import { uniswapV3UniswapQuoteSellExactly } from "@compass-labs/api-sdk/funcs/uniswapV3UniswapQuoteSellExactly.js";

// Use `CompassApiSDKCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const compassApiSDK = new CompassApiSDKCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await uniswapV3UniswapQuoteSellExactly(compassApiSDK, {
    tokenOut: "USDC",
    amountIn: 4736.09,
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("uniswapV3UniswapQuoteSellExactly failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.V1UniswapQuoteSellExactlyRequest](../../models/operations/v1uniswapquotesellexactlyrequest.md)                                                                     | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[components.UniswapSellQuoteInfoResponse](../../models/components/uniswapsellquoteinforesponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.HTTPValidationError | 422                        | application/json           |
| errors.APIError            | 4XX, 5XX                   | \*/\*                      |

## uniswapPoolPrice

This endpoint calculates the price of a token in a Uniswap pool.

The price is calculated based on the current pool state and the specified fee tier.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="v1_uniswap_pool_price" method="get" path="/v1/uniswap/pool_price" -->
```typescript
import { CompassApiSDK } from "@compass-labs/api-sdk";

const compassApiSDK = new CompassApiSDK({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await compassApiSDK.uniswapV3.uniswapPoolPrice({
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
import { uniswapV3UniswapPoolPrice } from "@compass-labs/api-sdk/funcs/uniswapV3UniswapPoolPrice.js";

// Use `CompassApiSDKCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const compassApiSDK = new CompassApiSDKCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await uniswapV3UniswapPoolPrice(compassApiSDK, {
    tokenOut: "USDC",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("uniswapV3UniswapPoolPrice failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.V1UniswapPoolPriceRequest](../../models/operations/v1uniswappoolpricerequest.md)                                                                                   | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[components.UniswapPoolPriceResponse](../../models/components/uniswappoolpriceresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.HTTPValidationError | 422                        | application/json           |
| errors.APIError            | 4XX, 5XX                   | \*/\*                      |

## uniswapLiquidityProvisionInRange

This endpoint allows users to check whether a specific liquidity provider ()
position is within the active tick range on the uniswap platform.

by providing the token id associated with the position, users can verify if the
position is currently within the tick range where trading occurs. this information
is essential for users to monitor the status of their lp positions and ensure that
they are actively participating in the trading activities within the liquidity pool
and earning trading fees.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="v1_uniswap_liquidity_provision_in_range" method="get" path="/v1/uniswap/liquidity_provision/in_range" -->
```typescript
import { CompassApiSDK } from "@compass-labs/api-sdk";

const compassApiSDK = new CompassApiSDK({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await compassApiSDK.uniswapV3.uniswapLiquidityProvisionInRange({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { CompassApiSDKCore } from "@compass-labs/api-sdk/core.js";
import { uniswapV3UniswapLiquidityProvisionInRange } from "@compass-labs/api-sdk/funcs/uniswapV3UniswapLiquidityProvisionInRange.js";

// Use `CompassApiSDKCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const compassApiSDK = new CompassApiSDKCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await uniswapV3UniswapLiquidityProvisionInRange(compassApiSDK, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("uniswapV3UniswapLiquidityProvisionInRange failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.V1UniswapLiquidityProvisionInRangeRequest](../../models/operations/v1uniswapliquidityprovisioninrangerequest.md)                                                   | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[components.UniswapCheckInRangeResponse](../../models/components/uniswapcheckinrangeresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.HTTPValidationError | 422                        | application/json           |
| errors.APIError            | 4XX, 5XX                   | \*/\*                      |

## uniswapLiquidityProvisionPositions

This endpoint retrieves the number of Liquidity Provider (LP) positions
associated with a specific sender address on the Uniswap platform.

Users can query this endpoint to obtain detailed information about their LP
positions, including the total number of positions and relevant metadata. This
information is crucial for users to manage and analyze their liquidity provision
activities effectively.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="v1_uniswap_liquidity_provision_positions" method="get" path="/v1/uniswap/liquidity_provision/positions" -->
```typescript
import { CompassApiSDK } from "@compass-labs/api-sdk";

const compassApiSDK = new CompassApiSDK({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await compassApiSDK.uniswapV3.uniswapLiquidityProvisionPositions({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { CompassApiSDKCore } from "@compass-labs/api-sdk/core.js";
import { uniswapV3UniswapLiquidityProvisionPositions } from "@compass-labs/api-sdk/funcs/uniswapV3UniswapLiquidityProvisionPositions.js";

// Use `CompassApiSDKCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const compassApiSDK = new CompassApiSDKCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await uniswapV3UniswapLiquidityProvisionPositions(compassApiSDK, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("uniswapV3UniswapLiquidityProvisionPositions failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.V1UniswapLiquidityProvisionPositionsRequest](../../models/operations/v1uniswapliquidityprovisionpositionsrequest.md)                                               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[components.UniswapLPPositionsInfoResponse](../../models/components/uniswaplppositionsinforesponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.HTTPValidationError | 422                        | application/json           |
| errors.APIError            | 4XX, 5XX                   | \*/\*                      |

## uniswapSwapBuyExactly

This endpoint allows users to trade a variable amount of one token to receive an
exact amount of another token using the Uniswap protocol.

The transaction is executed on the specified blockchain network, and the user must
provide the necessary transaction details, including the token to buy, the token to
pay with, and the exact amount to receive. If the token being paid with is ETH and
needs to be wrapped, the appropriate amount will be wrapped automatically.
                    <Info>
                    **Required Allowances**

                        In order to make this transaction, token allowances need to be set for the following contracts.

                     - `UniswapV3Router`
                    </Info>
                

### Example Usage

<!-- UsageSnippet language="typescript" operationID="v1_uniswap_swap_buy_exactly" method="post" path="/v1/uniswap/swap/buy_exactly" -->
```typescript
import { CompassApiSDK } from "@compass-labs/api-sdk";

const compassApiSDK = new CompassApiSDK({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await compassApiSDK.uniswapV3.uniswapSwapBuyExactly({
    tokenIn: "WETH",
    tokenOut: "WETH",
    fee: "1.0",
    amountOut: 1.5,
    maxSlippagePercent: 0.5,
    chain: "ethereum",
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
import { uniswapV3UniswapSwapBuyExactly } from "@compass-labs/api-sdk/funcs/uniswapV3UniswapSwapBuyExactly.js";

// Use `CompassApiSDKCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const compassApiSDK = new CompassApiSDKCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await uniswapV3UniswapSwapBuyExactly(compassApiSDK, {
    tokenIn: "WETH",
    tokenOut: "WETH",
    fee: "1.0",
    amountOut: 1.5,
    maxSlippagePercent: 0.5,
    chain: "ethereum",
    sender: "0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("uniswapV3UniswapSwapBuyExactly failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [components.UniswapBuyExactlyRequest](../../models/components/uniswapbuyexactlyrequest.md)                                                                                     | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[components.UniswapBuyExactlyTransactionResponse](../../models/components/uniswapbuyexactlytransactionresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.HTTPValidationError | 422                        | application/json           |
| errors.APIError            | 4XX, 5XX                   | \*/\*                      |

## uniswapSwapSellExactly

This endpoint allows users to trade a specific amount of one token into another
token using the Uniswap protocol.

The transaction is executed on the specified blockchain network, and the user must
provide the necessary transaction details, including the token to sell, the token to
receive, and the amount to sell. If the token being sold is ETH and needs to be
wrapped, the appropriate amount will be wrapped automatically.
                    <Info>
                    **Required Allowances**

                        In order to make this transaction, token allowances need to be set for the following contracts.

                     - `UniswapV3Router`
                    </Info>
                

### Example Usage

<!-- UsageSnippet language="typescript" operationID="v1_uniswap_swap_sell_exactly" method="post" path="/v1/uniswap/swap/sell_exactly" -->
```typescript
import { CompassApiSDK } from "@compass-labs/api-sdk";

const compassApiSDK = new CompassApiSDK({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await compassApiSDK.uniswapV3.uniswapSwapSellExactly({
    tokenIn: "WETH",
    tokenOut: "WETH",
    fee: "1.0",
    amountIn: 1.5,
    maxSlippagePercent: 0.5,
    chain: "ethereum",
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
import { uniswapV3UniswapSwapSellExactly } from "@compass-labs/api-sdk/funcs/uniswapV3UniswapSwapSellExactly.js";

// Use `CompassApiSDKCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const compassApiSDK = new CompassApiSDKCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await uniswapV3UniswapSwapSellExactly(compassApiSDK, {
    tokenIn: "WETH",
    tokenOut: "WETH",
    fee: "1.0",
    amountIn: 1.5,
    maxSlippagePercent: 0.5,
    chain: "ethereum",
    sender: "0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("uniswapV3UniswapSwapSellExactly failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [components.UniswapSellExactlyRequest](../../models/components/uniswapsellexactlyrequest.md)                                                                                   | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[components.UniswapSellExactlyTransactionResponse](../../models/components/uniswapsellexactlytransactionresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.HTTPValidationError | 422                        | application/json           |
| errors.APIError            | 4XX, 5XX                   | \*/\*                      |

## uniswapLiquidityProvisionMint

This endpoint allows users to open a new Liquidity Provider (LP) position on the
Uniswap platform.

By providing the necessary parameters, users can initiate a minting process to
create a new LP token, which represents their stake in a specific liquidity pool.
This operation is essential for users looking to participate in liquidity provision,
enabling them to earn fees from trades that occur within the pool. The endpoint
requires details such as the token pair, amount, and any additional parameters
needed for the minting process.
                    <Info>
                    **Required Allowances**

                        In order to make this transaction, token allowances need to be set for the following contracts.

                     - `UniswapV3NFTPositionManager`
                    </Info>
                

### Example Usage

<!-- UsageSnippet language="typescript" operationID="v1_uniswap_liquidity_provision_mint" method="post" path="/v1/uniswap/liquidity_provision/mint" -->
```typescript
import { CompassApiSDK } from "@compass-labs/api-sdk";

const compassApiSDK = new CompassApiSDK({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await compassApiSDK.uniswapV3.uniswapLiquidityProvisionMint({
    token0: "WETH",
    token1: "WETH",
    fee: "0.05",
    tickLower: -1000,
    tickUpper: 1000,
    amount0Desired: "1.5",
    amount1Desired: "1.7",
    amount0Min: "1.4",
    amount1Min: "1.6",
    recipient: "0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B",
    chain: "arbitrum",
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
import { uniswapV3UniswapLiquidityProvisionMint } from "@compass-labs/api-sdk/funcs/uniswapV3UniswapLiquidityProvisionMint.js";

// Use `CompassApiSDKCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const compassApiSDK = new CompassApiSDKCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await uniswapV3UniswapLiquidityProvisionMint(compassApiSDK, {
    token0: "WETH",
    token1: "WETH",
    fee: "0.05",
    tickLower: -1000,
    tickUpper: 1000,
    amount0Desired: "1.5",
    amount1Desired: "1.7",
    amount0Min: "1.4",
    amount1Min: "1.6",
    recipient: "0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B",
    chain: "arbitrum",
    sender: "0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("uniswapV3UniswapLiquidityProvisionMint failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [components.UniswapMintLiquidityProvisionRequest](../../models/components/uniswapmintliquidityprovisionrequest.md)                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
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

## uniswapLiquidityProvisionIncrease

This endpoint allows users to increase their existing Liquidity Provider (LP)
positions on the Uniswap platform.

By providing the necessary parameters, users can add more liquidity to their current
positions, thereby increasing their stake in the liquidity pool. This operation is
beneficial for users who wish to enhance their potential earnings from trading fees
within the pool. The endpoint requires details such as the token pair, additional
amount to be added, and any other parameters necessary for the liquidity increase
process.
                    <Info>
                    **Required Allowances**

                        In order to make this transaction, token allowances need to be set for the following contracts.

                     - `AerodromeSlipstreamRouter`
                    </Info>
                

### Example Usage

<!-- UsageSnippet language="typescript" operationID="v1_uniswap_liquidity_provision_increase" method="post" path="/v1/uniswap/liquidity_provision/increase" -->
```typescript
import { CompassApiSDK } from "@compass-labs/api-sdk";

const compassApiSDK = new CompassApiSDK({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await compassApiSDK.uniswapV3.uniswapLiquidityProvisionIncrease({
    tokenId: 991701,
    amount0Desired: "1.5",
    amount1Desired: "1.7",
    amount0Min: "1.4",
    amount1Min: "1.6",
    chain: "ethereum",
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
import { uniswapV3UniswapLiquidityProvisionIncrease } from "@compass-labs/api-sdk/funcs/uniswapV3UniswapLiquidityProvisionIncrease.js";

// Use `CompassApiSDKCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const compassApiSDK = new CompassApiSDKCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await uniswapV3UniswapLiquidityProvisionIncrease(compassApiSDK, {
    tokenId: 991701,
    amount0Desired: "1.5",
    amount1Desired: "1.7",
    amount0Min: "1.4",
    amount1Min: "1.6",
    chain: "ethereum",
    sender: "0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("uniswapV3UniswapLiquidityProvisionIncrease failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [components.UniswapIncreaseLiquidityProvisionRequest](../../models/components/uniswapincreaseliquidityprovisionrequest.md)                                                     | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
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

## uniswapLiquidityProvisionWithdraw

This endpoint allows users to withdraw their Liquidity Provider (LP) positions
from the Uniswap platform.

By specifying the necessary parameters, users can initiate the withdrawal process to
remove their stake from a specific liquidity pool. This operation is crucial for
users who wish to reclaim their assets or reallocate their liquidity to different
pools or investments. The endpoint requires details such as the token pair, the
amount to be withdrawn, and any additional parameters needed for the withdrawal
process. Users should ensure they meet any protocol requirements or conditions
before initiating a withdrawal to avoid potential issues or penalties.
                    <Info>
                    **Required Allowances**

                        In order to make this transaction, token allowances need to be set for the following contracts.

                     - `UniswapV3NFTPositionManager`
                    </Info>
                

### Example Usage

<!-- UsageSnippet language="typescript" operationID="v1_uniswap_liquidity_provision_withdraw" method="post" path="/v1/uniswap/liquidity_provision/withdraw" -->
```typescript
import { CompassApiSDK } from "@compass-labs/api-sdk";

const compassApiSDK = new CompassApiSDK({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await compassApiSDK.uniswapV3.uniswapLiquidityProvisionWithdraw({
    tokenId: 821299,
    percentageForWithdrawal: "25",
    chain: "ethereum",
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
import { uniswapV3UniswapLiquidityProvisionWithdraw } from "@compass-labs/api-sdk/funcs/uniswapV3UniswapLiquidityProvisionWithdraw.js";

// Use `CompassApiSDKCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const compassApiSDK = new CompassApiSDKCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await uniswapV3UniswapLiquidityProvisionWithdraw(compassApiSDK, {
    tokenId: 821299,
    percentageForWithdrawal: "25",
    chain: "ethereum",
    sender: "0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("uniswapV3UniswapLiquidityProvisionWithdraw failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [components.UniswapWithdrawLiquidityProvisionRequest](../../models/components/uniswapwithdrawliquidityprovisionrequest.md)                                                     | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
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