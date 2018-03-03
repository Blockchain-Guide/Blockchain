# Set up private network ethereum 
1. Produce Network 
2. Test Network
3. Private Network

## Step by Step 

* 1: create folder and genesis.json
```
C02VX21EHTD5:Work i325291$ mkdir EthereumPrivate
C02VX21EHTD5:Work i325291$ ls
Cache			EthereumPrivate		Sap Teched
Command			Gamification		Template
Development		INM			VirtualBox
EMS			On-boarding tools
C02VX21EHTD5:Work i325291$ cd EthereumPrivate/
C02VX21EHTD5:EthereumPrivate i325291$ ls
genesis.json
```
* 2: Execute the command to create the creation block

```
/Users/i325291/Work/EthereumPrivate
C02VX21EHTD5:EthereumPrivate i325291$ geth --datadir data0 init genesis.json
INFO [03-03|22:03:13] Maximum peer count                       ETH=25 LES=0 total=25
INFO [03-03|22:03:13] Allocated cache and file handles         database=/Users/i325291/Work/EthereumPrivate/data0/geth/chaindata cache=16 handles=16
INFO [03-03|22:03:13] Writing custom genesis block
INFO [03-03|22:03:13] Persisted trie from memory database      nodes=0 size=0.00B time=8.964µs gcnodes=0 gcsize=0.00B gctime=0s livenodes=1 livesize=0.00B
INFO [03-03|22:03:13] Successfully wrote genesis state         database=chaindata                                                hash=a0e580…a5e82e
INFO [03-03|22:03:13] Allocated cache and file handles         database=/Users/i325291/Work/EthereumPrivate/data0/geth/lightchaindata cache=16 handles=16
INFO [03-03|22:03:13] Writing custom genesis block
INFO [03-03|22:03:13] Persisted trie from memory database      nodes=0 size=0.00B time=2.133µs gcnodes=0 gcsize=0.00B gctime=0s livenodes=1 livesize=0.00B
INFO [03-03|22:03:13] Successfully wrote genesis state         database=lightchaindata                                                hash=a0e580…a5e82e
C02VX21EHTD5:EthereumPrivate i325291$ cd data0/
C02VX21EHTD5:data0 i325291$ ls
geth		keystore
C02VX21EHTD5:data0 i325291$ cd geth/
C02VX21EHTD5:geth i325291$ ls
chaindata	lightchaindata
C02VX21EHTD5:geth i325291$ cd chaindata/
C02VX21EHTD5:chaindata i325291$ ls
000001.log	CURRENT		LOCK		LOG		MANIFEST-000000
C02VX21EHTD5:chaindata i325291$
```

* start node 

```
C02VX21EHTD5:EthereumPrivate i325291$ geth --datadir ./data0 --networkid 11 console
INFO [03-03|22:08:09] Maximum peer count                       ETH=25 LES=0 total=25
INFO [03-03|22:08:09] Starting peer-to-peer node               instance=Geth/v1.8.1-stable/darwin-amd64/go1.10
INFO [03-03|22:08:09] Allocated cache and file handles         database=/Users/i325291/Work/EthereumPrivate/data0/geth/chaindata cache=768 handles=1024
INFO [03-03|22:08:09] Initialised chain configuration          config="{ChainID: 15 Homestead: 0 DAO: <nil> DAOSupport: false EIP150: <nil> EIP155: 0 EIP158: 0 Byzantium: <nil> Engine: unknown}"
INFO [03-03|22:08:09] Disk storage enabled for ethash caches   dir=/Users/i325291/Work/EthereumPrivate/data0/geth/ethash count=3
INFO [03-03|22:08:09] Disk storage enabled for ethash DAGs     dir=/Users/i325291/.ethash                                count=2
INFO [03-03|22:08:09] Initialising Ethereum protocol           versions="[63 62]" network=11
INFO [03-03|22:08:09] Loaded most recent local header          number=0 hash=a0e580…a5e82e td=262144
INFO [03-03|22:08:09] Loaded most recent local full block      number=0 hash=a0e580…a5e82e td=262144
INFO [03-03|22:08:09] Loaded most recent local fast block      number=0 hash=a0e580…a5e82e td=262144
INFO [03-03|22:08:09] Loaded local transaction journal         transactions=0 dropped=0
INFO [03-03|22:08:09] Regenerated local transaction journal    transactions=0 accounts=0
INFO [03-03|22:08:09] Starting P2P networking
INFO [03-03|22:08:11] UDP listener up                          self=enode://a9039f4477fcdadd1aa65b52aed1802af7d06d4e41fe29cb5a15e9025d4d7620ed9cb11e91d136c81691b377c5d5a00cf56fcef286eab5ed013f3389610c82eb@[::]:30303
INFO [03-03|22:08:11] RLPx listener up                         self=enode://a9039f4477fcdadd1aa65b52aed1802af7d06d4e41fe29cb5a15e9025d4d7620ed9cb11e91d136c81691b377c5d5a00cf56fcef286eab5ed013f3389610c82eb@[::]:30303
INFO [03-03|22:08:11] IPC endpoint opened                      url=/Users/i325291/Work/EthereumPrivate/data0/geth.ipc
Welcome to the Geth JavaScript console!
```
![start node](/picture/Start-node.png)
  
