# Swap
(*swap*)

## Overview

### Available Operations

* [swapOdos](#swapodos) - Odos Swap

## swapOdos

Swap between two tokens using Odos Smart Order Routing.
                    <Info>
                    **Required Allowances**

                        In order to make this transaction, token allowances need to be set for the following contracts.

                     - `OdosRouter`
                    </Info>
                

### Example Usage

<!-- UsageSnippet language="typescript" operationID="v1_swap_odos" method="post" path="/v1/swap/odos" -->
```typescript
import { CompassApiSDK } from "@compass-labs/api-sdk";

const compassApiSDK = new CompassApiSDK({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await compassApiSDK.swap.swapOdos({
    tokenIn: "0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48",
    tokenOut: "0xdac17f958d2ee523a2206206994597c13d831ec7",
    amount: 1.5,
    maxSlippagePercent: 0.5,
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
import { swapSwapOdos } from "@compass-labs/api-sdk/funcs/swapSwapOdos.js";

// Use `CompassApiSDKCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const compassApiSDK = new CompassApiSDKCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await swapSwapOdos(compassApiSDK, {
    tokenIn: "0xa0b86991c6218b36c1d19d4a2e9eb0ce3606eb48",
    tokenOut: "0xdac17f958d2ee523a2206206994597c13d831ec7",
    amount: 1.5,
    maxSlippagePercent: 0.5,
    chain: "arbitrum",
    sender: "0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("swapSwapOdos failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [components.OdosSwapRequest](../../models/components/odosswaprequest.md)                                                                                                       | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[components.OdosTransactionResponse](../../models/components/odostransactionresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.HTTPValidationError | 422                        | application/json           |
| errors.APIError            | 4XX, 5XX                   | \*/\*                      |