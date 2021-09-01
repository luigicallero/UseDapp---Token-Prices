🤝 useDapp - Getting Crypto and Token Prices
==============================================

## Framework for rapid Dapp development.
Simple. Robust. Extendable. Testable.
-----------------------------------------
> useDapp is a really valuable tool for both junior and experienced developers. It helps backend developer to rely on a tested and agile tool for most frontend features and scenarios. Great benefit for us as developers, is that we can get accurate information for our clients, since useDapp captures any change on the last executed block that could reflect in a change in our DApp. Thus becoming an extraordinary benefit, specially for Defi DApps, where you need the most up to date crypto values.

In this tutorial I am going to show how to capture the value of native UNISWAP token.

 ![uni_token](https://user-images.githubusercontent.com/58836287/131611654-2988ba83-d86c-42a2-8620-6fd16311f55e.png)

#
Requirements
===============
### In order to perform this tutorial you will need:
  **GIT** to be able to download (clone) our reposittory from Github (GitHub is a code hosting platform for version control and collaboration. It lets you and others work together on projects from anywhere)
  
  **NodeJS** to install and manage all required modules and dependencies in your machine (specifically on the repossitory that will be created when you clone our repo).


> GIT

https://git-scm.com/downloads

For Linux distributions use the following
```
sudo apt-get install git
```

Configure GIT using the following commands:
```
git config --global user.name "YOUR-USERNAME"
git config --global user.email "YOUR-EMAIL"
```

> Nodejs
 
Download and Install the recommended version from: https://nodejs.org/en/ 

![nodejs](https://user-images.githubusercontent.com/58836287/131609738-faa4cce2-3058-4824-b1ca-57b04dc52113.png)

#
Clonning the repo:
================
The **git clone** command will copy the reppository in Github to your machine creating a folder with the same name as the repo. Once completed, move into the new folder:
```
git clone https://github.com/luigicallero/UseDapp_TokenPrices.git
cd ./UseDapp_TokenPrices
```
Now execute this command to install all required packages and dependencies of the repo:
```
npm install
```

#
Start application with useDapp
===============
To start the Web Server and instantiate the application execute:
```
npm start
```
![npm_start](https://user-images.githubusercontent.com/58836287/131610483-080ab8c0-6489-41cf-986f-a9af3d8d42e8.png)

Open http://localhost:8080 to view it in the browser:

![useDapp_initial](https://user-images.githubusercontent.com/58836287/131610505-58d740ee-af08-4127-ba67-532b6906c1df.png)

#
Adding UNI token price to our App:
===========================

Go to https://www.coingecko.com/ and click for UNI coin

![coingecko_uni](https://user-images.githubusercontent.com/58836287/131666093-a66496e0-8edf-4b87-a90d-b23c1dfc10b9.png)



On the right side of the page under "Info" you will be able to click and copy the contract address where it says "Contract:" (we will use this contract address in next step)

![coingecko_uniswap_contract](https://user-images.githubusercontent.com/58836287/131666114-00a109c5-2bf2-40b0-ae74-d0d28090486d.png)


Go to the folder src/pages and look for the file Prices.tsx

Here we update the file with the token information we want to see the price of.

Code added:
 ```
 const UNISWAP_CONTRACT = '0x1f9840a85d5af5bf1d1762f925bdaddc4201f984'
 const uniswapPrice = useCoingeckoTokenPrice(UNISWAP_CONTRACT, 'usd') 
 ```
![uniswap_price_udpate](https://user-images.githubusercontent.com/58836287/131611099-3946b1e7-7e6f-4ab5-9978-1b4e81be4840.png)


I also updated "prices" file to add the uniswap price to the app with the following code (copy pasted the other coin price and modified as shown here):
```
            {uniswapPrice && (
              <ContentRow>
                <Label>Uniswap price:</Label> <Label>$ </Label>
                <TextInline>{uniswapPrice}</TextInline>
              </ContentRow>
            )}
```
![uniswap_price_print](https://user-images.githubusercontent.com/58836287/131611108-ce3332aa-c855-47d7-ac5a-cf467ef1f969.png)

Working perfectly!!! and updating every time there is a change in price (since useDapp checks for updates on every new block)

![uniswap_price_1](https://user-images.githubusercontent.com/58836287/131609569-ad04de74-dab3-43c7-b1b1-41636c715593.png)

#
Useful Documentation
=====
> https://usedapp.readthedocs.io/en/latest}

> https://www.youtube.com/watch?v=DlSj9E6NP5g&t=3125s
