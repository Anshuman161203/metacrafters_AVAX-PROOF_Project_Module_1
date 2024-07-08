# metacrafters_AVAX-PROOF_Project_Module_1
This report contains project assessment code for the AVAX PROOF course under metacrafter.

## Getting Started
Prerequisites
- Unix Computer (MacOS or Linux) or WSL in Windows
- Remix IDE
- Metamask

# #Build Your First Subnet
Installation

install the latest Avalanche-CLI binary is by running the install script:
```sh
curl -sSfL https://raw.githubusercontent.com/ava-labs/avalanche-cli/main/scripts/install.sh | sh -s
```
You can run all of the commands in this tutorial by calling ```~/bin/avalanche.```

You can also add the command to your system path by running

```
export PATH=~/bin:$PATH
```
If you add it to your path, you should be able to call the program anywhere with just ```avalanche```.
### Subnet 
 
Follow the below github repository's readme file in order to install avalanche CLI to your Ubuntu or Mac terminal:
 
 [https://docs.avax.network/tooling/cli-guides/install-avalanche-cli](https://github.com/ava-labs/avalanche-cli)

 Helping Resource: https://docs.avax.network/tooling/cli-create-deploy-subnets/create-subnet

In order to create a subnet, we run -

```
avalanche subnet create mySubnet
```

In order to deploy the created subnet, we run -

```
avalanche subnet deploy mySubnet
```


Welcome to Ubuntu 22.04.3 LTS (GNU/Linux 5.15.153.1-microsoft-standard-WSL2 x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage


This message is shown once a day. To disable it please create the
/root/.hushlogin file.
root@LAPTOP-M3IM9EU5:~# curl -sSfL https://raw.githubusercontent.com/ava-labs/avalanche-cli/main/scripts/install.sh | sh -s
ava-labs/avalanche-cli info checking GitHub for latest tag
ava-labs/avalanche-cli info found version: 1.6.3 for linux/amd64
ava-labs/avalanche-cli info installed /root/bin/avalanche
root@LAPTOP-M3IM9EU5:~# export PATH=~/bin:$PATH
root@LAPTOP-M3IM9EU5:~# export PATH=~/bin:$PATH >> .bashrc
root@LAPTOP-M3IM9EU5:~# avalanche --version
avalanche version 1.6.3
root@LAPTOP-M3IM9EU5:~# avalanche subnet create mySubnet
✔ Subnet-EVM
✔ Use latest release version
✔ Yes
✔ Yes
Installing subnet-evm-v0.6.6...
subnet-evm-v0.6.6 installation successful
creating genesis for subnet mySubnet
Enter your subnet's ChainId. It can be any positive integer.
ChainId: 14129
Select a symbol for your subnet's native token
Token symbol: ADDS
✔ Low disk use    / Low Throughput    1.5 mil gas/s (C-Chain's setting)
✔ Airdrop 1 million tokens to the default ewoq address (do not use in production)
prefunding address 0x8db97C7cEcE249c2b98bDC0226Cc4C2A57BF52FC with balance 1000000000000000000000000
✔ No
✓ Successfully created subnet configuration
root@LAPTOP-M3IM9EU5:~# avalanche subnet deploy mySubnet
✔ Local Network
Deploying [mySubnet] to Local Network
Backend controller started, pid: 1497, output at: /root/.avalanche-cli/runs/server_20240707_232121/avalanche-cli-backend.log
Installing avalanchego-v1.11.9...
avalanchego-v1.11.9 installation successful

Booting Network. Wait until healthy...
Node logs directory: /root/.avalanche-cli/runs/network_20240707_232134/node<i>/logs
Network ready to use.

Deploying Blockchain. Wait until network acknowledges...

Teleporter Messenger successfully deployed to c-chain (0x253b2784c75e510dD0fF1da844684a1aC0aa5fcf)
Teleporter Registry successfully deployed to c-chain (0x17aB05351fC94a1a67Bf3f56DdbB941aE6c63E25)

Teleporter Messenger successfully deployed to mySubnet (0x253b2784c75e510dD0fF1da844684a1aC0aa5fcf)
Teleporter Registry successfully deployed to mySubnet (0xeF74B365DC8fa2E32E1C20165a5096792BDB74B4)

using awm-relayer version (v1.3.3)
Installing AWM-Relayer v1.3.3
Executing AWM-Relayer...

Blockchain ready to use

+-------------------+------------------------------------------------------------------------------------+
|                                           mySubnet RPC URLs                                            |
+-------------------+------------------------------------------------------------------------------------+
| Localhost         | http://127.0.0.1:9650/ext/bc/mySubnet/rpc                                          |
+                   +------------------------------------------------------------------------------------+
|                   | http://127.0.0.1:9650/ext/bc/7kwFgbLvnncCUXL8Aca5NMZqHhsrXKCF3RDfSCSUoXceYCq7W/rpc |
+-------------------+------------------------------------------------------------------------------------+

+-------+------------------------------------------+-----------------------+
|                                  Nodes                                   |
+-------+------------------------------------------+-----------------------+
| Name  | Node ID                                  | Localhost Endpoint    |
+-------+------------------------------------------+-----------------------+
| node1 | NodeID-7Xhw2mDxuDS44j42TCB6U5579esbSt3Lg | http://127.0.0.1:9650 |
+-------+------------------------------------------+-----------------------+
| node2 | NodeID-MFrZFVCXPv5iCn6M9K6XduxGTYp891xXZ | http://127.0.0.1:9652 |
+-------+------------------------------------------+-----------------------+
| node3 | NodeID-NFBbbJ4qCmNaCzeW7sxErhvWqvEQMnYcN | http://127.0.0.1:9654 |
+-------+------------------------------------------+-----------------------+
| node4 | NodeID-GWPcbFJZFfZreETSoWjPimr846mXEKCtu | http://127.0.0.1:9656 |
+-------+------------------------------------------+-----------------------+
| node5 | NodeID-P7oB2McjBGgW2NXXWVYjV8JEDFoW9xDE5 | http://127.0.0.1:9658 |
+-------+------------------------------------------+-----------------------+

Browser Extension connection details (any node URL from above works):
RPC URL:           http://127.0.0.1:9650/ext/bc/7kwFgbLvnncCUXL8Aca5NMZqHhsrXKCF3RDfSCSUoXceYCq7W/rpc
Funded address:    0x8db97C7cEcE249c2b98bDC0226Cc4C2A57BF52FC with 1000000 (10^18) - private key: 56289e99c94b6912bfc12adc093c9b51124f0dc54ac7a766b2bc5ccf558d8027
Funded address:    0xd6467Ce664B7689B1c089a55312E8c069Fb9d32c with 600 (10^18)
Network name:      mySubnet
Chain ID:          14129
Currency Symbol:   ADDS

To connect your subnet to metamask, you will need to :

* Add network manually and enter Name, RPC URL, Token Symbol and Chain ID that you entered while creating the subnet.
* Import account with test tokens by entering the private key that you get from the terminal after you deploy the subnet.



## Project By
- Anshuman Roshan
