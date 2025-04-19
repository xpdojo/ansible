# Ansible Setup for macOS

## Prerequisites
```sh
brew install ansible
ansible --version
```

## 실행

```sh
ansible-playbook -i setup/macos/inventory setup/macos/main.yml -v
```
