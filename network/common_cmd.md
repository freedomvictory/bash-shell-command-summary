# COMMON NETWORK COMMAND 



## How to browse network port already used 

```bash 
less /etc/services  | grep 'PORTNUMER'
```


## ARP : got local area network all active ip address 

```bash
arp-scan  -l -I enp2s0 
```

## Configure network 

The flowing command is suitable for `UBUNTU`
```bash 
    # IP and netmask
    ifconfig eth0 192.168.1.11 netmask 255.255.255.0 up
    # default gateway
    route add default gw 192.168.1.1 
    # DNS
    echo "nameserver 8.8.8.8">/etc/resolv.conf 
```