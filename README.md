# .ansible

## Install MacOS environment

Install xcode cli tools
```bash
xcode-select --install
```

Install homebrew
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"

?? probably you will need to add homebrew directory to the $PATH
echo "export PATH=/opt/homebrew/bin:$PATH" >> ~/.zshrc
```

Install ansible
```bash
brew install ansible
```

Install environment
```bash
ansible-playbook local.yml --tags "mac_os" --ask-become-pass
```

## Install Debian environment
```bash
ansible-playbook local.yml --tags "debian" --ask-become-pass
```
