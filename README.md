# Sample Hardhat Project
Airdrop 1 Manual version Instructions:
______________________________________

installation instruction from tutorial

1. change private key in .env
PRIVATE_KEY="ENTER_YOUR_KEY"

2. run
cd Q-boilerplate
npm install dotenv --save --force
npm install --save-dev hardhat --force
npm install --force


3. Deploy contract in contracts/QRC20.sol using:
npx hardhat run scripts/AirDropV1/1_deploy_token.js --network testnet

copy contract address from 3 and save in .env
QRC20_TOKEN = "YOUR-CONTRACT-ADDRESS"

4. Set up and copy DAO Registry address from https://factory.q-dao.tools/
DAO_REGISTRY_ADDRESS = "YOUR-DAO-REGISTRY-ADDRESS"

Information about potential errors: You may encounter any of the following common errors, let me explain how you can resolve them:ProviderError: Insufficient funds for gas * price + value ⇒ Use the Q faucet at faucet.qtestnet.org to claim tokens to the wallet/private key you use for deploying the code.Error: Factory runner does not support sending transactions ⇒ There is a typo in your private key in the .env file, or the .env file with the private key is not in the right directory (should be in the root directory Q-boilerplate-code.)

5. Open scripts/AirDropV1/2_deploy_airdropV1.js file and enter all expected addresses, e.g. as .env variables

6. deploy airdrop contract
npx hardhat run scripts/AirDropV1/2_deploy_airdropV1.js --network testnet

Copy address
AirDropV1 address =

7. Claim the AirDrop Module
npx hardhat run scripts/AirDropV1/3_claim.js --network testnet
__________________________
Airdrop2 Better Version
__________________________
1. Deploy Airdropv2 module using:
npx hardhat run scripts/AirDropV2/1_deploy_airdropV2.js --network testnet

AirDrop V2 deployed to:

2. Create voting situation for DAO
npx hardhat run scripts/AirDropV2/2_createVoting.js --network testnet


3. add Airdropv2 module to DAO
npx hardhat run scripts/AirDropV2/3_addModule.js --network testnet


4. configure Airdropv2 module in DAO
npx hardhat run scripts/AirDropV2/4_initModule.js --network testnet










----------------other information---------------------------

This project demonstrates a basic Hardhat use case. It comes with a sample contract, a test for that contract, and a script that deploys that contract.

instruction from READMe
Try running some of the following tasks:

```shell
npx hardhat help
npx hardhat test
REPORT_GAS=true npx hardhat test
npx hardhat node
npx hardhat run scripts/deploy.js
```
