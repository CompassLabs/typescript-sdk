# @compass-labs/api-sdk

Developer-friendly & type-safe Typescript SDK specifically catered to leverage *@compass-labs/api-sdk* API.

<!-- Start Summary [summary] -->
## Summary

Compass API: Compass Labs DeFi API
<!-- End Summary [summary] -->

<!-- Start Table of Contents [toc] -->
## Table of Contents
<!-- $toc-max-depth=2 -->
* [@compass-labs/api-sdk](#compass-labsapi-sdk)
  * [SDK Installation](#sdk-installation)
  * [Requirements](#requirements)
  * [SDK Example Usage](#sdk-example-usage)
  * [Authentication](#authentication)
  * [Available Resources and Operations](#available-resources-and-operations)
  * [Standalone functions](#standalone-functions)
  * [Retries](#retries)
  * [Error Handling](#error-handling)
  * [Server Selection](#server-selection)
  * [Custom HTTP Client](#custom-http-client)
  * [Debugging](#debugging)
* [Development](#development)
  * [Maturity](#maturity)
  * [Contributions](#contributions)

<!-- End Table of Contents [toc] -->

<!-- Start SDK Installation [installation] -->
## SDK Installation

The SDK can be installed with either [npm](https://www.npmjs.com/), [pnpm](https://pnpm.io/), [bun](https://bun.sh/) or [yarn](https://classic.yarnpkg.com/en/) package managers.

### NPM

```bash
npm add @compass-labs/api-sdk
```

### PNPM

```bash
pnpm add @compass-labs/api-sdk
```

### Bun

```bash
bun add @compass-labs/api-sdk
```

### Yarn

```bash
yarn add @compass-labs/api-sdk
```

> [!NOTE]
> This package is published with CommonJS and ES Modules (ESM) support.


### Model Context Protocol (MCP) Server

This SDK is also an installable MCP server where the various SDK methods are
exposed as tools that can be invoked by AI applications.

> Node.js v20 or greater is required to run the MCP server from npm.

<details>
<summary>Claude installation steps</summary>

Add the following server definition to your `claude_desktop_config.json` file:

```json
{
  "mcpServers": {
    "CompassApiSDK": {
      "command": "npx",
      "args": [
        "-y", "--package", "@compass-labs/api-sdk",
        "--",
        "mcp", "start",
        "--api-key-auth", "..."
      ]
    }
  }
}
```

</details>

<details>
<summary>Cursor installation steps</summary>

Create a `.cursor/mcp.json` file in your project root with the following content:

```json
{
  "mcpServers": {
    "CompassApiSDK": {
      "command": "npx",
      "args": [
        "-y", "--package", "@compass-labs/api-sdk",
        "--",
        "mcp", "start",
        "--api-key-auth", "..."
      ]
    }
  }
}
```

</details>

You can also run MCP servers as a standalone binary with no additional dependencies. You must pull these binaries from available Github releases:

```bash
curl -L -o mcp-server \
    https://github.com/{org}/{repo}/releases/download/{tag}/mcp-server-bun-darwin-arm64 && \
chmod +x mcp-server
```

If the repo is a private repo you must add your Github PAT to download a release `-H "Authorization: Bearer {GITHUB_PAT}"`.


```json
{
  "mcpServers": {
    "Todos": {
      "command": "./DOWNLOAD/PATH/mcp-server",
      "args": [
        "start"
      ]
    }
  }
}
```

For a full list of server arguments, run:

```sh
npx -y --package @compass-labs/api-sdk -- mcp start --help
```
<!-- End SDK Installation [installation] -->

<!-- Start Requirements [requirements] -->
## Requirements

For supported JavaScript runtimes, please consult [RUNTIMES.md](RUNTIMES.md).
<!-- End Requirements [requirements] -->

<!-- Start SDK Example Usage [usage] -->
## SDK Example Usage

### Example

```typescript
import { CompassApiSDK } from "@compass-labs/api-sdk";

const compassApiSDK = new CompassApiSDK({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await compassApiSDK.aaveV3.aaveAaveSupportedTokens({});

  console.log(result);
}

run();

```
<!-- End SDK Example Usage [usage] -->

<!-- Start Authentication [security] -->
## Authentication

### Per-Client Security Schemes

This SDK supports the following security scheme globally:

| Name         | Type   | Scheme  |
| ------------ | ------ | ------- |
| `apiKeyAuth` | apiKey | API key |

To authenticate with the API the `apiKeyAuth` parameter must be set when initializing the SDK client instance. For example:
```typescript
import { CompassApiSDK } from "@compass-labs/api-sdk";

const compassApiSDK = new CompassApiSDK({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await compassApiSDK.aaveV3.aaveAaveSupportedTokens({});

  console.log(result);
}

run();

```
<!-- End Authentication [security] -->

<!-- Start Available Resources and Operations [operations] -->
## Available Resources and Operations

<details open>
<summary>Available methods</summary>

### [aaveV3](docs/sdks/aavev3/README.md)

* [aaveAaveSupportedTokens](docs/sdks/aavev3/README.md#aaveaavesupportedtokens) - Aave Supported Tokens
* [aaveRate](docs/sdks/aavev3/README.md#aaverate) - Interest Rates
* [aaveAvgRate](docs/sdks/aavev3/README.md#aaveavgrate) - Interest Rates: Time Average
* [aaveStdRate](docs/sdks/aavev3/README.md#aavestdrate) - Interest Rates: Standard Deviation
* [aaveReserveOverview](docs/sdks/aavev3/README.md#aavereserveoverview) - Reserve Overview
* [aaveTokenPrice](docs/sdks/aavev3/README.md#aavetokenprice) - Token Prices
* [aaveLiquidityChange](docs/sdks/aavev3/README.md#aaveliquiditychange) - Liquidity Index
* [aaveUserPositionSummary](docs/sdks/aavev3/README.md#aaveuserpositionsummary) - Positions - Total
* [aaveUserPositionPerToken](docs/sdks/aavev3/README.md#aaveuserpositionpertoken) - Positions - per Token
* [aaveHistoricalTransactions](docs/sdks/aavev3/README.md#aavehistoricaltransactions) - Historical Transactions
* [aaveSupply](docs/sdks/aavev3/README.md#aavesupply) - Supply/Lend
* [aaveBorrow](docs/sdks/aavev3/README.md#aaveborrow) - Borrow
* [aaveRepay](docs/sdks/aavev3/README.md#aaverepay) - Repay Loans
* [aaveWithdraw](docs/sdks/aavev3/README.md#aavewithdraw) - Unstake

### [aerodromeSlipstream](docs/sdks/aerodromeslipstream/README.md)

* [aerodromeSlipstreamLiquidityProvisionPositions](docs/sdks/aerodromeslipstream/README.md#aerodromeslipstreamliquidityprovisionpositions) - List LP Positions
* [aerodromeSlipstreamPoolPrice](docs/sdks/aerodromeslipstream/README.md#aerodromeslipstreampoolprice) - Pool Price
* [aerodromeSlipstreamSwapSellExactly](docs/sdks/aerodromeslipstream/README.md#aerodromeslipstreamswapsellexactly) - Swap - from Specified Amount
* [aerodromeSlipstreamSwapBuyExactly](docs/sdks/aerodromeslipstream/README.md#aerodromeslipstreamswapbuyexactly) - Swap - into Specified Amount
* [aerodromeSlipstreamLiquidityProvisionMint](docs/sdks/aerodromeslipstream/README.md#aerodromeslipstreamliquidityprovisionmint) - Open a New LP Position
* [aerodromeSlipstreamLiquidityProvisionIncrease](docs/sdks/aerodromeslipstream/README.md#aerodromeslipstreamliquidityprovisionincrease) - Increase an LP Position
* [aerodromeSlipstreamLiquidityProvisionWithdraw](docs/sdks/aerodromeslipstream/README.md#aerodromeslipstreamliquidityprovisionwithdraw) - Withdraw an LP Position


### [erc4626Vaults](docs/sdks/erc4626vaults/README.md)

* [vaultsVault](docs/sdks/erc4626vaults/README.md#vaultsvault) - Get Vault & User Position
* [vaultsDeposit](docs/sdks/erc4626vaults/README.md#vaultsdeposit) - Deposit to Vault
* [vaultsWithdraw](docs/sdks/erc4626vaults/README.md#vaultswithdraw) - Withdraw from Vault

### [ethena](docs/sdks/ethena/README.md)

* [ethenaVault](docs/sdks/ethena/README.md#ethenavault) - Get Vault & User Position
* [ethenaDeposit](docs/sdks/ethena/README.md#ethenadeposit) - Deposit USDe
* [ethenaRequest](docs/sdks/ethena/README.md#ethenarequest) - Request to Withdraw USDe
* [ethenaUnstake](docs/sdks/ethena/README.md#ethenaunstake) - Unstake USDe

### [morpho](docs/sdks/morpho/README.md)

* [morphoVaults](docs/sdks/morpho/README.md#morphovaults) - Get Vaults
* [morphoVault](docs/sdks/morpho/README.md#morphovault) - Get Vault & User Position
* [morphoMarkets](docs/sdks/morpho/README.md#morphomarkets) - Get Markets
* [morphoMarket](docs/sdks/morpho/README.md#morphomarket) - Get Market
* [morphoMarketPosition](docs/sdks/morpho/README.md#morphomarketposition) - Check Market Position
* [morphoUserPosition](docs/sdks/morpho/README.md#morphouserposition) - Check User Position
* [morphoDeposit](docs/sdks/morpho/README.md#morphodeposit) - Deposit to Vault
* [morphoWithdraw](docs/sdks/morpho/README.md#morphowithdraw) - Withdraw from Vault
* [morphoSupplyCollateral](docs/sdks/morpho/README.md#morphosupplycollateral) - Supply Collateral to Market
* [morphoWithdrawCollateral](docs/sdks/morpho/README.md#morphowithdrawcollateral) - Withdraw Collateral from Market
* [morphoBorrow](docs/sdks/morpho/README.md#morphoborrow) - Borrow from Market
* [morphoRepay](docs/sdks/morpho/README.md#morphorepay) - Repay to Market

### [pendle](docs/sdks/pendle/README.md)

* [pendleMarket](docs/sdks/pendle/README.md#pendlemarket) - Get Market & User Position
* [pendlePositions](docs/sdks/pendle/README.md#pendlepositions) - List User's Market Positions
* [pendleMarkets](docs/sdks/pendle/README.md#pendlemarkets) - List Market Data
* [pendlePt](docs/sdks/pendle/README.md#pendlept) - Trade Principal Token (PT)
* [pendleYt](docs/sdks/pendle/README.md#pendleyt) - Trade Yield Token (YT)
* [pendleLiquidity](docs/sdks/pendle/README.md#pendleliquidity) - Manage Liquidity (LP)
* [pendleRedeemYield](docs/sdks/pendle/README.md#pendleredeemyield) - Redeem Claimable Yield

### [sky](docs/sdks/sky/README.md)

* [skyPosition](docs/sdks/sky/README.md#skyposition) - Check USDS Position
* [skyBuy](docs/sdks/sky/README.md#skybuy) - Buy USDS
* [skySell](docs/sdks/sky/README.md#skysell) - Sell USDS
* [skyDeposit](docs/sdks/sky/README.md#skydeposit) - Deposit USDS
* [skyWithdraw](docs/sdks/sky/README.md#skywithdraw) - Withdraw USDS

### [smartAccount](docs/sdks/smartaccount/README.md)

* [smartAccountBatchedUserOperations](docs/sdks/smartaccount/README.md#smartaccountbatcheduseroperations) - Get Smart Account Batched User Operations

### [swap](docs/sdks/swap/README.md)

* [swapOdos](docs/sdks/swap/README.md#swapodos) - Odos Swap

### [token](docs/sdks/token/README.md)

* [tokenPrice](docs/sdks/token/README.md#tokenprice) - Token Price
* [tokenBalance](docs/sdks/token/README.md#tokenbalance) - Token Balance
* [tokenTransfer](docs/sdks/token/README.md#tokentransfer) - Transfer Tokens

### [transactionBundler](docs/sdks/transactionbundler/README.md)

* [transactionBundlerAuthorization](docs/sdks/transactionbundler/README.md#transactionbundlerauthorization) - Enable Transaction Bundling
* [transactionBundlerExecute](docs/sdks/transactionbundler/README.md#transactionbundlerexecute) - Construct Bundled Transaction
* [transactionBundlerAaveLoop](docs/sdks/transactionbundler/README.md#transactionbundleraaveloop) - AAVE Leverage Long/Short

### [uniswapV3](docs/sdks/uniswapv3/README.md)

* [uniswapQuoteBuyExactly](docs/sdks/uniswapv3/README.md#uniswapquotebuyexactly) - Get Quote - to Specified Amount
* [uniswapQuoteSellExactly](docs/sdks/uniswapv3/README.md#uniswapquotesellexactly) - Get quote - From Specified Amount
* [uniswapPoolPrice](docs/sdks/uniswapv3/README.md#uniswappoolprice) - Pool Price
* [uniswapLiquidityProvisionInRange](docs/sdks/uniswapv3/README.md#uniswapliquidityprovisioninrange) - Check if LP is Active.
* [uniswapLiquidityProvisionPositions](docs/sdks/uniswapv3/README.md#uniswapliquidityprovisionpositions) - List LP
* [uniswapSwapBuyExactly](docs/sdks/uniswapv3/README.md#uniswapswapbuyexactly) - Buy exact amount
* [uniswapSwapSellExactly](docs/sdks/uniswapv3/README.md#uniswapswapsellexactly) - Sell exact amount
* [uniswapLiquidityProvisionMint](docs/sdks/uniswapv3/README.md#uniswapliquidityprovisionmint) - Open a new LP position
* [uniswapLiquidityProvisionIncrease](docs/sdks/uniswapv3/README.md#uniswapliquidityprovisionincrease) - Increase an LP position
* [uniswapLiquidityProvisionWithdraw](docs/sdks/uniswapv3/README.md#uniswapliquidityprovisionwithdraw) - Withdraw an LP position

### [universal](docs/sdks/universal/README.md)

* [genericPortfolio](docs/sdks/universal/README.md#genericportfolio) - List User Portfolio
* [genericSupportedChains](docs/sdks/universal/README.md#genericsupportedchains) - List Supported Chains
* [genericAllowance](docs/sdks/universal/README.md#genericallowance) - Get Allowance
* [genericEns](docs/sdks/universal/README.md#genericens) - Resolve ENS
* [genericWrapEth](docs/sdks/universal/README.md#genericwrapeth) - Wrap ETH
* [genericUnwrapWeth](docs/sdks/universal/README.md#genericunwrapweth) - Unwrap WETH
* [genericAllowanceSet](docs/sdks/universal/README.md#genericallowanceset) - Set Allowance

</details>
<!-- End Available Resources and Operations [operations] -->

<!-- Start Standalone functions [standalone-funcs] -->
## Standalone functions

All the methods listed above are available as standalone functions. These
functions are ideal for use in applications running in the browser, serverless
runtimes or other environments where application bundle size is a primary
concern. When using a bundler to build your application, all unused
functionality will be either excluded from the final bundle or tree-shaken away.

To read more about standalone functions, check [FUNCTIONS.md](./FUNCTIONS.md).

<details>

<summary>Available standalone functions</summary>

- [`aaveV3AaveAaveSupportedTokens`](docs/sdks/aavev3/README.md#aaveaavesupportedtokens) - Aave Supported Tokens
- [`aaveV3AaveAvgRate`](docs/sdks/aavev3/README.md#aaveavgrate) - Interest Rates: Time Average
- [`aaveV3AaveBorrow`](docs/sdks/aavev3/README.md#aaveborrow) - Borrow
- [`aaveV3AaveHistoricalTransactions`](docs/sdks/aavev3/README.md#aavehistoricaltransactions) - Historical Transactions
- [`aaveV3AaveLiquidityChange`](docs/sdks/aavev3/README.md#aaveliquiditychange) - Liquidity Index
- [`aaveV3AaveRate`](docs/sdks/aavev3/README.md#aaverate) - Interest Rates
- [`aaveV3AaveRepay`](docs/sdks/aavev3/README.md#aaverepay) - Repay Loans
- [`aaveV3AaveReserveOverview`](docs/sdks/aavev3/README.md#aavereserveoverview) - Reserve Overview
- [`aaveV3AaveStdRate`](docs/sdks/aavev3/README.md#aavestdrate) - Interest Rates: Standard Deviation
- [`aaveV3AaveSupply`](docs/sdks/aavev3/README.md#aavesupply) - Supply/Lend
- [`aaveV3AaveTokenPrice`](docs/sdks/aavev3/README.md#aavetokenprice) - Token Prices
- [`aaveV3AaveUserPositionPerToken`](docs/sdks/aavev3/README.md#aaveuserpositionpertoken) - Positions - per Token
- [`aaveV3AaveUserPositionSummary`](docs/sdks/aavev3/README.md#aaveuserpositionsummary) - Positions - Total
- [`aaveV3AaveWithdraw`](docs/sdks/aavev3/README.md#aavewithdraw) - Unstake
- [`aerodromeSlipstreamAerodromeSlipstreamLiquidityProvisionIncrease`](docs/sdks/aerodromeslipstream/README.md#aerodromeslipstreamliquidityprovisionincrease) - Increase an LP Position
- [`aerodromeSlipstreamAerodromeSlipstreamLiquidityProvisionMint`](docs/sdks/aerodromeslipstream/README.md#aerodromeslipstreamliquidityprovisionmint) - Open a New LP Position
- [`aerodromeSlipstreamAerodromeSlipstreamLiquidityProvisionPositions`](docs/sdks/aerodromeslipstream/README.md#aerodromeslipstreamliquidityprovisionpositions) - List LP Positions
- [`aerodromeSlipstreamAerodromeSlipstreamLiquidityProvisionWithdraw`](docs/sdks/aerodromeslipstream/README.md#aerodromeslipstreamliquidityprovisionwithdraw) - Withdraw an LP Position
- [`aerodromeSlipstreamAerodromeSlipstreamPoolPrice`](docs/sdks/aerodromeslipstream/README.md#aerodromeslipstreampoolprice) - Pool Price
- [`aerodromeSlipstreamAerodromeSlipstreamSwapBuyExactly`](docs/sdks/aerodromeslipstream/README.md#aerodromeslipstreamswapbuyexactly) - Swap - into Specified Amount
- [`aerodromeSlipstreamAerodromeSlipstreamSwapSellExactly`](docs/sdks/aerodromeslipstream/README.md#aerodromeslipstreamswapsellexactly) - Swap - from Specified Amount
- [`erc4626VaultsVaultsDeposit`](docs/sdks/erc4626vaults/README.md#vaultsdeposit) - Deposit to Vault
- [`erc4626VaultsVaultsVault`](docs/sdks/erc4626vaults/README.md#vaultsvault) - Get Vault & User Position
- [`erc4626VaultsVaultsWithdraw`](docs/sdks/erc4626vaults/README.md#vaultswithdraw) - Withdraw from Vault
- [`ethenaEthenaDeposit`](docs/sdks/ethena/README.md#ethenadeposit) - Deposit USDe
- [`ethenaEthenaRequest`](docs/sdks/ethena/README.md#ethenarequest) - Request to Withdraw USDe
- [`ethenaEthenaUnstake`](docs/sdks/ethena/README.md#ethenaunstake) - Unstake USDe
- [`ethenaEthenaVault`](docs/sdks/ethena/README.md#ethenavault) - Get Vault & User Position
- [`morphoMorphoBorrow`](docs/sdks/morpho/README.md#morphoborrow) - Borrow from Market
- [`morphoMorphoDeposit`](docs/sdks/morpho/README.md#morphodeposit) - Deposit to Vault
- [`morphoMorphoMarket`](docs/sdks/morpho/README.md#morphomarket) - Get Market
- [`morphoMorphoMarketPosition`](docs/sdks/morpho/README.md#morphomarketposition) - Check Market Position
- [`morphoMorphoMarkets`](docs/sdks/morpho/README.md#morphomarkets) - Get Markets
- [`morphoMorphoRepay`](docs/sdks/morpho/README.md#morphorepay) - Repay to Market
- [`morphoMorphoSupplyCollateral`](docs/sdks/morpho/README.md#morphosupplycollateral) - Supply Collateral to Market
- [`morphoMorphoUserPosition`](docs/sdks/morpho/README.md#morphouserposition) - Check User Position
- [`morphoMorphoVault`](docs/sdks/morpho/README.md#morphovault) - Get Vault & User Position
- [`morphoMorphoVaults`](docs/sdks/morpho/README.md#morphovaults) - Get Vaults
- [`morphoMorphoWithdraw`](docs/sdks/morpho/README.md#morphowithdraw) - Withdraw from Vault
- [`morphoMorphoWithdrawCollateral`](docs/sdks/morpho/README.md#morphowithdrawcollateral) - Withdraw Collateral from Market
- [`pendlePendleLiquidity`](docs/sdks/pendle/README.md#pendleliquidity) - Manage Liquidity (LP)
- [`pendlePendleMarket`](docs/sdks/pendle/README.md#pendlemarket) - Get Market & User Position
- [`pendlePendleMarkets`](docs/sdks/pendle/README.md#pendlemarkets) - List Market Data
- [`pendlePendlePositions`](docs/sdks/pendle/README.md#pendlepositions) - List User's Market Positions
- [`pendlePendlePt`](docs/sdks/pendle/README.md#pendlept) - Trade Principal Token (PT)
- [`pendlePendleRedeemYield`](docs/sdks/pendle/README.md#pendleredeemyield) - Redeem Claimable Yield
- [`pendlePendleYt`](docs/sdks/pendle/README.md#pendleyt) - Trade Yield Token (YT)
- [`skySkyBuy`](docs/sdks/sky/README.md#skybuy) - Buy USDS
- [`skySkyDeposit`](docs/sdks/sky/README.md#skydeposit) - Deposit USDS
- [`skySkyPosition`](docs/sdks/sky/README.md#skyposition) - Check USDS Position
- [`skySkySell`](docs/sdks/sky/README.md#skysell) - Sell USDS
- [`skySkyWithdraw`](docs/sdks/sky/README.md#skywithdraw) - Withdraw USDS
- [`smartAccountSmartAccountBatchedUserOperations`](docs/sdks/smartaccount/README.md#smartaccountbatcheduseroperations) - Get Smart Account Batched User Operations
- [`swapSwapOdos`](docs/sdks/swap/README.md#swapodos) - Odos Swap
- [`tokenTokenBalance`](docs/sdks/token/README.md#tokenbalance) - Token Balance
- [`tokenTokenPrice`](docs/sdks/token/README.md#tokenprice) - Token Price
- [`tokenTokenTransfer`](docs/sdks/token/README.md#tokentransfer) - Transfer Tokens
- [`transactionBundlerTransactionBundlerAaveLoop`](docs/sdks/transactionbundler/README.md#transactionbundleraaveloop) - AAVE Leverage Long/Short
- [`transactionBundlerTransactionBundlerAuthorization`](docs/sdks/transactionbundler/README.md#transactionbundlerauthorization) - Enable Transaction Bundling
- [`transactionBundlerTransactionBundlerExecute`](docs/sdks/transactionbundler/README.md#transactionbundlerexecute) - Construct Bundled Transaction
- [`uniswapV3UniswapLiquidityProvisionIncrease`](docs/sdks/uniswapv3/README.md#uniswapliquidityprovisionincrease) - Increase an LP position
- [`uniswapV3UniswapLiquidityProvisionInRange`](docs/sdks/uniswapv3/README.md#uniswapliquidityprovisioninrange) - Check if LP is Active.
- [`uniswapV3UniswapLiquidityProvisionMint`](docs/sdks/uniswapv3/README.md#uniswapliquidityprovisionmint) - Open a new LP position
- [`uniswapV3UniswapLiquidityProvisionPositions`](docs/sdks/uniswapv3/README.md#uniswapliquidityprovisionpositions) - List LP
- [`uniswapV3UniswapLiquidityProvisionWithdraw`](docs/sdks/uniswapv3/README.md#uniswapliquidityprovisionwithdraw) - Withdraw an LP position
- [`uniswapV3UniswapPoolPrice`](docs/sdks/uniswapv3/README.md#uniswappoolprice) - Pool Price
- [`uniswapV3UniswapQuoteBuyExactly`](docs/sdks/uniswapv3/README.md#uniswapquotebuyexactly) - Get Quote - to Specified Amount
- [`uniswapV3UniswapQuoteSellExactly`](docs/sdks/uniswapv3/README.md#uniswapquotesellexactly) - Get quote - From Specified Amount
- [`uniswapV3UniswapSwapBuyExactly`](docs/sdks/uniswapv3/README.md#uniswapswapbuyexactly) - Buy exact amount
- [`uniswapV3UniswapSwapSellExactly`](docs/sdks/uniswapv3/README.md#uniswapswapsellexactly) - Sell exact amount
- [`universalGenericAllowance`](docs/sdks/universal/README.md#genericallowance) - Get Allowance
- [`universalGenericAllowanceSet`](docs/sdks/universal/README.md#genericallowanceset) - Set Allowance
- [`universalGenericEns`](docs/sdks/universal/README.md#genericens) - Resolve ENS
- [`universalGenericPortfolio`](docs/sdks/universal/README.md#genericportfolio) - List User Portfolio
- [`universalGenericSupportedChains`](docs/sdks/universal/README.md#genericsupportedchains) - List Supported Chains
- [`universalGenericUnwrapWeth`](docs/sdks/universal/README.md#genericunwrapweth) - Unwrap WETH
- [`universalGenericWrapEth`](docs/sdks/universal/README.md#genericwrapeth) - Wrap ETH

</details>
<!-- End Standalone functions [standalone-funcs] -->

<!-- Start Retries [retries] -->
## Retries

Some of the endpoints in this SDK support retries.  If you use the SDK without any configuration, it will fall back to the default retry strategy provided by the API.  However, the default retry strategy can be overridden on a per-operation basis, or across the entire SDK.

To change the default retry strategy for a single API call, simply provide a retryConfig object to the call:
```typescript
import { CompassApiSDK } from "@compass-labs/api-sdk";

const compassApiSDK = new CompassApiSDK({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await compassApiSDK.aaveV3.aaveAaveSupportedTokens({}, {
    retries: {
      strategy: "backoff",
      backoff: {
        initialInterval: 1,
        maxInterval: 50,
        exponent: 1.1,
        maxElapsedTime: 100,
      },
      retryConnectionErrors: false,
    },
  });

  console.log(result);
}

run();

```

If you'd like to override the default retry strategy for all operations that support retries, you can provide a retryConfig at SDK initialization:
```typescript
import { CompassApiSDK } from "@compass-labs/api-sdk";

const compassApiSDK = new CompassApiSDK({
  retryConfig: {
    strategy: "backoff",
    backoff: {
      initialInterval: 1,
      maxInterval: 50,
      exponent: 1.1,
      maxElapsedTime: 100,
    },
    retryConnectionErrors: false,
  },
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await compassApiSDK.aaveV3.aaveAaveSupportedTokens({});

  console.log(result);
}

run();

```
<!-- End Retries [retries] -->

<!-- Start Error Handling [errors] -->
## Error Handling

[`CompassAPISDKError`](./src/models/errors/compassapisdkerror.ts) is the base class for all HTTP error responses. It has the following properties:

| Property            | Type       | Description                                                                             |
| ------------------- | ---------- | --------------------------------------------------------------------------------------- |
| `error.message`     | `string`   | Error message                                                                           |
| `error.statusCode`  | `number`   | HTTP response status code eg `404`                                                      |
| `error.headers`     | `Headers`  | HTTP response headers                                                                   |
| `error.body`        | `string`   | HTTP body. Can be empty string if no body is returned.                                  |
| `error.rawResponse` | `Response` | Raw HTTP response                                                                       |
| `error.data$`       |            | Optional. Some errors may contain structured data. [See Error Classes](#error-classes). |

### Example
```typescript
import { CompassApiSDK } from "@compass-labs/api-sdk";
import * as errors from "@compass-labs/api-sdk/models/errors";

const compassApiSDK = new CompassApiSDK({
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  try {
    const result = await compassApiSDK.aaveV3.aaveAaveSupportedTokens({});

    console.log(result);
  } catch (error) {
    // The base class for HTTP error responses
    if (error instanceof errors.CompassAPISDKError) {
      console.log(error.message);
      console.log(error.statusCode);
      console.log(error.body);
      console.log(error.headers);

      // Depending on the method different errors may be thrown
      if (error instanceof errors.HTTPValidationError) {
        console.log(error.data$.detail); // ValidationError[]
      }
    }
  }
}

run();

```

### Error Classes
**Primary errors:**
* [`CompassAPISDKError`](./src/models/errors/compassapisdkerror.ts): The base class for HTTP error responses.
  * [`HTTPValidationError`](./src/models/errors/httpvalidationerror.ts): Validation Error. Status code `422`.

<details><summary>Less common errors (6)</summary>

<br />

**Network errors:**
* [`ConnectionError`](./src/models/errors/httpclienterrors.ts): HTTP client was unable to make a request to a server.
* [`RequestTimeoutError`](./src/models/errors/httpclienterrors.ts): HTTP request timed out due to an AbortSignal signal.
* [`RequestAbortedError`](./src/models/errors/httpclienterrors.ts): HTTP request was aborted by the client.
* [`InvalidRequestError`](./src/models/errors/httpclienterrors.ts): Any input used to create a request is invalid.
* [`UnexpectedClientError`](./src/models/errors/httpclienterrors.ts): Unrecognised or unexpected error.


**Inherit from [`CompassAPISDKError`](./src/models/errors/compassapisdkerror.ts)**:
* [`ResponseValidationError`](./src/models/errors/responsevalidationerror.ts): Type mismatch between the data returned from the server and the structure expected by the SDK. See `error.rawValue` for the raw value and `error.pretty()` for a nicely formatted multi-line string.

</details>
<!-- End Error Handling [errors] -->

<!-- Start Server Selection [server] -->
## Server Selection

### Override Server URL Per-Client

The default server can be overridden globally by passing a URL to the `serverURL: string` optional parameter when initializing the SDK client instance. For example:
```typescript
import { CompassApiSDK } from "@compass-labs/api-sdk";

const compassApiSDK = new CompassApiSDK({
  serverURL: "https://api.compasslabs.ai",
  apiKeyAuth: "<YOUR_API_KEY_HERE>",
});

async function run() {
  const result = await compassApiSDK.aaveV3.aaveAaveSupportedTokens({});

  console.log(result);
}

run();

```
<!-- End Server Selection [server] -->

<!-- Start Custom HTTP Client [http-client] -->
## Custom HTTP Client

The TypeScript SDK makes API calls using an `HTTPClient` that wraps the native
[Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API). This
client is a thin wrapper around `fetch` and provides the ability to attach hooks
around the request lifecycle that can be used to modify the request or handle
errors and response.

The `HTTPClient` constructor takes an optional `fetcher` argument that can be
used to integrate a third-party HTTP client or when writing tests to mock out
the HTTP client and feed in fixtures.

The following example shows how to use the `"beforeRequest"` hook to to add a
custom header and a timeout to requests and how to use the `"requestError"` hook
to log errors:

```typescript
import { CompassApiSDK } from "@compass-labs/api-sdk";
import { HTTPClient } from "@compass-labs/api-sdk/lib/http";

const httpClient = new HTTPClient({
  // fetcher takes a function that has the same signature as native `fetch`.
  fetcher: (request) => {
    return fetch(request);
  }
});

httpClient.addHook("beforeRequest", (request) => {
  const nextRequest = new Request(request, {
    signal: request.signal || AbortSignal.timeout(5000)
  });

  nextRequest.headers.set("x-custom-header", "custom value");

  return nextRequest;
});

httpClient.addHook("requestError", (error, request) => {
  console.group("Request Error");
  console.log("Reason:", `${error}`);
  console.log("Endpoint:", `${request.method} ${request.url}`);
  console.groupEnd();
});

const sdk = new CompassApiSDK({ httpClient: httpClient });
```
<!-- End Custom HTTP Client [http-client] -->

<!-- Start Debugging [debug] -->
## Debugging

You can setup your SDK to emit debug logs for SDK requests and responses.

You can pass a logger that matches `console`'s interface as an SDK option.

> [!WARNING]
> Beware that debug logging will reveal secrets, like API tokens in headers, in log messages printed to a console or files. It's recommended to use this feature only during local development and not in production.

```typescript
import { CompassApiSDK } from "@compass-labs/api-sdk";

const sdk = new CompassApiSDK({ debugLogger: console });
```
<!-- End Debugging [debug] -->

<!-- Placeholder for Future Speakeasy SDK Sections -->

# Development

## Maturity

This SDK is in beta, and there may be breaking changes between versions without a major version update. Therefore, we recommend pinning usage
to a specific package version. This way, you can install the same version each time without breaking changes unless you are intentionally
looking for the latest version.

## Contributions

While we value open-source contributions to this SDK, this library is generated programmatically. Any manual changes added to internal files will be overwritten on the next generation. 
We look forward to hearing your feedback. Feel free to open a PR or an issue with a proof of concept and we'll do our best to include it in a future release. 
