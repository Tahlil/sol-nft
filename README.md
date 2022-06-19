# Solana NFT Drop Project (adapted from Buildspace)

### Welcome 👋

To get started with this project, clone this repo and follow these commands:

1. cd into the `app` folder
2. Run `npm install` at the root of your directory
3. Run `npm run start` to start the project
4. Start coding!


### Instructions
1. Create new solana keeper address
```
solana-keygen new --outfile ~/.config/solana/devnet.json
```
2. Set the new key pair
```
solana config set --keypair ~/.config/solana/devnet.json
```
3. Add balance to the new account
```
solana airdrop 2 --url devnet
```
4. Verify balance
```
solana balance --url devnet
```
5. Clone [metaplex github project](https://github.com/metaplex-foundation/metaplex)
```
git clone https://github.com/metaplex-foundation/metaplex.git
```
6. Install metaplex cli
```
cd metaplex-foundation/metaplex/js
yarn install
```
7. Verify metaplex is installed
```
npm i -g ts-node
ts-node ./packages/cli/src/candy-machine-v2-cli.ts --version
```
(Assuming you are still in the `js` directory)

8. Go to the root project directory and run the following commant to uopload NFT
```
ts-node ~/Desktop/metaplex/js/packages/cli/src/candy-machine-v2-cli.ts upload -e devnet -k ~/.config/solana/devnet.json -cp config.json ./assets
```
(Assuming the `metaplex` project is cloned on Desktop directory)

9. Verify upload
```
ts-node ~/Desktop/metaplex/packages/cli/src/candy-machine-v2-cli.ts verify_upload -e devnet -k ~/.config/solana/devnet.json 
```
