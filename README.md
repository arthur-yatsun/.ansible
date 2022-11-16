# .ansible

Install MacOS environment
```
ansible-playbook local.yml --tags "mac_os" --ask-become-pass
```

Install Debian environment
```
ansible-playbook local.yml --tags "debian" --ask-become-pass
```
