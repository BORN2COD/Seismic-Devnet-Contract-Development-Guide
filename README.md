# Seismic Devnet Contract Deployment Guide

▶ **Overview**

This guide shows you how to deploy and work with an encrypted contract on Seismic Devnet. Follow each step closely for a smooth setup.

Note; Seismic has already clarified that this testnet action is not incentivized.

**Important Links:**

Network Name: Seismic Devnet
Currency Symbol: ETH

Chain ID: 5124

RPC URL (HTTP): https://node-2.seismicdev.net/rpc

RPC URL (WS): wss://node-2.seismicdev.net/ws

Explorer: https://explorer-2.seismicdev.net

Faucet: https://faucet-2.seismicdev.net

---

**◆ Pre-Requirements**
Before deploying the contract, install the necessary tools:

➤ 1. Install Rust

Run the following command to install Rust:

curl https://sh.rustup.rs -sSf | sh

After installation, apply the changes:

. "$HOME/.cargo/env"

Verify if Rust is installed correctly:

rustc --version

✔ If a version number appears, Rust is installed successfully.

➤ 2. Install jq

For WSL/Ubuntu, run:

sudo apt install jq

For Mac, run:

brew install jq

✔ After installation, jq will be available for processing JSON data.

➤ 3. Install sfoundryup

Run the following command to install sfoundryup:

curl -L \
     -H "Accept: application/vnd.github.v3.raw" \
     "https://api.github.com/repos/SeismicSystems/seismic-foundry/contents/sfoundryup/install?ref=seismic" | bash

Apply the changes to your terminal:

source ~/.bashrc

✔ Now, sfoundryup is installed and ready to use.

➤ 4. Run sfoundryup

Execute the command:

sfoundryup

⚡ This process may take some time to download all required dependencies.

▶ Deploy an Encrypted Contract

➤ 1. Clone & Navigate to the Repository

Clone the repository with:

git clone --recurse-submodules https://github.com/SeismicSystems/try-devnet.git

Navigate to the contract directory:

cd try-devnet/packages/contract/

✔ You are now in the correct directory to deploy the contract.

➤ 2. Deploy the Contract

Run the deployment script:

bash script/deploy.sh

✔ This script will:
• Generate a wallet address
• Provide a Faucet URL
• Display the wallet address

Next Steps:

Copy the Faucet URL and open it in your browser.

Fund your newly generated wallet using the Faucet.

Once the transaction is complete, your contract deployment is successful.

▶ Interact with an Encrypted Contract

➤ 1. Navigate to Home Directory

Move to the home directory to ensure a clean workspace:

cd $HOME

✔ You are now back in the home directory.

➤ 2. Install Bun

Run the following command to install Bun:

curl -fsSL https://bun.sh/install | bash

✔ This will install Bun, a fast JavaScript runtime.

➤ 3. Install Node Dependencies

Navigate to the CLI package directory:

cd try-devnet/packages/cli/

Install the required dependencies:

bun install

✔ Now, all dependencies needed for interacting with the contract are installed.

➤ 4. Send Transactions

Execute the transaction script:

bash script/transact.sh

✔ This will allow you to send transactions to the deployed contract.


---

◆ Follow me on X https://x.com/PhaResearcher for support and updates.
