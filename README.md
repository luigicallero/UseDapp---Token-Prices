# useDapp - Getting Crypto and Token Prices
## Framework for rapid Dapp development.
## Simple. Robust. Extendable. Testable.

#
## Documentation
> https://usedapp.readthedocs.io/en/latest
#
# Requirements
> Nodejs
#
# Clonning repo: 
```
git clone https://github.com/luigicallero/UseDapp_TokenPrices.git
cd ./UseDapp_TokenPrices
npm install
```
#
## Start application with useDapp
```
npm start
```
Open http://localhost:8080 to view it in the browser.
#
# Adding other token prices:
> Go to the folder src/pages and look for the file Prices.tsx
> Updating the file with the token information we want to see the price of:
```
  const UNISWAP_CONTRACT = '0x1f9840a85d5af5bf1d1762f925bdaddc4201f984'
  const uniswapPrice = useCoingeckoTokenPrice(UNISWAP_CONTRACT, 'usd') 
```
IMAGE OF FILE UPDATED
I updated "prices" file to add the uniswap price in the page

IMAGE from PAGE LIVE
Working perfectly!!! and updating every time there is a change in price (since useDapp checks for updates on every new block)
