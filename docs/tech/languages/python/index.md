---
title: Python
description: Programming Language
---

{{ description }}

## venv

Some [Python](https://www.python.org/ "Official Site")-based projects require a virtual env.

When a venv is activated for a proj, `pip` will install all pkgs in `[project_dir]/.venv`. This isolates the proj with its own specific Python interpreter, and software libs and binaries.

## Create venv

Create `.venv` under proj dir:

```bash
cd [proj-dir]
python3 -m venv .venv
```

## Activate venv

Activate Python virtual env:

```bash
source .venv/bin/activate
```
`pip` will now install every Python pkg into `./.venv` until venv is deactivated or terminal is closed.

## Add Shortcut to `.bash_aliases`

```bash
alias activate-venv="source ./.venv/bin/activate"
```
