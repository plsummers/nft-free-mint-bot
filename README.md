Environment configuration
Recommended system: Ubuntu 20.04

python version: Python 3.*

Commands that need to be executed before running:

`sudo apt-get update`

`sudo apt-get install python3-dev -y`

`sudo apt-get install screen -y`

`pip3 install bs4 lxml web3`

file configuration

Lines 20-25 are replaced with your own key, which is free to apply

Line 27 `MAX_GAS_FEE` The maximum `gas_fee` that can be accepted

28 lines `MAX_MINT_PER_NFT` The maximum number of mints that can be mint, if it exceeds, it will be skipped (inaccurate)

30 lines of `FOLLOW_ADDR_LIST` follow the mint address, support multiple

Line 31 `MAX_ETH_FOR_FOLLOW` The maximum price that can be accepted when copying mint (unit: ETH)

33 lines of blacklist blacklist, skip when nft_name contains these characters

Function

Get the freemint project via the free API in www.acnft.xyz

Automatically cancel transactions when they are stuck pending (hopefully useful)

Skip some imitation disks and mint nfts by setting a blacklist and minted logs

Random gasfee within range (maybe some projects detect bots?)

Automatically broadcast mint progress through TG robot

2022.5.31 Update

Added copy mint mode to support multiple addresses
run
After everything is configured, log in to your server (recommended US region, mint time is completed within 3 seconds on average, you can also use your own machine), enter screento open a new terminal to ensure continuous running in the background, and then enter python3 free_mint_nft.pyto start running, if If everything is normal, it will prompt init success like the picture below, and then it can be turned off. The next time the server is turned on, the input screen -rcan be restored to the terminal .


![image](https://github.com/jungleninja/nft-free-mint-bot/blob/main/1.png)
