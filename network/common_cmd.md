# COMMON NETWORK COMMAND 



## How to browse network port already used 

```bash 
less /etc/services  | grep 'PORTNUMER'
```


## ARP : got local area network all active ip address 

```bash
arp-scan  -l -I enp2s0 
```

## TELNET 

1. Instruction 
    It's a text-based program you can use to connect to another computer using the internet. 

2. How to use it 

    ```bash
    #connect
    Telnet <host_name> <port>
    # send data to host 
    


    ```


## DNS `nsloopup`

1. Instruction 

    It's a program to query internet domain name servers `nslookup` has two modes, interactive and non-interactive. 

2. How to use it

    - non-interactive mode 

        `nslookup [-option] [name |-] [server]`

    - interactive mode 

        `nslookup`

3. Reference 

    [`nslookup`](https://www.tutorialspoint.com/unix_commands/nslookup.htm)




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

another way configure DNS for `UBUNTU`

`systemd-resolve --set-dns=114.114.114.114 --interface=enp2s0`

