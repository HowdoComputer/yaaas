# Yet Another Attack Automation System (YAAAS)

YAAAS is a repository of prototype Ansible playbooks for building attack infrastructure. I intend to use this during my day job and with side projects.

## Disclaimers

- I made this project partly to learn Ansible. There will certainly be dumb decisions made in here. Use at your own risk.
- This whole repo is still in very early days. There's still lots of work to do.
- Everything here was tested on Kali and **only** Kali. For now.
- Sliver is the only non-metasploit C2 project installed. For now.
- The c2-servers doesn't do very much. For now.
- The redirectors role is just an idea. For now.
- Have I mentioned this isn't really complete? XD

Please note that the default configuration here will grant the account named in the `main_username` variable root privileges through the docker installation and group membership process! All these playbooks are written as though `main_username` has full `sudo` privileges already, but still.

## Setup

Clone this repo to the machine that will be your ansible controller.

Install ansible via the appropriate method for your controller, whatever that may be.

e.g.

```bash
sudo apt install ansible
```

Add your hosts to ![hosts.ini](./hosts.ini) or ![hosts.yml](./hosts.yml). The ![ansible.cfg](./ansible.cfg) file in this repo assumes `hosts.yml` by default.

Please also note that this repo uses `localhost` as an `attack_host` and a `c2_server` by default. See ![hosts.yml](./hosts.yml).

Check that your hosts are listed and organized correctly with something like this:

```bash
ansible-inventory --list    # List of hosts in JSON format
ansible-inventory --graph   # List of hosts in text tree format
```

## Configuration

![ansible.cfg](./ansible.cfg) for global Ansible configuration.

Inventory: ![hosts.ini](./hosts.ini) or ![hosts.yml](./hosts.yml). Set which one in ![ansible.cfg](./ansible.cfg) 

Global variables: ![./vars/global-vars.yml](./vars/global-vars.yml) has useful global variables defining things like your main username, destination directories, etc.

## Execution

Do all the things.

```bash
ansible-playbook runMe.yml
```

## Other useful snippets

Show all ansible facts on your local host with no SSH server required:

```bash
ansible -c local localhost ansible.builtin.setup
```

Run playbook and exclude any tasks with tag "tested":

```bash
ansible-playbook runMe.yml --skip-tags tested
```

## TODOs

See ![./TODO.md](./TODO.md)
