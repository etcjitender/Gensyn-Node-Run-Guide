
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



* Now It will promt `Would you like to push models you train in the RL swarm to the Hugging Face Hub? [y/N]` Enter `N`

![image](https://github.com/user-attachments/assets/b63da75d-389a-4ded-9c4e-cd23804d94ef)



![image](https://github.com/user-attachments/assets/35321942-1aa3-47f1-92a3-dae9881b64cd)

Here we go🚀

Its Done ✅

It will Generate Logs Soon🙌


* Detach from `screen session` **(vps)**

Use `Ctrl + A` and then press `D`

* Attach to gensyn Screen to see Logs

```
screen -r gensyn
```



<div align="center">

#  🛠 FAQ & Troubleshoot 🛠

</div>


#  How to Login or access  http://localhost:3000/ in VPS? 📶

* Open a new Terminal and login ur vps 

* Allow Incoming connection on VPS

```
sudo apt install ufw -y
sudo ufw allow 3000/tcp
```

* Enable ufw

```
sudo ufw enable
```

* Install cloudflared on the VPS

```
wget -q https://github.com/cloudflare/cloudflared/releases/latest/download/cloudflared-linux-amd64.deb
````

```
sudo dpkg -i cloudflared-linux-amd64.deb
```

* Check version

```
cloudflared --version
```

* Make sure your Node is running on port 3000 in Previous Screen

* Run the tunnel command

```
cloudflared tunnel --url http://localhost:3000
```

* Access the Link from your local machine

    
	
    ![image](https://github.com/user-attachments/assets/c5bdfec5-123d-4625-8da8-f46269700950)

* Now follow Login
 
How to get the Node Name?

* Check the image below to get your Node id!

![image](https://github.com/user-attachments/assets/728c6401-75c8-43b4-973c-e9d515c4b453)

#  Save your `swarm.pem` file (for future login)

* open a wsl window 

* If U have to copy this file to your local machine from VPS then Run this command from your local Terminal--

```
scp USERNAME@YOUR_IP:~/rl-swarm/swarm.pem ~/swarm.pem
```
Get Ip 

```
curl -s ifconfig.me
```

It will save here in ur Terminal's Root Directory!


#  How To start the Next Day (Local Pc)

*
 ```
  cd rl-swarm
 ```

*
 ```
  python3 -m venv .venv
```

*
```
source .venv/bin/activate
```

*
```
./run_rl_swarm.sh
```


That All Hope you are able to run Node without any problem 🚀🚀🚀
