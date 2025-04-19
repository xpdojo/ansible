# Ansible Setup for Ubuntu

# 설치

```sh
sudo apt install ansible
```

```sh
ansible -i setup/ubuntu/inventory all -m ping
```

## 실행

```sh
ansible-playbook -i setup/ubuntu/inventory setup/ubuntu/main.yml --ask-become-pass -v
```

- verbose 출력: `-v` ~ `-vvvv`
- 비밀번호 입력: `--ask-become-pass`
