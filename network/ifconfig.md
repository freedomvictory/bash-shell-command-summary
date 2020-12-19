# IFCONFIG 


## How to install it on `ubuntu`


`sudo apt-get install net-tools`

## How to use it  

```bash 
ifconfig eth0 up           //start netcard 
ifconfig eth0 down         //shutdown netcard
ifconfig eth0 192.168.0.18  //configure ip 
ifconfig eth0 netmask 255.255.255.0  // config netmask 
ifconfig -a  //show all the netcard  
```

## Expand 

1. Set Defualt gateway 

```
route add default gw 192.168.0.1 
```

2. Set Dns server 

```
echo "nameserver 1.1.1.1" > /etc/resolve.conf 
```






