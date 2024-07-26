# New Dev Env

## Description

Configure new dev env.

## Usage

Instructions for creating a new dev env for hosts, VM and cloud (GitPod).

## Dotfiles

Customized config using [GNU-Stow](https://gnu.org/software/stow/) symlink farm mgr.  See [dotfiles](../../../dev/projects.md#dotfiles) project.

```bash
$ sudo apt update
$ sudo apt update -y
$ git clone https://github.com/annebrown/dotfiles.git ~/.dotfiles
$ cd .dotfiles
$ stow bash vim code hyper konsole
$ bash
```

## Auth

### Install Pwd Mgr

Install a browser, if not present or working, then install fav pwd mgr extension.

###  Two Factor Authn

For convenient 2FA, install GitHub Mobile, from Playstore, on phone and other mobile devices.  

# [Configure Git](../../../tooling/apps/git.md)
