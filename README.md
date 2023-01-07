# DEX

- Build an exchange with only one asset pair (Eth / Crypto Dev)
- Your Decentralized Exchange should take a fees of 1% on swaps
- When user adds liquidity, they should be given Crypto Dev LP tokens (Liquidity Provider tokens)
- CD LP tokens should be given proportional to the Ether user is willing to add to the liquidity

## Prerequisites

- ICO Tutorial

## Setup Hardhat

```bash
mkdir hardhat-tutorial
cd hardhat-tutorial
npm init --yes
npm install --save-dev hardhat
# init hardhat
npx hardhat
npm install @openzeppelin/contracts
# remove boilerplate contract
rm contracts/Lock.sol
```

## Create Contract Files

```bash
touch contracts/Exchange.sol
code contracts/Exchange.sol
```

## Environment Variables

```bash
npm install dotenv
touch .env.example
echo 'QUICKNODE_HTTP_URL=""' >> .env.example
echo 'PRIVATE_KEY=""' >> .env.example
cp .env.example .env
# set nft contract address
mkdir constants
touch constants/index.js

code .env
code constants/index.js
code scripts/deploy.js
code hardhat.config.js
```

### Update files and deploy

```
npx hardhat compile
npx hardhat run scripts/deploy.js --network goerli
```

#

## Frontend

```bash
npx create-next-app@latest
cd my-app
# add deps
npm install web3modal ethers
# add contract addresses
mkdir constants
touch constants/index.js
# make changes
code styles/Home.modules.css
code pages/index.js
code constants/index.js
# run client
npm run dev
```
