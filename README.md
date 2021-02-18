# Dotfiles

> Personal dotfiles handled by [chezmoi](https://www.chezmoi.io).

## Requirements

| Name      | Description                    | Link                                                           |
|-----------|--------------------------------|----------------------------------------------------------------|
| chezmoi   | dotfiles manager               | https://www.chezmoi.io                                         |
| bspwm     | window manager                 | https://github.com/baskerville/bspwm                           |
| sxhkd     | hotkey daemon                  | https://github.com/baskerville/sxhkd                           |
| alacritty | terminal emulator              | https://github.com/alacritty/alacritty                         |
| fish      | command line shell             | https://fishshell.com/                                         |
| polybar   | status bar                     | https://polybar.github.io/                                     |
| rofi      | X11 dynamic menu               | https://github.com/davatorium/rofi                             |
| picom     | X11 compositor                 | https://github.com/yshui/picom                                 |
| feh       | image viewer                   | https://feh.finalrewind.org/                                   |
| xsetroot  | X11 utility                    | https://www.x.org/archive/X11R7.5/doc/man/man1/xsetroot.1.html |
| wmname    | wm name property getter/setter | https://tools.suckless.org/x/wmname/                           |

## Setup a new target

```shell
git clone https://github.com/joow/dotfiles.git
vim ~/.config/chezmoi/chezmoi.toml
# see below to fill data
chmod 0600 ~/.config/chezmoi/chezmoi.toml
chezmoi apply --verbose --dry-run
chezmoi apply
```

### Data

Some configuration files require data to be generated.

Fill `~/.config/chezmoi/chezmoi.toml` with the following values :

```toml
[data]

# Git configuration
[data.git]
    # mandatory
    name = "YOUR NAME"
    # mandatory
    email = "YOUR EMAIL
    # optional, if set commits and tags will be signed
    gpgKey = "0x0123456"
    # optional, may be used for specific additional git configuration
    raw = """
    ...
    """
```

