# config static ip on ubuntu server 


# An easy way to use `ifconfig `


## Set ip address 

``` 
ifconfig eth0 192.168.1.5 netmask 255.255.255.0 up 
```
## Set default gateway
``` 
route add default gw 192.168.1.1 
```

## Set DNS server 
```
echo "nameserver 114.114.114.114" > /etc/resolve.conf 
```

This is an easy way to configure static ip . It will take affect immediately but doesn't affect after restart the PC.


# A More better way is to use `Netplan`


## What is `Netplan`

`Netplan` is the default network management tool on Ubuntu, replacing the configuration file `/etc/network/interfaces` that had previously been used to configure the network on Ubuntu 

## How to use it 

We need to edit configuration file in `YAML` syntax on `/etc/netplan/*.yaml` .

First we need to open `YAML` configuration file with `vim`
```bash
$sudo vim -u NONE /etc/netplan/*.yaml 
```

And the file like this. When editing `Yaml` files, make sure you follow the YAML code indent standards.  

```
network:
  version: 2
  renderer: networkd
  ethernets:
    enp2s0:
      dhcp4: no
      addresses:
        - 192.168.121.199/24
      gateway4: 192.168.121.1
      nameservers:
          addresses: [8.8.8.8, 1.1.1.1]
```

And now we need to install netplan tools 

```
sudo apt-get install netplan.io netplan-
```

And Use the following command to load yaml configuration file  

```
sudo netplan apply
```

or excute the following command to show debug info  

```
sudo netpan -d apply 
```


And ,we can verify the changes by typing  

```
ip addr show dev enp2s0 
```


[REFER THIS NET](https://linuxize.com/post/how-to-configure-static-ip-address-on-ubuntu-18-04/)









