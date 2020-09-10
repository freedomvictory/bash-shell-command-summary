# Tmux configure 



## configure some key maps 


```bash
unbind-key C-b
set -g prefix 'C-\'
bind-key 'C-\' send-prefix

bind - split-window -v
unbind '%'

bind | split-window -h
unbind '"'


bind h select-pane -L
bind j select-pane -D
bind k select-pane -U
bind l select-pane -R

```


## install tmux plugin 




