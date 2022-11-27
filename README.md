# How to add Stargaze Testnet to wallets

You can follow these steps in Google Chrome, Brave browser, or any other browser which supports wallet extension(Keplr, Cosmostation, Leap, etc). 


## Keplr

### 1) Open Keplr wallet, right click on it and click on ``Inspect``.

This will open ``DevTools`` window.

![](./images/stargaze-testnet-keplr-01.png)

### 2) On the ``DevTools`` window, click on ``Console`` tab.

![](./images/stargaze-testnet-keplr-02.png)

### 3) Copy the following code.

```js
window.keplr.experimentalSuggestChain({
  rpc: 'https://rpc.elgafar-1.stargaze-apis.com/',
  rest: 'https://rest.elgafar-1.stargaze-apis.com/',
  chainId: 'elgafar-1',
  chainName: 'Stargaze Testnet',
  stakeCurrency: {
    coinDenom: 'STARS',
    coinMinimalDenom: 'ustars',
    coinDecimals: 6,
    coinGeckoId: 'stars',
    coinImageUrl: 'https://stargaze.zone/logo.png',
  },
  bip44: {
    coinType: 118,
  },
  bech32Config: {
    bech32PrefixAccAddr: 'stars',
    bech32PrefixAccPub: 'stars' + 'pub',
    bech32PrefixValAddr: 'stars' + 'valoper',
    bech32PrefixValPub: 'stars' + 'valoperpub',
    bech32PrefixConsAddr: 'stars' + 'valcons',
    bech32PrefixConsPub: 'stars' + 'valconspub',
  },
  currencies: [
    {
      coinDenom: 'STARS',
      coinMinimalDenom: 'ustars',
      coinDecimals: 6,
      coinGeckoId: 'stars',
      coinImageUrl: 'https://stargaze.zone/logo.png',
    },
  ],
  feeCurrencies: [
    {
      coinDenom: 'STARS',
      coinMinimalDenom: 'ustars',
      coinDecimals: 6,
      coinGeckoId: 'stargaze',
      coinImageUrl: 'https://stargaze.zone/logo.png',
    },
  ],
  coinType: 118,
  gasPriceStep: {
    low: 0.0,
    average: 0.0,
    high: 0.025,
  },
  features: ['stargate', 'ibc-transfer', 'no-legacy-stdTx'],
  explorerUrlToTx: 'https://www.mintscan.io/stargaze/txs/{txHash}',
});
```

### 4) Paste the code in ``Console`` tab.

![](./images/stargaze-testnet-keplr-03.png)

### 5) Press ``Enter``.

![](./images/stargaze-testnet-keplr-04.png)

### 6) Click ``Approve`` button on Keplr Wallet window.

![](./images/stargaze-testnet-keplr-05.png)

### 7) Close Keplr Wallet and re-open it.

### 8) Click on the networks present at top of Keplr Wallet, scroll down, and select ``Stargaze Testnet``.

![](./images/stargaze-testnet-keplr-06.png)

### 9) The wallet is ready and you can copy the address.

![](./images/stargaze-testnet-keplr-07.png)

## Cosmostation
- (TBU)

## Leap
- (TBU)

# How to get $STARS on Stargaze Testnet

1. Visit the faucet channel on the Stargaze discord

- https://discord.com/channels/755548171941445642/940653213022031912

2. Follow the guide suggested by the bot
