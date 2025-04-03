# Seismic Devnet Contract Deployment Guide

▶ **Overview**

This guide shows you how to deploy and work with an encrypted contract on Seismic Devnet. Follow each step closely for a smooth setup.

Note; Seismic has already clarified that this testnet action is not incentivized.

+----------------------+---------------------------------------------+
| Item                | Value                                       |
+----------------------+---------------------------------------------+
| Network Name        | Seismic Devnet                              |
| Currency Symbol     | ETH                                         |
| Chain ID           | 5124                                        |
| RPC URL (HTTP)     | https://node-2.seismicdev.net/rpc           |
| RPC URL (WS)       | wss://node-2.seismicdev.net/ws              |
| Explorer           | https://explorer-2.seismicdev.net/           |
| Faucet             | https://faucet-2.seismicdev.net/             |
| Starter Repo       | https://github.com/SeismicSystems/seismic-starter |
+----------------------+---------------------------------------------+

---

◆ **Pre-Requirements**
Make sure you have the following installed before you start:

➤ **1. Install Rust**
Run this command to install Rust:
```sh
curl https://sh.rustup.rs -sSf | sh
. "$HOME/.cargo/env"
```
✔ **Next Steps:**
• Verify the installation by running:
```sh
rustc --version
```
• If you see a version number, Rust is installed correctly.
• If not, restart your terminal and try again.

➤ **2. Install jq**
• For WSL/Ubuntu:
```sh
sudo apt install jq
```
• For Mac:
```sh
brew install jq
```
✔ **Next Steps:**
• Check the installation by running `jq --version`.
• If it fails, try running `sudo apt update && sudo apt install jq` on Ubuntu.

➤ **3. Install sfoundryup**
Run this command to install sfoundryup:
```sh
curl -L \
-H "Accept: application/vnd.github.v3.raw" \
"https://api.github.com/repos/SeismicSystems/seismic-foundry/contents/sfoundryup/install?ref=seismic" | bash
source ~/.bashrc
```
✔ **Next Steps:**
• Verify the installation by running `which sfoundryup`.
• If the command shows a path, sfoundryup is installed.
• If not, restart your terminal and run `source ~/.bashrc` again.

➤ **4. Run sfoundryup**
```sh
sfoundryup
```
⚡ **Note:** This may take some time.
✔ **Next Steps:**
• Wait for it to finish.
• If it fails, check your internet connection and try again.

---

▶ **Deploy an Encrypted Contract**

➤ **1. Clone & Navigate to the Repository**
Run these commands:
```sh
git clone --recurse-submodules https://github.com/SeismicSystems/try-devnet.git
cd try-devnet/packages/contract/
```
✔ **Next Steps:**
• Check if the repository cloned by running `ls`.
• If you see `contract/`, you are in the right place.

➤ **2. Deploy the Contract**
Run the script:
```sh
bash script/deploy.sh
```
✔ **Next Steps:**
• The script will create a wallet.
• It will show a **Faucet URL** and your **wallet address**.
• Copy the **Faucet URL**, open it in a browser, and claim your funds.
• After receiving the funds, your contract is deployed.
• If there are errors, check the logs and make sure all dependencies are installed.

---

▶ **Interact with an Encrypted Contract**

➤ **1. Navigate to Home Directory**
```sh
cd $HOME
```
✔ **Next Steps:**
• Run `pwd` to confirm you are in the home directory.

➤ **2. Install Bun**
```sh
curl -fsSL https://bun.sh/install | bash
```
✔ **Next Steps:**
• Restart your terminal.
• Run `bun --version` to check if it was installed successfully.

➤ **3. Install Node Dependencies**
```sh
cd try-devnet/packages/cli/
bun install
```
✔ **Next Steps:**
• Check if the dependencies installed correctly.
• If there are issues, delete `node_modules` and run `bun install` again.

➤ **4. Send Transactions**
```sh
bash script/transact.sh
```
✔ **Next Steps:**
• Verify if the transaction was successful.
• If there are errors, check your wallet balance and try again.

---

◆ Follow me on X https://x.com/PhaResearcher for support and updates.
