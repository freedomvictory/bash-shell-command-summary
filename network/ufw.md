
Please Refer 
[`THIS NET`](https://help.ubuntu.com/community/UFW)


# UFW BASIC USE 

1. enbale and check status
    - `sudo ufw enable`
    - `sudo ufw status`
2. set allow some port 
    - `sudo ufw allow 53`
    - `sudo ufw allow 53/tcp`
    - `sudo ufw allow 53/udp`
3. set deny some port 
    - `sudo ufw deny 53`
    - `sudo ufw deny 53/tcp`
    - `sudo ufw deny 53/udp`
4. delete some config 
    - `sudo ufw delete deny 80/tcp`
5. set allow some service 
    - `sudo ufw allow ssh`
    - `sudo ufw allow nfs`
6. set deny some service 
    - `sudo ufw deny ssh`
7. set allow by spec IP 
    - `sudo ufw allow from 207.46.232.182`



