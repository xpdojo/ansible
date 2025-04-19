# Ansible

```sh
# ansible-inventory -i hosts.ini --list -y
> ansible-inventory --inventory hosts.ini --list --yaml
all:
  children:
    home:
      hosts:
        local:
          ansible_connection: local
    ungrouped: {}
```

```sh
# ansible all -i hosts.ini -m ping
ansible all --inventory hosts.ini --module-name ping -vvv

# on MacOSX
local | SUCCESS => {
    "ansible_facts": {
        "discovered_interpreter_python": "/opt/homebrew/bin/python3.10"
    },
    "changed": false,
    "ping": "pong"
}

# on Ubuntu
local | SUCCESS => {
    "ansible_facts": {
        "discovered_interpreter_python": "/usr/bin/python3"
    },
    "changed": false,
    "ping": "pong"
}
```

```sh
ansible all --inventory hosts.ini --args "df -h" -vvv
```

## 참조

- [How To Install and Configure Ansible on Ubuntu 20.04](https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-ansible-on-ubuntu-20-04) - DigitalOcean
- [How To Set Up Ansible Inventories](https://www.digitalocean.com/community/tutorials/how-to-set-up-ansible-inventories) - DigitalOcean
