# ethExplorer
Blockchain explorer for the PoA network

Start the nodes

node1
`geth --datadir node1/ --syncmode 'full' --port 30311 --rpc --rpccorsdomain "localhost:8000" --rpcaddr 'localhost' --rpcport 8545 --rpcapi 'personal,db,eth,net,web3,txpool,miner' --bootnodes 'enode://501cd49296285093f1d6ff9b7c4a264e61039d83c09c3a50ce49b18ac6763b176bb95e876238b2c69ebb5ae139501713237f6344422cc46de1a8e1a8a043ab82@127.0.0.1:30310' --networkid 1515 --gasprice '1' --targetgaslimit 94000000 -unlock '078f75da2fc16799fd6989ade56819a7bbe84bfb' --password node1/password.txt --mine`

node2
`geth --datadir node2/ --syncmode 'full' --port 30312 --rpc --rpccorsdomain "localhost:8000" --rpcaddr 'localhost' --rpcport 8502 --rpcapi 'personal,db,eth,net,web3,txpool,miner' --bootnodes 'enode://501cd49296285093f1d6ff9b7c4a264e61039d83c09c3a50ce49b18ac6763b176bb95e876238b2c69ebb5ae139501713237f6344422cc46de1a8e1a8a043ab82@127.0.0.1:30310' --networkid 1515 --gasprice '0' --targetgaslimit 94000000 --unlock 'e68b8f3b08255a3433c43fec99143f58d2bd58fb' --password node2/password.txt --mine`

then run the explorer `npm start`

double check that the node command has `--rpc  --rpccorsdomain "http://localhost:8000"`

