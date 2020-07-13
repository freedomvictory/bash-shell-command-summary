# user manage on liunx 




## how to configure a user to sudoers 

1. Open the sudo configuration file by entering the command 
    - `visudo`

2. Scrool through the configuration file until you see the following entry:
    ```bash

    ## Allows people in froup wheel to run all commands 
    # %wheel ALL=(ALL) ALL

    ```
    just delete the` #` sign at the begining of the second line 

3. Save and exit 

4. add User to Group 

    ```bash
    usermod -aG wheel [UserName]
    ```

5. Switch to the sudo user 
    ```bash
    su - [UserName]
    ```
