# 18-Blockchain_HW


<img src="/screenshot/Screenshot_2022-01-09_19-01-59.png" style="width:800px;height:300px;">

## Instructions

1. Download and installed Go Ethereum Tools **"Geth & Tools 1.9.7"** and MyCrypto. You will need these tools in order to access ZBank's blockchain network and crypto wallets. 
2. Open your Terminal
3. Direct to the folder in which you have geth saved
4. 
5. To initialize the first node on the blockchain, run the command: ./geth init zbank.json --datadir node1
6. To initialize the first node on the blockchain, run the command: ./geth init zbank.json --datadir node2
7. Create a file called "password.txt" with the password for the node(s), and save it in the same directory as your node files
* Ensure that there is an empty line below the password in the file (i.e. hit enter)
8. To start mining the first node, run the command: ./geth --datadir node1 --mine --minerthreads 1 --rpc --unlock "0xD3E3B5F97806742ee1ee3ab53180edb1dC0D2751" --allow-insecure-unlock --password password.txt
* The --mine flag tells the node to mine new blocks.
* The --minerthreads flag tells geth how many CPU threads, or "workers" to use during mining. Since our difficulty is low, we can set it to 1.
* The --unlock flag unlocks the node for use - the password.txt value calls the file we created above
* The --allow-insecure-unlock flag allows us to unlock in an insecure mananer 
* The --rpc flag allows this node to communciate via the internet
9. To start mining the second node, run the command: ./geth --datadir node2 --port 30304 --bootnodes "enode://43b90bcf06d05f6ac8b395d5728c4ef26dcced85a897d5c623ce85d4894aab4719c304dca0af8b7142c828b2e4245c44b5d3a5b367e35de2a2c900ea8a5ea215@127.0.0.1:30303" 
10. Open the MyCrypto app, and create an account if you do not already have one
11. You will need to tap into the test network, in order to set this up on your app, please configure as shown in the "network-config" image in "Screenshots"
12. Once you have set up the network on your app, go to "View & Send" in the top left, and choose "Keystore File" as your authentication method. This will prompt you to direct to the file path of one of the crypto wallets below on your device. Select the file, and enter the password when prompted (also listed below).
13. You should now be in the wallet. In order to send ETH to the other account you are not currently in, copy and paste the receiving account's public key from below into the "To Address" input box, choose how much ETH you would like to send, and click on "Send Transaction"



## Accounts

* node1 

** Public address of the key:   0xD3E3B5F97806742ee1ee3ab53180edb1dC0D2751

** Path of the secret key file: node1/keystore/UTC--2022-01-10T09-07-28.858291009Z--d3e3b5f97806742ee1ee3ab53180edb1dc0d2751

** Port: 30303

* node2 

** Public address of the key:   0x38577877127C515f47dccE513cF39b9D7272D75b

** Path of the secret key file: node2/keystore/UTC--2022-01-10T09-08-09.757123959Z--38577877127c515f47dcce513cf39b9d7272d75b

** Port: 30304
