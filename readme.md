# **Truffle Tutorial**

- Truffle is basically kind of like a pipeline to deploy and compile your contracts. It provide you tools and features to manage deployment and compilation and create boilerplate code also.

- First of all you need to know that just install truffle as global cuz you're gonna use it many times

- Some common commands (ofc after `npm install truffle -g`)
```cpp
truffle compile         //compile all your contracts one by one
truffle migrate --reset         //use reset due to constant changes.... bt
truffle unbox react         //boxes are something that writes all the boilerplate code to save time
// Btw react box actually is a mix of react and truffle intialization boilerplate code so better not use truffle init before if not needed
//where react is one of the boilerplate code boxes which we are unboxing now although you can use create-react-app explicity but as you can see its more effficient and productive.

truffle unbox
// simply writing this will give you default truffle boilerplate code but truffle init is much better for very start 
truffle migrate --network development/ropsten/sopelia       
//This will simply help to deploy to a certain network
```

- Use `7545` Port for using truffle as service in `truffle.config`. and chain id in metamask if needed as `1337`

- Oh btw don't forget to add your account using private key from ganache to metamask --after adding ganache network in metamask.

- btw in the migration folder you need to have the `intial migration` files. They are taking care of migration btw.. get it by `truffle unbox`.

- Network id for goreli is `5` and sepolia is `11155111`

<hr>

# **What is infura and why do we use it**

### <p style="color:orange;">actually ganache is a tool to create a private blockchain creator and it means the blockchain is itself on your system. So there nothing like peer to peer system communication.</p>

### <p style="color:hotpink;">**So basicallly when you write truffle compile or migrate with infura then ofc you are trying to connect with the etherum blockchain wheather its testnet vali either. But for that you have to be a part of p2p system i.e:- either a node(p2p single node) or fullnode(store blockchain complete) But in that case you need a lot of resources and more tehnical knowledge so in this infura works as middleman it works as fullnode and handle everything which means it gives you backend compatiblity which cotains software for extra communcication like dapp backend and iaas (infrastructer as a service). Btw if you also want to make your pc work as node or full node you gotta use GETH software for that. THen your pc will directly work as a p2p node or full node**</p>

- Use `ws` connection url while changing in `truffle-config.js`

# **How to Change truffle config.js for usage**

1. Change network according to your usage preference. 
    - Install the required hdwalletprovider --> `@truffle/hdwallet-provider` 
    - with the network connection section you can use three arguments with `Hdwalletprovider` function `(mnemonic, infura Network URL(ws), account index of metamask)` 
    - Then according to the network use specific network id also
    - If using ganache i.e: development network then don't forget to use 7545 for ganache service PORT(is used to provide services rem)
    - ALso add the value of mnemonic in the top of file
    - uncomment the import of required hdwalletprovide line

1. HDwallterProvider:- HD Wallet-enabled Web3 provider. Use it to sign transactions for `ADDRESSES DERIVED FROM` a 12 or 24 word mnemonic

