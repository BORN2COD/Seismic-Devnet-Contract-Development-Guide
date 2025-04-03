# Seismic Devnet Contract Deployment Guide 🪢

This guide shows you how to deploy and work with an encrypted contract on Seismic Devnet. Follow each step closely for a smooth setup.

Note; Seismic has already clarified that this testnet action is not incentivized.

---

◆ **Pre-Requirements**
Before deploying the contract, install the necessary tools:

➤ **1. Install Rust**
- Run the following command to install Rust:
```sh
curl https://sh.rustup.rs -sSf | sh
```
- After installation, apply the changes:
```sh
. "$HOME/.cargo/env"
```
- Verify if Rust is installed correctly:
```sh
rustc --version
```
  ✔ If a version number appears, Rust is installed successfully.

➤ **2. Install jq**
- For WSL/Ubuntu, run:
```sh
sudo apt install jq
```
- For Mac, run:
```sh
brew install jq
```
  ✔ After installation, `jq` will be available for processing JSON data.

➤ **3. Install sfoundryup**
- Run the following command to install `sfoundryup`:
```sh
curl -L \
     -H "Accept: application/vnd.github.v3.raw" \
     "https://api.github.com/repos/SeismicSystems/seismic-foundry/contents/sfoundryup/install?ref=seismic" | bash
```
- Apply the changes to your terminal:
```sh
source ~/.bashrc
```
  ✔ Now, `sfoundryup` is installed and ready to use.

➤ **4. Run sfoundryup**
- Execute the command:
```sh
sfoundryup
```
  ⚡ This process may take some time to download all required dependencies.

---

▶ **Deploy an Encrypted Contract**

➤ **1. Clone & Navigate to the Repository**
- Clone the repository with:
```sh
git clone --recurse-submodules https://github.com/SeismicSystems/try-devnet.git
```
- Navigate to the contract directory:
```sh
cd try-devnet/packages/contract/
```
  ✔ You are now in the correct directory to deploy the contract.

➤ **2. Deploy the Contract**
- Run the deployment script:
```sh
bash script/deploy.sh
```
  ✔ This script will:
  • Generate a wallet address
  • Provide a Faucet URL
  • Display the wallet address

- **Next Steps:**
  1. Copy the Faucet URL and open it in your browser.
  2. Fund your newly generated wallet using the Faucet.
  3. Once the transaction is complete, your contract deployment is successful.

---

▶ **Interact with an Encrypted Contract**

➤ **1. Navigate to Home Directory**
- Move to the home directory to ensure a clean workspace:
```sh
cd $HOME
```
  ✔ You are now back in the home directory.

➤ **2. Install Bun**
- Run the following command to install `Bun`:
```sh
curl -fsSL https://bun.sh/install | bash
```
  ✔ This will install `Bun`, a fast JavaScript runtime.

➤ **3. Install Node Dependencies**
- Navigate to the CLI package directory:
```sh
cd try-devnet/packages/cli/
```
- Install the required dependencies:
```sh
bun install
```
  ✔ Now, all dependencies needed for interacting with the contract are installed.

➤ **4. Send Transactions**
- Execute the transaction script:
```sh
bash script/transact.sh
```
  ✔ This will allow you to send transactions to the deployed contract.

That's all ✓ You have successfully Deployed and Interacted with the contract.
---

◆ Follow me on X https://x.com/PhaResearcher for support and updates.
