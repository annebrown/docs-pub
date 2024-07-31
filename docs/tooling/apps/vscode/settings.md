---
title: Settings
description: VSCode Config
tags:
  - VSCode
---

## Description

{{ description }}

## Usage

Move VSCode settings to `~/.dotfiles`.  See [Dotfiles Project](../../../dev/projects/index.md#dotfiles-project).

This allows customized VSCode settings to be pulled into new dev envs (bare metal server, VM, GitPod, etc.).  See [New Dev Env](../../../tech/oses/linux/new-dev-env.md) and the [dotfiles](../../../dev/projects/index.md#dotfiles-project) project.

### User Settings

```bash
mv ~/.config/Code/User/settings.json ~/.dotfiles/code/.config/Code/User/settings.json
```

Alphabetizing this file facilitates mods and helps reduce dups.

### Profiles

```bash
mv ~/.config/Code/User/profiles/ ~./dotfiles/code/.config/Code/User/profiles/
```

## Default Settings

See [VSCode Default Settings](https://code.visualstudio.com/docs/getstarted/settings#_default-settings) for default values.

## Auto-Save

```json
"files.autoSave": "onFocusChange"
```

## Color

Theme colors can be overriden in [user-settings](#user-settings).  See [VS Code Workbench Color List](workbench.colorCustomizations.md) for available customizations.

### Dark Theme

```json
 "window.systemColorTheme": "dark",
```

## Custom Title Bar

When KDE Global Menu is in use, the bar displaying icons to open and close panels, e.g. terminal panel, is not visible.  To make the 
custom title bar visible:

Settings > window: CCustom Title Bar Visibility > windowed

## Editors

### Page Border

Visible page border at 80 cols.

```json
"editor.rulers": [
    80,
],
```

### Folding

```json
Editor>Show Folding Controls [always]
```

### Lightbulb

Annoying Lightbulb covers gutter info:

```json
Lightbulb:Enabled [off]
```

### Tab Completion

```json
Tab Completion: on
```

### Word Wrap

```json
Word Wrap: Word Wrap Column
Word Wrap Column: 80
```

## Explorer

### Emply Dirs

Don't display `dir/emptyDir/` as single dir tree entry:

```json
"explorer.compactFolders": false,
```

### Tree Indent

Default tree indentation size makes indentions difficult to percceive.  Make indentations more visible:

```json
Tree Indent: Workbench>Appearance>Tree:Indent [25]
Tree: Render Indent Guildes [always]
```

## Telemetry

Bugger off, Micr:money_mouth:soft:

```json
"telemetry.telemetryLevel": "off",
```

## Window Borders

Window edges not clearly visible.  Give active and inactive window borders pretty colors and makde them more visible on dark and light backgrounds:

```json
"workbench.colorCustomizations": { 
    "window.activeBorder": "#00ff88",
    "window.inactiveBorder": "#d42aeb"
},
```

See [VS Code Workbench Color List](workbench.colorCustomizations.md) for available customizations.

## Workbench

### Layout

Respect my editor widths:

`Centered Layout Auto Resize: [false]`

`Centered Layout Fixed Width: [true]`


## Extensions

### [Git](extensions.md#git)

### [MarkdownLint](extensions.md#markdownlint)

### [Vim](extensions.md#vim)

### [YAML](extensions.md#yaml)