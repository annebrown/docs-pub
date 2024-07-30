---
title: Modules
description: Hugo Modules
---

## Description

{{ description }}

## Module Dependencies

If build throws:

 `Error: failed to load modules: module "github.com/[some-git-acct]/[some-module]: not found in ...`
 
then import the module by adding an entry to `hugo.yaml` (or `hugo.toml` or `hugo.json`):

```yaml
module:
  imports:
    - path: github.com/[some-git-acct]/[some-module]
```

and

```bash
cd [path-to-proj]/themes/github.com/hugomods/[mod-name]
```

Also:

> Is this necessary? Shouldn't conf.yaml work?

```bash
 cd [path-to-proj]/github.com/
 mkdir [some-git-user]
 cd [some-git-user]
 git clone https://github.com/[some-git-user]/[some-module]
```

