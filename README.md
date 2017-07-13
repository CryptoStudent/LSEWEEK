# LSE WEEK 2017

Programs and scripts for mining.

## Mining Pool Hub

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



