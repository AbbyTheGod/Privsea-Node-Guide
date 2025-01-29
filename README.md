🚀 PRIVASEA NODE SETUP GUIDE
SYSTEM REQUIREMENTS
• OS: Debian/Ubuntu
• Storage: 100GB
• RAM: 8GB
• CPU: 6 cores (x86)

Buy VPS M HERE 👉 CLICKME


— — — — — — — — — -
1. INSTALL DOCKER
— — — — — — — — — -
source <(wget -O - https://raw.githubusercontent.com/zunxbt/installation/main/docker.sh)

sudo groupadd docker && sudo usermod -aG docker $(whoami) && newgrp docker

— — — — — — — — — -
2. PULL DOCKER IMAGE
— — — — — — — — — -
docker pull privasea/acceleration-node-beta:latest

— — — — — — — — — -
3. CREATE DIRECTORY
— — — — — — — — — -
mkdir -p /privasea/config && cd /privasea

docker run -it -v “/privasea/config:/app/config” privasea/acceleration-node-beta:latest ./node-calc new_keystore

— — — — — — — — — -
4. CONFIGURE KEYSTORE
— — — — — — — — — -
cd /privasea/config
mv ./UTC — * ./wallet_keystore

— — — — — — — — — -
5. START NODE
— — — — — — — — — -
cd /privasea/

docker run -d -v “/privasea/config:/app/config” -e KEYSTORE_PASSWORD=YOUR_PASSWORD privasea/acceleration-node-beta:latest

— — — — — — — — — -
6. CHECK LOGS
— — — — — — — — — -
docker ps
docker logs -f CONTAINER_ID

— — — — — — — — — -
IMPORTANT LINKS
— — — — — — — — — -
• Dashboard: https://deepsea-beta.privasea.ai
• Faucet: https://deepsea-beta.privasea.ai/deepSeaFaucet
• Staking: https://deepsea-beta.privasea.ai/staking

— — — — — — — — — -
STAKING SETTINGS
— — — — — — — — — -
• Gas Limit: 300000
• Network Commission: 0.101
• Priority Fee: 0.10

⚠️ Save your node address and password!

Join My Telegram Channel 👉 https://t.me/alphabyabby
