---
title: Settings Sync
description: Syncs VSCODE Config Settings Across Dev Envs
---

## Description

{{ description }}:

  - Extensions Settings
  - Keyboard Shortcuts
  - Profiles
  - User Settings
  - User Snippets
  - UI State
  - User Tags

## Settings Files

Alphabetizing these files facilitates mods and helps reduce dups.  

  - User Settings: `~/.config/Code/User/settigns.json`
  - User Snippets: `~/.config/Code/User/snippets`

## Move Config Files to .dotfiles

To ease VSCode config for new dev envs, move settings to `~/.dotfiles`.  See [New Dev Env](../../../oses/linux/new-dev-env.md) and the [Dotfiles Project](../../../../dev/projects/dotfiles/index.md).  Skip if using VSCode built-in settings sync. Currently, using built-in sync appears to be less problematic.

User Settings File:

```bash
mv ~/.config/Code/User/settings.json ~/.dotfiles/code/.config/Code/User/settings.json
```


Snippets Dir:

```bash
mv ~/.config/Code/User/snippets/ ~./dotfiles/code/.config/Code/User/snippets
```
