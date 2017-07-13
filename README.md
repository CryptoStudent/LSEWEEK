# LSE WEEK 2017

Tutorial for mining easily.
1. [Create a Wallet](#create-a-wallet)
   * [Ethereum](#ethereum)
   * [Zcash](#zcash)
   * [Bitcoin](#bitcoin)
2. [Mining](#mining)
   * [Mining Pool Hub](#mining-pool-hub)
   * [Zcash](#zcash-mining)
   * [Ethereum](#ethereum-mining)
   * [Dual Mining](#dual-mining-ethereum--siacoin)
3. [Buy/Sell Cryptocurrency](#exchangebuysell-cryptocurrency)
   * [Coinbase](#coinbase)
   * [Poloniex/Bittrex](#poloniex--bittrex)
   * [Livecoin](#livecoin)
4. [Interesting Links](#interesting-links)
   
     

## Create a Wallet

### Ethereum

1. Online Wallet, accessible anywhere [MyEtherWallet](https://www.myetherwallet.com/)
2. Offline Wallet, [Exodus](https://www.exodus.io/)

### Zcash
1. Online Wallet, accessible anywhere Web And Android [Cryptonator](https://fr.cryptonator.com/). Also a wallet for Bitcoin, dash, Litecoin, Monero.

### Bitcoin
1. Online Wallet, [Coinbase](https://www.coinbase.com/).


## Mining

### Mining Pool Hub

Auto-switch algorithm script. Best profitability.

1. Create an account [here](https://miningpoolhub.com/index.php?page=register)
2. [Download](https://github.com/aaronsace/MultiPoolMiner/releases) the miner
3. Unzip
4. Replace Start.bat with this and change [USERNAME] and [WORKERNAME]
```shell
## Script for NVIDIA
powershell -version 5.0 -noexit -executionpolicy bypass -windowstyle maximized -command "&.\multipoolminer.ps1 -username [USERNAME] -workername [WORKERNAME] -interval 60 -location europe -ssl -type nvidia -algorithm cryptonight,ethash,equihash,groestl,lyra2z,neoscrypt,pascal,sia -poolname miningpoolhub -currency btc,eur "
## Script for AMD
setx GPU_FORCE_64BIT_PTR 1
setx GPU_MAX_HEAP_SIZE 100
setx GPU_USE_SYNC_OBJECTS 1
setx GPU_MAX_ALLOC_PERCENT 100
setx GPU_SINGLE_ALLOC_PERCENT 100
powershell -version 5.0 -noexit -executionpolicy bypass -windowstyle maximized -command "&.\multipoolminer.ps1 -username [USERNAME] -workername [WORKERNAME] -interval 60 -location europe -ssl -type amd -algorithm cryptonight,ethash,equihash,groestl,lyra2z,neoscrypt,pascal,sia -poolname miningpoolhub -currency btc,eur "
## You can add or remove algorith depending on which coin you want to mine.
```
5. Launch start.bat
6. Wait for the benchmark to finish.
7. Go to your MiningPoolHub account, go to Auto Exchange and set the currency you want to get at the end. MPH will auto exchange the coin you mine to this currency.
8. Click on the left in the pool tab on the currency you set in Auto Exchange.
9. Click on Wallet then add your Wallet address to this specific currency.

MPH will automatically pay you once the threshold has been reached.
Enjoy !

### Zcash Mining

1. Go to [Flypool](https://zcash.flypool.org/)
2. Follow tutorial according to your GPU(AMD/NVIDIA)
3. Use EWBF for NVIDIA, Claymore Miner for AMD
4. Example of start.bat for EWBF to place in the folder, [WORKERNAME] can be anything
```shell
miner --server eu1-zcash.flypool.org --port 3333 --user [YOURZCASHADDRESS].[YOURWORKERNAME] --pass x --cuda_devices 0 1 2 3
```

### Ethereum Mining

1. Go to [Ethermine](https://ethermine.org/)
2. Follow tutorial
3. Download Claymores Miner
4. Example of start.bat for NVIDIA and AMD to place in the folder.
```shell
## NVIDIA
EthDcrMiner64.exe -epool eu1.ethermine.org:4444 -ewal [YOURETHEREUMADRESS].[YOURWORKERNAME] -epsw x
## AMD
setx GPU_FORCE_64BIT_PTR 0
setx GPU_MAX_HEAP_SIZE 100
setx GPU_USE_SYNC_OBJECTS 1
setx GPU_MAX_ALLOC_PERCENT 100
setx GPU_SINGLE_ALLOC_PERCENT 100
EthDcrMiner64.exe -epool eu1.ethermine.org:4444 -ewal [YOURETHEREUMADRESS].[YOURWORKERNAME] -epsw x
```

### Dual Mining Ethereum + Siacoin
1. Go to [Ethermine](https://ethermine.org/)
2. Download Claymores Miner
3. Create an account at [MiningPoolHub](https://miningpoolhub.com/index.php?page=register)
4. Create a start.bat
```shell
EthDcrMiner64.exe -epool eu1.ethermine.org:14444 -ewal [YOURETHEREUMADRESS].[YOURWORKERNAME] -esm 2 -epsw x -allpools 1 -dpool stratum+tcp://hub.miningpoolhub.com:20550 -dwal [YOURMPHUSERNAME].[YOURWORKERNAME] -dpsw x -dcoin sc
```

## Exchange/Buy/Sell Cryptocurrency

### Coinbase

Great website to buy and sell Bitcoin/Ethereum/Litecoin
[Coinbase](https://www.coinbase.com/)

### Poloniex / Bittrex

Great website for buying and selling a lot of currencies and Altcoins but less user-friendly
[Poloniex](https://poloniex.com/) , [Bittrex](https://bittrex.com/)

### Livecoin

Great website for buying and selling new currencies.
[Livecoin](https://www.livecoin.net)

## Interesting Links

### What To Mine

Great website that tells you what is the most profitable coin to mine depending on your hardware.
[What To Mine](https://whattomine.com/coins)

### Crypto Compare

Great website to get mnore information on Mining, Wallets, different coins, and portfolio.
[Crypto Compare](https://www.cryptocompare.com)

### Youtube Node Investor

Interesting Youtube Channel around Bitcoin & Altcoins
[Node Investor Youtube](https://www.youtube.com/channel/UCa81HAp1se359Sr5qEMMP7A)

## Contact

You can ask us any questions by creating an issue.

Created by Antidote


