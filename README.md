**README**

This is a recipe to install netcheck

The file `playbooks/vars/main.yaml` is encrypted using ansible vault it can be replaced with
```
---

django_secret_key: ++++++++++++++++++++++BIGSTRING+++++++++++++++++++++++++++++++++++
```

**How to Install:**
```
pip install ansible
```

**How to Run:**
```
# password file
export ANSIBLE_VAULT_PASSWORD_FILE='$HOME/ansible-conf/vault_pass'
# hosts file
export ANSIBLE_INVENTORY='$HOME/ansible-conf/hosts'
# ssh key
export ANSIBLE_PRIVATE_KEY_FILE='$HOME/.ssh/id_rsa'
```

Command:
```
ansible-playbook playbooks/netcheck.yaml
```

**Example contents of hosts file**
```
[netcheck]
netcheck_0 ansible_ssh_host=127.0.0.1
netcheck_1.exampledns.com
```
**Example contents of passowrd file**
```
MYSUPERPASSWORDW
```
