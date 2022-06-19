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
