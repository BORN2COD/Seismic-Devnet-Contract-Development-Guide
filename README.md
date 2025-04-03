# Seismic Devnet Contract Development Guide

▶ **Overview**
This guide walks you through deploying and interacting with an encrypted contract on Seismic Devnet. Follow the steps carefully to set up everything correctly.

---

◆ **Pre-Requirements**
Ensure you have the following installed before proceeding:

➤ **1. Install Rust**
```sh
curl https://sh.rustup.rs -sSf | sh  
. "$HOME/.cargo/env"
```
✔ Verify Installation:
```sh
rustc --version
```

➤ **2. Install jq**
• For WSL/Ubuntu:
```sh
sudo apt install jq
```
• For Mac:
```sh
brew install jq
```

➤ **3. Install sfoundryup**
```sh
curl -L \
     -H "Accept: application/vnd.github.v3.raw" \
     "https://api.github.com/repos/SeismicSystems/seismic-foundry/contents/sfoundryup/install?ref=seismic" | bash
source ~/.bashrc
```

➤ **4. Run sfoundryup**
```sh
sfoundryup
```
⚡ This process may take a while to complete.

---

▶ **Deploy an Encrypted Contract**

➤ **1. Clone & Navigate to the Repository**
```sh
git clone --recurse-submodules https://github.com/SeismicSystems/try-devnet.git
cd try-devnet/packages/contract/
```

➤ **2. Deploy the Contract**
Run the script:
```sh
bash script/deploy.sh
```
✔ This will:
• Generate a wallet
• Prompt a Faucet URL
• Display the wallet address

⚠ Make sure to claim the faucet before proceeding. Once done, your contract is deployed!

---

▶ **Interact with an Encrypted Contract**

➤ **1. Navigate to Home Directory**
```sh
cd $HOME
```

➤ **2. Install Bun**
```sh
curl -fsSL https://bun.sh/install | bash
```

➤ **3. Install Node Dependencies**
```sh
cd try-devnet/packages/cli/
bun install
```

➤ **4. Send Transactions**
```sh
bash script/transact.sh
```
✔ Done!

---

◆ **Need Help?**
• Follow me on X for updates and support: https://x.com/PhaResearcher

Happy Coding!
