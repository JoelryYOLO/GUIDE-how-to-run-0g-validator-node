# GUIDE-how-to-run-0g-validator-node
This repository talks about how to install and run the 0G_LABS validator node.
Hi all! If you wanted to install the validator node of the 0g_labs project, but didn’t know how exactly to do it, then this repository is especially for you! Just follow the instructions and you will definitely succeed!
Before you start, it’s worth mentioning the system requirements; below are the **minimum** requirements under which you can run a node!

```bash
- Memory: 64 GB
- CPU: 8 cores
- Disk: 1 TB NVME SSD
- Bandwidth: 100 MBps for Download / Upload
```

Double check that your computer meets these requirements.

# Install
Great, now we can move on to the installation itself! Installation will take place using a code.

```bash
git clone -b v0.2.3 https://github.com/0glabs/0g-chain.git
./0g-chain/networks/testnet/install.sh
source ~/.profile
```

**Set Chain ID**
```bash
0gchaind config chain-id zgtendermint_16600-2
```

# Initialize Node
```bash
0gchaind config chain-id zgtendermint_16600-2
```

# Download Genesis File and add Seeds
1. Download Genesis
   ```bash
   sudo apt install -y unzip wget
   rm ~/.0gchain/config/genesis.json
   wget -P ~/.0gchain/config https://github.com/0glabs/0g-chain/releases/download/v0.2.3/genesis.json
   ```
   **Validate the Genesis File**
   ```bash
   0gchaind validate-genesis
   ```
2. Add Seed Nodes
   ```bash
   # To config.toml
   
   81987895a11f6689ada254c6b57932ab7ed909b6@54.241.167.190:26656,010fb4de28667725a4fef26cdc7f9452cc34b16d@54.176.175.48:26656,e9b4bc203197b62cc7e6a80a64742e752f4210d5@54.193.250.204:26656,68b9145889e7576b652ca68d985826abd46ad660@18.166.164.232:26656
   ```
# Start Node
```bash
0gchaind start
```
     
