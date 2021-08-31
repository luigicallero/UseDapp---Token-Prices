# 🤝 useDapp - Getting Crypto and Token Prices
## Framework for rapid Dapp development.
## Simple. Robust. Extendable. Testable.
> useDapp is a really valuable tool for both junior and experienced developers. It helps backend developer to rely on a tested and agile tool for most frontend features and scenarios. Great benefit for us as developers, is that we can get accurate information for our clients, since useDapp captures any change on the last executed block that could reflect in a change in our DApp. Thus becoming an extraordinary benefit, specially for Defi DApps, where you need the most up to date crypto values.

> In this tutorial I am goint to show how to capture the value of native UNISWAP token. 

#
# Requirements
### In order to perform this tutorial you will need:
  *** "git" to be able to download (clone) our reposittory from Github (GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere)
  
  *** NodeJS to install all required modules and dependencies in your machine (specifically on the repossitory that will be created when you clone our repo) used by our project

> GIT
 
> For Linux distributions use the following
```
sudo apt-get install git
```
> Configure GIT using the following commands:
```
git config --global user.name "YOUR-USERNAME"
git config --global user.email "YOUR-EMAIL"
```

> Nodejs
 
>   Check recommended version from: https://nodejs.org/en/ 

>   Install recommended version following this link: https://github.com/nodesource/distributions/blob/master/README.md

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

#
## Documentation
> https://usedapp.readthedocs.io/en/latest
