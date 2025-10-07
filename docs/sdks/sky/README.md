# Sky
(*sky*)

## Overview

### Available Operations

* [skyPosition](#skyposition) - Check USDS Position
* [skyBuy](#skybuy) - Buy USDS
* [skySell](#skysell) - Sell USDS
* [skyDeposit](#skydeposit) - Deposit USDS
* [skyWithdraw](#skywithdraw) - Withdraw USDS

## skyPosition

Check the USDS overall position.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="v1_sky_position" method="get" path="/v1/sky/position" -->
```typescript
import { CompassApiSDK } from "@compass-labs/api-sdk";

const compassApiSDK = new CompassApiSDK({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await compassApiSDK.sky.skyPosition({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { CompassApiSDKCore } from "@compass-labs/api-sdk/core.js";
import { skySkyPosition } from "@compass-labs/api-sdk/funcs/skySkyPosition.js";

// Use `CompassApiSDKCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const compassApiSDK = new CompassApiSDKCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await skySkyPosition(compassApiSDK, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("skySkyPosition failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.V1SkyPositionRequest](../../models/operations/v1skypositionrequest.md)                                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[components.SkyCheckPositionResponse](../../models/components/skycheckpositionresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.HTTPValidationError | 422                        | application/json           |
| errors.APIError            | 4XX, 5XX                   | \*/\*                      |

## skyBuy

Buy USDS with DAI or USDC on a 1:1 basis. There are no fees.

If buying with DAI, user will need to set an allowance on the DAI contract for the
'SkyDaiUsdsConverter' contract beforehand.

If buying with USDC, user will need to set an allowance on the USDC contract for the
'SkyUsdcUsdsConverter' contract beforehand.
                    <Info>
                    **Required Allowances**

                        In order to make this transaction, token allowances need to be set for the following contracts.

                     - `SkyUsdcUsdsConverter`
 - `SkyDaiUsdsConverter`
                    </Info>
                

### Example Usage

<!-- UsageSnippet language="typescript" operationID="v1_sky_buy" method="post" path="/v1/sky/buy" -->
```typescript
import { CompassApiSDK } from "@compass-labs/api-sdk";

const compassApiSDK = new CompassApiSDK({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await compassApiSDK.sky.skyBuy({
    tokenIn: "USDC",
    amount: 1.5,
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
import { skySkyBuy } from "@compass-labs/api-sdk/funcs/skySkyBuy.js";

// Use `CompassApiSDKCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const compassApiSDK = new CompassApiSDKCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await skySkyBuy(compassApiSDK, {
    tokenIn: "USDC",
    amount: 1.5,
    chain: "ethereum",
    sender: "0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("skySkyBuy failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [components.SkyBuyRequest](../../models/components/skybuyrequest.md)                                                                                                           | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
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

## skySell

Sell USDS for DAI or USDC on a 1:1 basis. There are no fees.

If swapping to DAI, user will need to set an allowance on the USDS contract for the
'SkyDaiUsdsConverter' contract beforehand.

If swapping to USDC, user will need to set an allowance on the USDS contract for the
'SkyUsdcUsdsConverter' contract beforehand.
                    <Info>
                    **Required Allowances**

                        In order to make this transaction, token allowances need to be set for the following contracts.

                     - `SkyUsdcUsdsConverter`
 - `SkyDaiUsdsConverter`
                    </Info>
                

### Example Usage

<!-- UsageSnippet language="typescript" operationID="v1_sky_sell" method="post" path="/v1/sky/sell" -->
```typescript
import { CompassApiSDK } from "@compass-labs/api-sdk";

const compassApiSDK = new CompassApiSDK({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await compassApiSDK.sky.skySell({
    tokenOut: "DAI",
    amount: 1.5,
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
import { skySkySell } from "@compass-labs/api-sdk/funcs/skySkySell.js";

// Use `CompassApiSDKCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const compassApiSDK = new CompassApiSDKCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await skySkySell(compassApiSDK, {
    tokenOut: "DAI",
    amount: 1.5,
    chain: "ethereum",
    sender: "0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("skySkySell failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [components.SkySellRequest](../../models/components/skysellrequest.md)                                                                                                         | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
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

## skyDeposit

Deposit USDS to earn yield. Deposited USDS is represented as sUSDS.

Allowance must be set on USDS contract for UsdsVault.

There are no fees.
                    <Info>
                    **Required Allowances**

                        In order to make this transaction, token allowances need to be set for the following contracts.

                     - `SkyUsdsVault`
                    </Info>
                

### Example Usage

<!-- UsageSnippet language="typescript" operationID="v1_sky_deposit" method="post" path="/v1/sky/deposit" -->
```typescript
import { CompassApiSDK } from "@compass-labs/api-sdk";

const compassApiSDK = new CompassApiSDK({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await compassApiSDK.sky.skyDeposit({
    amount: 1.5,
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
import { skySkyDeposit } from "@compass-labs/api-sdk/funcs/skySkyDeposit.js";

// Use `CompassApiSDKCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const compassApiSDK = new CompassApiSDKCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await skySkyDeposit(compassApiSDK, {
    amount: 1.5,
    sender: "0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("skySkyDeposit failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [components.SkyDepositRequest](../../models/components/skydepositrequest.md)                                                                                                   | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
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

## skyWithdraw

Withdraw USDS. Exchange yield-bearing sUSDS for USDS.

Allowance must be set on USDS contract for UsdsVault.

There are no fees.
                    <Info>
                    **Required Allowances**

                        In order to make this transaction, token allowances need to be set for the following contracts.

                     - `SkyUsdsVault`
                    </Info>
                

### Example Usage

<!-- UsageSnippet language="typescript" operationID="v1_sky_withdraw" method="post" path="/v1/sky/withdraw" -->
```typescript
import { CompassApiSDK } from "@compass-labs/api-sdk";

const compassApiSDK = new CompassApiSDK({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await compassApiSDK.sky.skyWithdraw({
    amount: 4514.13,
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
import { skySkyWithdraw } from "@compass-labs/api-sdk/funcs/skySkyWithdraw.js";

// Use `CompassApiSDKCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const compassApiSDK = new CompassApiSDKCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await skySkyWithdraw(compassApiSDK, {
    amount: 4514.13,
    sender: "0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("skySkyWithdraw failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [components.SkyWithdrawRequest](../../models/components/skywithdrawrequest.md)                                                                                                 | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
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