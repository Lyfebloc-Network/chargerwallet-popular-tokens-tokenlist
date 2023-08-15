## chargerwallet-popular-tokens-tokenlist
*Disclaimer: 
The list is from the Popular tokenlist filtered by Volume (24H) on explorers listed below:*
https://polygonscan.com/tokens

https://gnosisscan.io/tokens

https://etherscan.io/tokens

https://bscsscan.com/tokens

**Date of snapshot: August 15, 2023**

Chargerwallet SDK PopularTokens token list

Web: [https://chargerwallet.com](https://chargerwallet.com)

Docs: [https://docs.chargerwallet.com/](https://docs.chargerwallet.com/)

Use Chargerwallet SDK to fetch popular token list

```
import { Sdk, NetworkNames, randomPrivateKey } from 'chargerwallet';
const privateKey = randomPrivateKey();
let sdk: Sdk
sdk = new Sdk({
  privateKey,
  }, {
    networkName: 'mainnet' as NetworkNames, 
    });
async function main() {
  const output = await sdk.getTokenListTokens({
    name: 'ChargerwalletPopularTokens',
  });

  console.log('token list tokens', output);
}

main().catch(console.error);
