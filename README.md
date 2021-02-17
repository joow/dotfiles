# Dotfiles

> Personal dotfiles handled by [chezmoi](https://www.chezmoi.io).

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

