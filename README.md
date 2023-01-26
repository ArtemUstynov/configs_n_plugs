\# tmux_conf
\# Send prefix
set-option -g prefix M-c

unbind-key M-c

bind-key M-c send-prefix

\# Use Alt-arrow keys to switch panes

bind -n M-Left select-pane -L

bind -n M-Right select-pane -R

bind -n M-Up select-pane -U

bind -n M-Down select-pane -D

\# Shift arrow to switch windows

bind -n S-Left previous-window

bind -n S-Right next-window

\# Mouse mode

setw -g mouse on

\# Set easier window split keys

bind-key v split-window -h

bind-key h split-window -v

\# Easy config reload

bind-key r source-file ~/.tmux.conf \; display-message "~/.tmux.conf reloaded."

set -g default-terminal "xterm-256color"
