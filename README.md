## mhddos docker compose

### Based on [mhddos](https://github.com/porthole-ascend-cinnamon/mhddos_proxy_releases), [openvpn-client](https://github.com/wfg/docker-openvpn-client), [speedtest](https://github.com/volkovskiyda/docker-speedtest) and [mhddos setup](https://github.com/sadviq99/mhddos_proxy-setup)

### Configuration
#### VPN
##### Put *.ovpn files into `vpn` folder

#### Telegram Bot Notifications [`tg.sh`]
##### Create bot via [BotFather](https://t.me/BotFather) -> `/newbot` -> Save token as `TG_TOKEN`
##### Open bot -> `/start`
##### Get Chat id via [RawDataBot](https://t.me/RawDataBot) -> `/start` -> Save `chat_id` as `TG_CHAT_ID`

### **To create and start containers run docker compose:**
```bash
docker-compose -f docker-mhddos/docker-compose.yml up -d
```

### **Change ownership for docker containers:**
```bash
sudo chown $USER:$USER /var/lib/docker/ ; sudo chown -R $USER:$USER /var/lib/docker/containers/
```

### **Send telegram notification:**
```bash
bash docker-mhddos/tg.sh
```
##### Create cronjob to schedule notifications

### **Run a speedtest (without vpn):**
```bash
docker exec mhddos_speedtest bash run.sh
```

### **Run a speedtest (using vpn):**
```bash
docker exec mhddos_speedtest_vpn bash run.sh
```
