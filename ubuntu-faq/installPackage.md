# FAQ install package on ubuntu 




## How to solve depency problem 


- 1.update the ubuntu source to chinese huawei source 


refer huaweicloud network 


- 2.update everything 

```bash
sudo apt-get clean
sudo apt-get update
sudo apt-get install -f 
sudo dpkg -a --configure 
sudo apt-get dist-upgrade 
```

- 3. handle the depency problem 

If you want to install `build essential`, just run the following line command 

```bash
sudo apt-get install build-essential  
```

And, If have error occured, the message indicates that the package you not installed , you just installed correct versition package 

```bash 
sudo apt-get install libdpkg-perl=1.19.0.5ubuntu2 
```

