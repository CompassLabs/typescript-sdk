# SmartAccount
(*smartAccount*)

## Overview

### Available Operations

* [smartAccountBatchedUserOperations](#smartaccountbatcheduseroperations) - Get Smart Account Batched User Operations

## smartAccountBatchedUserOperations

Generate a list of user operations for smart account batching.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="v1_smart_account_batched_user_operations" method="post" path="/v1/smart_account/batched_user_operations" -->
```typescript
import { CompassApiSDK } from "@compass-labs/api-sdk";

const compassApiSDK = new CompassApiSDK({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await compassApiSDK.smartAccount.smartAccountBatchedUserOperations({
    chain: "arbitrum",
    sender: "0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B",
    operations: [
      {
        body: {
          actionType: "SET_ALLOWANCE",
          token: "USDC",
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
import { smartAccountSmartAccountBatchedUserOperations } from "@compass-labs/api-sdk/funcs/smartAccountSmartAccountBatchedUserOperations.js";

// Use `CompassApiSDKCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const compassApiSDK = new CompassApiSDKCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await smartAccountSmartAccountBatchedUserOperations(compassApiSDK, {
    chain: "arbitrum",
    sender: "0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B",
    operations: [
      {
        body: {
          actionType: "SET_ALLOWANCE",
          token: "USDC",
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
    console.log("smartAccountSmartAccountBatchedUserOperations failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [components.BatchedUserOperationsRequest](../../models/components/batcheduseroperationsrequest.md)                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[components.BatchedUserOperationsResponse](../../models/components/batcheduseroperationsresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.HTTPValidationError | 422                        | application/json           |
| errors.APIError            | 4XX, 5XX                   | \*/\*                      |