
## Setup software and tools:
| Name                       | ansible-playbook tag(s)                                                                    | Tools                                                                                                 |
|----------------------------|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| MacOS complete setup       | mac_os                                                                                     | Complete MacOS setup                                                                                  |
| Debian linux complete setup | debian_linux                                                                               | Complete Debian (Ubuntu/Mint) setup                                                                   |
| Shell                      | mac_os_shell, debian_linux_shell                                                           | zsh, oh-my-zsh, zsh-autosuggestions, zsh-syntax-highlighting, zsh-autoswitch-virtualenv, powerlevel10k |
| Dotfiles                   | mac_os_dotfiles,  debian_linux_dotfiles                                                    | stow, https://github.com/arthur-yatsun/.dotfiles                                                      |
| Fonts                      | mac_os_fonts, ~~debian_linux_fonts~~                                                       | Hack Nerd Font                                                                                        |
| Tmux                       | mac_os_tmux, debian_linux_tmux                                                             | tmux, tpm                                                                                             |
| Core                       | mac_os_core, ~~debian_linux_core~~                                                         | curl wget htop jq ... (OS dependent)                                                                  |
| Nvim                       | mac_os_nvim, ~~debian_linux_nvim~~                                                         | nvim, packer                                                                                          |
| Python                     | mac_os_python, ipython, python3.7, python3.8, python3.9, python3.10, python3.11, python2.7 | virtualenv, pyenv, ipython, ipdb, 3.7, 3.8, 3.9, 3.10, 3.11, 2.7                                      |
| Databases                  | mac_os_databases                                                                           | MySQL, PostgresSQL, Redis, MongoDB                                                                    |
| Cloud SDKs                 | mac_os_cloud                                                                               | gcloud, aws cli, kubectl                                                                              |


Configure base filesystem structure:
tag - `mac_os_filesystem` or `debian_linux_filesystem`
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

Install using specific tag:
```bash
ansible-playbook install.yml --tags "<tag_name>" --ask-become-pass
```

## Ubuntu/Mint setup

### Prerequisites

```bash
TBA
```

### Run ansible playbook

```bash
ansible-playbook install.yml --tags "debian_linux" --ask-become-pass
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
ansible-playbook install.yml --tags "mac_os" --ask-become-pass
```

