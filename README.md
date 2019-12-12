Zbank Blockchain instructions

Proof of Work Blockchain called Zbank

Blocktime= =2.4496ms
Network name= Zbank
Chain ID =224
URL= hhp://127.0.0.1/8545  (Do not use https:// as suggested in MyCrypto wallet as it will not connect)
Password for Node1: Aggie1
Node1 port: 30303
Password for Node2: Aggie2
Node2 port: 30304

#Geth Flags to mine 
--datadir           directory to use for mining
--mine              command to get the node to mine blocks
--minerthreads1     uses 1 to tell the cpu to use 1 thread for mining.
--port              tells whick port to use (30303 for node1 and 30304 for node2)
--ipcdisable        used for windows machines to disable ipc and enable rpc
--rpc               remote procedure call

#Instructions to mine zbank Blockchain

1.  Open a terminal and clone the repo.
2.  CD into file BLOCKCHAIN-TOOLS
3.  Launch the first node by using the following command:
        ./geth --datadir node1 --mine --minerthreads 1
        Make sure to copy the "enode://...." after launch to use for launching Node2
4.  Open a different terminal and CD into same directory used for node 1 launch
5. Launch the second node by using the following command:
        ./geth --datadir node2 --port 30304 --bootnodes "enode copy from node1 goes here" --ipcdisable
        Make sure to insert enode copy from node1 in the quotes ".." area in the above line
6.  Both nodes in the Blockchain should now be mining

#Instructions for using MyCrypto wallet
1.  Download MyCrypto https://mycrypto.com/account and establish an account if you haven't already done so.
2.  Click on "Change Network" on the left side of your MyCrypto wallet account.
3.  Click on "Add Custom Node" at the bottom of the dropdown choices.
4.  Your next window will prompt you to Set Up Your Custom Node.  In the "Network" box with a dropdown menu choose "Custom"
5.  Fill out the following fields 

    Node Name:  Whatever you would like to call it
    Network Name: zbank
    Currency: ETH 
    Chain ID: 224
    URL: http://127.0.0.1:8545     !!!Do NOT use https as it suggests!!!


