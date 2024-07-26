---
tags:
  - Issues
  - SOLVED
---

# nvm install - code EACCES

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