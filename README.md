# How to add Stargaze Testnet to wallets

You can follow these steps in Google Chrome, Brave browser, or any other browser which supports wallet extension(Keplr, Cosmostation, Leap, etc). 


## Keplr
> download link: https://www.keplr.app/download

<p align="center">
  <img src="https://user-images.githubusercontent.com/6451384/205146901-66a6c2fe-1a42-46d3-8946-3f83f4684457.png">
</p>


### 1) Open Keplr wallet, right-click on it, and click on ``Inspect``.

This will open ``DevTools`` window.

![](./images/stargaze-testnet-keplr-01.png)

### 2) On the ``DevTools`` window, click on the ``Console`` tab.

![](./images/stargaze-testnet-keplr-02.png)

### 3) Copy the following code.

```js
window.keplr.experimentalSuggestChain({
  chainId: 'elgafar-1',
  chainName: 'Stargaze Testnet',
  rpc: 'https://rpc.elgafar-1.stargaze-apis.com/',
  rest: 'https://rest.elgafar-1.stargaze-apis.com/',
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
      gasPriceStep: {
        low: 0.0,
        average: 0.0,
        high: 0.025,
      },
    },
  ],
  stakeCurrency: {
    coinDenom: 'STARS',
    coinMinimalDenom: 'ustars',
    coinDecimals: 6,
    coinGeckoId: 'stars',
    coinImageUrl: 'https://stargaze.zone/logo.png',
  },
  coinType: 118,
  features: ['ibc-transfer'],
  explorerUrlToTx: 'https://www.mintscan.io/stargaze/txs/{txHash}',
});
```

### 4) Paste the code in the ``Console`` tab.

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

> download link: https://www.cosmostation.io/wallet/#extension

<p align="center">
  <img src="https://user-images.githubusercontent.com/6451384/204154092-935309eb-a227-42a5-aa72-40d463aae4be.png">
</p>

### 1) Open Cosmostation wallet, right-click on it, and click on ``Inspect``.

This will open ``DevTools`` window.

![image](https://user-images.githubusercontent.com/6451384/205151532-c8d381b9-e5a2-41db-8f7f-3c0be4497333.png)

### 2) On the ``DevTools`` window, click on the ``Console`` tab.

![image](https://user-images.githubusercontent.com/6451384/205151772-6351ed75-9e5f-499c-b962-eeb8ed9aa37c.png)

### 3) Copy the following code.

```js
window.cosmostation.cosmos.request({
  method: "cos_addChain",
  params: {
    chainId: 'elgafar-1',
    chainName: 'Stargaze Testnet',
    addressPrefix: 'stars',
    baseDenom: 'ustars',
    displayDenom: 'STARS',
    restURL: 'https://rest.elgafar-1.stargaze-apis.com/',
    coinType: '118',
    decimals: 6,
    gasRate: {
      low: '0.0',
      average: '0.0',
      tiny: '0.025',
    },
  },
});
```

### 4) Paste the code in the ``Console`` tab.

![image](https://user-images.githubusercontent.com/6451384/205151980-fb782523-05b3-4a8e-85d1-3a73bb8f406a.png)

### 5) Press ``Enter``.

![image](https://user-images.githubusercontent.com/6451384/205152165-c499d334-88e9-4a58-a149-27b32123aa67.png)

### 6) Click ``Confirm`` button on Cosmostation Wallet window.

![image](https://user-images.githubusercontent.com/6451384/205155693-ff8f1e86-4157-4a41-b806-a93c1f93b195.png)

### 7) Close Cosmostation Wallet and re-open it.

### 8) Click on the networks present at top of Cosmostation Wallet,and select ``Stargaze Testnet``.

![image](https://user-images.githubusercontent.com/6451384/205156071-fda9e235-8589-4666-b03b-eae34e983cac.png)

### 9) The wallet is ready and you can copy the address.

![image](https://user-images.githubusercontent.com/6451384/205156198-74d396df-10c5-41ce-9bde-9daf73c4ef6a.png)


## Leap

> download link: https://www.leapwallet.io/

<p align="center">
  <img src="https://user-images.githubusercontent.com/6451384/204154095-cdf57f24-2c4f-42ab-a408-78e04c5abba6.png">
</p>

### 1) Click the hamburger button.

![image](https://user-images.githubusercontent.com/6451384/205367915-c2b02c71-961d-424b-977d-769bbf921633.png)

### 2) Click the `Network` menu under the Preferences category.

![image](https://user-images.githubusercontent.com/6451384/205368066-36dd0e3f-d6be-4dc8-877f-dd5c13d8fef8.png)

### 3) Click the `Testnet` option.

![image](https://user-images.githubusercontent.com/6451384/205368218-19b15f70-d595-47e6-81cf-89bb4e066348.png)


### 4) The wallet is ready for testnet and you can copy the address.

![image](https://user-images.githubusercontent.com/6451384/205368356-d549c66a-7708-4055-975e-354fbd81933d.png)



# How to get $STARS on Stargaze Testnet

1. Visit the faucet channel on the Stargaze discord

- https://discord.com/channels/755548171941445642/940653213022031912

2. Copy your stargaze address from your wallet
3. Send a request in the #faucet channel with a following command:

- `$request YOUR_STARS_ADDRESS`

![image](https://user-images.githubusercontent.com/6451384/204154109-393de5cb-7894-4a5e-86ac-cf62cf421444.png)

4. The bot will reply with the transaction info
