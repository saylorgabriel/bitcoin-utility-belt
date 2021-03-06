# Bitcoin Utility Belt
[![NPM](https://img.shields.io/npm/v/bitcoin-utility-belt.svg?style=flat-square)](https://www.npmjs.com/package/bitcoin-utility-belt)
[![NPM](https://img.shields.io/david/MiguelMedeiros/bitcoin-utility-belt.svg?style=flat-square)](https://david-dm.org/MiguelMedeiros/bitcoin-utility-belt#info=dependencies)
[![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat-square)](https://github.com/MiguelMedeiros/bitcoin-utility-belt)

I've made this project to make easy to use a lot of Bitcoin functions that you need to build a website or a NodeJS application. You can read the examples to find out how to use it! Feel free to contribute with code or a donation!

## Readme Index
  * [NodeJS Installation](#nodejs-installation)
  * [Browser Installation](#browser-installation)
  * [How to compile a new browser version](#how-to-compile-a-new-browser-version)
  * [Functions](#functions)
    * [Blockchain](#blockchain-3pbp)
    * [Messages](#messages)
    * [Wallets](#wallets)
  * [Examples](#examples)
    * Random Wallet Generator
  * [Contributing](#contributing)
  * [Donate](#donate-btc)
  * [License](#license-mit)

## NodeJS Installation
You just need to install the [npm package](https://www.npmjs.com/package/bitcoin-utility-belt) to your project.
``` bash
npm install bitcoin-utility-belt --save
```

Here is an example: 
``` node
// import bitcoin utility belt
let belt = require("bitcoin-utility-belt");

// creating random wallets
// type: P2PKH (default)
let wallet = belt.wallet.create();
console.log(wallet);
```

## Browser Installation
You just need to import the `/dist/bitcoin-utility-belt.js` to your HTML to have access to the functions.  
Here is an example:
``` html
<!-- Importing Bitcoin Utility Belt script -->
<script src="../../dist/bitcoin-utility-belt.min.js"></script>
<script>
  // creating random wallets
  // type: P2PKH (default)
  var wallet = belt.wallet.create();
  console.log(wallet);
</script>
```

## How to compile a new browser version
You have already a compiled version in the directory `/dist` (extended and minified files).  
But if you want to compile for your self run the script:
``` bash
npm run build
```

## Functions
The list below should be very easy to understand. 
Some of them interact (via HTTPS) with a 3rd Party Blockchain Provider (3PBP).
I've made HTML and NodeJS examples, so you can understand how it works!

### Blockchain (3PBP)
- Get Address Info [[HTML example]](https://github.com/MiguelMedeiros/bitcoin-utility-belt/blob/master/examples/html/blockchain-address-info.html) [[NodeJS example]](https://github.com/MiguelMedeiros/bitcoin-utility-belt/blob/master/examples/nodejs/blockchain-address-info.js)
- Get Blocks Info [[HTML example]](https://github.com/MiguelMedeiros/bitcoin-utility-belt/blob/master/examples/html/blockchain-blocks-info.html) [[NodeJS example]](https://github.com/MiguelMedeiros/bitcoin-utility-belt/blob/master/examples/nodejs/blockchain-blocks-info.js)
- Get Blockchain Pools Info [[HTML example]](https://github.com/MiguelMedeiros/bitcoin-utility-belt/blob/master/examples/html/blockchain-pools-info.html) [[NodeJS example]](https://github.com/MiguelMedeiros/bitcoin-utility-belt/blob/master/examples/nodejs/blockchain-pools-info.js)
- Search for OP_RETURN texts [[HTML example]](https://github.com/MiguelMedeiros/bitcoin-utility-belt/blob/master/examples/html/blockchain-search-op_return.html) [[NodeJS example]](https://github.com/MiguelMedeiros/bitcoin-utility-belt/blob/master/examples/nodejs/blockchain-search-op_return.js)
- Get Blockchain Statistics [[HTML example]](https://github.com/MiguelMedeiros/bitcoin-utility-belt/blob/master/examples/html/blockchain-statistics.html) [[NodeJS example]](https://github.com/MiguelMedeiros/bitcoin-utility-belt/blob/master/examples/nodejs/blockchain-statistics.js)
- Get Blockchain Totals Info [[HTML example]](https://github.com/MiguelMedeiros/bitcoin-utility-belt/blob/master/examples/html/blockchain-totals-info.html) [[NodeJS example]](https://github.com/MiguelMedeiros/bitcoin-utility-belt/blob/master/examples/nodejs/blockchain-totals-info.js)

### Messages
- Sign and Verify Messages [[HTML example]](https://github.com/MiguelMedeiros/bitcoin-utility-belt/blob/master/examples/html/message-sign-verify.html) [[NodeJS example]](https://github.com/MiguelMedeiros/bitcoin-utility-belt/blob/master/examples/nodejs/message-sign-verify.js)

### Wallets
- Creating Wallets (P2PKH, P2SH, P2WPKH and P2WSH) [[HTML example]](https://github.com/MiguelMedeiros/bitcoin-utility-belt/blob/master/examples/html/wallet-create.html) [[NodeJS example]](https://github.com/MiguelMedeiros/bitcoin-utility-belt/blob/master/examples/nodejs/wallet-create.js)
- Creating Brain Wallet [[HTML example]](https://github.com/MiguelMedeiros/bitcoin-utility-belt/blob/master/examples/html/wallet-brainwallet.html) [[NodeJS example]](https://github.com/MiguelMedeiros/bitcoin-utility-belt/blob/master/examples/nodejs/wallet-brainwallet.js)
- Creating and Validating Mnemonic Words [[HTML example]](https://github.com/MiguelMedeiros/bitcoin-utility-belt/blob/master/examples/html/wallet-mnemonic-words.html) [[NodeJS example]](https://github.com/MiguelMedeiros/bitcoin-utility-belt/blob/master/examples/nodejs/wallet-mnemonic-words.js)
- Create MultiSig Address [[HTML example]](https://github.com/MiguelMedeiros/bitcoin-utility-belt/blob/master/examples/html/wallet-multisig-address.html) [[NodeJS example]](https://github.com/MiguelMedeiros/bitcoin-utility-belt/blob/master/examples/nodejs/wallet-multisig-address.js)
- Creating Seed (bip32 format) [[HTML example]](https://github.com/MiguelMedeiros/bitcoin-utility-belt/blob/master/examples/html/wallet-create-seed-bip32.html) [[NodeJS example]](https://github.com/MiguelMedeiros/bitcoin-utility-belt/blob/master/examples/nodejs/wallet-create-seed-bip32.js)
- Creating Seed (bip44 format) [[HTML example]](https://github.com/MiguelMedeiros/bitcoin-utility-belt/blob/master/examples/html/wallet-create-seed-bip44.html) [[NodeJS example]](https://github.com/MiguelMedeiros/bitcoin-utility-belt/blob/master/examples/nodejs/wallet-create-seed-bip44.js)
- Creating Seed (bip49 format) [[HTML example]](https://github.com/MiguelMedeiros/bitcoin-utility-belt/blob/master/examples/html/wallet-create-seed-bip49.html) [[NodeJS example]](https://github.com/MiguelMedeiros/bitcoin-utility-belt/blob/master/examples/nodejs/wallet-create-seed-bip49.js)
- Encrypt and Decrypt Private Key (bip38) [[HTML example]](https://github.com/MiguelMedeiros/bitcoin-utility-belt/blob/master/examples/html/wallet-encrypt-decrypt.html) [[NodeJS example]](https://github.com/MiguelMedeiros/bitcoin-utility-belt/blob/master/examples/nodejs/wallet-encrypt-decrypt.js)
- Recover Address from Private Key (WIF format) [[HTML example]](https://github.com/MiguelMedeiros/bitcoin-utility-belt/blob/master/examples/html/wallet-recover-address.html) [[NodeJS example]](https://github.com/MiguelMedeiros/bitcoin-utility-belt/blob/master/examples/nodejs/wallet-recover-address.js)
- Recover Wallets from Seed [[HTML example]](https://github.com/MiguelMedeiros/bitcoin-utility-belt/blob/master/examples/html/wallet-recover-seed.html) [[NodeJS example]](https://github.com/MiguelMedeiros/bitcoin-utility-belt/blob/master/examples/nodejs/wallet-recover-seed.js)
- Validate Wallet Address [[HTML example]](https://github.com/MiguelMedeiros/bitcoin-utility-belt/blob/master/examples/html/wallet-validate-address.html) [[NodeJS example]](https://github.com/MiguelMedeiros/bitcoin-utility-belt/blob/master/examples/nodejs/wallet-validate-address.js)

## Examples
- Random Wallet Generator: [[Github Code]](https://github.com/MiguelMedeiros/bitcoin-utility-belt-examples/blob/master/wallet-generator.html) [[Live Coding Video]](https://www.youtube.com/watch?v=z2GjZU1cpb8)
- Brain Wallet Generator: [[Github Code]](https://github.com/MiguelMedeiros/bitcoin-utility-belt-examples/blob/master/brainwallet-generator.html) [[Live Coding Video]](https://www.youtube.com/watch?v=7Iqsl9C1g-4)

## Contributing
I'll be glad to receive new pull requests to improve this project! Feel free to contribute!

## Donate BTC
If you really liked the project and want to donate, here is the official wallet for this project.  
Official Wallet: 18kXMmrDtgfeQgVmwfmygTaYLyQuVS4chK

## LICENSE [MIT](LICENSE)