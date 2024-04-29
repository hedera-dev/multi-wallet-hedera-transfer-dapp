# Hedera DApp Integrated with WalletConnect
Explore DApp development using the Mirror Node API and Hedera Token Service (HTS). Discover how to integrate HTS functionality into your DApp for seamless token management and transactions. This guide uses React, Material UI, Ethers, and TypeScript with the [Create React App (CRA) Hedera DApp template](https://github.com/hedera-dev/cra-hedera-dapp-template) integrated with walletconnect, streamlining your development process.

## Tutorial
This repo is intended to be used alongside the tutorial:
[Create a Hedera DApp Integrated with WalletConnect](https://docs.hedera.com/hedera/tutorials/more-tutorials/develop-a-hedera-dapp-integrated-with-walletconnect)

To follow along, start with the `main` branch,
which is the default branch of this repo.
This gives you the initial state from which you can follow along
with the steps as described in the tutorial.

```shell
git clone git+ssh://git@github.com/hedera-dev/multi-wallet-hedera-transfer-dapp.git
```

To skip ahead to the final state, use the `completed` branch.
This gives you the final state with which you can compare your implementation
to the completed steps of the tutorial.

```shell
git fetch origin completed:complete
git checkout completed
```
## Completed Branch Usage

1. Execute ```npm i```
2. Execute ```npm run start``` to start the project

## Prerequisites

### Hedera Testnet account

Don't have one? Create one by going to [portal.hedera.com](https://portal.hedera.com/register). The daily limit is 1000 test HBAR and users will be able to request for a refill every 24 hours!

### Hashpack Wallet
* Install the [Hashpack extension](https://chrome.google.com/webstore/detail/hashpack/gjagmgiddbbciopjhllkdnddhcglnemk).  

### Blade Wallet
* Install the [Blade extension](https://chrome.google.com/webstore/detail/blade-%E2%80%93-hedera-web3-digit/abogmiocnneedmmepnohnhlijcjpcifd).  

### Metamask Wallet
* Install the [MetaMask extension](https://chrome.google.com/webstore/detail/metamask/nkbihfbeogaeaoehlefnkodbefgpgknn).
* Import a Hedera ECDSA based testnet account into MetaMask.  

### Kabila Wallet
* Install the [Kabila extension](https://www.kabila.app/wallet).

#### How to activate your account on Hedera Testnet

* Activate it by transferring any 100 test HBAR to your EVM address using our faucet at https://portal.hedera.com/faucet

-----

## Configuration
This project uses a configuration file located `src/config/networks.ts`.

```TypeScript
export const networkConfig: NetworkConfigs = {
  testnet: {
    network: "testnet",
    jsonRpcUrl: "https://testnet.hashio.io/api", // check out the readme for alternative RPC Relay urls
    mirrorNodeUrl: "https://testnet.mirrornode.hedera.com",
    chainId: "0x128",
  }
}
```

---

## JSON RPC Relay Endpoint Alternatives
This DApp utilizes [Hashio](https://swirldslabs.com/hashio/) to connect to Hedera Testnet over RPC.
There are three options available to establish a connection to Hedera Networks:
* Hashio
* Arkhia
* Hedera JSON RPC Relay

Follow the guide [how to connect to Hedera Networks over RPC](https://docs.hedera.com/hedera/tutorials/more-tutorials/json-rpc-connections) to connect using Arkhia or a local version of the Hedera JSON RPC Relay.

## Links
* [The Hedera DApp CRA Template](https://github.com/hedera-dev/cra-hedera-dapp-template)
* Need to quickly create Hedera Testnet accounts to act as Sender/Receiver? Check out [Create Hedera Accounts with Tokens Helper](https://github.com/hedera-dev/hedera-create-account-and-token-helper)
* [Hashscan](https://hashscan.io/testnet/dashboard) network explorer


## License
Apache 2.0
