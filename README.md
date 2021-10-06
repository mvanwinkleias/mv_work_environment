# Bootstrapping

```
sudo apt-get install tmux openssh-server fail2ban
sudo service sshd start
```

## Bash Environment

This sets up paths, and other things.

```
mkdir ~/junk
cd ~/junk
git clone https://github.com/mvanwinkle/mv_bashrc_d.git
cd mv_bashrc_d/src/bin
./set_me_up.sh
```

## SSH Keys

Individual SSH keys can be handled on a case-by-case basis.

But, if I have a lot of SSH keys to manage, I'll use this to manage it
(currently private...)

* git@gitlab.com:mvanwinkleias/mv_ssh_keygen_utils.git

## Revision Control - Git Cloning

I like to have my git repositories organized under *~/src/git/* .

However, we need to "pivot" to that first.

```
mkdir ~/junk
cd ~/junk
git clone https://github.com/mvanwinkleias/mv_git_repo_utils
cd mv_git_repo_utils/src/bin

./git_cloner.sh git@github.com:mvanwinkleias/mv_git_repo_utils.git

cd ~/bin/
ln -s ../src/git/github.com/mvanwinkleias/mv_git_repo_utils/src/bin/git_cloner.sh
```

Now, when we want to clone a repo, we do this (for example):

```
git_cloner.sh git@github.com/mvanwinkleias/mv_git_repo_utils.git
```


