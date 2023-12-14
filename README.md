# Piccadilly-peers
This repo is to help increase the node sync speed on Piccadilly network using static-nodes

If you are facing node-sync issues on Piccadilly Testnet like not able to connect to peers or slow sync speed.
You can follow below steps to resolve this. 


## Step 1

Copy the `static-nodes.json file from this repo.


## Step 2

Create `--datadir` folder and copy `static-nodes.json` file there.
eg:
```
mkdir autonity-chaindata
cp static-nodes.json ./autonity-chaindata
```

**Note**: If you already have `--datadir` folder then copy this file inside it and restart your node.


## Step 3

Add this directory in the `--datadir` flag and start your node.

eg:
```
autonity \
   --datadir ./autonity-chaindata \
   --piccadilly  \
   --http  \
   --http.addr 0.0.0.0 \
   --http.api aut,eth,net,txpool,web3,admin  \
   --http.vhosts \* \
   --ws  \
   --ws.addr 0.0.0.0 \
   --ws.api aut,eth,net,txpool,web3,admin  \
   --nat extip:<IP_ADDRESS>
```
