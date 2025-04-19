# Ansible Setup for Ubuntu

# 설치

```sh
sudo apt install ansible
ansible --version
```

```sh
ansible -i setup/ubuntu/inventory all -m ping
```

## 실행

```sh
ansible-playbook -i setup/ubuntu/inventory setup/ubuntu/main.yml --ask-become-pass -v
```
