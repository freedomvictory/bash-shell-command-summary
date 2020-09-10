# EXPECT 


## Instruction 

The name of the program itself gives you an idea about its use case it. We tell `expect` what to look for while executing another program. We also tell what the response should be. 


## How to use it 

### Install it 

```bash
# yum install expect 
# apt-get install expect 
# pacman -S expect 
```

### Arguments list 

- `spawn` Start a script or a program 
- `expect` Wait for program output
- `send` Sends a reply to your program 
- `interact` Allows you to interact with your program 



### Use examples 


1. Set user passwd  

```bash
#!/usr/bin/expect 

user_name=""
passwd=""
spawn passwd $user_name
expect -exact "Enter new UNIX password: "
send -- "$passwd\r"
expect -exact "\rRetype new UNIX password: "
send -- "$pass_word\r"
expect eof 

```



2. rsync files to remote host 

```

#!/usr/bin/expect 

spawn rsync -ap ./ pi@10.10.18.123:~/Documents/code
expect -exact "pi@10.18.123's password:\r"
send -- "2184as\r"
expect eof
```