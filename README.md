# tmux-config
Tmux configuration

### Install tmux on mac m1
```
brew install tmux
```

#### Create .tmux.config
```
touch ~/.tmux.config
```

### Configuration

#### restart your tmux server:
``` tmux kill-server && tmux ```

#### Change statusbar colors
set -g status-fg black
set -g status-bg violet

#### switch panes using Alt-arrow without prefix
bind -n M-Left select-pane -L 
bind -n M-Right select-pane -R
bind -n M-Up select-pane -U
bind -n M-Down select-pane -D

#### remap prefix from C-b to C-a
unbind C-b
set-option -g prefix C-a
bind-key C-a send-prefix

#### escape time
set-option -sg escape-time 10

#### focus events
set-option -g focus-events on

#### default terminal 256color
TERM=screen-256color
set-option -g default-terminal "screen-256color"

#### default terminal color RGB
set-option -sa terminal-overrides ',screen-256color:RGB'

## License
MIT
