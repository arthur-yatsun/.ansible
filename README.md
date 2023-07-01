
## Setup software and tools:
| Name                   | ansible-playbook tag(s)                 | Tools                                                                                                 |
|------------------------|-----------------------------------------|-------------------------------------------------------------------------------------------------------|
| MacOS complete setup   | mac_os                                  | Complete MacOS setup                                                                                  |
| Debian linux complete setup | debian_linux                            | Complete Debian (Ubuntu/Mint) setup                                                                   |
| Shell                  | mac_os_shell, debian_linux_shell        | zsh, oh-my-zsh, zsh-autosuggestions, zsh-syntax-highlighting, zsh-autoswitch-virtualenv, powerlevel10k |
| Dotfiles               | mac_os_dotfiles,  debian_linux_dotfiles | stow, https://github.com/arthur-yatsun/.dotfiles                                                      |
| Tmux                   | mac_os_tmux, debian_linux_tmux          | tmux, tpm                                                                                             |
| Core                   | mac_os_core, debian_linux_core          | curl wget htop jq ... (OS dependent)                                                                  |
|                        | Programming languages                   | Python3.8 pip3 virtualenv NodeJS npm Java Maven Lua                                                   |
| ---                    | Databases                               | MySQL PostgreSQL MongoDB                                                                              |
| ---                    | Cloud SDKs                              | gcloud                                                                                                |


 

Configure base filesystem structure:
tag - `filesystem`
```bash
- ~/ 
  --- ~/documents/repos
  --- ~/documents/stuff
  --- ...
```


Require manual installation: 
```
Alacritty, Iterm2, tilix
Firefox DE, Chrome
Slack, Discord, Zoom, Microsoft Teams, Telegram
Jetbrains Toolbox, PyCharm, DataGrip, VSCode
Docker (Mac OS only)
Google Drive, Notion, Obsidian
CopyQ, xclip
```

## Ubuntu/Mint setup

### Prerequisites

```bash
TBA
```

### Run ansible playbook

```bash
ansible-playbook local.yml --tags "debian_linux"
```

## Mac OS setup

### Preprequisites
1. Install brew and xcode cli tools
```bash
# xcode
xcode-select --install

# brew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
export PATH=/opt/homebrew/bin:$PATH
```

2. Install git and ansible
3. Ensure you have valid ssh key to clone private repos

### Run ansible playbook

```bash
ansible-playbook local.yml --tags "mac_os"
```

