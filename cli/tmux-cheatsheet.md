# Tmux Cheatsheet

## Sessions

```sh
# Start a new tmux session
tmux new -s my_session

# List all active sessions
tmux ls

# Attach to a session
tmux a -t my_session

# Kill a session
tmux kill-session -t my_session

# Kill all sessions
tmux kill-server

# Detach from a session
ctrl-b + d

# Rename a session
ctrl-b + $
```

## Windows

```sh
# Create a new window
ctrl-b + c

# Navigate between windows (forward)
ctrl-b + n

# Navigate between windows (backward)
ctrl-b + p

# List all windows
ctrl-b + w

# Rename current window
ctrl-b + ,

# Kill current window
ctrl-b + &
```

## Panes

```sh
# Kill current pane
ctrl-b + x

# Split window vertically (creates a pane)
ctrl-b + %

# Split window horizontally (creates a pane)
ctrl-b + "

# Move current pane to a new window
ctrl-b + !
```

## Navigation

```sh
# Navigate between panes (forward)
ctrl-b + o

# Navigate between panes (backward)
ctrl-b + ;

# Show pane numbers
ctrl-b + q

# Swap with the next pane
ctrl-b + ctrl-o

# Fullscreen current pane
ctrl-b + z
```

## Copy Mode

```sh
# Enter Copy mode
ctrl-b + [

# Exit Copy mode
q

# Select and Copy text (Enter Copy mode first)
space + nagication keys + enter

# Paste text
ctrl-b + ]
```

### Tips:

1. Increase the window timeout of `ctrl-b + q` to make it easier to navigate between panes.

```sh
# Add this to your tmux.conf file
set -g display-panes-time 3000
```
