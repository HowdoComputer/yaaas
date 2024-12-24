# Stuff to be done

- [x] Create a role for attack-hosts
  - [x] Add packages and git repos into var list files
  - [x] add update and upgrade packages to playlist
  - [x] get git repos to save to directories named the same as the repo
- [x] Update `tldr` if present
- [x] Download sliver binary releases
  - [x] Do check based on how old the last modified timestamp is?
- [ ] Install sliver armory
  - [x] This is a difficult task. For now, just implementing instructions for the user to do this.
  - [ ] finish the message instructions
  - [ ] Add post-sliver-setup.yml playbook to automate moving `/root/.sliver-client` to `{{ main_username }}` homedir
- [x] Grab linpeas & winpeas
  - [x] Do check based on how old the last modified timestamp is?
- [x] Figure out directory structure. Mimic kit2?
- [x] Set up variables which can be configured
  - [x] Directory locations. ~/targets/\[tools|c2\], for example
  - [x] Main user account
- [x] Add obfuscation tooling
  - [x] Docker.io installation
  - [x] Configure user account to be docker user. Same as "main" from above?
  - [x] pull pezor docker container
  - [x] Write note file with pezor start syntax
- [x] add sliver and sliver.wiki to GitHub list
- [ ] Add `bat` alias for `batcat`
  - [ ] Implement this as part of per-user customization
- [x] Add [Sherlock privesc PS1 repository](https://github.com/rasta-mouse/Sherlock.git) to github repos
- [x] Add [Watson .NET repository](https://github.com/rasta-mouse/Watson.git) to github repos
- [x] Add [SharpC2 repository](https://github.com/rasta-mouse/SharpC2.git) to github repos
- [x] Alphabetize github repos by repo name
- [x] Add `vim` to required packages list
- [ ] Create playbooks for creating custom users
  - [ ] Add variable for new users
  - [ ] Add variable for custom aliases
  - [ ] Add variable for custom environment variables
- [ ] Download and install sublime
- [ ] Download and install vscodium
~~- [ ] Download and install poetry crackmapexec. Ugh.~~
- [x] Download and install pipx and netexec (nxc)
- [ ] Download and install autorecon
- [ ] Enable installation of pip packages
  - [ ] Install defaultcreds-cheat-sheet for each user account
- [ ] Enable installation of pipx packages
- [ ] Add installation of `nxc` through pipx
- [ ] Enable installation of pypi packages
- [ ] Set up python virtual environments for certain projects
  - [ ] pywhisker
  - [ ] PKINIT
  - [ ] targetedKerberoast
- [ ] laZagne.exe binary download
- [ ] Update nmap's script database? see kit2
- [ ] Add silence_pcbeep function from kit2
- [ ] Initialize msfdb?
- [ ] Initialize neo4j?
- [ ] nginx config from kit2?
- [ ] Unzip /usr/share/wordlists/rockyou.txt.gz
- [ ] update searchsploit: `sudo searchsploit -u`
- [ ] `sudo updatedb` toward the end of the changes
- [ ] Adjust tldr-update.yml so the update task won't halt playbook if it fails
- [ ] Add [`conpass` password-policy-compliant brute forcer](https://github.com/login-securite/conpass) to installed packages
  - Will require installation with `pip` or `pipx`, perhaps
- [ ] Add `sstimap` burpsuite extension?

## WSL compatibility
- [ ] Troubleshoot / fix installing docker in WSL, if possible.
- [ ] Add check in `tldr-update.yml` to verify `~/.local/share/tldr` exists. Doesn't in WSL OOTB
- [ ] Change `root_install_path` variable to be full path, no using `~`. Breaks in WSL OOTB

## From existing Kali master image, create/verify
- [ ] Create generic pentester user
- [ ] Add pentester user to sudoers
- [ ] Enable SSH service
- [x] Add packages to packages.yml for attack box
- [x] `btop`?
- [x] `hollywood`?
- [x] Add github repos to git-repos.yml
- [ ] Solve installing `Autorecon`
  - [ ] Add AutoRecon.git to git repos
  - [ ] pip install requirements.txt
  - [ ] pip install AutoRecon dir
- [ ] Binary downloads of:
  - [x] linpeas.sh
  - [x] winPEAS.bat
  - [x] winPEASany.exe
  - [ ] kerbrute_linux_amd64
  - [ ] kerbrute_linux_amd64.exe
  - [ ] pspy64
  - [ ] laxagne.exe
  - [ ] lasagne.exe
  - [ ] lazagne.exe
  - [ ] linux-exploit-suggester.sh
  - [ ] 
- [ ] Compile Chisel from source?

## Extras, beyond MVP

- [ ] Add other malware frameworks?
  - [ ] Merlin
  - [ ] PoshC2?
  - [ ] Mythic? Maybe this should be for a C2 server?
- [ ] Sort/alphabetize GitHub repo list
- [ ] Set up file / download tags? Allow downloading to particular directories based on category?

## The real extras

- [ ] Another Jon function? Maybe an Ian function?
