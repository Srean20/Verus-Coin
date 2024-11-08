# Installation:
0. Download & install [AutoStartApp](https://download.apkcombo.com/com.sugarapps.autostartmanager/AutoStart%20App%20Manager_5.1_apkcombo.com.apk?ecp=Y29tLnN1Z2FyYXBwcy5hdXRvc3RhcnRtYW5hZ2VyLzUuMS8zMy42MzY4ZTMyMzc2YWU5YzhhODNiNzhiZDEwNmRhZTg2ODllNWFiZTA1LmFwaw==&iat=1730945626&sig=79165e089ea6a27c857991d052b342cd&size=8254287&from=cf&version=latest&lang=id&fp=3af295969bbb303a83cee62cae314cde&ip=96.9.94.145)
1. Download & install [Termux](https://github.com/termux/termux-app/releases/download/v0.118.0/termux-app_v0.118.0+github-debug_arm64-v8a.apk)
2. Get Termux ready:
- Type `y` then enter key in any prompts!
```
yes | pkg update && pkg upgrade
yes | pkg install libjansson wget nano
```
3. Download ccminer, config, start:
```
mkdir ccminer && cd ccminer
wget https://raw.githubusercontent.com/Srean20/Verus-Coin/main/ccminer
wget https://raw.githubusercontent.com/Srean20/Verus-Coin/main/config.json
wget https://raw.githubusercontent.com/Srean20/Verus-Coin/main/start.sh
chmod +x ccminer start.sh
```
```
nano config.json
```
Termux Autorun Start.sh
```
cd && cd && cd && nano ../usr/etc/bash.bashrc
```
Copy and Paste
```
cd ccminer/&&./start.sh
```


# Usage:

1. Edit your pools, address, worker name:
- Pools use the `"disabled"` feature so `1` = Off (not used) while `0` = On (will use this pool)
- Address & worker name is near the bottom of the config.json in format `address here.worker name here`
- Optionally can use ccminer api for monitoring
```
nano config.json
```
2. Start ccminer with:
```
~/ccminer/start.sh
```
3. Close ccminer with:
```
CTRL + c
```
# Tips & Tricks:
- If Termux can't complete update & upgrade please clear app cache and data.
- Disable battery manager, battery optimization for Termux app.
- If you have a "protect battery" option to stop charge at 85% or similar enable it to help preserve battery health.
- If you long press anywhere within Termux then click `More` there is an option to `Keep screen on`.
- Alternatively you can pull down the notification drawer and expand Termux notification to `Acquire wakelock` this will enable you to mine with the screen off **(NOTE! not all devices obey this rule is a hit or miss)**
- Use a pool with low latency to your location/internet.
- Give the miner/stratum time to stabilize hashrate(~30m-1h).
