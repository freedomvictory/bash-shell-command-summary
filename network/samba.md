# samba server construct 


```
https://www.linuxbabe.com/ubuntu/install-samba-server-file-share
```




## What is samba 


`Samba` is a free and open-source SMB/CIFS protocol implementation for Unix and Linux that allows for file and print sharing between Unix/Linux, Windows, and macOS machines in a local area network . 

It comprises serveral programs that serve different but related purposes, the most important two of which are :

- `smbd`:provides SMB/CIFS service 
- `nmbd`:This daemon provides `NetBIOS` name service, listen for name-server requests. It also allows the Samba server to be found by other computers on the network.


## How to install Samaba server on Ubuntu  

```
sudo apt install samba samba-common-bin 
```

you can use the following command to check your Samba version , run 
```
smbd --version 
```
To check if Samaba service is running, issue the following command 
```
systemctl status smbd nmbd 
```
To start these two services, issue the following command 
```
sudo systemctl start smbd nmbd 
```


## Create a Private Samba Share 

In this section , we will see how to create a private Samaba share that requires the client to enter username and password in order to gain access. <br/>
The main Samba configuratiojn file is located at: `/etc/samba/smb.conf`. we can edit it using the following command 

```
sudo vim /etc/samba/smb.conf 
```

![](https://www.linuxbabe.com/wp-content/uploads/2017/01/samba-share-ubuntu.png)

in the `[global]` section , make sure the value of `workgroup` is the same with the worgroup setting fo windows computers 

```
workgroup = WORKGROUP 
```

![](https://www.linuxbabe.com/wp-content/uploads/2017/01/samba-ubuntu-server.png)

And then sroll down the bottom of the file. Add a new section like below. 


```
[Private]

comment = needs username and password to access
path = /srv/samba/private/
browseable = yes
guest ok = no
writable = yes
valid users = @samba
```
Explanation:

- Private is the folder name that will be displayed on the Windows network.
- The `comment` is a description for the shared folder.
- The `path` parameter specifies the path to the shared folder. I use `/srv/samba/private/` as an example. You can also use a folder in your home directory.
- `browseable = yes`: Allow other computers in the network to see the Samba server and Samba share. If set to no, users have to know the name of the Samba server and then manually enter a path in the file manager to access the shared folder.
- `guest ok = no`: Disable guest access. In other words, you need to `enter username and password` on the client computer to access the shared folder.
- `writable = yes`: Grants both read and write permission to clients.
- `valid users = @samba`: Only users in the samba group are allowed to access this Samba share.

And then do the following things 

```bash
sudo add user username  #create a linux user 
sudo smbpasswd -a username #set a new user seprate Samba password  
sudo groupadd samba #create the samba group 
sudo gpasswd -a username samba #add this user to samba group
sudo mkdir -p /srv/samba/private # create the private share folder
#set the samba gropu have read, write and execute permission on the shared folder  
sudo setfacl -R -m "g:samba:rwx" /srv/samba/private 

```

Next, run the following command to check if there’s syntactic errors.
```
testparm
```
Now all left to do is to restart smbd and nmbd daemon.
```
sudo systemctl restart smbd nmbd
```