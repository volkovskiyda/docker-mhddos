## mhddos docker compose

### Based on [mhddos](https://github.com/porthole-ascend-cinnamon/mhddos_proxy_releases) and [speedtest](https://github.com/volkovskiyda/docker-speedtest)

### Configuration
#### Put *.ovpn files into `vpn` folder

### **To create and start containers run docker compose:**
```bash
docker-compose -f docker-mhddos/docker-compose.yml up -d
```

### **Run a speedtest (without vpn):**
```bash
docker exec mhddos_speedtest bash run.sh
```

### **Run a speedtest (using vpn):**
```bash
docker exec mhddos_speedtest_vpn bash run.sh
```
