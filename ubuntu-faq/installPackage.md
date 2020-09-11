# FAQ install package on ubuntu 




## How to solve depency problem 

 
Reference Link [CLICK THIS](https://appuals.com/fix-unmet-dependencies-error-ubuntu/)

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

- 3.handle the depency problem 

If you want to install `build essential`, just run the following line command 

```bash
sudo apt-get install build-essential  
```

And, If have error occured, the message indicates that the package you not installed , you just installed correct versition package 

```bash 
sudo apt-get install libdpkg-perl=1.19.0.5ubuntu2 
```


**NOTE**
    if last 3 method, can't solve your problem , you can try the following command 

```bash 
#install aptitude , and using it install software 
sudo apt-get install aptitude 
sudo aptitude install PACKAGENAME 
```

## Fix "Fail to Start Session" Error At Ubuntu Login 

[REFER THIS](https://opensourceinside.blogspot.com/2016/07/how-to-fix-failed-to-start-session.html)