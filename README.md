
**🔹 You can access Gensyn Node Step-by-Step YouTube Guide from here https://www.youtube.com/@etccryptoairdrops/videos **



**❤️Follow our TG for Update : https://t.me/etccryptoairdrops**


# 💻 Gensyn-ai-Rl-Swarm_Guide {Mac/Linux} 💻

</div>


# Device/System Requirements 🖥️

![image](https://github.com/user-attachments/assets/594d0847-362b-4ea6-9e61-8590105421c8)

**❌The Node Wont work on low Specs Devices, See you Specs ❌**

* For Vps [Vps Details]
```
ssh username@ip
```


## Install Dependencies
**. Update System Packages**
```bash
sudo apt-get update && sudo apt-get upgrade -y
```
**. Install Node.js and npm**
```console
curl -sSL https://raw.githubusercontent.com/zunxbt/installation/main/node.sh | bash
```
 **.Install other dependencies using the command below**
 ```console
sudo apt update && sudo apt install -y python3 python3-venv python3-pip curl screen git yarn && curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add - && echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list && sudo apt update && sudo apt install -y yarn
```
**. Clone this repository**

```console
rm -rf rl-swarm && git clone https://github.com/zunxbt/rl-swarm.git && cd rl-swarm
```
**. Create a screen session**

```console
screen -S gensyn
```
**. Run the swarm**

```console
python3 -m venv .venv && source .venv/bin/activate && ./run_rl_swarm.sh
```

- Now U can see A `ORG_ID` On ur Terminal..Save it!


That All Hope you are able to run Node without any problem 🚀🚀🚀
