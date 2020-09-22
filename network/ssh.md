# Install and configure SSH server on `UBUNTU`


## Install it 

`sudo apt install openssh-server `


## Configure steps  

- back it 


    ```bash
    sudo cp /etc/ssh//sshd_config /etc/ssh/sshd_config.original //back
    sudo chmod a-w /etc/ssh/sshd_config.original //anyone can't write it 
    ```
- Edit it 

    `sudo vim /etc/ssh/sshd_config`

- Test it 

    `sudo sshd -t -f /etc/ssh/sshd_config`

- restart it and check the status of it running 

    `sudo systemctl restart sshd.service`

    `sudo systemctl status sshd.service`

## Configure file reference 

```
PermitRootLogin no  //disable the login of user root 
PasswordAuthentication yes //have to input passwd when login 

```

## limit SSH access to specific clients by IP address 


[`Refer it`](https://unix.stackexchange.com/questions/406245/limit-ssh-access-to-specific-clients-by-ip-addr)

[`hosts.allow`](https://www.smartdomotik.com/2015/02/09/using-etchosts-allow-and-etchosts-deny-to-secure-unix/)

Using TCP wrappers 

edit your hosts.allow file 

```
sshd : 10.10.18.23: ALLOW                                                  
sshd : ALL: DENY    
```





