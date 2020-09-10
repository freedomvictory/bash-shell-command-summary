# `RSYNC` 




## Instruction 

This command lets you transfer and synchronize data between different machines and directories .Using the `SSH` protocol, you can copy your files securely to another location 


## How to use it 


### Install it 

On your machine and remote machine , install `rsync`

1. debian 

    `sudo apt-get install rsync`

2. centos 

    `sudo yum install rsync`


### Use it 

1. transfer files 

    ```bash
    rsync ~/Dir/dource.pdf test@192.168.1.123:~/Desktop/test
    ```

2. transfer direcotries 

    ```bash 
    rsync ~/SourceDirectory/* username@192.168.1.100:~/Destination 
    ```

3. tansfer all subdirectories 

    ```bash
    rsync -aP ~/Desktop/Dir1/ test@192.168.56.100:~/Desktop/test  # -P (got transfer status)
    ```



