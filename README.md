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

### NordVPN
Authenticate and configure after first-time setup.
```
nordvpn login
nordvpn settings
nordvpn set killswitch on
nordvpn set autoconnect on
```

Common Commands
```
nordvpn countries
nordvpn cities us
nordvpn connect us
nordvpn status
nordvpn disconnect
nordvpn --help
```

