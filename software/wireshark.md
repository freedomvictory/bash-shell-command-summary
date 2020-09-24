# Wireshark 


## Install it on  `Ubuntu`


 [`Refer it`](https://linuxhint.com/install_wireshark_ubuntu/)
 


 - use `apt-get` install it 
 ```bash
 sudo apt-get update 
 sudo apt install wireshark 
 ```
 - selected YES to `run Wireshark without root access` 

 - add your user to the `wireshark` group, so that you can access `wireshark`
 ```bash 
 sudo usemod -aG wireshark $(whoami)
 ```
- reboot
```bash 
 sudo reboot

```
