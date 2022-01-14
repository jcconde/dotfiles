# dotfiles

Dotfile's configuration files for bash, zsh, git, ruby, and more.

## Installation

Clone somewhere, then run the `install` script:

~~~ sh
$ git clone git://github.com/jcconde/dotfiles.git ~/dotfiles
$ ~/dotfiles/install
~~~

It won't touch your existing dotfiles, but will symlink the ones that don't
exist. If you want to replace your existing dotfiles, simply move them to a
backup location and run `install` again.

## Misc. commands in `bin`

Check [the `bin` directory](https://github.com/jcconde/dotfiles/tree/master/bin) for awesome commands such as:

- tmux-session

## zsh

- enables completions

- enables Emacs key bindings:
    - `C-a`/`C-e` - beginning/end of line
    - `C-r`/`C-s` - incremental history search backward/forward

- `C-x C-e` - edit current command-line in $EDITOR

- shell prompt includes:
    1. current directory
    2. last command failed status indicator
    3. git branch
    4. rbenv version

- `autobin` - whitelists current directory's `bin` dir that it should get
  prepended to $PATH whenever we `cd` into this project and removed when we
  leave.

## tmux

- `C-h/j/k/l` - switch to pane in the given direction
- `C-\\` - toggle between last active panes

Under tmux prefix `C-a`:

- `C-l` - clear terminal
- `S` - switch to a session that starts with given name, or switch to the last
  session if no name given
- `m` - open man page in a vertical split
- `g` - tail `log/development.log` in a new window
- `R` - source `~/.tmux.conf` after changes

Regular tmux keybindings:

    % vertical split
    " horizontal split
    ! break pane into new window
    c new window

    o select next pane
    { swap pane with previous
    } swap pane with next
    n next window
    p previous window
    ) next session
    ( previous session
    ; select previously active pane
    l select previously active window

    s interactive session & window browser
    w interactive window browser

    $ rename session
    , rename window

    : command prompt
    d detach
    f search text in open windows

    [ copy mode
    ] paste buffer
    # list buffers
    - delete buffer