## Misc

Open VS Code from cli:

```shell
cat << EOF >> ~/.zshrc
# Add Visual Studio Code (code)
export PATH="$PATH:/Applications/Visual Studio Code.app/Contents/Resources/app/bin"
EOF
```

### Git:

- env variable `GIT_TRACE=true` to check all git exec (useful for debugging hooks)


### clips of my zshrc 

zshell: automatically pushd all cds:

```ini
setopt autopushd
setopt AUTO_PUSHD
setopt PUSHD_IGNORE_DUPS
```

aliases:
```ini 
alias ll='ls -Al'

# Git Flow
alias gffs='git flow feature start'
alias gfff='git flow feature finish'
alias gfrs='git flow release start'
alias gfrf='git flow release finish'
alias gfhs='git flow hotfix start'
alias gfhf='git flow hotfix finish'
alias gfbs='git flow bugfix start'
alias gfbf='git flow bugfix finish'
alias gv='gitversion'

# Ansible
alias ap='ansible-playbook'
```
