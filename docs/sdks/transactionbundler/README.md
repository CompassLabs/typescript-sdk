# TransactionBundler
(*transactionBundler*)

## Overview

### Available Operations

* [transactionBundlerAuthorization](#transactionbundlerauthorization) - Enable Transaction Bundling
* [transactionBundlerExecute](#transactionbundlerexecute) - Construct Bundled Transaction
* [transactionBundlerAaveLoop](#transactionbundleraaveloop) - AAVE Leverage Long/Short

## transactionBundlerAuthorization

Get authorization for bundling transactions.

Currently this is required for every transaction bundle to prevent replay attacks
and ensure transaction ordering when batching multiple actions into a single
transaction. The authorization includes a nonce and chain ID to guarantee
transaction uniqueness and proper network targeting.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="v1_transaction_bundler_authorization" method="post" path="/v1/transaction_bundler/authorization" -->
```typescript
import { CompassApiSDK } from "@compass-labs/api-sdk";

const compassApiSDK = new CompassApiSDK({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await compassApiSDK.transactionBundler.transactionBundlerAuthorization({
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
import { transactionBundlerTransactionBundlerAuthorization } from "@compass-labs/api-sdk/funcs/transactionBundlerTransactionBundlerAuthorization.js";

// Use `CompassApiSDKCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const compassApiSDK = new CompassApiSDKCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await transactionBundlerTransactionBundlerAuthorization(compassApiSDK, {
    chain: "arbitrum",
    sender: "0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("transactionBundlerTransactionBundlerAuthorization failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [components.MulticallAuthorizationRequest](../../models/components/multicallauthorizationrequest.md)                                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[components.MulticallAuthorizationResponse](../../models/components/multicallauthorizationresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.HTTPValidationError | 422                        | application/json           |
| errors.APIError            | 4XX, 5XX                   | \*/\*                      |

## transactionBundlerExecute

Bundle arbitrary transactions together into a single multicall transaction using
EIP-7702.

This endpoint allows bundling multiple contract calls into a single atomic
transaction, reducing gas costs and ensuring all operations succeed or fail
together. The transaction must be authorized using the /authorization endpoint to
prevent replay attacks.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="v1_transaction_bundler_execute" method="post" path="/v1/transaction_bundler/execute" -->
```typescript
import { CompassApiSDK } from "@compass-labs/api-sdk";

const compassApiSDK = new CompassApiSDK({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await compassApiSDK.transactionBundler.transactionBundlerExecute({
    chain: "ethereum",
    sender: "0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B",
    signedAuthorization: {
      nonce: 1000,
      address: "0xcA11bde05977b3631167028862bE2a173976CA11",
      chainId: 42161,
      r: "0x5f9f3f3226ac91bc01a72dd117141f6c6de1ed30d3af9f95c3423316dc21d615",
      s: "0x78f7982ede9dabc53d7153974c5692fda8a21fc73bdafc42aaf135505e22817c",
      yParity: 0,
    },
    actions: [
      {
        body: {
          actionType: "SET_ALLOWANCE",
          token: "WETH",
          contract: "UniswapV3Router",
          amount: "1000",
        },
      },
    ],
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { CompassApiSDKCore } from "@compass-labs/api-sdk/core.js";
import { transactionBundlerTransactionBundlerExecute } from "@compass-labs/api-sdk/funcs/transactionBundlerTransactionBundlerExecute.js";

// Use `CompassApiSDKCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const compassApiSDK = new CompassApiSDKCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await transactionBundlerTransactionBundlerExecute(compassApiSDK, {
    chain: "ethereum",
    sender: "0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B",
    signedAuthorization: {
      nonce: 1000,
      address: "0xcA11bde05977b3631167028862bE2a173976CA11",
      chainId: 42161,
      r: "0x5f9f3f3226ac91bc01a72dd117141f6c6de1ed30d3af9f95c3423316dc21d615",
      s: "0x78f7982ede9dabc53d7153974c5692fda8a21fc73bdafc42aaf135505e22817c",
      yParity: 0,
    },
    actions: [
      {
        body: {
          actionType: "SET_ALLOWANCE",
          token: "WETH",
          contract: "UniswapV3Router",
          amount: "1000",
        },
      },
    ],
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("transactionBundlerTransactionBundlerExecute failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [components.MulticallExecuteRequest](../../models/components/multicallexecuterequest.md)                                                                                       | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[components.BundlerTransactionResponse](../../models/components/bundlertransactionresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.HTTPValidationError | 422                        | application/json           |
| errors.APIError            | 4XX, 5XX                   | \*/\*                      |

## transactionBundlerAaveLoop

Execute an Aave looping strategy that involves repeated supply and borrow
operations.

This endpoint creates a multicall transaction that performs a series of operations:
1. Approves and supplies initial token
2. For each loop:
    - Borrows another token
    - Swaps borrowed token back to supply token
    - Supplies the swapped tokens

The transaction must be authorized using the /authorization endpoint to prevent replay attacks.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="v1_transaction_bundler_aave_loop" method="post" path="/v1/transaction_bundler/aave/loop" -->
```typescript
import { CompassApiSDK } from "@compass-labs/api-sdk";

const compassApiSDK = new CompassApiSDK({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await compassApiSDK.transactionBundler.transactionBundlerAaveLoop({
    chain: "base",
    sender: "0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B",
    signedAuthorization: {
      nonce: 1000,
      address: "0xcA11bde05977b3631167028862bE2a173976CA11",
      chainId: 42161,
      r: "0x5f9f3f3226ac91bc01a72dd117141f6c6de1ed30d3af9f95c3423316dc21d615",
      s: "0x78f7982ede9dabc53d7153974c5692fda8a21fc73bdafc42aaf135505e22817c",
      yParity: 0,
    },
    collateralToken: "USDC",
    borrowToken: "WETH",
    initialCollateralAmount: "1000",
    multiplier: "2.5",
    maxSlippagePercent: 2.5,
    loanToValue: 20.5,
    isAccountAbstraction: true,
  });

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { CompassApiSDKCore } from "@compass-labs/api-sdk/core.js";
import { transactionBundlerTransactionBundlerAaveLoop } from "@compass-labs/api-sdk/funcs/transactionBundlerTransactionBundlerAaveLoop.js";

// Use `CompassApiSDKCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const compassApiSDK = new CompassApiSDKCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await transactionBundlerTransactionBundlerAaveLoop(compassApiSDK, {
    chain: "base",
    sender: "0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B",
    signedAuthorization: {
      nonce: 1000,
      address: "0xcA11bde05977b3631167028862bE2a173976CA11",
      chainId: 42161,
      r: "0x5f9f3f3226ac91bc01a72dd117141f6c6de1ed30d3af9f95c3423316dc21d615",
      s: "0x78f7982ede9dabc53d7153974c5692fda8a21fc73bdafc42aaf135505e22817c",
      yParity: 0,
    },
    collateralToken: "USDC",
    borrowToken: "WETH",
    initialCollateralAmount: "1000",
    multiplier: "2.5",
    maxSlippagePercent: 2.5,
    loanToValue: 20.5,
    isAccountAbstraction: true,
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("transactionBundlerTransactionBundlerAaveLoop failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [components.AaveLoopRequest](../../models/components/aavelooprequest.md)                                                                                                       | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[operations.ResponseV1TransactionBundlerAaveLoop](../../models/operations/responsev1transactionbundleraaveloop.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.HTTPValidationError | 422                        | application/json           |
| errors.APIError            | 4XX, 5XX                   | \*/\*                      |