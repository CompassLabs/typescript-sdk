# Erc4626Vaults
(*erc4626Vaults*)

## Overview

### Available Operations

* [vaultsVault](#vaultsvault) - Get Vault & User Position
* [vaultsDeposit](#vaultsdeposit) - Deposit to Vault
* [vaultsWithdraw](#vaultswithdraw) - Withdraw from Vault

## vaultsVault

Get Vault data & User Position.

The user position is only included if 'user_address' parameter is included.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="v1_vaults_vault" method="get" path="/v1/vaults/vault" -->
```typescript
import { CompassApiSDK } from "@compass-labs/api-sdk";

const compassApiSDK = new CompassApiSDK({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await compassApiSDK.erc4626Vaults.vaultsVault({});

  console.log(result);
}

run();
```

### Standalone function

The standalone function version of this method:

```typescript
import { CompassApiSDKCore } from "@compass-labs/api-sdk/core.js";
import { erc4626VaultsVaultsVault } from "@compass-labs/api-sdk/funcs/erc4626VaultsVaultsVault.js";

// Use `CompassApiSDKCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const compassApiSDK = new CompassApiSDKCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await erc4626VaultsVaultsVault(compassApiSDK, {});
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("erc4626VaultsVaultsVault failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [operations.V1VaultsVaultRequest](../../models/operations/v1vaultsvaultrequest.md)                                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
| `options`                                                                                                                                                                      | RequestOptions                                                                                                                                                                 | :heavy_minus_sign:                                                                                                                                                             | Used to set various options for making HTTP requests.                                                                                                                          |
| `options.fetchOptions`                                                                                                                                                         | [RequestInit](https://developer.mozilla.org/en-US/docs/Web/API/Request/Request#options)                                                                                        | :heavy_minus_sign:                                                                                                                                                             | Options that are passed to the underlying HTTP request. This can be used to inject extra headers for examples. All `Request` options, except `method` and `body`, are allowed. |
| `options.retries`                                                                                                                                                              | [RetryConfig](../../lib/utils/retryconfig.md)                                                                                                                                  | :heavy_minus_sign:                                                                                                                                                             | Enables retrying HTTP requests under certain failure conditions.                                                                                                               |

### Response

**Promise\<[components.VaultGetVaultResponse](../../models/components/vaultgetvaultresponse.md)\>**

### Errors

| Error Type                 | Status Code                | Content Type               |
| -------------------------- | -------------------------- | -------------------------- |
| errors.HTTPValidationError | 422                        | application/json           |
| errors.APIError            | 4XX, 5XX                   | \*/\*                      |

## vaultsDeposit

Deposit tokens into a Vault (ERC-4626 Standard) to earn passive yield.

Each vault accepts one unique token that can be deposited.
                    <Info>
                    **Required Allowances**

                        In order to make this transaction, token allowances need to be set for the following contracts.

                     - `<vault_address>`
                    </Info>
                

### Example Usage

<!-- UsageSnippet language="typescript" operationID="v1_vaults_deposit" method="post" path="/v1/vaults/deposit" -->
```typescript
import { CompassApiSDK } from "@compass-labs/api-sdk";

const compassApiSDK = new CompassApiSDK({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await compassApiSDK.erc4626Vaults.vaultsDeposit({
    vaultAddress: "0xbEef047a543E45807105E51A8BBEFCc5950fcfBa",
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
import { erc4626VaultsVaultsDeposit } from "@compass-labs/api-sdk/funcs/erc4626VaultsVaultsDeposit.js";

// Use `CompassApiSDKCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const compassApiSDK = new CompassApiSDKCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await erc4626VaultsVaultsDeposit(compassApiSDK, {
    vaultAddress: "0xbEef047a543E45807105E51A8BBEFCc5950fcfBa",
    amount: 1.5,
    chain: "ethereum",
    sender: "0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("erc4626VaultsVaultsDeposit failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [components.VaultDepositRequest](../../models/components/vaultdepositrequest.md)                                                                                               | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
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

## vaultsWithdraw

Withdraw deposited tokens from a Vault (ERC-4626 Standard).

The passive yield earned on token deposits is represented by the increased value of
the shares received upon depositing tokens. Trade in these shares for the tokens you
deposited plus any accrued yield.

### Example Usage

<!-- UsageSnippet language="typescript" operationID="v1_vaults_withdraw" method="post" path="/v1/vaults/withdraw" -->
```typescript
import { CompassApiSDK } from "@compass-labs/api-sdk";

const compassApiSDK = new CompassApiSDK({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await compassApiSDK.erc4626Vaults.vaultsWithdraw({
    vaultAddress: "0xbEef047a543E45807105E51A8BBEFCc5950fcfBa",
    amount: 1.5,
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
import { erc4626VaultsVaultsWithdraw } from "@compass-labs/api-sdk/funcs/erc4626VaultsVaultsWithdraw.js";

// Use `CompassApiSDKCore` for best tree-shaking performance.
// You can create one instance of it to use across an application.
const compassApiSDK = new CompassApiSDKCore({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const res = await erc4626VaultsVaultsWithdraw(compassApiSDK, {
    vaultAddress: "0xbEef047a543E45807105E51A8BBEFCc5950fcfBa",
    amount: 1.5,
    chain: "arbitrum",
    sender: "0x29F20a192328eF1aD35e1564aBFf4Be9C5ce5f7B",
  });
  if (res.ok) {
    const { value: result } = res;
    console.log(result);
  } else {
    console.log("erc4626VaultsVaultsWithdraw failed:", res.error);
  }
}

run();
```

### Parameters

| Parameter                                                                                                                                                                      | Type                                                                                                                                                                           | Required                                                                                                                                                                       | Description                                                                                                                                                                    |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `request`                                                                                                                                                                      | [components.VaultWithdrawRequest](../../models/components/vaultwithdrawrequest.md)                                                                                             | :heavy_check_mark:                                                                                                                                                             | The request object to use for the request.                                                                                                                                     |
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