---
title: Issue - nvm Install EACCESS Error
description: Permissions error installing Node.js
tags:
  - Issues
  - SOLVED
---

{{ description }}

## Error

```bash
nvm install 20
npm ERR! code EACCES
  ...
```

## Solution

```bash
sudo chown -R $(whoami) ~/.npm
```