# UBUNTU remap keyboard keys 

## find keyborad identifiers 


```bash
xmodmap -pke > ~/keymaptable 
vim ~/keymaptable 
```
run this command , you will see a rather long list of all the keyboard identifiers 


## configure remap 

- open the configure file 

```bash
sudo gedit /usr/share/X11/xkb/symbols/pc 
```

- save it 

- clear xkb setting cache 

```bash
sudo rm -rf /var/lib/xkb/* 
```

## Reference Link 

**http://www.fascinatingcaptain.com/projects/remap-keyboard-keys-for-ubuntu/**





