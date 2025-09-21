# dotfiles-ubuntu
Ubuntu configuration files, runnable using Ansible.

## Setup 
Install Ansible:
```
sudo apt install ansible
```

## Running 
Run all install playbooks:
```
ansible-playbook -i localhost, -c local setup-ubuntu.yml -K
```

Run just one install playbook:
```
ansible-playbook -i localhost, -c local install-software.yml -K
```

## Post Install Steps

### gh (Github CLI)
Create ssh key, and register it with Github.
```
ssh-keygen -t ed25519 -C "jake@ubuntu"
gh auth login
```

### LazyVim
Run `nvim` once to install everything.

