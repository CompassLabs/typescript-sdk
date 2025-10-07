<!-- Start SDK Example Usage [usage] -->
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