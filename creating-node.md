# Creating GETH node to a Private Testing Ethereum Network

## Creating the datadir
```bash
geth --datadir <<your local directory to host ethnode>> init ./genesis.json
``` 
### Example
```bash
geth --datadir /Users/thunderbolt/myproject init /Users/thunderbolt/myproject/genesis.json
```

## Creating coinbase (or any) Ethereum account and his keystore file
```bash
geth --datadir <<your local directory to host ethnode>> account new
``` 

### Example
```bash
geth --datadir /Users/thunderbolt/myproject account new
``` 

## Starting a node only accepting local connections
```bash
geth --datadir "<<your local directory to host ethnode>>" --networkid="<<>>" --ws --wsaddr "127.0.0.1" --rpc --rpcaddr "127.0.0.1" --rpccorsdomain "*" --wsapi "admin,eth,debug,miner,net,txpool,personal,web3" --rpcapi "admin,eth,debug,miner,net,txpool,personal,web3" --graphql --graphql.addr "127.0.0.1" --graphql.corsdomain "*"
```

### Example
```bash
geth --datadir "/Users/thundebolt/myproject" --networkid="15" --ws --wsaddr "127.0.0.1" --rpc --rpcaddr "127.0.0.1" --rpccorsdomain "*" --wsapi "admin,eth,debug,miner,net,txpool,personal,web3" --rpcapi "admin,eth,debug,miner,net,txpool,personal,web3" --graphql --graphql.addr "127.0.0.1" --graphql.corsdomain "*"
```

## Connecting to the node via terminal
```bash
geth attach "<<your local directory to host ethnode>>/geth.ipc" 
```

### Example
```bash
geth attach "/Users/thundebolt/myproject/geth.ipc"
```
