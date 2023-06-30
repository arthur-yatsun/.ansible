## Ubuntu/Mint setup

1. Install ansible
```bash
TBA
```

2. Run ansible playbook
```bash
ansible-playbook install.yml --tags "debian" --ask-become-pass
```

## Mac OS setup
1. Install brew and xcode cli tools 
```bash
# xcode
xcode-select --install

# brew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```

2. Install ansible
```bash
brew install ansible
```

3. Run ansible playbook
```bash
ansible-playbook install.yml --tags "mac_os" --ask-become-pass
```