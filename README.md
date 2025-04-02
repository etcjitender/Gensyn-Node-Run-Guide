# Gensyn-Node-Run-Guide
In this i  Will explain how to Run Gensyn Node  
➡️You can Also Watch video coming - https://www.youtube.com/@etccryptoairdrops/videos  
📌Join Telegram For More - https://t.me/etccryptoairdrops

Install Dependencies
1. Update System Packages

sudo apt-get update && sudo apt-get upgrade -y
2. Install General Utilities and Tools

sudo apt install screen curl iptables build-essential git wget lz4 jq make gcc nano automake autoconf tmux htop nvme-cli libgbm1 pkg-config libssl-dev libleveldb-dev tar clang bsdmainutils ncdu unzip libleveldb-dev  -y
3. Install Docker

# Remove old Docker installations
for pkg in docker.io docker-doc docker-compose podman-docker containerd runc; do sudo apt-get remove $pkg; done

# Add Docker repository
sudo apt-get update
sudo apt-get install ca-certificates curl gnupg
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
sudo chmod a+r /etc/apt/keyrings/docker.gpg

echo \
  "deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  "$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

# Install Docker
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

# Test Docker
sudo docker run hello-world
Tip: To run Docker without sudo, add your user to the Docker group:
sudo usermod -aG docker $USER
4. Install Python

sudo apt-get install python3 python3-pip python3-venv python3-dev -y
5. Install Node

sudo apt-get update
curl -fsSL https://deb.nodesource.com/setup_22.x | sudo -E bash -
sudo apt-get install -y nodejs
node -v
sudo npm install -g yarn
yarn -v
6. Install Yarn

curl -o- -L https://yarnpkg.com/install.sh | bash
export PATH="$HOME/.yarn/bin:$HOME/.config/yarn/global/node_modules/.bin:$PATH"
source ~/.bashrc
Run Node

python3 -m venv .venv && source .venv/bin/activate && ./run_rl_swarm.sh
Clone the Repository

git clone https://github.com/gensyn-ai/rl-swarm/
cd rl-swarm
7. Run the swarmn Open a screen to run it in background

screen -S swarm
Install swarm

python3 -m venv .venv
source .venv/bin/activate
./run_rl_swarm.sh
