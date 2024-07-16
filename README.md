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
