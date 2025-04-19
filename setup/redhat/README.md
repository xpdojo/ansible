# Ansible Setup for Red Hat

## Prerequisites
```sh
sudo dnf install ansible -y
ansible --version
```

## 실행

```sh
ansible-playbook -i inventory main.yml -v
```
