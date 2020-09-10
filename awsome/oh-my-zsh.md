# OH-MY-ZSH




## Install oh-my-zsh 


- update the packags 
    ```bash
    sudo apt-get update`
    sudo apt upgrade`
    ```
- install prerequisite package 

    ```sh
    sudo apt-get install zsh 
    sudo apt-get install powerline fonts-powerline 
    ```

- clone the oh-my-zsh repo 

    ```sh
    git clone https://github.com/robbyrussell/oh-my-zsh.git ~/.oh-my-zsh 
    ```

- create a New `ZSH` configuration file 

    ```sh
    cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc
    ```

## Configure oh-my-zsh

open `.zshrc` file and edit it

```zsh
ZSH_THEME="***"


```


## Reference Link 

**https://dev.to/mskian/install-z-shell-oh-my-zsh-on-ubuntu-1804-lts-4cm4**