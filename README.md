# IPSec_L2TP_IKEV2
IPSec_L2TP_IKEV2 vpn solution with docker


```bash
docker run --name ipsec-vpn-server --restart=always --env-file ./vpn.env  -v /mnt/ikev2-vpn-data:/etc/ipsec.d -v /lib/modules:/lib/modules:ro -p 500:500/udp -p 4500:4500/udp -d --privileged hwdsl2/ipsec-vpn-server
```


```bash
VPN_IPSEC_PSK=your_ipsec_pre_shared_key
VPN_USER=your_vpn_username
VPN_PASSWORD=your_vpn_password

docker logs ipsec-vpn-server
```
