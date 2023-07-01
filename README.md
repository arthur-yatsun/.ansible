
## Setup software and tools:
| Category             | Tools                                                                                                                              |
|----------------------|------------------------------------------------------------------------------------------------------------------------------------|
| Shell                | zsh, oh-my-zsh, zsh-autosuggestions, zsh-syntax-highlighting, zsh-autoswitch-virtualenv, powerlevel10k                             |
| Dotfiles             | stow, https://github.com/arthur-yatsun/.dotfiles                                                                                   |
| Tmux                 | tmux, tpm                                                                                                                          |
| Core                 | curl vim wget git xclip htop zsh software-properties-common stow libreadline-dev ripgrep build-essential neovim + Packer tmux + tpm |
| Programming languages | Python3.8 pip3 virtualenv NodeJS npm Java Maven Lua                                                                                |
| Databases            | MySQL PostgreSQL MongoDB                                                                                                           |
| Cloud SDKs           | gcloud                                                                                                                             |

Configure base filesystem structure:
```bash
- ~/ 
  --- ~/documents/repos
  --- ~/documents/stuff
  --- ...
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

2. Install ansible

```bash
brew install ansible
```

3. Ensure you have valid ssh key to clone private repos

### Run ansible playbook

```bash
ansible-playbook local.yml --tags "mac_os"
```

