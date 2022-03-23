# ETH_HDwallet_Generator

This package allows you to create a ethereum wallet, that you can use anywhere , all wallets are unique with Mnemonic that will allow you to recover accounts

## Installation

Install [Node js](https://nodejs.org/en/) to use this package and run any of below command

### npm

```bash
npm i eth_hdwallet_generator
```
### yarn

```bash
yarn add eth_hdwallet_generator
```

## Usage
The package is fairly very easy to use
# Creating wallet
```javascript
const {GenerateWallet} = require('eth_hdwallet_generator')
GenerateWallet().then(wallet=>{
    console.log(wallet)
})
/*
== Output == 
{
  address: '0x97Dd8C0383B32148A7b5cF0Edb65aFee921cbfcA',
  privKey: '0xe28b675af4dd828b32a73afff4f071cc9bcde437995661c66af507ef13efc2b7',
  mnemonic: 'Dog Parashoot Boy Cat Super Monday Noob Sniper US Damn At Stamp Stupid Goat Jake'
}
*/
```

# Recover wallet
```javascript
const {recoverWallet} = require('eth_hdwallet_generator')
let mnemonic = "Dog Parashoot Boy Cat Super Monday Noob Sniper US Damn At Stamp Stupid Goat Jake"
recoverWallet(mnemonic).then(wallet=>{
    console.log(wallet)
})
/*
== Output == 
{
  address: '0x97Dd8C0383B32148A7b5cF0Edb65aFee921cbfcA',
  privKey: '0xe28b675af4dd828b32a73afff4f071cc9bcde437995661c66af507ef13efc2b7'
}
*/
```

## Special Thanks 
This package came into existance because of [tboydston]('https://www.npmjs.com/package/hdaddressgenerator') wallet generator, We added support for Mnemonics only

