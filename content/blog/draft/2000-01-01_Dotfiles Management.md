+++
title = "Manage dot files in a git repo"
date = 2000-01-01
draft = true
+++


<https://news.ycombinator.com/item?id=11071754>

```bash
git init --bare $HOME/.myconf
alias config='/usr/bin/git --git-dir=$HOME/.myconf/ --work-tree=$HOME'
config config status.showUntrackedFiles no
```
where my ~/.myconf directory is a git bare repository.
Then any file within the home folder can be versioned with normal commands like:

```bash
config status
config add .vimrc
config commit -m "Add vimrc"
config add .config/redshift.conf
config commit -m "Add redshift config"
config push
```

No extra tooling, no symlinks, files are tracked on a version control system,
you can use different branches for different computers, you can replicate you
configuration easily on new installation.
