Here's how to make all the content copiable by formatting it in code blocks:

## 🚀 Privasea Node Setup Guide

```
SYSTEM REQUIREMENTS
• OS: Ubuntu (Recommended)
• Storage: 100GB
• RAM: 8GB
• CPU: 6 cores (x86)
```

+ Buy VPS M HERE 👉 [Click Me ](https://my.virtarix.com/aff.php?aff=42)

### 1. Install Docker
```bash
source <(wget -O - https://raw.githubusercontent.com/zunxbt/installation/main/docker.sh)

sudo groupadd docker && sudo usermod -aG docker $(whoami) && newgrp docker
```

### 2. Pull Docker Image
```bash
docker pull privasea/acceleration-node-beta:latest
```

### 3. Create Directory & Configure
```bash
# Create directory
mkdir -p ~/privasea/config && cd ~/privasea

# Generate keystore
docker run --rm -it -v "$HOME/privasea/config:/app/config" \
privasea/acceleration-node-beta:latest ./node-calc new_keystore

# Rename keystore file
mv $HOME/privasea/config/UTC--* $HOME/privasea/config/wallet_keystore
```

### 4. Start Node
```bash
# Replace YOUR_PASSWORD with your keystore password
KEYSTORE_PASSWORD=YOUR_PASSWORD && docker run -d --name privanetix-node \
-v "$HOME/privasea/config:/app/config" \
-e KEYSTORE_PASSWORD=$KEYSTORE_PASSWORD \
privasea/acceleration-node-beta:latest
```

### 5. Monitor Node
```bash
# Check container ID
docker ps

# Check logs
docker logs -f CONTAINER_ID
```

### 6. Dashboard Setup
```
1. Visit https://deepsea-beta.privasea.ai
2. Connect wallet (ensure ETH on Arbitrum Sepolia)
3. Click "Set up now"
4. Enter node name
5. Set commission (1-3% recommended)
6. Enter node address from step 3
7. Click "Setup my node"
```

### 7. Staking Setup
```
1. Get TPRAI tokens:
   - Visit: https://deepsea-beta.privasea.ai/deepSeaFaucet
   - Claim 1 TPRAI

2. Stake tokens:
   - Go to: https://deepsea-beta.privasea.ai/staking
   - Click "Details" under Staking Details
   - Enter amount: 1 TPRAI
   - Set gas: 300000
   - Network commission: 0.101
   - Priority fee: 0.10
```

### Important Notes
```
⚠️ REMEMBER:
- Save your node address and password
- Only supports Ubuntu OS
- CPU must not be ARM architecture
- OKX wallet recommended
```
